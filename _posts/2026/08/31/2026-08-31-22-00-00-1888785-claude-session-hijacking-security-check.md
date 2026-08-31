---
layout: post
title: "Claude 로그인 세션 탈취 경고 - 사용량이 갑자기 줄었다면 지금 확인할 것"
description: "Anthropic이 Claude 로그인 세션을 훔쳐 사용량을 소진하는 악성코드를 경고했다. 비밀번호 변경만으로 끝나지 않는 이유와 일반 사용자의 점검·복구 순서를 정리했다."
date: 2026-08-31
tags: [Claude, AI뉴스, Anthropic, AI보안, AI입문, 업무자동화]
comments: true
share: true
---

![Claude 로그인 세션 탈취와 계정 보안 경고를 표현한 일러스트](https://images.unsplash.com/photo-1563013544-824ae1b704d3?auto=format&fit=crop&w=1200&q=80)

Claude 사용량이 내가 쓰지 않았는데 빠르게 줄었다면 표시 오류로 넘기면 안 된다. 2026년 8월 30일 Anthropic은 감염된 컴퓨터에서 Claude 로그인 세션을 훔쳐 사용량을 소진한 사례를 알렸다. 비밀번호가 아니라 이미 로그인된 브라우저 상태를 가져간 방식이다.

## 무슨 일이 있었나

BleepingComputer에 따르면 Vidar, LummaC2, StealC, RedLine 같은 infostealer(비밀번호·쿠키를 훔치는 악성코드)가 Claude 세션도 수집했다. 공격자는 비밀번호나 2단계 인증 없이 세션을 재사용할 수 있다. Claude 자체보다 PC 감염이 먼저였을 가능성이 크다.

| 보이는 현상 | 바로 할 일 |
|---|---|---|
| 사용하지 않았는데 사용량 급감 | 계정 활동·결제 확인 |
| 낯선 결제 또는 카드 알림 | 카드 잠금·Anthropic 문의 |
| 로그아웃 후에도 이상함 | 해당 PC에서 재로그인하지 않기 |

## 비개발자용 복구 순서

Claude를 쓰던 PC에서 로그아웃한다. 다른 깨끗한 기기에서 Claude와 이메일 비밀번호를 바꾸고, 계정 설정에서 다른 세션을 취소한다. 비밀번호만 바꿔서는 부족할 수 있다. 훔친 세션은 별도로 살아 있기 때문이다.

저장된 결제수단과 최근 사용량도 확인한다. Anthropic은 영향을 받은 계정을 로그아웃시키고 결제수단을 제거하며 무단 결제를 환불한다고 안내했다. 카드 명세서도 확인한다.

감염 가능성이 있는 PC는 Windows 보안 전체 검사와 운영체제·브라우저 업데이트를 진행한다. 불법 게임, 비공식 패치, 출처 불명의 AI 앱을 설치했다면 전문가에게 점검받는다. Mac에서도 Atomic Stealer(AMOS) 사례가 언급됐다.

## 앞으로 바꿀 습관

공용 PC에서는 사용 후 로그아웃하고, “무료 Claude 앱”이나 크랙 파일은 설치하지 않는다. 사용량이 회복됐다가 다시 빠지면 요금제 오류로 단정하지 않는다. 같은 PC의 Gmail·메신저·결제 서비스도 함께 점검한다.

2단계 인증은 필요하지만 이미 인증된 세션 탈취까지 막지는 못한다. 사용량 급감은 이상 신호다. 다른 기기에서 세션을 정리하고 감염된 PC에서는 다시 로그인하지 않는다.

출처: [BleepingComputer의 Anthropic 경고 보도](https://www.bleepingcomputer.com/news/artificial-intelligence/anthropic-warns-infostealer-malware-is-hijacking-claude-sessions-to-drain-usage/), [Anthropic 보안 취약점 공개 대시보드](https://red.anthropic.com/2026/cvd/)
