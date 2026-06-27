---
layout: post
title: "AI 칩 전쟁, 엔비디아 독점에 균열 — 퀄컴이 텐스토런트를 14조에 사는 게 내 ChatGPT와 무슨 관계"
description: "퀄컴이 AI 칩 스타트업 텐스토런트를 최대 14조 원에 인수 협상 중이다. 엔비디아 독점 AI 칩 시장에 경쟁자가 생기면 ChatGPT·Claude 같은 AI 서비스 비용이 어떻게 바뀌는지 풀어봤다."
date: 2026-06-27
tags: [AI뉴스, AI트렌드, ChatGPT, AI입문, 직장인AI]
comments: true
share: true
---

# AI 칩 전쟁, 엔비디아 독점에 균열 — 퀄컴이 텐스토런트를 14조에 사는 게 내 ChatGPT와 무슨 관계

![AI semiconductor chip microprocessor circuit board](https://images.unsplash.com/photo-1518770660439-4636190af475?w=800&q=80)

엔비디아가 AI 칩 시장을 거의 독점하는 동안, 조용히 다른 방향을 파온 스타트업이 있다. 퀄컴이 그 회사 텐스토런트(Tenstorrent)를 최대 14조 원에 사려 한다는 뉴스가 어제(6월 26일) 터졌다. 대기업 돈 싸움처럼 보이는데, ChatGPT나 Claude 쓰는 사람한테도 의미가 있다.

## 왜 지금 이 뉴스가 나왔나

로이터가 보도했다. 퀄컴이 텐스토런트를 8조~14조 원 사이 금액으로 인수 협상 중이라고. 퀄컴과 텐스토런트 양쪽 다 공식 확인은 안 했다. 협상 중이라는 뜻이고, 아직 확정은 아니다.

텐스토런트는 AMD Ryzen, Apple M1 칩 설계에 관여한 짐 켈러(Jim Keller)가 만든 회사다. AI 전용 칩을 만들되, 엔비디아와 달리 오픈 소스 기반 RISC-V 방식으로 간다는 게 핵심이다. 기술 쪽 사람들 사이에서는 꽤 유명했는데 일반 뉴스엔 별로 안 나왔던 회사다.

## AI 칩이 뭔데, 왜 이게 중요한가

ChatGPT에 "이 이메일 요약해줘"라고 치면, 그 답변은 어딘가 거대한 서버에서 나온다. 그 서버 안에 AI 전용 칩이 들어가 있다. 지금 그 칩의 80% 이상이 엔비디아 제품이다.

엔비디아 칩 하나에 수천만 원씩 한다. AI 서비스 회사들은 이걸 수천~수만 개씩 사야 한다. 그 비용이 결국 우리가 내는 구독료에 반영된다. ChatGPT Plus 월 29달러, Claude Pro 월 20달러의 상당 부분이 여기서 나온다.

독점이라 가격을 내릴 이유도 없고, 기다리는 줄도 길다. 엔비디아가 공급 못 하면 그냥 기다려야 한다. OpenAI·구글·메타 같은 회사들이 왜 그렇게 자체 칩 개발에 집착하는지 이걸 보면 이해가 된다.

## 퀄컴이 텐스토런트를 사면 뭐가 달라지나

![data center server room AI computing infrastructure](https://images.unsplash.com/photo-1558618666-fcd25c85cd64?w=800&q=80)

당장 내일 ChatGPT 요금이 내려가진 않는다.

다만 구조가 바뀐다. 지금까지는 "AI 칩 = 엔비디아"가 거의 공식이었는데, 퀄컴+텐스토런트 조합이 나오면 실제로 쓸 수 있는 대안이 생긴다. AMD도 AI 칩 시장에 뛰어들었고, 구글·아마존은 자체 칩을 만들고 있고, 얼마 전엔 OpenAI가 코드명 '재러피뇨(Jalapeño)' 자체 칩을 만든다고 했다({% post_url 2026-06-26-23-00-00-395040-openai-jalapeno-chip-chatgpt-faster-cheaper %} 참고).

경쟁자가 여러 개 생기면 엔비디아도 가격 압박을 받는다. AI 서비스 운영 비용이 내려가면, 그게 쌓여서 언젠가 구독료 인하나 성능 향상으로 돌아온다.

텐스토런트 칩의 특징이 하나 있다. 엔비디아 칩은 자사 전용 소프트웨어(CUDA)에 묶여 있어서 한번 쓰기 시작하면 벗어나기 어렵다. 텐스토런트는 RISC-V 오픈 소스 기반이라 그 묶임이 없다. 회사들이 자유롭게 AI 인프라를 바꿀 수 있다는 뜻이다.

## 근데 퀄컴이 왜 지금

퀄컴은 스마트폰 칩 회사로 알려졌는데, 사실 수년 전부터 PC·서버 쪽 칩 시장에 들어오려 했다. 텐스토런트 인수는 AI 서버 칩 시장에 직접 뛰어드는 카드다.

14조 원이 작은 금액은 아닌데, AI 칩 시장 자체가 이미 수백조 규모다. 늦게 들어가더라도 일부만 가져가도 본전 이상이라는 계산이 있는 것 같다.

## 솔직히 이렇게 생각했다

처음 이 뉴스 봤을 때 "그래서 나랑 무슨 상관?"이었다. 대기업 M&A 소식이잖아.

근데 생각해보면 지금 내가 쓰는 AI 서비스 요금의 구조가 AI 칩에 달려 있다. 엔비디아 독점이 느슨해질수록, ChatGPT나 Claude 같은 서비스를 더 싸고 더 빠르게 쓸 수 있는 날이 빨라진다. 당장은 아니고, 2~3년 안에 서서히.

아직 협상 중이고 확정도 아니다. 잘못되면 그냥 없던 일이 된다. 하지만 이 방향 자체는 계속 가고 있다.

## 한 줄 정리

퀄컴 + 텐스토런트는 엔비디아 AI 칩 독점에 생긴 첫 번째 진짜 균열이다. AI 서비스 비용과 속도는 이 경쟁 구도가 자리잡으면서 천천히 바뀐다.

---

다음엔 구글·아마존·애플이 각자 AI 칩을 만드는 이유와, 그게 우리가 쓰는 서비스에 어떤 식으로 영향을 주는지 다뤄볼 예정이다.

**참고 링크**
- [Qualcomm in Talks to Acquire Tenstorrent for $8-10B (GuruFocus)](https://www.gurufocus.com/news/8918277/qualcomm-in-talks-to-acquire-ai-chip-startup-tenstorrent-for-810-billion)
- [Qualcomm Bets on Cracking Nvidia's AI Monopoly With RISC-V (TechTimes)](https://www.techtimes.com/articles/319017/20260624/qualcomm-bets-14-billion-cracking-nvidias-ai-monopoly-risc-v-open-compiler.htm)
- [What Qualcomm Is Actually Buying From Tenstorrent (Medium)](https://medium.com/@noahbean3396/qualcomm-is-in-advanced-negotiations-to-buy-tenstorrent-for-10-billion-82d6801896e6)
