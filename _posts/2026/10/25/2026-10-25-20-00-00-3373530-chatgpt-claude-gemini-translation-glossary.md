---
layout: post
title: "ChatGPT·Claude·Gemini 번역 용어집 검수 - 로컬라이제이션 담당자가 오류표 만드는 법"
description: "번역·로컬라이제이션 담당자가 ChatGPT·Claude·Gemini로 용어집과 번역문을 대조하고, 오류 근거·수정안·무료와 유료 선택 기준을 검수표로 정리한다."
date: 2026-10-25
tags: [ChatGPT, Claude, Gemini, 업무자동화, 프롬프트, 번역]
comments: true
share: true
---
![번역 용어집과 번역문을 대조해 오류 검수표를 만드는 로컬라이제이션 업무 화면](https://images.unsplash.com/photo-1455390582262-044cdead277a?auto=format&fit=crop&w=1400&q=80)

이 그림에서 볼 부분은 AI가 번역을 승인하는 장면이 아니라, 용어집·원문·번역문을 나란히 놓고 사람이 확인할 행을 줄이는 흐름이다.

제품 화면이나 기술 문서를 여러 언어로 관리하는 담당자라면 ChatGPT·Claude·Gemini 무료 플랜으로 **승인 용어 누락, 금지 표현, 숫자·태그 불일치가 표시된 검수표**부터 만들 수 있다. 문장 전체를 새로 번역해 달라고 맡기는 방식보다 결과를 확인하기 쉽다. 법률·의료·안전 문서, 공개 전 제품명처럼 오류 비용이 큰 자료를 개인 계정에 원문 그대로 올리는 경우에는 이 방법을 적용하지 않는다.

## 용어집 검수의 결과물

번역 품질은 자연스러움 하나로 판단하기 어렵다. 같은 원문 용어가 문서마다 다르게 번역되거나, 제품명·변수·숫자가 바뀌면 실제 배포에서 문제가 된다. 번역 일관성은 같은 대상에 같은 표현을 쓰는지 확인하는 항목이며, 특히 기술 용어와 반복 문구에서 중요하다는 설명도 있다([University of Michigan CCSG 용어 일관성 안내](https://ccsg.isr.umich.edu/glossary/consistency/)).

| 입력 | AI가 만들 표 | 사람이 확인할 것 |
|---|---|---|
| 원문 문장, 번역문, 승인 용어집 | 원문 용어·승인 표현·실제 표현·판정·근거 | 문맥, 조사·활용, 제품명 |
| 금지 표현 목록 | 금지 표현 발견 위치·대체안 | 금지 사유와 최신 정책 |
| 숫자·단위·자리표시자 | 원문 값·번역 값·불일치 유형 | 소수점, 통화, 변수 보존 |

## 복사해서 쓰는 검수 프롬프트

파일을 올리기 전에 이름, 고객명, 미공개 제품명과 계약 내용을 가상 값으로 바꾼다. CSV는 `segment_id, source, target` 열을 유지하고, 용어집은 `source_term, approved_target, forbidden_variant, note`처럼 한 행에 한 용어를 둔다. OpenAI도 파일 분석에서 설명적인 열 이름과 레코드당 한 행을 권장한다([ChatGPT 데이터 분석 안내](https://help.openai.com/ko-kr/articles/8437071-data-analysis-with-chatgpt)).

```text
너는 번역 QA 보조자다. 번역을 승인하거나 전체 문장을 다시 쓰지 마라.
[용어집]의 승인 표현과 금지 표현만 기준으로 [번역 데이터]를 검사하라.
원문에 없는 오류를 추측하지 말고, 판단할 수 없으면 '확인 필요'라고 표시하라.
다음 열의 표로만 출력하라:
segment_id | source_term | approved_target | actual_target | 판정(통과/수정/확인 필요) | 근거 | 수정안
숫자, 통화, HTML 태그, {변수}, 고유명사는 원문과 보존됐는지도 별도 판정하라.
```

핵심은 `수정안`보다 `근거` 열이다. 예를 들어 실제 표현이 승인 용어와 다르다는 사실, 숫자 하나가 빠졌다는 사실, 아니면 문맥상 허용되는 변형인지 구분해야 재검수 때 같은 오류를 반복하지 않는다. 번역 전문 용어 관리는 용어집뿐 아니라 스타일 가이드와 사람의 검토를 함께 쓰는 작업이라는 점도 기억할 필요가 있다([CIOL 번역 기술 용어집](https://www.ciol.org.uk/node/6404)).

## 무료와 유료를 가르는 기준

| 상황 | 시작할 선택 | 유료·업무용을 검토할 순간 |
|---|---|---|
| 공개 샘플 10~30문장, 월 1~2회 | 세 도구 중 회사가 허용한 무료 계정 | 사람 수정 행 수를 기록 |
| 언어별 파일 5개 이상, 매주 반복 | ChatGPT 프로젝트·Gemini 업로드·Claude 프로젝트를 소량 비교 | 업로드 한도와 문맥 유지가 병목일 때 |
| 고객 문서·미공개 소스·규제 문서 | 회사 승인 환경 또는 번역 QA 도구 | 개인용 유료 계정으로 해결하려 하지 않음 |

확인 날짜는 2026년 10월 25일이다. ChatGPT는 무료 사용자도 파일 업로드가 가능하지만 별도 사용 한도가 있고, 프로젝트 파일은 무료 5개·Plus/Go 25개·일부 상위 플랜 40개로 안내한다([OpenAI 파일 업로드 안내](https://help.openai.com/en/articles/8555545-uploading-files-and-audio-to-chatgpt), [Projects 제한](https://help.openai.com/en/articles/10169521-projects-in-chatgpt)). Claude는 CSV와 XLSX를 지원하지만 파일당 30MB 제한과 요금제별 사용량이 있다([Claude 문서 업로드 안내](https://support.anthropic.com/en/articles/8241126-what-kinds-of-documents-can-i-upload-to-claude-ai), [Claude 요금제](https://support.anthropic.com/en/articles/11049762-choosing-a-claude-ai-plan)). Gemini는 한 프롬프트 최대 10개 파일, 일반 파일 100MB 조건을 안내하며 상위 Google AI 플랜에서 더 높은 한도를 제공한다([Gemini 파일 분석 안내](https://support.google.com/gemini/answer/14903178?hl=en-gw)). 이 숫자는 계정·지역·정책에 따라 바뀔 수 있다.

개인용 데이터 처리 조건도 무료와 유료만으로 판단하면 안 된다. OpenAI 개인 플랜은 설정에 따라 모델 개선에 사용될 수 있어 `Improve the model for everyone`을 확인해야 한다. Gemini는 Keep Activity가 켜진 경우 일부 대화가 사람 검토에 사용될 수 있다고 안내한다. Claude도 소비자 서비스와 Claude for Work의 조건이 다르다([OpenAI 데이터 사용 안내](https://help.openai.com/en/articles/5722486-how-your-data-is-used-to-improve-model-performance), [Gemini 개인정보 허브](https://support.google.com/gemini/answer/13594961?hl=en), [Anthropic 민감정보 안내](https://support.anthropic.com/en/articles/8325621-i-would-like-to-input-sensitive-data-into-free-claude-ai-or-my-pro-max-account-who-can-view-my-conversations)).

## 발행 전 검수 체크리스트

- [ ] 승인 용어집과 금지 표현의 버전을 기록했다.
- [ ] 숫자·단위·변수·태그를 별도 열로 확인했다.
- [ ] AI가 수정한 행이 아니라 사람이 재확인할 행을 분리했다.
- [ ] 10~30문장 샘플에서 누락 행 수와 수정 시간을 기록했다.
- [ ] 원문 업로드가 허용된 계정인지, 개인정보·기밀이 제거됐는지 확인했다.

정리하면, 번역 업무에서 유료 AI를 살 이유는 “더 자연스러운 문장”보다 반복 파일과 긴 용어집을 안정적으로 유지해야 하는지에 있다. 무료 샘플에서 `근거가 있는 오류표`가 만들어지는지부터 확인하고, 오류 누락과 업로드 제한이 실제 병목일 때만 유료 또는 전문 CAT 도구를 검토하는 편이 낫다.
