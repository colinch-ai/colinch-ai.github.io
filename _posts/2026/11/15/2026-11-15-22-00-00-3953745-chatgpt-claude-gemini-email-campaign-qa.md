---
layout: post
title: "ChatGPT·Claude·Gemini 이메일 캠페인 발송 전 검수 - 마케터가 링크와 조건 누락을 찾는 법"
description: "마케팅 담당자가 ChatGPT·Claude·Gemini로 이메일 캠페인의 링크, UTM, 개인화, 할인 조건과 수신거부 누락을 검수하는 방법을 정리한다. 무료 시험과 유료 전환 기준도 함께 다룬다."
date: 2026-11-15
tags: [ChatGPT, Claude, Gemini, 업무자동화, 프롬프트, AI글쓰기]
comments: true
share: true
---

![이메일 캠페인 발송 전 링크와 조건을 검수하는 마케팅 업무 화면](https://images.unsplash.com/photo-1556761175-b413da4baf72?auto=format&fit=crop&w=1400&q=80)

이메일을 주 1~3회 보내는 마케터라면 ChatGPT·Claude·Gemini 무료 플랜에 비식별화한 테스트 메일을 넣고 **발송 차단 항목과 확인 항목 표**를 만드는 것부터 시작하는 선택이 유리하다. 고객 데이터가 섞인 원문을 개인 계정에 올리거나 AI의 `GO` 판정만 믿고 발송하는 경우에는 적용하지 않는다. AI는 링크 클릭과 모바일 렌더링을 보장하지 못한다.

## 이메일 QA에서 AI가 맡을 일

“문장이 자연스러운가?”만 물으면 칭찬으로 끝난다. 승인된 오퍼 원본과 메일 초안을 함께 주고 실패 조건을 고정해야 한다.

| 항목 | AI 결과 | 사람 확인 |
|---|---|---|
| 링크·UTM | 목적지·누락·오타 | 테스트 메일 클릭 |
| 제목·프리헤더 | 빈 값·길이·불일치 | 수신함 표시 |
| 개인화 | 변수·기본값 누락 | 테스트 수신자 |
| 가격·할인·기한 | 원본과 다른 숫자·날짜 | 승인 원본 |
| 수신거부·주소 | 링크·정보 누락 | 플랫폼 설정·법무 기준 |

Mailchimp는 UTM이 실제 사이트에서 받아들여지는지 라이브 테스트 메일로 확인하라고 안내한다. Klaviyo의 공식 프롬프트도 목적지·UTM·개인화·가격·수신거부를 `발송 차단`과 `수정 권장`으로 나눈다. AI 표는 링크가 살아 있다는 증명이 아니라 확인 목록이다.

## 복사해서 쓰는 검수 프롬프트

아래 프롬프트는 세 도구에 공통으로 쓸 수 있다. 원본에는 가격표·프로모션 문서를, 초안에는 텍스트·링크 목록을 넣는다.

```text
너는 이메일 캠페인 발송 전 QA 담당자다.
[승인 원본]
...
[메일 초안]
...

원문에 없는 사실은 추정하지 말고 아래 표만 작성해라.
열: 구분 | 상태(BLOCK/REVIEW/PASS) | 문제 | 근거 | 수정 제안
검사: 1) 모든 링크의 목적지와 placeholder 여부 2) utm_source, utm_medium, utm_campaign의 누락·허용값 위반 3) 제목·프리헤더의 빈 값 4) 개인화 변수와 기본값 5) 가격·할인율·통화·종료일 6) 수신거부 링크와 사업자 주소.
원본에 근거가 없으면 REVIEW로 표시하고, BLOCK 행만 발송 전 체크리스트로 다시 출력해라.
```

`근거`가 비어 있는 행은 통과로 보지 않는다. `utm_campaign`은 실제 URL을 열고, 개인화 변수는 테스트 주소 2개 이상으로 수신한다. 실제 캠페인을 발송한 글은 아니다.

## 무료와 유료의 경계

| 상황 | 선택 |
|---|---|
| 짧은 텍스트·가명 데이터 | 무료 샘플 검수 |
| 긴 HTML·반복 업로드 | 사용량 한도 확인 후 유료 검토 |
| 고객 정보·팀 승인 필요 | 회사 승인 환경 |
| 발송·자동화 연결 | 메일 플랫폼 권한·로그 검토 |

무료 계정은 파일·분석 기능에 별도 사용량 제한이 있다. Gemini와 Claude도 소비자 계정의 활동 저장·모델 개선 설정을 확인해야 한다. 유료 결제는 한 달간 `누락 행 수`, `재검수 시간`, `발송 차단 오류`가 줄어드는지로 판단한다.

핵심은 AI에게 발송 승인을 맡기지 않는 것이다. 승인 원본과 초안을 대조한 오류표를 만들고, 링크 클릭·렌더링·수신거부·최종 조건은 사람이 확인해야 검증 가능한 결과물이 된다.

참고한 문서는 [Mailchimp의 깨진 링크·UTM 안내](https://mailchimp.com/help/troubleshoot-broken-links/), [Klaviyo의 공식 발송 전 감사 프롬프트](https://www.klaviyo.com/ai-prompt-library/pre-send-audit-campaign-message), [OpenAI 무료 사용량 FAQ](https://help.openai.com/en/articles/9275245-using-chatgpt-without-logging-in), [Gemini 개인정보 보호 허브](https://support.google.com/gemini/answer/13594961?hl=en), [Anthropic의 소비자 대화 개인정보 안내](https://support.anthropic.com/en/articles/8325621-i-would-like-to-input-sensitive-data-into-my-free-pro-or-max-plan-claude-account-who-can-view-my-conversations)다.
