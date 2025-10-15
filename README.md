# GitHub 초보자 가이드

## 목차
1. [GitHub란?](#github란)
2. [기본 용어 이해하기](#기본-용어-이해하기)
3. [Git 설치 및 설정](#git-설치-및-설정)
4. [저장소 만들기](#저장소-만들기)
5. [기본 Git 명령어](#기본-git-명령어)
6. [README 작성하기](#readme-작성하기)
7. [.gitignore 사용하기](#gitignore-사용하기)
8. [브랜치 사용하기](#브랜치-사용하기)
9. [Pull Request](#pull-request)

---

## GitHub란?

GitHub는 Git을 사용하는 프로젝트를 위한 호스팅 플랫폼입니다. 코드를 저장하고, 버전을 관리하며, 다른 개발자들과 협업할 수 있습니다.

### GitHub의 주요 기능
- 코드 저장 및 버전 관리
- 협업 도구 (Issues, Pull Requests)
- 프로젝트 문서화 (README, Wiki)
- 포트폴리오로 활용 가능

---

## 기본 용어 이해하기

### Repository (저장소)
프로젝트 파일들이 저장되는 공간입니다.

### Commit (커밋)
변경 사항을 저장하는 단위입니다. 스냅샷을 찍는다고 생각하면 됩니다.

### Push (푸시)
로컬 컴퓨터의 변경 사항을 GitHub 서버로 업로드하는 것입니다.

### Pull (풀)
GitHub 서버의 최신 변경 사항을 로컬 컴퓨터로 다운로드하는 것입니다.

### Branch (브랜치)
독립적인 작업 공간입니다. 메인 코드를 건드리지 않고 새로운 기능을 개발할 수 있습니다.

### Clone (클론)
GitHub의 저장소를 내 컴퓨터로 복사하는 것입니다.

---

## Git 설치 및 설정

### Git 설치
1. [Git 공식 사이트](https://git-scm.com/)에서 다운로드
2. 운영체제에 맞는 버전 선택
3. 설치 프로그램 실행

### Git 초기 설정
터미널이나 명령 프롬프트를 열고 다음 명령어를 입력하세요:

```bash
# 사용자 이름 설정
git config --global user.name "당신의 이름"

# 이메일 설정 (GitHub 가입 이메일과 동일하게)
git config --global user.email "your.email@example.com"

# 설정 확인
git config --list
```

---

## 저장소 만들기

### GitHub에서 새 저장소 생성
1. GitHub.com에 로그인
2. 오른쪽 상단의 `+` 버튼 클릭
3. `New repository` 선택
4. 저장소 이름 입력
5. Public (공개) 또는 Private (비공개) 선택
6. `Create repository` 클릭

### 로컬 저장소와 연결
```bash
# 프로젝트 폴더로 이동
cd your-project-folder

# Git 저장소 초기화
git init

# 원격 저장소 연결
git remote add origin https://github.com/사용자명/저장소명.git
```

---

## 기본 Git 명령어

### 저장소 복제하기
```bash
git clone https://github.com/사용자명/저장소명.git
```

### 변경 사항 추가 및 커밋
```bash
# 현재 상태 확인
git status

# 모든 변경 사항 스테이징
git add .

# 특정 파일만 스테이징
git add 파일명

# 커밋 (메시지와 함께)
git commit -m "커밋 메시지"
```

### GitHub에 업로드
```bash
# 변경 사항 푸시
git push origin main

# 처음 푸시할 때
git push -u origin main
```

### 최신 변경 사항 가져오기
```bash
# 원격 저장소의 변경 사항 가져오기
git pull origin main
```

### 커밋 이력 확인
```bash
git log
```

---

## README 작성하기

README.md는 프로젝트의 얼굴입니다. 다른 사람들이 가장 먼저 보는 파일이에요.

### README 기본 구조
```markdown
# 프로젝트 제목

프로젝트에 대한 간단한 설명

## 주요 기능
- 기능 1
- 기능 2
- 기능 3

## 설치 방법
```bash
npm install
```

## 사용 방법
프로젝트를 어떻게 사용하는지 설명

## 기여하기
기여 방법에 대한 안내

## 라이선스
라이선스 정보
```

---

## .gitignore 사용하기

.gitignore 파일은 Git이 추적하지 않을 파일들을 지정합니다.

### .gitignore 예시
```
# 운영체제 파일
.DS_Store
Thumbs.db

# 에디터 설정
.vscode/
.idea/

# 의존성
node_modules/
venv/

# 환경 변수
.env
.env.local

# 빌드 결과물
dist/
build/

# 로그 파일
*.log
```

---

## 브랜치 사용하기

브랜치를 사용하면 메인 코드를 건드리지 않고 새로운 기능을 개발할 수 있습니다.

### 브랜치 명령어
```bash
# 새 브랜치 생성
git branch feature-name

# 브랜치 전환
git checkout feature-name

# 브랜치 생성과 동시에 전환
git checkout -b feature-name

# 브랜치 목록 확인
git branch

# 브랜치 병합 (main 브랜치에서 실행)
git checkout main
git merge feature-name

# 브랜치 삭제
git branch -d feature-name
```

---

## Pull Request

Pull Request(PR)는 내가 작성한 코드를 프로젝트에 반영해달라고 요청하는 것입니다.

### PR 생성 방법
1. 브랜치에서 작업 완료
2. GitHub 저장소 페이지로 이동
3. `Pull requests` 탭 클릭
4. `New pull request` 버튼 클릭
5. 변경 사항 설명 작성
6. `Create pull request` 클릭

### PR 설명 작성 팁
- 무엇을 변경했는지 명확히 설명
- 왜 이 변경이 필요한지 설명
- 스크린샷이나 테스트 결과 포함

---

## 유용한 팁

### 좋은 커밋 메시지 작성법
```bash
# 나쁜 예
git commit -m "수정"

# 좋은 예
git commit -m "로그인 버튼 클릭 시 발생하는 오류 수정"
```

### 커밋 메시지 컨벤션
- `feat`: 새로운 기능 추가
- `fix`: 버그 수정
- `docs`: 문서 수정
- `style`: 코드 포맷팅, 세미콜론 누락 등
- `refactor`: 코드 리팩토링
- `test`: 테스트 코드
- `chore`: 빌드 업무 수정, 패키지 매니저 수정 등

예시:
```bash
git commit -m "feat: 사용자 프로필 페이지 추가"
git commit -m "fix: 로그인 버튼 오류 수정"
```

---

## 자주 발생하는 문제 해결

### 푸시가 거부될 때
```bash
# 원격 저장소의 변경사항을 먼저 받아오기
git pull origin main
# 충돌 해결 후 다시 푸시
git push origin main
```

### 잘못된 커밋 취소
```bash
# 마지막 커밋 취소 (변경사항은 유지)
git reset --soft HEAD^

# 마지막 커밋 완전히 취소
git reset --hard HEAD^
```

### 커밋 메시지 수정
```bash
# 마지막 커밋 메시지 수정
git commit --amend -m "새로운 커밋 메시지"
```

---

## 추가 학습 자료

- [Git 공식 문서](https://git-scm.com/doc)
- [GitHub 공식 가이드](https://guides.github.com/)
- [Git 시각화 학습](https://learngitbranching.js.org/?locale=ko)

---

## 마치며

GitHub는 처음에는 어려워 보이지만, 자주 사용하다 보면 금방 익숙해집니다. 작은 프로젝트부터 시작해서 꾸준히 연습하세요!

**기억할 핵심 명령어:**
1. `git add .` - 변경사항 추가
2. `git commit -m "메시지"` - 커밋
3. `git push` - 업로드
4. `git pull` - 다운로드

화이팅! 🚀
