# 🎯 Prompt Trainer - Frontend

AI 프롬프트 작성 능력을 향상시키는 질문력 트레이너 서비스의 프론트엔드 레포지토리입니다.

## 🔗 Related Repositories
- 🔧 Backend: [prompt-trainer-backend](https://github.com/prompt-trainer-team/prompt-trainer-backend)

---

## 🌿 브랜치 전략

| 브랜치 | 설명 |
|--------|------|
| `main` | 🚀 배포 브랜치 (직접 수정 금지) |
| `develop` | 🔧 개발 통합 브랜치 |
| `feat/*` | ✨ 기능 개발 브랜치 |
| `fix/*` | 🐛 버그 수정 브랜치 |
| `refactor/*` | ♻️ 리팩토링 브랜치 |
| `style/*` | 💄 UI/스타일 관련 브랜치 |
| `chore/*` | 🔨 설정/빌드 관련 브랜치 |

### 브랜치 네이밍 규칙

```
{타입}/#{이슈번호}-{간단한-설명}
```

**예시:**
- `feat/#1-login-page`
- `fix/#12-header-layout`
- `style/#15-button-design`

---

## 🔄 작업 순서

### 1️⃣ 작업 시작 전 최신화
```bash
# develop 브랜치로 이동
git checkout develop

# 최신 코드 받기
git pull origin develop

# 새 작업 브랜치 생성
git checkout -b feat/#1-기능명
```

### 2️⃣ 작업 진행 및 커밋
```bash
# 변경사항 스테이징
git add .

# 커밋 (컨벤션 준수)
git commit -m "feat: 로그인 페이지 UI 구현"

# 원격 저장소에 푸시
git push origin feat/#1-기능명
```

### 3️⃣ 작업 중 develop 변경사항 반영
```bash
git checkout develop
git pull origin develop
git checkout feat/#1-기능명
git merge develop
```

---

## 📮 Pull Request 규칙

### PR 방향
```
feat/* → develop  ✅
develop → main   ✅ (배포 시)
```

### PR 전 체크리스트
- [ ] 로컬에서 정상 동작 확인
- [ ] 반응형 디자인 확인 (모바일/태블릿/PC)
- [ ] 커밋 컨벤션 준수
- [ ] 충돌(conflict) 해결 완료
- [ ] 관련 이슈 번호 연결

### PR 절차
1. 기능 개발 완료 후 로컬 테스트
2. `develop` 브랜치로 PR 생성
3. **팀 채널에 리뷰 요청** 💬
4. 리뷰 후 승인되면 머지
5. 머지된 브랜치는 삭제

---

## ✍️ 커밋 컨벤션

```
<type>: <subject>
```

### Type 종류
| Type | 설명 |
|------|------|
| `feat` | 새로운 기능 추가 |
| `fix` | 버그 수정 |
| `refactor` | 코드 리팩토링 (기능 변화 X) |
| `style` | UI/CSS 스타일 변경 |
| `design` | 사용자 UI 디자인 변경 |
| `docs` | 문서 수정 |
| `test` | 테스트 코드 |
| `chore` | 빌드, 설정 파일 수정 |

### 예시
```bash
git commit -m "feat: 로그인 페이지 UI 구현"
git commit -m "fix: 헤더 반응형 레이아웃 오류 수정"
git commit -m "style: 버튼 hover 효과 추가"
git commit -m "refactor: API 호출 로직 분리"
git commit -m "chore: axios 라이브러리 설치"
```

---

## ⚠️ 주의사항

### 🚫 절대 금지
- ❌ `main`, `develop` 브랜치에 직접 push
- ❌ 다른 사람 브랜치에 함부로 push
- ❌ `.env` 파일 커밋
- ❌ API Key, 비밀번호 등 민감 정보 커밋
- ❌ `node_modules` 커밋

### ✅ 필수 수칙
- 충돌 발생 시 팀원과 상의 후 해결
- PR 전 반드시 로컬 테스트
- 커밋 메시지는 컨벤션 준수

---

## 🔒 환경 변수 관리

보안을 위해 모든 API Key 및 민감 정보는 `.env` 파일에서 관리합니다.

- `.env` 파일은 절대 GitHub에 push하지 마세요 (`.gitignore`에 등록됨)
- 필요한 API Key 목록은 **[팀 노션 페이지](https://app.notion.com/p/K-4a28475fe3f2822aaeca81ac1cbf8353)** 에서 확인 후 로컬에 복사하여 사용해주세요
