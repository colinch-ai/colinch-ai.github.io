---
layout: post
title: "OpenAI가 자체 칩 Jalapeño를 만든 이유 — ChatGPT 사용자한테 뭐가 달라지나"
description: "OpenAI가 Broadcom과 함께 자체 AI 칩 Jalapeño를 발표했다. NVIDIA 의존을 줄이고, ChatGPT를 더 빠르고 저렴하게 만들기 위한 전략이다."
date: 2026-06-26
tags: [ChatGPT, OpenAI, AI뉴스, AI트렌드, 생산성]
comments: true
share: true
---

![반도체 칩 클로즈업, AI 하드웨어 기술](https://images.unsplash.com/photo-1518770660439-4636190af475?w=800&q=80)

OpenAI가 자체 AI 칩을 만들기 시작했다. 이름은 Jalapeño. 6월 24일 Broadcom과 공동으로 발표했다. 직접 눈에 보이는 변화는 아니지만, ChatGPT를 쓰는 사람이라면 결과적으로 더 빠른 응답과 더 저렴한 요금으로 이어질 수 있다.

## 왜 이게 지금 화제인가

지금까지 OpenAI는 ChatGPT를 돌리는 데 필요한 칩을 거의 전부 NVIDIA에서 사 왔다. NVIDIA H100, H200 같은 GPU를 대량으로 임대하거나 구매해서 ChatGPT를 운영하는 구조다. 문제는 돈이다. NVIDIA 칩은 비싸고, 수요가 폭발적으로 늘어나면서 공급도 빠듯하다.

Jalapeño는 거기서 벗어나려는 시도다. OpenAI가 직접 설계하고 Broadcom이 제조한다. ChatGPT가 답변을 생성하는 과정(AI 업계 용어로 '인퍼런스')에 특화되어 있다. 6월 24일 OpenAI 샌프란시스코 본사에서 실제 칩 샘플이 물리적으로 전달됐고, 2026년 말 첫 데이터센터 배포를 목표로 하고 있다.

![AI 데이터센터와 서버 인프라](https://images.unsplash.com/photo-1558494949-ef010cbdcc31?w=800&q=80)

## 사용자 입장에서 뭐가 달라지나

솔직히 말하면, 칩 이름이 뭔지는 ChatGPT 쓰는 사람한테 아무 상관이 없다. 중요한 건 결과다.

**속도.** 지금도 ChatGPT가 긴 글을 쓰거나 복잡한 질문에 답할 때 몇 초씩 기다려야 하는 경우가 있다. 칩이 바뀌면 이 부분이 개선될 수 있다. Jalapeño는 정확히 ChatGPT 같은 대형 언어 모델이 텍스트를 뱉어내는 속도를 높이도록 설계됐다.

**비용.** OpenAI가 NVIDIA에 내는 칩 비용이 줄면, 이론적으로 사용자 요금도 낮아질 수 있다. 실제로 연결이 될지는 더 지켜봐야 하지만, 업계 분석가들은 API 가격 인하 가능성을 언급하고 있다.

**안정성.** ChatGPT 사용량이 갑자기 몰릴 때 응답이 느려지거나 오류가 뜨는 경우가 있다. 자체 칩을 쓰면 이 상황을 더 유연하게 대응할 수 있다.

## 이런 점은 아쉬웠다

아직 체감하기엔 이르다. Jalapeño 첫 배포가 2026년 말로 잡혀 있고, 실제 사용자가 속도나 비용 변화를 느끼려면 그 이후로도 시간이 더 걸린다. 지금 단계에서는 "OpenAI가 NVIDIA 의존도를 줄이기 시작했다"는 신호 정도로 읽는 게 맞다.

그리고 자체 칩을 가진다고 해서 NVIDIA를 바로 끊는 건 아니다. 당분간은 병행해서 쓸 가능성이 높다. NVIDIA 주가가 이 발표에 별 반응을 보이지 않은 것도 그 이유다.

## 한 줄 정리

OpenAI가 자체 칩을 만드는 건, 결국 ChatGPT를 더 빠르고 싸게 운영하기 위한 인프라 독립 선언이다.

---

다음엔 AI 회사들이 직접 하드웨어에 투자하는 이유 — 구글 TPU, Apple Neural Engine과 비교해 살펴볼 예정이다.

**참고 링크**
- [OpenAI Jalapeño 공식 발표](https://openai.com/index/openai-broadcom-jalapeno-inference-chip/)
- [TechCrunch: OpenAI unveils its first custom chip, built by Broadcom](https://techcrunch.com/2026/06/24/openai-unveils-its-first-custom-chip-built-by-broadcom/)
- [CNBC: OpenAI and Broadcom reveal Jalapeno](https://www.cnbc.com/2026/06/24/openai-and-broadcom-reveal-jalapeno-first-ai-chip-in-partnership.html)
