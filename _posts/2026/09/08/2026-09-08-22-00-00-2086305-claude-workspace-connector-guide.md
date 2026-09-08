---
layout: post
title: "Claude 커넥터 사용법 - Gmail·캘린더·문서를 한 번에 정리하는 실전 흐름"
description: "2026년 9월 업데이트된 Claude Workspace 커넥터 사용법을 정리했다. Gmail, Google Calendar, Drive와 Microsoft 365를 연결해 메일·일정·문서를 정리하는 프롬프트와 주의사항을 담았다."
date: 2026-09-08
tags: [Claude, 업무자동화, AI요약, 프롬프트, 직장인AI, AI뉴스, Anthropic]
comments: true
share: true
---

![Claude 커넥터로 이메일·캘린더·문서를 연결하는 업무 흐름](/images/2026-09-08-claude-workspace-connector.png)

이 그림에서 봐야 할 점은 Claude가 답변만 만드는 도구가 아니라, 연결한 메일·일정·문서에서 맥락을 모아 다음 일을 정리하는 창구가 된다는 것이다.

최근 Claude에는 Gmail·Google Calendar·Google Drive를 연결해 대화 안에서 메일을 찾고, 일정을 관리하고, 문서를 다루는 기능이 들어갔다. Microsoft 365도 Outlook, OneDrive, SharePoint, Teams 검색을 지원한다. 특히 관리자가 write tools(메일 발송·일정 변경·파일 작성 권한)를 켜면 Claude가 실제 작업까지 이어갈 수 있다는 점이 이번 변화의 핵심이다. [Claude 공식 도움말](https://support.claude.com/en/articles/10166901-use-google-workspace-connectors)과 [Microsoft 365 연결 안내](https://support.claude.com/en/articles/15183774-connect-to-microsoft-365)에서 확인한 2026년 9월 기준 내용이다.

## 연결하면 어디에 쓰나

처음에는 메일을 검색하는 정도로 생각했는데, 실제로 유용한 건 서로 다른 자료를 한 요청에 묶는 방식이다. 예를 들어 회의 전 준비라면 캘린더의 참석자와 시간을 확인하고, 관련 메일과 Drive 문서를 찾아 한 장짜리 브리핑으로 만들 수 있다.

| 하고 싶은 일 | Claude에게 맡길 요청 |
|---|---|
| 지난 회의 정리 | 지난 7일간 해당 프로젝트 메일과 문서를 찾아 결정사항·미해결 과제 정리 |
| 고객 미팅 준비 | 캘린더의 내일 미팅을 기준으로 최근 메일, 제안서, 고객 요청을 5개 항목으로 요약 |
| 일정 후속 조치 | 오늘 회의 관련 메일을 찾아 담당자별 할 일과 마감일을 표로 작성 |
| 파일 찾기 | Drive 또는 OneDrive에서 키워드와 날짜를 기준으로 최신 문서 3개 비교 |

## 실제로 쓰는 프롬프트

커넥터를 켠 뒤에는 범위와 결과 형식을 같이 지정하는 게 좋다. “관련 자료 찾아줘”라고만 쓰면 자료가 너무 많이 섞인다.

```text
내일 오전 10시 ‘신규 서비스’ 캘린더 일정에 맞춰 회의 브리핑을 만들어줘.
지난 30일의 관련 Gmail과 Google Drive 문서만 참고해.
참석자, 지금까지 합의한 내용, 상대방의 미해결 질문,
내가 회의에서 확인할 질문 3개를 표로 정리하고
각 항목 뒤에 출처 파일명이나 메일 제목을 붙여줘.
확인되지 않은 내용은 추측하지 말고 ‘확인 필요’라고 표시해.
```

회의가 끝난 뒤에는 아래처럼 후속 작업을 분리한다.

```text
방금 회의와 관련된 오늘 메일을 찾아줘.
결정사항과 할 일을 분리하고, 할 일은 담당자·기한·근거 메일로 정리해.
메일 발송이나 일정 변경은 하지 말고 초안과 변경 후보만 보여줘.
```

이렇게 요청하면 AI가 바로 보내버리는 실수를 줄일 수 있다. 초안 확인 후 “내게만 테스트 메일로 보내”처럼 작은 작업부터 권한을 확인하는 편이 안전하다.

## 연결 전에 확인할 것

Google 계정은 Claude의 Connectors 메뉴에서 Gmail, Calendar, Drive를 각각 인증하면 된다. Microsoft 365는 회사용 Entra 계정과 관리자 동의가 필요하다. 개인 Outlook 계정으로는 연결되지 않는다. 조직에서 write tools를 허용하지 않았다면 검색·분석만 가능하다.

메일 첨부파일은 현재 write tools로 보내거나 전달할 수 없다. Claude가 보낸 메일에는 agent-initiated라는 표시가 붙지만, 파일·캘린더 변경은 같은 방식으로 눈에 띄게 표시되지 않을 수 있다. 민감한 인사·계약 자료를 연결할 땐 내가 볼 수 있는 자료만 Claude도 볼 수 있다는 권한 구조를 확인하고, 자동 실행보다 승인 요청을 기본값으로 두는 게 낫다.

짧게 정리하면, Claude 커넥터는 “자료를 올려서 요약”하는 기능보다 “메일·일정·문서 사이를 오가며 업무 맥락을 만드는” 기능에 가깝다. 오늘 바로 쓴다면 회의 브리핑 검색부터 시작하고, 메일 발송과 일정 변경은 초안 검수 뒤에 단계적으로 열면 된다.

출처: [Claude Google Workspace 커넥터 공식 안내](https://support.claude.com/en/articles/10166901-use-google-workspace-connectors), [Claude Microsoft 365 연결 공식 안내](https://support.claude.com/en/articles/15183774-connect-to-microsoft-365), [Microsoft 365 write tools 설정 안내](https://support.claude.com/en/articles/12542951-set-up-the-microsoft-365-connector)
