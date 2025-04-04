# BuildBox

AI 기반 DevOps 프로젝트 자동화 플랫폼

## 개요

사용자가 템플릿을 선택해 프로젝트를 생성하고, GitHub 연동으로 자동 빌드 및 배포를 수행하며, ChatGPT API를 활용해 코드 리뷰와 문서 생성을 지원하는 SaaS형 DevOps 플랫폼입니다.

## 주요 기능
- 회원가입 / 로그인 (JWT)
- 템플릿 기반 프로젝트 생성
- GitHub 연동 → 자동 빌드
- ChatGPT API로 코드 리뷰/문서화
- Docker Compose 기반 배포
- 로그 및 빌드 상태 모니터링

## 기술 스택
- **Backend**: Spring Boot / Django REST Framework
- **Frontend**: React / Django Template
- **DB**: PostgreSQL, Redis
- **Auth**: JWT, GitHub OAuth
- **CI/CD**: GitHub Webhook + Docker Build
- **AI**: OpenAI API
- **Infra**: Docker, Nginx, Prometheus + Grafana

## 설계 문서
- [ERD](./docs/buildbox_erd.jpg)
- [API 명세서](./docs/api_spec.md)
- 아키텍처 다이어그램 (작성 예정)

## 프로젝트 목표
- 클라우드 인프라와 DevOps 자동화 흐름 이해
- RESTful API 설계 및 인증/배포 시스템 구현
- OpenAI API를 통한 스마트한 코드 리뷰/문서화
