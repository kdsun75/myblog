# 📝 Jekyll 블로그 사용 가이드

이 문서는 Jekyll 블로그를 사용하는 방법을 정리한 것입니다.

---

## 📁 프로젝트 구조

```
myblog/
├── _config.yml          # 블로그 설정 파일
├── index.md            # 메인 페이지 (홈)
├── about.md            # 소개 페이지
├── GUIDE.md            # 이 파일 (사용 가이드)
├── _posts/             # 게시물 폴더
│   ├── 2025-04-08-welcome.md
│   └── 2025-04-08-how-to-write-post.md
└── images/             # 이미지 폴더 (선택사항)
```

---

## ✏️ 새 게시물 작성하기

### 1단계: 게시물 파일 생성

`_posts/` 폴더에 새 파일을 만듭니다.

**파일명 규칙 (반드시 지켜야 함):**
```
YYYY-MM-DD-제목.md
```

예시:
- `2025-04-09-python-study.md`
- `2025-04-10-book-review.md`
- `2025-04-12-trip-to-seoul.md`

### 2단계: 파일 내용 작성

**기본 템플릿:**

```markdown
---
layout: post
title: "게시물 제목"
date: 2025-04-09 14:30:00 +0900
categories: [카테고리1, 카테고리2]
tags: [태그1, 태그2, 태그3]
---

# 여기에 본문을 작성합니다

내용을 자유롭게 작성하세요.
```

**실제 예시:**

```markdown
---
layout: post
title: "파이썬 공부 시작"
date: 2025-04-09 14:30:00 +0900
categories: [개발, Python]
tags: [python, 공부, 입문]
---

# 파이썬 공부를 시작했습니다

오늘부터 파이썬을 배우기로 했습니다.

## 설치 방법

1. Python.org에서 다운로드
2. 설치 진행
3. 환경변수 설정

## 첫 코드

```python
print("Hello, Python!")
```

앞으로 열심히 해보겠습니다! 🚀
```

### 3단계: GitHub에 올리기

터미널에서 아래 명령어를 순서대로 실행:

```bash
# 1. 변경사항 추가
git add .

# 2. 커밋 (변경사항 저장)
git commit -m "Add: 파이썬 공부 포스팅"

# 3. 푸시 (GitHub에 업로드)
git push
```

푸시 후 1-2분 뒤에 웹사이트에 자동 반영됩니다.

---

## 🎨 마크다운 문법

### 제목
```markdown
# H1 제목 (가장 큼)
## H2 제목
### H3 제목
#### H4 제목
```

### 텍스트 스타일
```markdown
**굵은 글씨**
*기울임*
~~취소선~~
`인라인 코드`
```

결과:
- **굵은 글씨**
- *기울임*
- ~~취소선~~
- `인라인 코드`

### 리스트
```markdown
- 순서 없는 리스트
- 항목 1
- 항목 2
  - 들여쓴 항목

1. 순서 있는 리스트
2. 두 번째 항목
3. 세 번째 항목
```

### 링크
```markdown
[링크 텍스트](https://github.com)
```

