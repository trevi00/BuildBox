# BuildBox 기획서

## 🔰 프로젝트 명
**BuildBox**  
AI 기반 DevOps 자동화 SaaS 플랫폼

---

## 1️⃣ 프로젝트 개요

BuildBox는 사용자가 선택한 템플릿(블로그, 쇼핑몰 등)을 기반으로 프로젝트를 생성하고,  
GitHub 연동을 통해 자동 빌드 및 배포 과정을 수행하며,  
OpenAI API를 통해 코드 리뷰 및 문서 생성을 지원하는 개발자 친화형 DevOps 플랫폼입니다.

---

## 2️⃣ 기획 배경

| 문제점 | 해결 방안 |
|--------|------------|
| GitHub 프로젝트의 초기 설정 및 배포가 번거로움 | 자동화된 템플릿 기반 생성 및 CI/CD 구성 |
| 코드 품질 관리가 어렵고 리뷰 자원이 부족함 | ChatGPT 기반 코드 리뷰 및 문서 지원 |
| 백엔드 중심 개발자의 DevOps 실습 환경 부족 | Docker + 배포 + 모니터링 구성 실습 가능 플랫폼 제공 |

---

## 3️⃣ 주요 기능 요약

| 기능 | 설명 |
|------|------|
| 회원 가입 / 로그인 | JWT 기반 인증 + GitHub OAuth 연동 |
| 템플릿 선택 프로젝트 생성 | 블로그/쇼핑몰/예약 시스템 등 |
| GitHub 연동 및 Webhook 등록 | 커밋 → 자동 빌드 트리거 |
| ChatGPT API 연동 | 코드 리뷰, 문서화, 코드 설명 |
| 배포 기능 | Docker Compose + Nginx 기반 |
| 빌드 로그 및 모니터링 | Prometheus + Grafana 기반 로그 확인 |

---

## 4️⃣ 시스템 아키텍처 요약

사용자 → 프론트엔드 → 백엔드 API 서버  
백엔드 ↔ DB, Docker 빌더, OpenAI API  
Webhook ↔ GitHub 커밋 트리거  
빌드 후 배포 → Nginx + Docker  
배포된 상태는 모니터링 시스템으로 확인

---

## 5️⃣ 기술 스택

| 구분 | 기술 |
|------|------|
| 백엔드 | Django REST / Spring Boot |
| 프론트엔드 | React / Django Template |
| DB | PostgreSQL, Redis |
| 인증 | JWT + GitHub OAuth |
| 배포 | Docker, Docker Compose, Nginx |
| 모니터링 | Prometheus, Grafana |
| AI 연동 | OpenAI GPT API |

---

## 6️⃣ 기대 효과

- DevOps와 백엔드 개발 능력을 함께 보여줄 수 있는 실전형 포트폴리오
- 기술 트렌드(AI API, GitHub 연동, Docker 자동화)를 실제로 구현해본 경험 강조
- 확장성과 실무 유사도를 갖춘 시스템 설계 역량 어필
