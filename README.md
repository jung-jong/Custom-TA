# Custom-TA
> **강사의 시간을 돌려주고, 학생의 성장을 가시화하는** AI 맞춤형 교육 보조 플랫폼
[![Frontend](https://img.shields.io/badge/Frontend-TypeScript-3178c6?logo=typescript)](https://github.com/jung-jong/Front)
[![Backend](https://img.shields.io/badge/Backend-Python-3776ab?logo=python)](https://github.com/jung-jong/Back)
[![Live Demo](https://img.shields.io/badge/Live-Demo-37b1b1)](https://custom-ta.vercel.app/)
---
## 서비스 한 줄 소개
강사가 올린 강의 자료를 AI가 학습하여, **학생 질의응답 자동화**와 **맞춤 퀘스트 생성**을 제공하고,  
**학생 성취도 객관 지표**를 강사에게 실시간으로 제공하는 교육 특화 RAG AI 플랫폼입니다.
---
## 핵심 Pain Point & 해결
| 대상 | 문제 | Custom-TA의 해결 |
|------|------|-----------------|
| 강사 | 반복 질의로 낭비되는 수업 외 시간 | 강의 자료 기반 AI가 24/7 학생 질문 자동 응답 |
| 강사 | 학생 개별 수준 파악 불가 | 참여율·정답률·취약 키워드 대시보드 제공 |
| 강사 | 문제 출제에 드는 높은 시간·비용 | AI 문제 초안 자동 생성 → 강사는 검토만 |
| 강사 | 범용 AI와 강의 방향성 불일치 | 강사 자료만 학습한 전용 RAG 지식 베이스 구축 |
| 학생 | 수업 외 질문 창구 부재 | 언제든 강의 자료 기반 AI에게 즉시 질문 |
| 학생 | 자기 약점·진도를 객관적으로 모름 | XP·퀘스트 결과 기반 성취도 지표 시각화 |
---
## 시스템 아키텍처
```
[학생 / 강사 브라우저] 
        │ 
        ▼
[Frontend — React + TypeScript + Vite]
        │ (Vercel 배포) 
        │ REST API / Bearer Token
        ▼
[Backend — FastAPI + Python]
        ├── 인증 서버 (JWT)
        ├── RAG 엔진 (강의 자료 벡터 인덱싱)
        ├── LLM 연동 (질의응답 / 문제 생성)
        └── 분석 엔진 (성취도·취약점 집계)
        │
        ▼
[Database / Storage]
        ├── 관계형 DB (사용자·강의·퀘스트)
        └── 벡터 DB (RAG 임베딩 인덱스)
```
---
## 레포지토리
| 구분 | 링크 | 기술 스택 |
|------|------|-----------|
| **Frontend** | [바로가기](https://github.com/jung-jong/Front) | React 19, TypeScript, Tailwind CSS, Vite |
| **Backend** | [바로가기](https://github.com/jung-jong/Back) | Python, FastAPI, RAG, LLM |
---
## 배포 주소 (Live Demo)
> [https://custom-ta.vercel.app](https://custom-ta.vercel.app/)
---
## 사용자 흐름
### 강사
회원가입(강사) → 강의 개설 → 수강 코드 발급 → 강의 자료 업로드 (RAG 인덱싱 자동 진행) → AI 퀘스트 초안 생성 → 검토 후 배포 → 대시보드에서 학생 성취도 모니터링

### 학생
회원가입(학생) → 수강 코드 입력 → 강의 입장 → AI 채팅으로 질문 → 출처 포함 답변 수신 → 퀘스트 수행 → XP 획득 → 성취도 확인

