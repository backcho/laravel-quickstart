# 01. PHP 개발환경 준비

> 목표: PHP + Composer + 로컬 서버 환경 구축

Laravel을 사용하려면 먼저 PHP 개발 환경이 필요합니다. 운영체제별로 가장 쉬운 방법을 안내합니다.

---

## Mac 환경

### 방법 1: Herd (추천 ⭐)

Herd는 Laravel 팀에서 만든 올인원 PHP 개발 환경입니다. GUI로 모든 것을 관리할 수 있어 초보자에게 추천합니다.

#### 설치

1. [https://herd.laravel.com](https://herd.laravel.com) 에서 다운로드
2. DMG 파일 실행 후 Applications 폴더로 드래그
3. Herd 실행

#### 주요 기능

- **PHP 버전 관리**: GUI에서 클릭 한 번으로 PHP 버전 변경
- **사이트 자동 감지**: `~/Herd` 폴더에 프로젝트를 넣으면 자동으로 `.test` 도메인 생성
- **Node.js 포함**: npm/npx도 함께 설치됨
- **데이터베이스**: MySQL, PostgreSQL, Redis 등 선택적 설치 가능

#### 사용법

```bash
# Herd 설치 후 터미널에서 바로 사용 가능
php -v
composer -v

# 프로젝트 폴더를 ~/Herd에 생성하면 자동으로 접근 가능
# 예: ~/Herd/my-project → http://my-project.test
```

### 방법 2: Valet (대안)

Homebrew를 사용해 직접 설정하는 방법입니다. 더 세밀한 제어가 필요한 경우 선택합니다.

#### 설치

```bash
# Homebrew 설치 (없는 경우)
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# PHP 설치
brew install php

# Composer 설치
brew install composer

# Valet 설치
composer global require laravel/valet
valet install

# 프로젝트 폴더 설정
cd ~/Sites  # 또는 원하는 폴더
valet park
```

#### 사용법

```bash
# ~/Sites 폴더에 프로젝트를 생성하면 자동으로 접근 가능
# 예: ~/Sites/my-project → http://my-project.test
```

---

## Windows 환경

### Laragon (추천 ⭐)

Laragon은 Windows에서 가장 쉽게 PHP 개발 환경을 구축할 수 있는 도구입니다.

#### 설치

1. [https://laragon.org/download](https://laragon.org/download) 에서 **Full 버전** 다운로드
2. 설치 프로그램 실행 (기본 설정 그대로 진행)
3. Laragon 실행 → "Start All" 클릭

#### 포함된 구성요소 (Full 버전)

- PHP 8.x
- MySQL 8.x
- Node.js
- Composer
- Git
- HeidiSQL (DB 관리 도구)

#### 주요 기능

- **Pretty URLs**: 자동으로 `.test` 도메인 생성
- **빠른 프로젝트 생성**: 우클릭 → Quick app → Laravel
- **PHP 버전 변경**: 우클릭 → PHP → Version
- **포터블**: USB에 넣어서 들고 다닐 수 있음

#### 사용법

```bash
# Laragon 터미널에서 (Menu → Terminal)
php -v
composer -v

# 프로젝트 폴더: C:\laragon\www
# 예: C:\laragon\www\my-project → http://my-project.test
```

#### hosts 파일 자동 설정

Laragon은 프로젝트 생성 시 자동으로 Windows hosts 파일을 수정합니다. 관리자 권한이 필요할 수 있습니다.

---

## 설치 확인

어떤 방법을 선택했든, 터미널에서 다음 명령어로 설치를 확인합니다:

```bash
# PHP 버전 확인 (8.2 이상 권장)
php -v
# 출력 예: PHP 8.3.x (cli) ...

# Composer 버전 확인
composer -v
# 출력 예: Composer version 2.x.x ...

# Laravel Installer 설치 (선택사항)
composer global require laravel/installer
laravel --version
```

---

## 문제 해결

### Mac: "command not found: composer"

Composer 글로벌 bin 경로를 PATH에 추가해야 합니다.

```bash
# ~/.zshrc 또는 ~/.bash_profile에 추가
export PATH="$HOME/.composer/vendor/bin:$PATH"

# 적용
source ~/.zshrc
```

### Windows: PHP가 인식되지 않음

Laragon 터미널을 사용하거나, 시스템 환경 변수에 PHP 경로를 추가합니다.

1. 시스템 속성 → 환경 변수
2. Path 편집 → `C:\laragon\bin\php\php-8.x.x` 추가

### 포트 충돌 (80, 443)

다른 프로그램(Skype, IIS 등)이 포트를 사용 중일 수 있습니다.

- Laragon: 우클릭 → Preferences → Services & Ports에서 포트 변경
- Herd: Preferences에서 포트 설정 변경

---

## 다음 단계

환경 설정이 완료되었으면 [02_프로젝트_설치_생성.md](./02_프로젝트_설치_생성.md)로 진행합니다.
