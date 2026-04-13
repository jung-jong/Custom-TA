# Custom-TA
AI 기반 맞춤형 교육 보조 플랫폼

# Custom-TA
> **강사의 시간을 돌려주고, 학생의 성장을 가시화하는** AI 맞춤형 교육 보조 플랫폼
[![Frontend](https://img.shields.io/badge/Frontend-TypeScript-3178c6?logo=typescript)](프론트엔드_링크)
[![Backend](https://img.shields.io/badge/Backend-Python-3776ab?logo=python)](백엔드_링크)
[![Live Demo](https://img.shields.io/badge/Live-Demo-37b1b1)](배포_URL)
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
[학생 / 강사 브라우저] │ ▼ [Frontend — React + TypeScript + Vite] ← Vercel 배포 │ REST API (Bearer Token) ▼ [Backend — FastAPI + Python] ├── 인증 서버 (JWT) ├── RAG 엔진 (강의 자료 벡터 인덱싱) ├── LLM 연동 (질의응답 / 문제 생성) └── 분석 엔진 (성취도·취약점 집계) │ ▼ [Database / Storage] ├── 관계형 DB (사용자·강의·퀘스트) └── 벡터 DB (RAG 임베딩 인덱스)

---
## 레포지토리
| 구분 | 링크 | 기술 스택 |
|------|------|-----------|
| **Frontend** | [바로가기](프론트엔드_링크) | React 19, TypeScript, Tailwind CSS, Vite |
| **Backend** | [바로가기](백엔드_링크) | Python, FastAPI, RAG, LLM |
---
## 배포 주소 (Live Demo)
> [https://배포주소.vercel.app](배포주소)
---
## 주요 화면
| 화면 | 설명 |
|------|------|
| ![랜딩](스크린샷_링크) | 서비스 소개 랜딩 페이지 |
| ![학생 워크스페이스](스크린샷_링크) | 3-column AI 채팅 + 퀘스트 + 자료 |
| ![강사 대시보드](스크린샷_링크) | 성취도 분석 및 퀘스트 관리 |
---
## 팀 정보
| 이름 | 역할 |
|------|------|
| (이름) | Frontend |
| (이름) | Backend / AI |
