---
layout: post
title: "ChatGPT·Claude·Gemini UTM CSV 검수 - 마케팅 담당자가 캠페인 누락표 만드는 법"
description: "마케팅 담당자가 UTM CSV의 누락·오타·규칙 위반을 ChatGPT·Claude·Gemini로 찾아 검수표로 만드는 방법과 무료·유료 선택 기준을 정리한다."
date: 2026-10-22
tags: [ChatGPT, Claude, Gemini, 업무자동화, 프롬프트, AI분석]
comments: true
share: true
---

![UTM 캠페인 CSV를 AI 검수표로 바꾸는 마케팅 업무](https://images.unsplash.com/photo-1551288049-bebda4e38f71?auto=format&fit=crop&w=1400&q=80)

매주 광고·뉴스레터·SNS 링크의 UTM CSV를 확인한다면 ChatGPT·Claude·Gemini 무료 기능으로 `누락 행 / 규칙 위반 / 확인 필요` 표를 만들 수 있다. 고객 식별자나 매출 원본을 그대로 업로드하거나 AI 결과만 믿고 성과를 확정하는 경우에는 적용하지 않는다.

Google Analytics는 `utm_id`, `utm_source`, `utm_medium`, `utm_campaign` 등으로 유입 캠페인을 구분한다. 실제 오류는 값이 아예 없는 경우보다 `facebook`과 `Facebook`, `paid-social`과 `paid_social`처럼 팀 규칙이 섞이는 데서 생긴다.

| 검수 항목 | AI가 찾을 후보 | 사람이 확인할 것 |
|---|---|---|
| 누락 | 필수 UTM이 빈 행 | 실제 링크가 발행됐는지 |
| 표기 차이 | 대소문자·하이픈·공백 혼용 | 팀의 표준 사전 |
| 불일치 | 매체와 목적이 어긋난 값 | 광고 설정 |
| URL 오류 | `?`·`&` 또는 랜딩 주소 문제 | 실제 링크와 GA4 |

## 복사해서 쓰는 프롬프트

CSV를 올리기 전에 이름, 이메일, 주문번호, 매출액을 가명 또는 범주값으로 바꾼다.

```text
너는 마케팅 데이터 검수 보조자다. 첨부한 UTM CSV를 아래 규칙으로 검사해 표 하나로 출력해줘.

필수 열: landing_url, utm_id, utm_source, utm_medium, utm_campaign
허용 source: google, meta, naver, newsletter
허용 medium: cpc, paid-social, organic, email
규칙: 값 앞뒤 공백 금지, 영문 소문자, 날짜는 YYYY-MM-DD

열은 행번호 / 판정 / 문제 유형 / 해당 값 / 수정 제안 / 근거 열로 고정해. 원문에 없는 의도나 성과는 추측하지 말고, 근거가 없으면 '확인 필요'로 표시해. 마지막에 정상 행 수와 검수 필요 행 수를 세어줘.
```

결과의 `수정 제안`만 복사하고 원본은 덮어쓰지 않는다. URL 오류는 실제 링크를 열어 확인한다. UTM이 있다고 전환 데이터가 자동으로 정확해지는 것도 아니다.

## 무료로 시작할 조건과 유료 전환선

확인 날짜는 2026년 10월 22일이다. ChatGPT 무료 플랜은 파일 업로드가 가능하지만 하루 3회 제한과 별도 도구 한도가 있다. Gemini는 한 번에 최대 10개 파일을 올릴 수 있고, 유료 요금제는 더 높은 사용량을 제공한다. Claude도 CSV를 지원하지만 파일 크기·대화 수·모델별 한도가 달라진다.

| 상황 | 선택 |
|---|---|
| 월 1~4회, 100행 안팎, 가명 CSV | 무료 플랜으로 샘플 1개부터 검증 |
| 매일 여러 파일 | 업로드 한도가 병목인지 기록한 뒤 유료 검토 |
| 고객·매출 원본 | 개인 계정 대신 회사 승인 환경 확인 |

Gemini 개인 앱은 일부 대화가 사람 검토 대상이 될 수 있다. Claude for Work는 고객 조직이 데이터 관리 주체이고 상업용 데이터로 모델을 학습하지 않는다고 설명한다. 개인 계정에는 기밀 CSV를 넣지 않는 기준이 안전하다.

## 발행 전 검수 체크리스트

- [ ] 필수 UTM 열과 허용값 사전을 팀 문서에 고정했다
- [ ] AI 결과에 행번호와 근거 열이 붙어 있다
- [ ] `확인 필요` 행을 원본 링크에서 다시 열었다
- [ ] GA4 보고서의 캠페인 이름과 표기 규칙을 대조했다
- [ ] 수정본과 원본을 별도 파일로 보관했다

UTM 자동화의 결과물은 AI 성과 분석 문장이 아니라 사람이 다시 확인할 오류 목록이다. 하루 몇 건이면 무료 플랜과 가명 데이터로 시험하고, 유료 결제는 업로드 한도와 팀 보안 설정이 실제 병목일 때 검토한다.

참고한 공식 문서: [Google Analytics URL Builder](https://support.google.com/analytics/answer/10917952), [ChatGPT 파일 업로드](https://help.openai.com/en/articles/8555545-uploading-files-and-audio-to-chatgpt), [Gemini 파일 업로드](https://support.google.com/gemini/answer/14903178), [Claude 문서 업로드](https://support.anthropic.com/en/articles/8241126-what-kinds-of-documents-can-i-upload-to-claude-ai)
