---
layout: post
title: "게시물 작성 방법"
date: 2025-04-08 14:30:00 +0900
categories: [튜토리얼]
tags: [jekyll, 마크다운, 작성법]
---

# 게시물 작성 방법 📖

새로운 게시물을 작성하는 방법을 알아보겠습니다.

## 파일명 규칙

```
YYYY-MM-DD-title.md
```

예시: `2025-04-08-my-first-post.md`

## Front Matter

파일 최상단에 아래와 같이 작성합니다:

```yaml
---
layout: post
title: "게시물 제목"
date: 2025-04-08 10:00:00 +0900
categories: [카테고리1, 카테고리2]
tags: [태그1, 태그2]
---
```

## 마크다운 작성법

### 제목
```markdown
# H1 제목
## H2 제목
### H3 제목
```

### 리스트
- 항목 1
- 항목 2
- 항목 3

### 코드 블록
```python
print("Hello, World!")
```

### 링크
[링크 텍스트](https://example.com)

### 이미지
![이미지 설명](이미지경로.jpg)

## 게시물 저장 위치

모든 게시물은 `_posts/` 폴더에 저장됩니다.

이제 여러분만의 게시물을 작성해보세요! ✍️
