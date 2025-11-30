---
layout: default
title: 홈
nav_order: 1
---

# Laravel 빠른 시작 가이드

> 바이브 코더를 위한 0원 MVP 개발

## 소개

이 가이드는 **AI로 코딩하는 바이브 코더**들을 위한 Laravel 시작 가이드입니다.

Next.js + Vercel의 "딸깍 배포"에 익숙하신가요? Laravel로도 똑같이 할 수 있습니다. 게다가 **진짜 백엔드**까지 포함해서요.

### 이 가이드를 마치면

- 로컬 PHP 개발 환경 구축
- Laravel 프로젝트 생성 및 설정
- 인증 시스템 (회원가입/로그인/로그아웃)
- 게시판 CRUD
- 백오피스 (관리자 페이지 + RBAC 권한 관리)
- ngrok으로 외부 공개하여 피드백 받기
- UI 커스터마이징

이 모든 것을 **비용 0원**으로 시작할 수 있습니다.

## 왜 Laravel인가?

### Next.js로 같은 걸 만들려면?

| 기능 | Laravel | Next.js |
|------|---------|---------|
| 인증 | `laravel/breeze` 한 줄 | NextAuth + 설정 지옥 |
| 권한 관리 (RBAC) | `spatie/permission` | 직접 구현 or 외부 서비스 |
| 백오피스 | `filament` 패키지 | 직접 구현 필요 |
| 데이터베이스 | Eloquent ORM 내장 | Prisma 별도 설치 |
| 이메일 발송 | Mail 파사드 내장 | Resend, SendGrid 등 연동 |
| 큐/백그라운드 작업 | Queue 내장 | 없음 (외부 서비스 필요) |

Laravel은 **"batteries included"** 철학으로, 웹 애플리케이션에 필요한 거의 모든 것이 프레임워크에 포함되어 있습니다.

## 문서 목차

1. [PHP 개발환경 준비](./01-setup)
2. [프로젝트 설치/생성](./02-create-project)
3. [바이브코딩: 게시판 + 백오피스](./03-vibe-coding)
4. [서비스 공개 (ngrok)](./04-deploy)
5. [보너스: UI 커스텀](./05-ui-custom)

## 핵심 기술 스택

- **PHP** 8.2+
- **Laravel** 12.x
- **인증**: laravel/breeze (Blade + Tailwind)
- **백오피스**: Filament (관리자 패널)
- **권한 관리**: spatie/laravel-permission
- **Database**: SQLite (초기) → MySQL/PostgreSQL (확장 시)

## 대상 독자

- AI로 코딩하는 "바이브 코더"
- Next.js 외의 대안을 찾는 프론트엔드 개발자
- Laravel을 처음 접하는 입문자
- PHP로 빠르게 MVP를 만들고 싶은 누구나

## 시작하기

[01. PHP 개발환경 준비](./01-setup)부터 순서대로 따라오세요!

---

## 라이선스

MIT License

## 기여

이슈와 PR 환영합니다!
