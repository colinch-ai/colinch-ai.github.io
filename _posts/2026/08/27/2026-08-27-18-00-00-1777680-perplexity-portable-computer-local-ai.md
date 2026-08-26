---
layout: post
title: "Perplexity Portable Computer 출시 - 내 파일을 지키는 로컬 AI, 지금 쓸 만할까"
description: "Perplexity Portable Computer가 공개됐다. 파일을 내 PC에서 처리하고 어려운 작업만 클라우드로 넘기는 방식과 실제 사용 대상, 비용·보안 한계를 비개발자 눈높이로 정리했다."
date: 2026-08-27
tags: [Perplexity, AI뉴스, AI트렌드, AI검색, 업무자동화, AI입문]
comments: true
share: true
---

![Perplexity Portable Computer가 로컬 파일과 클라우드 AI를 나눠 처리하는 업무 흐름](https://images.unsplash.com/photo-1498050108023-c5249f4df085?auto=format&fit=crop&w=1200&q=80)

내 파일을 AI에게 맡기고 싶지만 회사 자료가 외부 서버로 올라가는 건 걱정됐다면, 오늘 뉴스에서 볼 만한 이름은 Perplexity Portable Computer다. 2026년 8월 25일 공개됐고, 파일과 실행 과정을 PC 안에 둔 뒤 어려운 추론이 필요할 때만 클라우드 사용 허락을 묻는다.

핵심은 모든 작업을 인터넷 서버로 보내지 않고, 로컬 처리와 클라우드 처리를 나눈다는 점이다.

## Portable Computer가 기존 Perplexity와 다른 점

Portable Computer는 파일 읽기·문서 검색·음성 받아쓰기·도구 실행을 PC 안에서 처리하는 AI 에이전트(여러 단계를 대신 수행하는 AI)다.

| 구분 | 일반적인 클라우드 AI | Portable Computer |
|---|---|---|
| 파일 처리 | 서버로 전송 | 기본은 내 PC 안에서 처리 |
| 어려운 질문 | 자동으로 서버 처리 | 클라우드 전송 전 허락 요청 |
| 비용 | 사용량에 따라 차감 | 로컬 처리분은 크레딧 차감 없음 |
| 연결 기능 | 웹 중심 | 파일·Gmail·Slack 등 |

“지난달 회의록에서 고객 불만을 유형별로 묶어줘”처럼 시키면 폴더를 읽고 표를 만드는 과정은 로컬에서 진행한다. 최신 시장자료를 찾는 순간에는 클라우드 사용 여부를 묻는 식이다.

## 비개발자가 실제로 쓸 만한 업무

민감정보를 지운 회의록에서 결정사항과 담당자를 뽑거나, 여러 PDF에서 환불 조건만 찾아 표로 만들 수 있다. 자기소개서 초안과 프로젝트 메모도 후보가 된다.

다만 일반 노트북용 앱은 아니다. 공식 발표 기준 대상은 Perplexity Pro·Max 구독자 중 NVIDIA DGX Spark 사용자다. 첫 버전은 Linux에서 제공되고 24GB 이상 VRAM(그래픽 메모리)이 필요하다. Windows 지원은 예정 상태다.

## 보안 설명을 그대로 믿으면 안 되는 이유

“로컬 처리”가 “절대 외부로 나가지 않음”과 같은 뜻은 아니다. 고급 추론을 위해 전송을 승인하면 해당 단계의 정보가 밖으로 나간다. Gmail·Slack을 연결하면 읽을 수 있는 범위도 넓어진다.

승인 창을 매번 읽고, 업무 전체 폴더 대신 시험 폴더만 연결해야 한다. 고객·금액·계약 조건은 원문과 대조하고 전용 GPU 가격까지 계산한다.

민감한 자료를 다루면서 고성능 NVIDIA 장비를 이미 가진 사람에게는 흥미롭다. 일반 사용자는 당장 장비를 살 이유가 없다. “인터넷 없이 처리해도 되는가”, “실패해도 복구 가능한가”를 기준으로 업무를 골라두면 된다.

편리함보다 파일 경계를 정하는 습관이 중요하다.

출처: [Perplexity Portable Computer 공식 발표](https://www.perplexity.ai/sv/hub/blog/introducing-portable-computer-for-local-first-ai)
