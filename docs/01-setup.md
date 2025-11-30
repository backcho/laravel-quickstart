---
layout: default
title: 01. PHP 개발환경 준비
nav_order: 2
permalink: /01-setup/
---

# 01. PHP 개발환경 준비

> 목표: PHP + Composer + 로컬 서버 환경 구축

Laravel을 사용하려면 먼저 PHP 개발 환경이 필요합니다. 운영체제별로 가장 쉬운 방법을 안내합니다.

---

## Mac 환경

### Herd (추천)

Herd는 Laravel 팀에서 만든 올인원 PHP 개발 환경입니다. GUI로 모든 것을 관리할 수 있어 초보자에게 추천합니다.

**설치:**
1. [https://herd.laravel.com](https://herd.laravel.com) 에서 다운로드
2. DMG 파일 실행 후 Applications 폴더로 드래그
3. Herd 실행

**주요 기능:**
- PHP 버전 관리: GUI에서 클릭 한 번으로 버전 변경
- 사이트 자동 감지: `~/Herd` 폴더에 프로젝트를 넣으면 자동으로 `.test` 도메인 생성
- Node.js 포함: npm/npx도 함께 설치됨

---

## Windows 환경

### Laragon (추천)

Laragon은 Windows에서 가장 쉽게 PHP 개발 환경을 구축할 수 있는 도구입니다.

**설치:**
1. [https://laragon.org/download](https://laragon.org/download) 에서 **Full 버전** 다운로드
2. 설치 프로그램 실행 (기본 설정 그대로 진행)
3. Laragon 실행 → "Start All" 클릭

**포함된 구성요소 (Full 버전):**
- PHP 8.x, MySQL 8.x, Node.js, Composer, Git

**주요 기능:**
- Pretty URLs: 자동으로 `.test` 도메인 생성
- 빠른 프로젝트 생성: 우클릭 → Quick app → Laravel
- 포터블: USB에 넣어서 들고 다닐 수 있음

---

## 설치 확인

어떤 방법을 선택했든, 터미널에서 다음 명령어로 설치를 확인합니다:

```bash
# PHP 버전 확인 (8.2 이상 권장)
php -v

# Composer 버전 확인
composer -v
```

---

## 다음 단계

환경 설정이 완료되었으면 [02. 프로젝트 설치/생성](./02-create-project)으로 진행합니다.
