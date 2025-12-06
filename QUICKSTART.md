# 🚀 Jjigit Website - Quick Start Guide

완성된 Jjigit 웹사이트 프로젝트입니다. GitHub Pages와 Jekyll을 사용하여 구축되었습니다.

## 📦 포함된 내용

### 페이지
- ✅ **홈페이지** (index.md) - 미션 선언문, 주요 링크, 기능 미리보기
- ✅ **기능 소개** (features.md) - 5가지 핵심 기능 상세 설명
- ✅ **커뮤니티** (community.md) - Discord, GitHub Discussions, 메일링 리스트 등
- ✅ **연락처** (contact.md) - 연락 양식, 이메일, 소셜 링크

### 디자인 특징
- 🎨 모던하고 전문적인 디자인
- 🌈 인디고/시안 색상 테마 (Jjigit 브랜드에 맞춤)
- 📱 완전한 반응형 디자인
- ⚡ 빠른 로딩 속도
- 🎯 Apache Hadoop 스타일 영감

### 기술 스택
- Jekyll 4.3
- GitHub Pages
- 순수 CSS (프레임워크 없음)
- 자동 배포 (GitHub Actions)

## 🏃‍♂️ 5분 안에 시작하기

### 1단계: GitHub에 업로드

```bash
# 프로젝트 디렉토리로 이동
cd jjigit-website

# Git 초기화
git init
git add .
git commit -m "Initial commit: Jjigit website"

# GitHub 저장소 생성 후 연결
git remote add origin https://github.com/YOUR_USERNAME/jjigit-website.git
git branch -M main
git push -u origin main
```

### 2단계: GitHub Pages 활성화

1. GitHub 저장소로 이동
2. **Settings** → **Pages** 클릭
3. Source에서 **GitHub Actions** 선택
4. 자동으로 배포가 시작됩니다!

### 3단계: 설정 업데이트

`_config.yml` 파일을 열고 다음을 업데이트하세요:

```yaml
# 필수 변경 사항
url: "https://YOUR_USERNAME.github.io"
github_username: YOUR_USERNAME

project:
  github_url: "https://github.com/YOUR_USERNAME/jjigit"
  discord_url: "YOUR_DISCORD_INVITE_LINK"
  discussions_url: "https://github.com/YOUR_USERNAME/jjigit/discussions"
```

### 4단계: 사이트 확인

배포 후 접속: `https://YOUR_USERNAME.github.io/jjigit-website`

## 📝 주요 설정 항목

### ⚠️ 꼭 변경해야 할 것들

1. **_config.yml**
   - `url`: GitHub Pages URL
   - `github_username`: 본인의 GitHub 사용자명
   - `email`: 연락 이메일
   - 모든 `project.*_url`: 실제 프로젝트 URL

2. **contact.md**
   - Formspree form ID 교체 (contact@jjigit.io로 이메일 받기)
   - 라인 99: `YOUR_FORM_ID` → 실제 Formspree ID

3. **커뮤니티 플랫폼 설정**
   - Discord 서버 생성 및 초대 링크
   - GitHub Discussions 활성화
   - 소셜 미디어 계정 생성

## 🎨 커스터마이징

### 색상 변경

`assets/css/style.css` 파일의 상단:

```css
:root {
  --primary: #4F46E5;      /* 주 색상 */
  --secondary: #06B6D4;    /* 보조 색상 */
  --accent: #F59E0B;       /* 강조 색상 */
}
```

### 로고 변경

`_layouts/default.html`에서 이모지를 이미지로 교체:

```html
<!-- 현재 -->
<span class="logo-icon">🗳️</span>

<!-- 이미지로 변경 -->
<img src="/assets/images/logo.png" alt="Jjigit" class="logo-icon">
```

## 📂 프로젝트 구조

```
jjigit-website/
├── _config.yml              # Jekyll 설정
├── _layouts/
│   └── default.html         # 기본 레이아웃
├── assets/
│   └── css/
│       └── style.css        # 메인 스타일시트
├── index.md                 # 홈페이지
├── features.md              # 기능 소개
├── community.md             # 커뮤니티
├── contact.md               # 연락처
├── .github/
│   └── workflows/
│       └── pages.yml        # 자동 배포 설정
├── Gemfile                  # Ruby 의존성
├── README.md                # 프로젝트 설명
└── SETUP.md                 # 상세 설정 가이드
```

## 🔧 로컬에서 테스트

```bash
# 의존성 설치
bundle install

# 개발 서버 실행
bundle exec jekyll serve

# 브라우저에서 열기
# http://localhost:4000
```

## ✅ 체크리스트

배포 전 확인사항:

- [ ] `_config.yml`의 모든 URL 업데이트
- [ ] GitHub 저장소 생성 및 푸시
- [ ] GitHub Pages 활성화
- [ ] Discord 서버 생성 및 링크 업데이트
- [ ] GitHub Discussions 활성화
- [ ] Formspree 계정 생성 및 form ID 설정
- [ ] 모든 링크 테스트
- [ ] 모바일에서 테스트
- [ ] 연락 양식 테스트

## 🎯 다음 단계

1. **커뮤니티 플랫폼 설정**
   - Discord 서버 구조화
   - GitHub Discussions 카테고리 생성
   - 메일링 리스트 설정 (Mailchimp 또는 Buttondown)

2. **소셜 미디어**
   - Twitter/X: @jjigit_official
   - LinkedIn 페이지 생성
   - YouTube 채널 개설

3. **분석 도구 추가**
   - Google Analytics 설정
   - GitHub Pages 트래픽 모니터링

4. **SEO 최적화**
   - 메타 태그 최적화
   - 사이트맵 생성
   - robots.txt 추가

## 📚 추가 문서

- **README.md** - 일반 프로젝트 정보
- **SETUP.md** - 상세 설정 및 배포 가이드
- **Jekyll 공식 문서** - https://jekyllrb.com/docs/

## 🆘 도움이 필요하신가요?

- GitHub Issues에 질문 올리기
- Discord 서버 참여
- 이메일: contact@jjigit.io

## 🎉 완료!

축하합니다! Jjigit의 멋진 웹사이트가 준비되었습니다.

**주요 특징:**
- ✨ 전문적인 디자인
- 📱 모바일 최적화
- 🚀 자동 배포
- 🎨 쉬운 커스터마이징
- 📊 확장 가능한 구조

이제 `git push`만 하면 자동으로 배포됩니다!

---

Made with ❤️ for Jjigit
