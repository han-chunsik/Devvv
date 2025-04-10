# ADR 0001: 초기 기술 스택 및 MVP 1차 범위 정의

Status: accepted    
Deciders: 한성경   
Date: 2025-04-10    
Technical Story: MVP를 빠르게 개발하고 기능의 방향성과 기술 스택을 명확히 정의하기 위함   

---

## 상황 및 문제 설명 (Context and Problem Statement)

개발 생산성 도구 + 커뮤니티 기능을 갖춘 생산성 서비스 **devvv** 의 MVP를 개발하려고 한다.    
빠른 개발과 구조 확장을 고려하여, 어떤 기술 스택과 기능을 선택할지 결정이 필요했다.    
  
- 질문: MVP를 어떤 기술 스택과 기능 범위로 시작하는 것이 가장 효율적인가?

---

## 결정에 영향을 준 요소들 (Decision Drivers)
- 빠른 개발 속도와 MVP 완성
- 본인이 익숙한 기술 스택 활용
- 확장 가능성과 운영 편의성
- 다양한 소도구 기능의 빠른 구현
- 커뮤니티 기능 포함으로 인한 최소한의 인증/권한 체계 필요

---

## 고려했던 옵션들 (Considered Options)
1. Java(Spring Boot) + MySQL + Swagger + Go(CLI)  
2. Python(FastAPI) + SQLite + No CLI 구현

---

## 결정 결과 (Decision Outcome)
선택한 옵션: **"1. Java(Spring Boot) + MySQL + Swagger + Go(CLI)"**    
→ 이유: 가장 익숙한 기술 스택이며, 운영/배포 측면에서 안정적이고 문서화/CLI도 빠르게 구현 가능함.

---

## 긍정적인 결과 (Positive Consequences)
- 빠른 개발 진행 가능
- 본인에게 익숙한 기술이라 리스크 적음
- CLI 도구가 Go로 단일 바이너리로 배포 가능

---

## 부정적인 결과 (Negative Consequences)
- Spring Boot 초기 설정 비용이 살짝 있음
- 프론트엔드가 미정이라 API 인터페이스 설계 시 더 유연성이 요구됨

---
## 옵션별 장단점 (Pros and Cons of the Options)
### Option 1: Java(Spring Boot) + MySQL + Swagger + Go(CLI)

좋은 점:  
- 익숙하게 사용할 수 있는 기술
- Go로 CLI 만들면 배포 용이 (단일 바이너리)
- Swagger로 API 문서 자동화 쉬움

안 좋은 점:  
- 설정이 간단하지는 않음 (Spring 특유의 초기 세팅)
- 프론트엔드 결정되지 않아 백엔드만으로 테스트해야 함

---
### Option 2: Python(FastAPI) + SQLite

좋은 점:  
- 초경량 MVP에 적합
- 개발 빠르고 진입 장벽 낮음

안 좋은 점:  
- 실제 운영 단계에선 DB/인증 구조 교체가 필요함
- CLI와 잘 어울리는 구조 설계가 필요

---

## 링크 (Links)
- [기능 정의 문서 (작성중)]()
