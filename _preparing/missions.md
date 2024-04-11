---
title: Test Missions
layout: upj_design
permalink: /drafts/missions/
---

#### Table Of Contents

- TOC
{:toc}

# Missions
{: #upj_1676632642607}

미션을 완료할 수 있습니다.

## Git
{: #upj_1676632650695}

### Git Mission 1 - IDE and Git
{: #upj_1676632655207}

미션
: 다음 IDE 중 하나를 사용하여 (이클립스 / 인텔리제이 / 안드로이드 스튜디오) 나의 Github 계정을 연결한 후 repository 를 생성하고 commit 과 push 하세요.

### Git Mission 2 - branch and merge
{: #upj_1676632660454}

미션
: 사칙연산 모듈을 Java 를 사용해서 만들려고 합니다.
: 각 연산을 함수로 만들어 작성하고, 연산 기능을 만들 때마다 branch 를 만들어 git 에 업로드 하고,
: 완성 후 기본 브랜치에 병합(merge)하세요.

### Git Mission 3 - Collaborators
{: #upj_1676632664792}

미션
: 도형의 넓이를 계산하는 모듈을 Java 를 사용해서 만들려고 합니다.
: 한사람은 삼각형을 계산하는 클래스를 각각 만들고, 다른 한 사람은 원을 계산하는 클래스를 각각 만든 후 하나의 모듈로 합쳐서 완성하세요.

깃 브랜치

```text
  main(master) ← 기본 브랜치
  ├ triangle
  └ circle
```

소스코드

```java
---Main.java---

class Main {
  public static void main(String[] args) {
  }
}
---Shape.java---

public interface Shape {
  double getArea();
}
---Triangle.java---

public class Triangle implements Shape {
}
---Circle.java---

public class Circle implements Shape {
}
```

## Linux
{: #upj_1676632668791}

### Linux Mission 1 - Add To Path
{: #upj_1676632676479}

미션
: 다음 경로에 디렉터리를 생성(/opt/jdk11/)하고 해당 경로를 PATH 환경변수에 추가하세요.

### Linux Mission 2 - alias
{: #upj_1676632680448}

미션
: alias 사용해서 c 라는 명령어를 치면 clear 를 실행해서 화면을 깨끗하게 하도록 하세요.

### Linux Mission 3 - Vim
{: #upj_1676632686639}

미션
: vim 편집기를 실행하여 다음 세개의 파일(a.txt, b.txt, c.txt)을 만들고 아래과 같이 화면분할을 하세요.

<a href="/assets/images/linux-missiong-03.png" target="_blank">
<img src="/assets/images/linux-missiong-03.png" style="width: 75%; height:auto; "/>
</a>

### Linux Mission 4 - Symbolic Link
{: #upj_1676632690760}

미션
: /opt/jdk11/ 폴더에 hello.txt 파일을 만들고 ~/Documents 폴더에 해당 파일의 소프트 링크를 만드세요.

### Linux Mission 5 - Shell
{: #upj_1676632695055}

미션
: Oh My Zsh, PowerLevel10K 를 설치해서 다음과 같이 내가 원하는 모습으로 쉘을 바꿔보세요.

<a href="/assets/images/linux-missiong-05.png" target="_blank">
<img src="/assets/images/linux-missiong-05.png" style="width: 75%; height:auto; "/>
</a>

### Linux Mission 6 - Permissions
{: #upj_1676632700399}

미션
: sungil 이라는 사용자를 생성하고 암호를 12345로 설정한 뒤, 관리자권한을 주세요.
: /opt/jdk11/ 폴더의 소유자를 sungil 사용자로 바꾸고 폴더와 파일의 모든 권한을 다음과 같이 설정하세요.
: 소유자: 쓰기/읽기/실행 가능
: 그룹 사용자: 읽기/실행 가능
: 기타 사용자: 읽기/실행 가능

### Linux Mission 7 - Setup Web Server
{: #upj_1676632704622}

미션
: nodejs 를 설치하고 서비스를 구동한 뒤 다음과 같이 http://localhost:8080 페이지를 웹 브라우저에 띄우세요.

<a href="/assets/images/linux-missiong-07.png" target="_blank">
<img src="/assets/images/linux-missiong-07.png" style="width: 75%; height:auto; "/>
</a>
