---
layout: post
title: "Gemini Daily Brief·Spark 사용법 - 메일과 일정을 아침 브리핑으로 받는 법"
description: "Google이 공개한 Gemini Daily Brief와 Spark가 메일·캘린더·문서를 어떻게 정리하는지, 비개발자가 맡길 업무와 한국 사용자가 확인할 조건을 정리했다."
date: 2026-08-08
tags: [Gemini, GoogleAI, 업무자동화, 생산성, AI뉴스, AI입문, 직장인AI]
comments: true
share: true
---

![Gemini가 이메일·캘린더·문서를 모아 아침 업무 브리핑으로 정리하는 모습](https://images.unsplash.com/photo-1556761175-b413da4baf72?auto=format&fit=crop&w=1200&q=80)

Gemini를 검색창처럼만 쓰고 있다면, 이번 변화에서 놓치는 부분이 있다. Google은 2026년 5월 Gemini Daily Brief와 Gemini Spark를 공개했다. 메일과 캘린더를 읽고 오늘 필요한 일을 정리하거나 반복 업무를 처리하는 기능이다.

## Daily Brief와 Spark는 뭐가 다른가

Daily Brief는 아침 보고서에 가깝다. Gmail의 긴급 메일과 Google Calendar 일정을 모아 읽기 쉬운 목록으로 만든다. Spark는 반복 작업이나 여러 단계를 맡기는 에이전트(AI가 정해진 작업을 대신 수행하는 기능)다.

| 기능 | 맡길 수 있는 일 | 잘 맞는 사람 |
|---|---|---|
| Daily Brief | 오늘 일정·중요 메일 요약 | 출근 후 받은 편지함부터 여는 사람 |
| Spark | 반복 확인·문서 초안 | 매주 비슷한 보고서를 만드는 사람 |
| 연결 앱 | Gmail·Calendar·Docs·Slides | Google 서비스 사용자 |

카드 명세서에서 새 구독을 찾거나 회의 메모를 Google Docs 초안으로 만드는 식이다. 메일 발송이나 일정 변경은 실행 전 확인이 필요하다.

1. Gemini 설정에서 Daily Brief 또는 Spark의 연결 앱을 확인한다.
2. Gmail과 Calendar만 켜고 일주일 동안 결과를 본다.
3. 원하는 정보와 제외할 정보를 알려준다.
4. 읽기·분류부터 맡긴다.

복사해서 쓸 프롬프트는 이렇게 쓰면 된다.

```text
매일 오전 8시에 오늘의 업무 브리핑을 만들어줘.
- Gmail에서 오늘 답장이 필요한 메일 5개까지 찾기
- Calendar에서 오늘과 내일 일정을 시간순으로 정리하기
- 일정에 준비물이 있으면 표시하기
- 광고와 뉴스레터는 제외하기
- 답장을 보내거나 일정을 바꾸지는 말고 초안과 근거 링크만 보여주기
```

“내 일을 알아서 처리해줘”보다 메일 범위와 실행 금지를 적어야 결과를 검토하기 쉽다.

## 한국 사용자라면 확인할 점

Google은 Daily Brief를 미국에서 시작한다고 적었고, Spark는 초기 Google AI Ultra 구독자 중심의 베타로 예고했다. 한국 화면에 메뉴가 없으면 계정 등급과 국가 제공 여부를 확인하면 된다.

개인 메일에는 계약서와 고객 정보가 섞일 수 있다. 연결 전 보관 정책과 회사 계정 사용 가능 여부를 확인해야 한다.

Daily Brief는 읽기 전용으로, Spark는 되돌릴 수 있는 반복 작업부터 맡기는 편이 현실적이다.

출처: [Google Gemini 앱의 Daily Brief·Spark 공식 발표](https://blog.google/innovation-and-ai/products/gemini-app/next-evolution-gemini-app/)
