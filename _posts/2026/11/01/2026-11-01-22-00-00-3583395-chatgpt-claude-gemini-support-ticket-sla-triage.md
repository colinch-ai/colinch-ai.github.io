---
layout: post
title: "ChatGPT·Claude·Gemini 고객 문의 SLA 트리아지 - CS 담당자가 긴급도와 담당 큐를 검수하는 법"
description: "고객지원 담당자가 ChatGPT·Claude·Gemini로 문의를 긴급도·영향도·SLA·담당 큐로 나누고, 무료 사용과 유료 플랜의 경계를 검수하는 실전 프롬프트다."
date: 2026-11-01
tags: [ChatGPT, Claude, Gemini, 업무자동화, 프롬프트, AI요약]
comments: true
share: true
---
![고객 문의를 영향도와 긴급도로 나눠 SLA 트리아지 표로 바꾸는 AI 업무 흐름](/images/2026-09-17-ai-customer-reply-checklist.png)

그림에서 볼 것은 AI가 답변을 대신 보내는 장면이 아니라, 문의를 **담당 큐·긴급도·SLA 시각·사람이 확인할 이유**가 있는 표로 바꾸는 과정이다.

고객지원 티켓이 반복해서 쌓이는 팀에는 유용하지만, 환불 승인·계정 잠금·장애 복구처럼 권한 확인이 필요한 업무는 AI가 제안만 하고 사람이 결정해야 한다. 2026년 11월 1일 확인 기준, Zendesk도 AI 트리아지를 주제·감정·언어·상품명 분류와 라우팅에 연결하는 방식으로 안내한다.

## 무료로 시작할 범위와 유료가 필요한 순간

| 작업 | 무료 계정으로 가능한 범위 | 유료·업무용을 검토할 조건 |
|---|---|---|
| 20건 샘플 분류 | 비식별 CSV로 우선순위 제안 | 반복 업로드·높은 사용량 |
| 긴 문의·첨부 분석 | 짧은 텍스트·핵심 발췌 | 파일이 많거나 긴 맥락 |
| 결과물 | 복사 가능한 표 | 팀 공유·관리자 통제·감사 로그 |

ChatGPT 무료 사용자는 파일 업로드와 데이터 분석에 별도 한도가 있고, OpenAI 안내에는 무료 파일 업로드가 하루 3회로 표시된다. Claude도 파일 크기와 대화 길이에 따라 한도가 달라진다. Gemini는 한 프롬프트에 최대 10개 파일, 일반 파일 100MB까지 지원하지만 기간별 업로드 한도가 있다. 무료는 소량 샘플 검증까지로 보는 편이 안전하다.

## 같은 입력을 세 도구에 넣는 프롬프트

고객명·전화번호·주문번호를 지우고 `ticket_id`, `created_at`, `message`만 남긴 CSV를 준비한다. 답변보다 판단 근거를 남기는 프롬프트다.

```text
너는 고객지원 1차 트리아지 담당자다. 아래 티켓을 답변하지 말고 표로 분류해라.

기준:
- impact: 고객 1명 / 여러 명 / 전체 장애
- urgency: 오늘 안 / 24시간 안 / 일반
- priority: P1~P4. impact와 urgency가 충돌하면 이유를 적어라.
- queue: billing, account, technical, bug, policy 중 하나
- sla_risk: 현재 정보만으로 breach 위험을 low/medium/high로 표시

출력 열: ticket_id | priority | impact | urgency | queue | sla_risk |
근거 문장(원문 그대로 15자 이내) | 빠진 정보 | 사람 확인 필요 여부
근거가 없으면 추측하지 말고 unknown으로 써라.
```

검수 대상은 P1 개수보다 `빠진 정보`가 있는 행, 원문 근거와 priority가 맞지 않는 행, 같은 유형인데 queue가 달라진 행이다. SLA 시각은 원 시스템의 생성 시각과 영업시간 규칙으로 다시 계산한다. Zendesk도 우선순위별 응답·해결 시간을 정책으로 정의한다.

## 검수 체크리스트

- [ ] 고객 식별자와 결제·인증 정보가 제거됐나
- [ ] P1/P2 기준이 팀의 실제 영향도·긴급도 규칙과 같은가
- [ ] 모든 priority에 원문 근거가 붙었나
- [ ] SLA 시각을 티켓 시스템의 시간대와 영업일로 재계산했나
- [ ] 환불·보안·법적 문의는 자동 답변 대상에서 제외했나
- [ ] 샘플 20건의 오분류 행을 저장해 기준을 고쳤나

개인용 ChatGPT에 회사 티켓을 그대로 넣지 않는다. OpenAI는 소비자 서비스와 Business·Enterprise·API의 데이터 처리 조건이 다르다고 설명하고, Gemini도 업로드 파일과 프롬프트를 개인정보 안내 대상으로 둔다. 내부 보안 승인·보존 기간·접근 권한을 확인한 뒤 비식별 샘플부터 시작한다.

검증 가능한 결과물은 그럴듯한 답변이 아니라 `ticket_id`별 분류, 원문 근거, 빠진 정보, 사람 확인 여부다. 이 네 칸이 남으면 무료 도구로 작은 큐를 시험하고, 사용량·협업·감사 요구가 생길 때만 유료 플랜이나 전용 헬프데스크를 비교할 수 있다.

확인한 문서: [Zendesk 지능형 트리아지](https://support.zendesk.com/hc/en-us/articles/5222280338202-Intelligent-triage-use-cases-and-workflows), [OpenAI 파일 업로드 FAQ](https://help.openai.com/en/articles/8555545-file-uploads-faq), [Anthropic 사용량 안내](https://support.anthropic.com/en/articles/9797557-usage-limit-best-practices), [Google Gemini 파일 업로드 안내](https://support.google.com/gemini/answer/14903178)
