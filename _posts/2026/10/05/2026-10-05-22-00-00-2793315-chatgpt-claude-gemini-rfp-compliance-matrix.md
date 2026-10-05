---
layout: post
title: "ChatGPT·Claude·Gemini RFP 요구사항 검수 - 영업 담당자가 무료로 제안서 누락을 찾는 법"
description: "영업·제안 담당자가 RFP 요구사항을 ChatGPT·Claude·Gemini로 추적표로 만들고, 무료 사용과 유료 전환의 경계, 개인정보와 사람 검수 기준을 확인한다."
date: 2026-10-05
tags: [ChatGPT, Claude, Gemini, 업무자동화, 프롬프트, AI업무]
comments: true
share: true
---

![RFP 요구사항과 제안서 답변 위치를 추적표로 검수하는 업무 화면](/images/2026-09-29-ai-contract-version-comparison.png)

RFP나 입찰 제안서를 반복해서 만드는 영업·제안 담당자라면 ChatGPT·Claude·Gemini 무료 플랜으로 요구사항 누락 1차 검수를 시작할 수 있다. 다만 고객명, 가격, 보안 조건이 들어간 원문은 익명화해야 하며, AI가 만든 표를 제출본으로 믿으면 안 된다. 이 글의 결과물은 “요구사항 원문-제안서 위치-근거-상태”가 연결된 검수표다.

## 왜 단순 요약보다 추적표인가

RFP compliance matrix는 요구사항마다 제안서의 어느 부분에서 답했는지 연결하는 표다. 실제 가이드들도 요구사항 ID, 원문, 응답 위치, 준수 상태를 한 행씩 관리하라고 설명한다. [Proposit의 설명](https://www.getproposit.com/guides/compliance-matrix)과 [ProposalWorkspace의 예시](https://proposalworkspace.com/proposal-guides/proposal-compliance-matrix-template)가 이 구조를 보여준다.

| 열 | AI에게 맡길 일 | 사람이 확인할 일 |
|---|---|---|
| 요구사항 ID·원문 | 문서와 첨부파일에서 추출 | 누락·중복·해석 오류 |
| 제안서 위치 | 섹션·페이지 후보 연결 | 실제 제출본의 위치 |
| 상태 | 충족·부분 충족·예외 후보 분류 | 계약상 수용 가능한지 |
| 근거·담당자 | 근거 문장과 담당자 정리 | 최신 승인 자료인지 |

## 복사해서 쓰는 프롬프트

익명화한 RFP와 제안서 초안을 각각 올린 뒤 아래처럼 요청한다. 문서가 길면 한 번에 결론을 요구하지 말고 요구사항 추출과 대조를 나눈다.

```text
너는 제안서 QA 담당자다. 아래 RFP와 제안서만 근거로 요구사항 추적표를 만들어라.
열: ID | RFP 원문(짧게) | 출처 페이지 | 제안서 위치 | 근거 문장 | 상태 | 누락 질문 | 담당자 후보
규칙:
1) 원문에 없는 요구사항을 만들지 말 것
2) 제안서 위치를 찾지 못하면 '미확인'으로 쓸 것
3) 충족/부분 충족/미충족/판단 불가를 구분할 것
4) 각 행 뒤에 사람이 확인할 질문을 한 문장으로 붙일 것
5) 마지막에 미충족과 마감 전 확인 순서만 따로 정리할 것
```

AI 답변을 받은 뒤에는 표에서 `미확인`, `부분 충족`, `판단 불가`만 필터링한다. 그 행의 RFP 페이지를 직접 열고 제안서 문장을 대조하면 전체 문서를 다시 읽는 부담을 줄일 수 있다. 단, 페이지 번호는 파일 형식과 변환 방식에 따라 달라질 수 있으므로 원본 PDF 화면에서 재확인한다.

## 무료로 충분한 경우와 유료가 필요한 경우

| 상황 | 무료 플랜으로 시작 | 유료·업무용 검토가 필요한 경우 |
|---|---|---|
| 문서량 | 짧은 RFP 1개, 요구사항 표 초안 | 여러 첨부파일과 반복 갱신 |
| 사용량 | 가끔 한 번씩 검수 | 마감 주간에 여러 번 재검수 |
| 결과물 | CSV로 옮길 표와 누락 질문 | 팀 공유, 권한·보관·감사 요구 |
| 선택 기준 | 업로드 한도와 답변 품질을 먼저 확인 | 가격보다 조직의 데이터 정책을 우선 |

확인 날짜는 2026년 10월 5일이다. OpenAI는 무료 사용자의 파일 업로드가 별도 제한을 받으며, 파일 하나는 512MB·문서 2M 토큰 한도가 있다고 안내한다. [OpenAI 파일 업로드 FAQ](https://help.openai.com/en/articles/8555545-file-uploads)에 따르면 무료 사용자는 하루 3개 업로드로 제한될 수 있다. Claude는 요금제가 아니라 메시지 길이, 첨부파일 크기, 대화 길이 등에 따라 사용량이 달라진다고 설명한다. [Anthropic 사용량 안내](https://support.anthropic.com/en/articles/9797557-usage-limit-best-practices)

Gemini는 한 프롬프트에 최대 10개 파일을 올릴 수 있지만 사용량은 순환 제한을 받는다. Google은 더 높은 업로드·컨텍스트 한도가 필요하면 Google AI Pro나 Ultra를 안내한다. [Gemini 파일 분석 안내](https://support.google.com/gemini/answer/14903178)

## 개인정보와 최종 검수표

무료 소비자 계정에 실제 RFP를 그대로 올리는 것은 구매 결정 이전에 해결해야 할 문제다. 고객명·연락처·계좌·비공개 가격·접근 키를 가상 값으로 바꾸고, 회사 정책상 외부 AI 업로드가 금지된 문서는 사용하지 않는다. 더 높은 한도가 곧 기업 보안을 뜻하지도 않는다.

- 요구사항 행 수와 원문 페이지 수가 맞는가
- 모든 `미확인` 행을 담당자에게 배정했는가
- 제안서 문장이 RFP의 의무 표현을 빠뜨리지 않았는가
- AI가 만든 근거 문장을 원본에서 다시 찾았는가
- 가격·법무·보안 예외를 사람이 승인했는가

AI에게 맡길 부분은 반복적인 추출과 대조다. 충족 여부를 최종 선언하는 일은 담당자와 법무·보안 검토자의 몫이다. 무료 플랜으로도 짧은 문서의 초안은 만들 수 있지만, 이 표를 제출 직전의 유일한 품질 게이트로 쓰면 안 된다.

참고한 문서: [RFP compliance matrix 설명](https://legalclarity.org/compliance-matrix-example-how-to-build-one-for-rfps/) · [ChatGPT 파일 업로드 FAQ](https://help.openai.com/en/articles/8555545-file-uploads) · [Claude 요금제 선택 안내](https://support.anthropic.com/en/articles/11049762-choosing-a-claude-ai-plan) · [Gemini 파일 분석 안내](https://support.google.com/gemini/answer/14903178) (2026-10-05 확인)
