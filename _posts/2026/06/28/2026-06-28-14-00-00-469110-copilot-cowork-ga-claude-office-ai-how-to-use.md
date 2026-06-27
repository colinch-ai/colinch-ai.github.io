---
layout: post
title: "Microsoft Copilot Cowork 정식 출시 — Excel·Outlook에서 AI가 알아서 일하는 시대"
description: "2026년 6월 Microsoft Copilot Cowork가 정식 출시됐다. Claude 기반의 자율 AI 에이전트가 Outlook·Excel·Teams를 넘나들며 업무를 처리한다. 직장인이 알아야 할 것만 정리했다."
date: 2026-06-28
tags: [Copilot, Claude, 업무자동화, 직장인AI, AI뉴스]
comments: true
share: true
---

# Microsoft Copilot Cowork 정식 출시 — Excel·Outlook에서 AI가 알아서 일하는 시대

![사무실 노트북에서 AI 업무 자동화를 활용하는 직장인](https://images.unsplash.com/photo-1498050108023-c5249f4df085?w=800&q=80)

기존 Copilot이 "물어봐야 대답하는 AI"였다면, Cowork는 "시켜두면 혼자 처리하는 AI"다. 6월 16일 Microsoft가 Copilot Cowork를 정식 출시했고, 내부에서 Anthropic의 Claude 모델이 돌아간다.

## 왜 이게 지금 화제인가

Microsoft 365 Copilot은 2023년부터 있었다. Word에서 문장 제안하고, Excel에서 함수 추천하는 정도. 솔직히 쓸 만한 기능이 많지 않았다는 얘기를 주변에서 많이 들었다.

Cowork는 결이 다르다. 6월 16일 GA(정식 서비스 시작) 발표 내용을 요약하면:

- **멀티스텝 자율 실행**: "이 보고서 만들어서 팀장한테 이메일로 보내줘" 같은 여러 단계 작업을 한 번의 지시로 처리
- **앱을 넘나들며 작동**: Outlook, Excel, Teams, SharePoint, Calendar 전부 연결
- **백그라운드 실행**: 노트북 꺼도 클라우드에서 계속 돌아간다
- **Claude 통합**: Copilot Chat에서 모델 선택기로 Claude를 직접 선택 가능

클로드가 Microsoft 공식 업무 도구에 들어왔다는 게 포인트다. 사용자 입장에서는 ChatGPT 계열(GPT-5)이냐 Claude냐를 업무 성격에 따라 고를 수 있다.

## 실제로 이렇게 쓴다

Copilot Chat 열면 모델 선택기가 생겼다. 여기서 Claude를 고르면 된다.

어느 모델을 언제 쓰면 좋은지 공식 가이드 기준으로 정리하면:

- **Claude 선택 → 긴 문서 분석, 구조화된 보고서 작성, 복잡한 다단계 지시**
- **GPT-5 선택 → 빠른 답변, 간단한 요약, 이미지 분석**

Cowork 자체 기능을 쓰려면 IT 부서가 Microsoft 365 관리 센터에서 먼저 활성화해야 한다. 개인이 직접 켤 수는 없다.

**바로 써볼 수 있는 프롬프트 예시:**
```
지난주 Teams 회의 내용 정리해서 회의록 초안 만들고,
참석자 전원한테 다음 주 액션 아이템 목록이랑 같이 Outlook으로 보내줘.
```

```
이 첨부파일 3개 읽고 공통 이슈 뽑아서 경영진 보고용 요약본 만들어줘.
슬라이드 구조로 정리해서 내 OneDrive에 저장해.
```

이런 게 한 번의 지시로 처리된다는 게 Cowork의 핵심이다.

![Microsoft 365 환경에서 Copilot이 Outlook과 Teams를 연결해 자율 업무를 처리하는 흐름](https://images.unsplash.com/photo-1553877522-43269d4ea984?w=800&q=80)

## 이런 점은 아쉬웠다

대부분의 회사에서는 당장 못 쓴다. 이유가 몇 가지다.

**IT 부서 벽**: 개인이 직접 활성화 불가. 회사 IT 담당자가 없는 곳은 처음부터 막힌다.

**요금**: Microsoft 365 E3/E5에서는 사용량 기반 추가 과금이 붙는다. E7 요금제($99/user/월)에서만 기본 포함인데, 한 명당 14만 원이 넘는다. 팀 전체에 적용하면 만만찮다.

**한국어 최적화 미지수**: GA 발표에 한국어 관련 언급이 없었다. Teams 실시간 번역 정확도는 개선됐다는 발표가 있었는데, Cowork의 한국어 지시 처리 수준은 직접 써봐야 안다. 영어로 프롬프트 넣으면 더 잘 돌아갈 가능성이 높다.

**데이터 보안 우려**: 회사 문서를 AI가 자율로 처리하는 구조라, 민감한 정보 취급 기준이 명확하지 않으면 IT·법무 쪽에서 제동 걸릴 수 있다.

## 한 줄 정리

Claude를 등에 업은 Microsoft가 "진짜 업무 자동화 AI"를 꺼냈는데, 써보려면 회사 IT 부서 설득부터 해야 한다.

---

다음엔 Gemini 2.5 Pro의 Deep Think 모드가 일반인한테 언제 쓸 만한지 다룰 예정이다.

**참고 링크**
- [Copilot Cowork 정식 출시 공식 블로그](https://www.microsoft.com/en-us/microsoft-365/blog/2026/06/16/copilot-cowork-is-now-generally-available/)
- [Microsoft 365 Copilot 한국어 페이지](https://www.microsoft.com/ko-kr/microsoft-365-copilot)
- [Copilot Cowork 사용 시작 가이드](https://adoption.microsoft.com/ko-kr/copilot/cowork/ai-user/)
