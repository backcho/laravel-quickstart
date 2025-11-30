---
layout: default
title: 04. 서비스 공개 (ngrok)
nav_order: 5
permalink: /04-deploy/
---

# 04. 서비스 공개 (ngrok)

> 목표: 로컬 개발 환경을 외부에서 접근 가능하게 공개

MVP를 만들었다면 피드백을 받아야 합니다. ngrok을 사용하면 로컬 환경을 외부에 임시로 공개할 수 있습니다.

---

## ngrok 설치 및 설정

### 1. 회원가입

1. [https://ngrok.com](https://ngrok.com) 접속
2. 무료 회원가입
3. Dashboard에서 Authtoken 확인

### 2. 설치

**Mac:**
```bash
brew install ngrok
```

**Windows:**
[https://ngrok.com/download](https://ngrok.com/download)에서 다운로드

### 3. 인증

```bash
ngrok config add-authtoken YOUR_AUTH_TOKEN
```

---

## 사용법

```bash
# Herd/Laragon 사용 시 (기본 포트 80)
ngrok http 80

# artisan serve 사용 시
ngrok http 8000

# 특정 도메인으로 터널링 (Herd/Valet)
ngrok http --host-header=my-project.test 80
```

실행하면 다음과 같은 URL을 받습니다:
```
https://abc123.ngrok-free.app
```

이 URL을 공유하면 됩니다!

---

## 피드백 받기

### 테스트 계정 준비

외부에 공유하기 전에 시더로 테스트 계정을 만들어두세요:

```
AI에게 요청:

테스트 계정 시더를 만들어줘.
- 일반 사용자: test@example.com / password123
- 관리자: admin@example.com / password123
```

### URL 공유 시 안내 예시

```
MVP 테스트 링크: https://abc123.ngrok-free.app

테스트 계정:
- 일반 사용자: test@example.com / password123
- 관리자: admin@example.com / password123

피드백 부탁드려요:
- 회원가입/로그인이 잘 되나요?
- 게시글 작성/수정/삭제가 정상 동작하나요?
- (관리자) 대시보드가 잘 보이나요?
```

---

## 대안: Cloudflare Tunnel

```bash
# 설치 (Mac)
brew install cloudflared

# 빠른 터널 (계정 없이)
cloudflared tunnel --url http://localhost:80
```

장점: 완전 무료, 브랜딩 페이지 없음

---

## 다음 단계: 실제 배포

MVP 피드백을 받고 서비스가 검증되었다면, 실제 서버에 배포할 차례입니다.

### 저비용 배포 옵션

- **Vultr / DigitalOcean**: 월 $5~6부터
- **AWS Lightsail**: 월 $3.5부터
- **Laravel Forge**: 서버 관리 자동화

---

## 다음 단계

서비스를 외부에 공개했습니다! [05. 보너스: UI 커스텀](./05-ui-custom)에서 UI를 커스터마이징하는 방법을 알아봅니다.