결과: [링크 텍스트](https://github.com)

### 코드 블록
````markdown
```python
def hello():
    print("Hello, World!")
    return True
```
````

### 인용문
```markdown
> 이것은 인용문입니다.
> 여러 줄도 가능합니다.
```

결과:
> 이것은 인용문입니다.
> 여러 줄도 가능합니다.

### 수평선
```markdown
---
```

결과:

---

### 표
```markdown
| 제목1 | 제목2 | 제목3 |
|-------|-------|-------|
| 내용1 | 내용2 | 내용3 |
| 내용4 | 내용5 | 내용6 |
```

결과:

| 제목1 | 제목2 | 제목3 |
|-------|-------|-------|
| 내용1 | 내용2 | 내용3 |
| 내용4 | 내용5 | 내용6 |

---

## 🖼️ 이미지 넣기

### 방법 1: 외부 이미지 URL 사용
```markdown
![고양이 사진](https://example.com/cat.jpg)
```

### 방법 2: 프로젝트 내 이미지 사용

1. 먼저 `images/` 폴더 생성:
   ```bash
   mkdir images
   ```

2. 이미지 파일을 `images/` 폴더에 복사

3. 마크다운에서 참조:
   ```markdown
   ![내 사진](/images/photo.jpg)
   ![스크린샷](/images/screenshot.png)
   ```

4. GitHub에 이미지도 함께 올리기:
   ```bash
   git add images/
   git commit -m "Add: 이미지 추가"
   git push
   ```

---

## 📄 고정 페이지 만들기

게시물이 아닌 상단 메뉴에 표시되는 페이지입니다.
(예: About, Contact, Projects 등)

### 방법

1. 프로젝트 루트에 파일 생성 (예: `contact.md`)

2. 다음 내용 작성:
   ```markdown
   ---
   layout: page
   title: "Contact"
   permalink: /contact/
   ---

   # 연락처

   - 이메일: kdsun75@gmail.com
   - GitHub: [kdsun75](https://github.com/kdsun75)
   ```

3. GitHub에 푸시하면 `/contact/` 주소로 접근 가능

---

## 🔧 자주 쓰는 Git 명령어

| 작업 | 명령어 |
|------|--------|
| **상태 확인** | `git status` |
| **파일 추가** | `git add 파일명` 또는 `git add .` (모든 파일) |
| **커밋** | `git commit -m "메시지"` |
| **푸시** | `git push` |
| **변경사항 확인** | `git diff` |
| **로그 확인** | `git log --oneline` |

### 전체 작업 흐름 예시

```bash
# 1. 현재 상태 확인
git status

# 2. 새 게시물 파일 추가
git add _posts/2025-04-09-new-post.md

# 3. 커밋
git commit -m "Add: 새 게시물 작성"

# 4. GitHub에 업로드
git push

# 또는 한 번에 모든 변경사항 처리
git add .
git commit -m "Add: 여러 파일 추가"
git push
```

---

## 💡 유용한 팁

### 글 작성 중 임시저장
- 파일을 저장만 하면 됩니다 (커밋하지 않아도 됨)
- 완성된 후에 한꺼번에 커밋&푸시

### 게시물 미리보기 (로컬)
```bash
# Jekyll 설치 필요
gem install bundler jekyll

# 로컬 서버 실행
bundle exec jekyll serve

# 브라우저에서 http://localhost:4000 접속
```

### 날짜/시간 형식
```
2025-04-09 14:30:00 +0900
└─┬─┘ └─┬─┘ └─┬─┘ └─┬─┘ └┬┘
  연   월    일    시:분:초 시간대
```

### 파일명에 사용 가능한 문자
- ✅ 영문 소문자, 숫자, 하이픈(-), 언더스코어(_)
- ✅ 한글도 가능하지만 영문 권장
- ❌ 띄어쓰기는 언더스코어 `_` 또는 하이픈 `-` 사용

---

## 📌 빠른 참고

**새 게시물 작성 단축:**
```
1. _posts 폴더에 YYYY-MM-DD-제목.md 파일 생성
2. Front Matter 작성 (title, date, categories, tags)
3. 마크다운으로 본문 작성
4. git add . && git commit -m "Add: 제목" && git push
```

**블로그 주소:** https://kdsun75.github.io/myblog

---

## ❓ 문제 해결

### GitHub Pages가 업데이트 안 될 때
- 푸시 후 1-2분 정도 기다려보세요
- https://github.com/kdsun75/myblog/actions 에서 빌드 상태 확인

### 이미지가 안 보일 때
- 경로 확인: `/images/파일명.jpg` (슬래시로 시작)
- 대소문자 확인: Git에서 대소문자 구분함
- 파일이 실제로 push 되었는지 확인

### 기타 문의
- Jekyll 공식 문서: https://jekyllrb.com/docs/
- GitHub Pages 문서: https://pages.github.com/
