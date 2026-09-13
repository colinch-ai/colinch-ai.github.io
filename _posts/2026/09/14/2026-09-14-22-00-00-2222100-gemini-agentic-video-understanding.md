---
layout: post
title: "Gemini 동영상 분석 사용법 - 긴 영상에서 필요한 장면만 찾는 방법"
description: "Gemini Agentic Video Understanding이 긴 영상에서 필요한 장면·자막·소리만 골라 분석하는 방식과 회의·강의에 쓰는 프롬프트를 정리했다."
date: 2026-09-14
tags: [Gemini, AI요약, AI뉴스, AI업데이트, GoogleAI, 생산성]
comments: true
share: true
---

![Gemini가 긴 영상의 필요한 장면만 골라 분석하는 작업 흐름](/assets/images/2026-09-14-gemini-agentic-video-understanding.png)

Gemini 동영상 분석이 9월 1일 바뀌었다. Google DeepMind의 `Agentic Video Understanding`은 영상을 1초에 한 장씩 읽는 대신 질문과 관련된 구간을 다시 찾는다. 자막·소리·화면 중 무엇을 볼지도 고른다. ([Google 공식 발표](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-agentic-video-in-gemini/))

## 실제로 어디에 쓰나

90분 회의 영상이라면 “가격 정책이 바뀐 부분과 담당자를 찾아줘”라고 물을 수 있다. 강의는 “시험에 나올 개념을 타임스탬프와 함께 정리해줘”, 유튜브는 “제품 비교 장면과 차이를 표로 만들어줘”라고 요청하면 된다.

Google은 긴 영상에서 토큰(영상과 글을 AI가 처리하는 단위)을 최대 88% 줄이고 비용은 최대 66% 낮췄다고 설명한다. 현재는 일반 Gemini 채팅이 아니라 Google AI Studio와 Gemini API에서 제공된다. AI Studio에서 영상 업로드 후 질문할 수 있지만 계정과 사용량 설정은 필요하다. ([공식 안내](https://ai.google.dev/gemini-api/docs/video-understanding))

## 복사해서 쓰는 프롬프트

영상 파일이나 공개 YouTube 주소를 넣고 아래처럼 질문하면 된다.

```text
이 영상을 처음부터 단순 요약하지 말고 필요한 구간을 찾아 분석해줘.
1. 핵심 주장 5개를 타임스탬프와 함께 정리
2. 숫자·날짜·고유명사는 영상의 말과 화면을 대조
3. 실행할 일과 '확인 필요' 내용을 분리
```

| 상황 | 이렇게 요청하면 좋다 | 결과물 |
|---|---|---|
| 회의 녹화 | 결정사항·담당자·기한만 찾아줘 | 실행 목록 |
| 강의·리뷰 | 개념·비교 장면과 근거를 찾아줘 | 복습 노트·비교표 |

“이 영상 요약해줘”보다 찾을 기준과 출력 형식을 같이 적는 편이 낫다. 작은 글씨, 겹쳐 말하는 장면, 비공개 영상의 접근 권한은 틀릴 수 있으니 중요한 결정과 숫자는 타임스탬프를 직접 확인해야 한다.

Gemini Agentic Video Understanding은 긴 영상에서 질문과 관련된 순간을 찾아주는 검색 도구에 가깝다. 회의·강의·리뷰를 자주 확인한다면 짧은 영상부터 시험해볼 만하다.

출처: [Google DeepMind 공식 발표](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-agentic-video-in-gemini/), [Gemini API 동영상 분석 문서](https://ai.google.dev/gemini-api/docs/video-understanding)
