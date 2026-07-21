---
layout: post
title: "Microsoft 365 Copilot GPT-5.6 사용법 - Word·Excel·PowerPoint에 바로 쓰는 프롬프트"
description: "Microsoft 365 Copilot의 GPT-5.6 적용 소식을 바탕으로 Word·Excel·PowerPoint에서 문서 작성, 표 분석, 발표자료 수정을 맡기는 실전 사용법과 검수 기준을 정리했다."
date: 2026-07-21
tags: [Copilot, GPT-5.6, AI글쓰기, 업무자동화, AI뉴스, 직장인AI]
comments: true
share: true
---

![Microsoft 365 Copilot으로 Word·Excel·PowerPoint 업무를 처리하는 흐름](https://images.unsplash.com/photo-1553877522-43269d4ea984?w=800&q=80)

Microsoft 365 Copilot에 GPT-5.6가 기본 모델로 들어간다는 발표가 나왔다. OpenAI는 2026년 7월 9일 Word, Excel, PowerPoint, Copilot Chat, Cowork에 새 모델이 적용된다고 밝혔다. ChatGPT를 따로 열어 파일을 옮기는 흐름보다, 원래 일하던 화면에서 초안과 분석을 맡기는 쪽이 핵심이다.

체감할 부분은 “한 번에 완벽한 결과”보다 수정 지시를 덜 반복해도 되는 점이다. 다만 Microsoft 365 Copilot 사용 권한과 회사 계정의 파일 접근 권한이 필요하다.

## 앱별로 맡기기 좋은 일

| 앱 | Copilot에 맡길 일 | 사람이 확인할 부분 |
|---|---|---|
| Word | 회의 메모를 보고 보고서 초안으로 정리 | 숫자, 고유명사, 문서 톤 |
| Excel | 월별 표에서 증감과 이상값 찾기 | 계산식, 원본 범위, 단위 |
| PowerPoint | 보고서에서 5장 발표자료 만들기 | 메시지 순서, 그래프 수치, 공개 범위 |

Word에서는 참고 파일을 먼저 열고 독자와 분량, 빠진 정보 처리 방식을 함께 적는다.

```text
첨부한 회의 메모를 팀장 보고용 1페이지 보고서로 바꿔줘.
구성은 현황, 문제 2개, 결정이 필요한 사항, 담당자와 기한으로 해줘.
메모에 없는 내용은 추측하지 말고 [확인 필요]로 표시해줘.
```

Excel은 표 전체 요약보다 판단 기준을 넣어야 한다. “지난달 대비 매출이 10% 이상 줄었거나 비용이 15% 이상 늘어난 행만 표로 정리하고, 계산 기준도 적어줘”처럼 범위를 지정한다. 결과를 붙여넣기 전 원본 셀과 계산식을 확인한다.

PowerPoint에서는 디자인보다 발표 목적을 먼저 정한다. “첨부한 월간 보고서를 바탕으로 임원 회의용 6장 발표자료를 만들어줘. 한 장에 메시지 하나, 숫자는 원본과 일치시켜줘” 정도면 시작하기 좋다. 초안 뒤에는 근거 없는 문장을 표시해달라고 한 번 더 검수시킨다.

가장 현실적인 시작점은 오래된 월간 보고서 하나다. 원본과 결과를 나란히 놓고 숫자 5개, 고유명사 5개, 누락 문장만 확인한다. 이 검사를 통과하기 전에는 고객 명단이나 인사 자료를 넣지 않는다.

GPT-5.6가 Copilot에 들어왔다는 뉴스만 보고 구독을 결정할 필요는 없다. Word·Excel·PowerPoint를 매일 쓰고, 매주 같은 형식의 문서를 반복한다면 시간이 줄어드는지 작은 파일로 시험해볼 만하다. 반대로 메신저 질문이나 짧은 검색이 대부분이라면 무료 Copilot이나 기존 AI 도구로도 충분할 수 있다.

출처: [OpenAI - GPT-5.6 is now the preferred model in Microsoft 365 Copilot](https://openai.com/index/gpt-5-6-preferred-model-microsoft-365-copilot/) (2026년 7월 9일)
