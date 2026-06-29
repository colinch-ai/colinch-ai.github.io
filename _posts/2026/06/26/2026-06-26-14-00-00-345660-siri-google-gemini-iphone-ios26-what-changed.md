---
layout: post
title: "시리가 구글 Gemini로 바뀐다 — iOS 26 업데이트에서 내 아이폰에 실제로 뭐가 달라지는가"
description: "WWDC 2026에서 공개된 Siri x Google Gemini 연동 핵심 정리. iOS 26.4부터 달라지는 기능, 지원 기기, 개인정보 처리 방식까지 비개발자 눈높이로 설명한다."
date: 2026-06-26
tags: [Gemini, GoogleAI, AI뉴스, AI업데이트, AI입문, 직장인AI]
comments: true
share: true
---

![Apple iPhone Siri AI interface redesign 2026](https://images.unsplash.com/photo-1611532736597-de2d4265fba3?w=800&q=80)

솔직히 말하면 기존 Siri는 너무 오래 실망을 줬다. "타이머 5분 맞춰줘", "날씨 알려줘" 수준 말고는 쓸 게 없었다. 근데 이번 WWDC 2026에서 애플이 꺼낸 카드가 꽤 충격적이다. 구글 Gemini를 아예 Siri의 두뇌로 넣겠다는 얘기다.

## 왜 이게 지금 화제인가

1월에 애플이 구글과 연간 약 1조 4천억 원(약 10억 달러) 규모의 계약을 맺었다는 뉴스가 나왔을 때만 해도 반신반의했다. 근데 6월 WWDC 2026에서 직접 시연을 보여줬다. 기존 Siri 껍데기는 그대로인데, 어려운 질문을 던지면 Gemini가 뒤에서 처리하는 구조다.

ChatGPT와 Claude가 스마트폰 AI 시장을 두드리는 상황에서 애플이 자체 모델 대신 경쟁사인 구글의 것을 가져다 쓰기로 했다는 게 핵심이다.

## 실제로 어떻게 작동하는가

Siri가 세 단계로 나뉘어서 처리한다.

**1단계 — 기기 안에서 직접 처리:**
"알람 취소해줘", "이 사진 편집해줘" 같은 단순 명령은 아이폰 안에서 끝난다. 서버로 안 나간다.

**2단계 — 애플 클라우드에서 처리:**
조금 복잡한 요청. 애플이 "Private Cloud Compute"라고 부르는 서버에서 처리하고 기록은 남기지 않는다고 한다.

**3단계 — Gemini로 넘어가는 요청:**
"이 PDF 내용 요약해서 이메일 초안 써줘" 같은 복잡한 작업. 이 경우 구글 서버로 간다. 애플은 이 때 내 데이터가 구글에 저장되지 않는다고 하는데, 믿을지 말지는 각자 판단해야 한다.

## iOS 26.4부터 바뀌는 것 (2026년 봄)

이번에 먼저 풀린 기능들이다.

- **이메일 요약:** 긴 이메일을 한 줄로 요약해준다. 실제로 써보면 꽤 정확하다.
- **화면 인식:** "지금 보고 있는 이 식당 예약해줘"처럼 화면에 보이는 걸 Siri가 인식해서 처리한다.
- **앱 간 연동:** 카카오톡 메시지를 캘린더 일정으로 바꿔주는 것도 된다고 한다. 아직 한국 앱 지원은 제한적이다.
- **채팅 방식 Siri 앱:** 말 대신 타이핑으로 질문할 수 있는 앱이 생겼다. PDF나 이미지도 첨부 가능.

## 이런 점은 아쉬웠다

아이폰 15 Pro(A17 Pro 칩) 이상이 아니면 화면 인식 같은 핵심 기능을 온전히 쓸 수 없다. 기존 모델은 클라우드 처리로 기본 대화 기능만 된다. iPhone 15 일반 모델도 해당 안 된다는 뜻이다.

한국어 지원이 영어보다 늦다. iOS 26.4 기준으로 아직 영어, 일부 유럽어 우선이고 한국어는 올해 하반기 예정이라고 했다. 막상 써보려면 더 기다려야 할 수도 있다.

그리고 Gemini 연동 기능은 기본 꺼진 상태로 출시된다. 설정에서 직접 켜야 한다.

## 한 줄 정리

아이폰 15 Pro 이상 쓴다면 올 하반기부터 Siri가 ChatGPT 수준으로 대화할 수 있게 된다. 그 아래 모델이라면 체감 변화는 크지 않다.

---

다음엔 갤럭시 AI와 아이폰 Gemini Siri를 실제 사용 시나리오로 비교해볼 예정이다.

**참고 링크**
- [CNBC — Apple picks Google's Gemini to run AI-powered Siri](https://www.cnbc.com/2026/01/12/apple-google-ai-siri-gemini.html)
- [MacRumors — Google Confirms Gemini-Powered Siri Coming Later This Year](https://www.macrumors.com/2026/04/22/google-gemini-powered-siri-2026/)
- [Business Standard — WWDC 2026: Apple unveils Siri AI, Gemini-powered Apple Intelligence](https://www.business-standard.com/amp/technology/tech-news/wwdc-2026-apple-unveils-siri-ai-gemini-powered-apple-intelligence-more-126060900042_1.html)
