---
layout: post
title: "알리바바가 Claude를 훔쳤다? — AI '증류 공격' 논란 쉽게 설명"
description: "Anthropic이 알리바바 Qwen 연구진이 2만 5천 개 가짜 계정으로 Claude에게 2,880만 번 질문해 기술을 복사했다고 고발했다. 증류 공격이 뭔지, 내 Claude 사용에 영향이 있는지 비개발자 눈높이로 정리했다."
date: 2026-06-28
tags: [Claude, Anthropic, AI뉴스, AI트렌드, AI보안]
comments: true
share: true
---

# 알리바바가 Claude를 훔쳤다? — AI '증류 공격' 논란 쉽게 설명

![사이버 해킹과 AI 보안 개념 이미지](https://images.unsplash.com/photo-1526374965328-7f61d4dc18c5?w=800&q=80)

2만 5천 개 가짜 계정을 만들어 Claude에게 2,880만 번 질문을 던졌다 — Anthropic이 알리바바 Qwen 연구진을 이렇게 고발했다. 내가 매일 쓰는 Claude가 이런 식으로 '복사' 당하고 있다는 게 무슨 의미인지 풀어봤다.

## 무슨 일이 일어났나

2026년 6월 10일, Anthropic은 미국 상원 은행위원회에 공식 편지를 보냈다.

내용은 이렇다. 알리바바 산하 Qwen AI 연구진이 2026년 4월 22일부터 6월 5일까지, 약 2만 5천 개의 가짜 계정을 이용해 Claude에게 총 2,880만 번의 질문을 던졌다는 것. 이 과정이 44일 동안 계속됐다.

목적은 하나다. Claude의 답변을 모두 수집해서 자신들 AI인 Qwen을 더 똑똑하게 만드는 것. AI 업계에서는 이걸 '증류 공격(distillation attack)'이라고 부른다.

## '증류'가 뭔지 모르겠다면 이렇게 생각하면 된다

![데이터 복사와 AI 학습 개념 이미지](https://images.unsplash.com/photo-1558618666-fcd25c85cd64?w=800&q=80)

Anthropic은 수년간 수십억 달러를 들여 Claude를 만들었다. Claude는 어떤 질문에도 정교하게 답변한다.

이걸 그대로 복사하려면 어떻게 해야 할까? 직접 설계도를 훔치는 건 불가능하다. 그래서 나온 방법이 이렇다:

**질문 수천만 개를 던지고 → 그 답변을 전부 저장하고 → 그 답변으로 더 싼 모델을 훈련시킨다**

결과적으로 Anthropic이 수년간 개발한 능력을 훨씬 적은 시간과 돈으로 흉내낼 수 있게 된다. 쉽게 말하면 정답지를 통째로 베껴서 시험을 보는 것이다.

이번 건에서는 소프트웨어 개발 능력과 복잡한 추론 능력이 주된 타깃이었다고 Anthropic은 밝혔다.

## 근데 이전에도 있었나

있었다. 올해 2월에도 Anthropic은 DeepSeek, MiniMax, Moonshot AI 등 중국 AI 스타트업 여러 곳이 비슷한 방식으로 1,600만 건 이상의 Claude 대화를 수집했다고 발표했다. 그때도 약 2만 4천 개의 가짜 계정이 동원됐다.

이번 알리바바 건은 그보다 규모가 크고, 단순 스타트업이 아닌 글로벌 대기업이 직접 연루됐다는 점에서 파장이 다르다. Anthropic 역사상 가장 큰 규모의 증류 공격이라고 공식 문서에서 표현했다.

## 내가 쓰는 Claude에 문제는 없나

지금 당장은 없다. 가짜 계정들은 이미 차단됐고 캠페인도 종료됐다.

다만 이 사태가 가져올 변화가 있다. 앞으로 Claude 같은 프리미엄 AI 서비스들이 무분별한 대량 사용에 더 강한 제한을 걸 가능성이 높다. 무료 플랜의 하루 사용량 한도나 API 호출 규정이 더 엄격해질 수 있다.

또 하나, 알리바바 Qwen을 쓰고 있다면 그 능력 일부가 Claude에서 나온 것일 수 있다. '무료 AI'라는 이름 뒤에 이런 구조가 있다.

## 왜 Anthropic은 이걸 공개한 건가

회사 내부에서 조용히 차단만 하고 끝낼 수도 있었다. 미국 상원에 편지를 보낸 건 입법 대응을 끌어내기 위해서다.

반응은 벌써 나왔다. 미국 상원의원 두 명이 이런 증류 공격을 벌이는 단체를 제재하는 조항을 국방 예산안에 포함하려는 움직임을 보이고 있다.

AI 기술 패권 싸움이 단순한 제품 경쟁을 넘어서 법적·외교적 분쟁으로 번지는 중이다. Anthropic의 이번 고발은 그 흐름에서 꽤 의도적인 선택이다.

참고로 Anthropic이 지금 얼마나 주목받는 기업인지가 궁금하다면 [이 글]({% post_url 2026-06-26-22-00-00-382695-anthropic-ipo-965b-claude-what-changes %})에서 IPO 이야기를 다뤘다.

## 한 줄 정리

알리바바가 Claude를 '복사'하려 한 건 사실이고, Anthropic은 그걸 법적으로 막으려 하고 있다. 내 Claude 사용에 당장 영향은 없지만 AI 서비스의 사용 제한이 앞으로 더 빡빡해질 수 있다.

---

다음엔 Qwen이 실제로 Claude를 얼마나 따라잡고 있는지, 중국 AI가 쓸 만한지 직접 비교해볼 예정이다.

**참고 링크**
- [Anthropic accuses Alibaba of 'largest known distillation attack' on Claude — Nikkei Asia](https://asia.nikkei.com/business/technology/artificial-intelligence/anthropic-accuses-alibaba-of-largest-known-distillation-attack-on-claude)
- [Anthropic accuses Alibaba of running largest distillation campaign — The Next Web](https://thenextweb.com/news/anthropic-accuses-alibaba-distillation-claude-qwen)
- [Inside Anthropic's Claims of Distillation Attack by Alibaba — Cybersecurity Magazine](https://cybermagazine.com/news/inside-anthropics-claims-of-distillation-attack-by-alibaba)
