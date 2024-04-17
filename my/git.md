---
title: Git
layout: upj_design
permalink: /git/
---

#### Table Of Contents

- TOC
{:toc}

# Git
{: #upj_1676460352694}

리누스 토르발스가 개발한 분산형 버전 관리 시스템(VCS)이다.

> 오픈소스계의 영원한 아이돌 리누스 토르발스는 리눅스 커널을 관리하는 기존 툴이 엉망인 것에 너무 빡친 바람에 Git이라는 소스관리 툴을 만든다. 리누스는 하도 빡친 나머지, 단 2주만에 완성하는 기염을 토했다.
> －오픈소스의 승리 중에서.

## Install
{: #upj_1676460515047}

- [git](https://git-scm.com/)
- [GitHub Desktop](https://desktop.github.com/)
- [Sourcetree](https://www.sourcetreeapp.com/)
- [위키백과](https://ko.wikipedia.org/wiki/%EA%B9%83_(%EC%86%8C%ED%94%84%ED%8A%B8%EC%9B%A8%EC%96%B4))
- [나무위키](https://namu.wiki/w/Git)

## Markdown Guide
{: #upj_1703307119262}

### 기본 구문
{: #upj_1703308040150}

| Element | Markdown Syntax |
| :- | :- |
| [제목](https://www.markdownguide.org/basic-syntax/#headings) | `# H1`<br>`## H2` |
| [굵게](https://www.markdownguide.org/basic-syntax/#bold) | `**bold text**` |
| [이텔릭](https://www.markdownguide.org/basic-syntax/#italic) | `*italicized text*` |
| [인용](https://www.markdownguide.org/basic-syntax/#blockquotes-1) | `> blockquote` |
| [순서 리스트](https://www.markdownguide.org/basic-syntax/#ordered-lists) | `1. First item` |
| [순서 없는 리스트](https://www.markdownguide.org/basic-syntax/#unordered-lists) | `- Second item` |
| [코드](https://www.markdownguide.org/basic-syntax/#code) | `'code'` |
| [수평선](https://www.markdownguide.org/basic-syntax/#horizontal-rules) | `---` |
| [링크](https://www.markdownguide.org/basic-syntax/#links) | `[title](https://www.example.com)` |
| [이미지](https://www.markdownguide.org/basic-syntax/#images-1) | `![alt text](image.jpg)` |

### 확장 구문
{: #upj_1703323403912}

| Element | Markdown Syntax |
| :- | :- |
| [테이블](https://www.markdownguide.org/extended-syntax/#tables) | `| Syntax | Description |`<br>`| :- | :-: |`<br>`| a | b |`<br>`| c | d |` |
| [코드 블럭](https://www.markdownguide.org/extended-syntax/#fenced-code-blocks) | `'''java`<br>`int a = 1;` |
| [바닥글](https://www.markdownguide.org/extended-syntax/#footnotes) | `Here is a sentence with a footnote.[^1]`<br>`[^1]: This is the footnote.` |
| [헤딩 아이디](https://www.markdownguide.org/extended-syntax/#heading-ids) | `### My Heading {#custom-id}` |
| [정의 리스트](https://www.markdownguide.org/extended-syntax/#definition-lists) | `term`<br>`: definition` |
| [취소](https://www.markdownguide.org/extended-syntax/#strikethrough) | `~~The World is flat.~~` |
| [할일 리스트](https://www.markdownguide.org/extended-syntax/#task-lists) | `- [x] Task 1`<br>`- [ ] Task 2`<br>`- [ ] Task 2` |
| [이모지](https://www.markdownguide.org/extended-syntax/#emoji)<br>[이모지 사용법](https://www.markdownguide.org/extended-syntax/#copying-and-pasting-emoji) | `This is so funny! :joy:` |
| [하이라이트](https://www.markdownguide.org/extended-syntax/#highlight) | `I need to highlight these ==very important words==`. |

## Markdown 사용팁
{: #upj_1704851726011}

### 링크 타겟을 새창으로
{: #upj_1704851762796}

```markdown
[레이블](url){:target="_blank"}
```

### details 로 접기 사용
{: #upj_1704858148299}

```markdown
<details>
<summary>요약
</summary>

내용 입력하기
</details>
```

## Init my repository
{: #upj_1676460528550}

```shell
git init
git config user.name {MY ID}
git config user.email {MY EMAIL}
git config user.password {MY PASSWORD}
git remote add origin {MY REMOTE GIT ADDRESS}
git pull origin master
```

## Pull and Push
{: #upj_1676460536207}

### Trace my status
{: #upj_1676460541534}

```shell
git add -A
git status
```

### Save and Upload
{: #upj_1676460546359}

```shell
git add .
git commit -m '{MY MESSAGE}'
git push origin +master ← {MY MAIN BRANCH NAME}
git push origin +{MY BRANCH NAME}
```

## Branch
{: #upj_1676460553895}

### List Branch
{: #upj_1676460563551}

```shell
     Local Branch
git branch  -a

     Remote Branch
git branch  -r
```

### Create Branch and Move to the branch created
{: #upj_1676460569366}

```shell
git branch {MY BRANCH NAME}
git checkout {MY BRANCH NAME}

     ▼ all together

git checkout -b {MY BRANCH NAME}
```

### Delete Branch
{: #upj_1676460576919}

```shell
     Local Branch
git branch -d {MY LOCAL BRANCH NAME}
git branch -D {MY LOCAL BRANCH NAME}  ←  Force to delete

     Remote Branch
git push origin --delete {MY REMOTE BRANCH NAME}
```

### Rename Branch
{: #upj_1676460583039}

```shell
     Local Branch
git branch -m {MY OLD BRANCH NAME} {MY NEW BRANCH NAME}

     Remote Branch
git push origin {MY NEW BRANCH NAME}
git push origin --delete {MY OLD BRANCH NAME}

     ↕ Same

git push origin :{MY OLD BRANCH NAME} {MY NEW BRANCH NAME}
```

## Merge
{: #upj_1676460588295}

### Merge Branch
{: #upj_1676460597143}

```shell
git checkout master
git merge {MY BRANCH NAME}
```

### Merge Specific File Only
{: #upj_1676460604606}

```shell
git checkout -p  {MY BRANCH NAME} -- {MY FILE NAME}
git checkout -p   ParkWonjune   index.md
```

## 사용팁
{: #upj_1676508313337}

### .gitignore 가 제대로 작동 안할 때
{: #upj_1676508319848}

```shell
git rm -r --cached .
git add .
git commit -m "fixed untracked files"
```

### git push 자동 스크립트
{: #upj_1705714728900}

~/.local/bin/git-push.sh

```bash
#!/bin/bash
read -p "Enter git commit message: " msg
git add . && git commit -m "$msg" && git push origin +master
```

### git config 등록 후 git push helper
{: #upj_1705714728882}

.git/config

```text
[core]
	repositoryformatversion = 0
	filemode = true
	bare = false
	logallrefupdates = true
[remote "origin"]
	url = https://github.com/upj53/upj53.github.io.git
	fetch = +refs/heads/*:refs/remotes/origin/*
[branch "master"]
	remote = origin
	merge = refs/heads/master
[user]
	name = upj53
	email = unitedparks@gmail.com
	password = 암호
[credential]
	helper = store
```

