# BuildBox API 명세서

## 🔐 회원 관련

### [POST] /api/register
- 설명: 회원가입
- 요청:
```json
{ "username": "devlee", "password": "securepass" }
```

### [POST] /api/login
- 설명: 로그인 (JWT 발급)
- 요청:
```json
{ "username": "devlee", "password": "securepass" }
```
- 응답:
```json
{ "token": "eyJhbGciOi..." }
```

---

## 프로젝트 관련

### [POST] /api/projects/
- 설명: 템플릿 선택 후 새 프로젝트 생성
- 요청:
```json
{ "template": "blog", "name": "MyBlog" }
```

### [GET] /api/projects/{id}/
- 설명: 프로젝트 상세 조회

### [DELETE] /api/projects/{id}/
- 설명: 프로젝트 삭제

---

## GitHub 연동

### [POST] /api/github/connect/
- 설명: GitHub OAuth 연동

### [POST] /api/github/webhook/
- 설명: GitHub Webhook 수신 → Docker 빌드 실행

---

## AI 기능

### [POST] /api/ai/assist/
- 설명: 코드 리뷰, 요약, 문서 생성
- 요청:
```json
{
  "project_id": 5,
  "request_type": "review",
  "code": "def hello(): print('hi')"
}
```

---

## 배포 관련

### [POST] /api/deploy/{project_id}/
- 설명: Docker Compose로 프로젝트 배포

### [GET] /api/deploy/{project_id}/status/
- 설명: 컨테이너 상태 확인

---

## 빌드 로그

### [GET] /api/projects/{id}/builds/
- 설명: 빌드 이력 목록

### [GET] /api/builds/{build_id}/
- 설명: 빌드 로그 상세 보기

---

## 인증 방식
- Authorization: Bearer <JWT_TOKEN>
