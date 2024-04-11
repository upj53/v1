---
title: Flutter
layout: upj_design
permalink: /resource/flutter/
private: private
---

#### Table Of Contents

- TOC
{:toc}

## 공식 튜토리얼
{: #upj_1703330308371}

[Official Tutorials](https://flutter.dev/learn)

## Nomadcoders
{: #upj_1678579027299}

### 1. Variables
{: #upj_1678579038955}

```dart
void main() {
  print("Hello World");
  int a = 1;
  var b = "abc";
  a = 7;
  b = "cde";
  final String c = 'upj53';
  // c = '123123'; Error
  dynamic d;
  d = true;
  // d = 1;
  if(d is String) {
    //
  }
  const api_key = '121213134';
  String e = "wjpark";
  // e = null; Error
  String? nico = 'nico';
  if(nico != null) {

  }
  nico?.isEmpty;
  late final String name;
  name = 'Wait for the name';
}
```

### 2. Data Types
{: #upj_1678579043915}

```dart
void main() {
  // List
  var giveMeFive = true;
  var numbers = [1, 2, 3, 4, if (giveMeFive) 5];
  print(numbers);

  // Collection For
  var oldFriends = ['nico', 'lynn'];
  var newFriends = [
    'lewis',
    'ralph',
    'darren',
    for(var friend in oldFriends) "♡ $friend"
  ];
  print(newFriends);

  // Maps
  var player = {
    'name':'nico',
    'xp':19.99,
    'superpower':false
  };
  Map<int, bool> gammer = {
    1: true,
    2: false,
    3: true
  };

  // Sets
  var numberSet = {1, 2, 3, 4, 5};
  Set<int> numSet = {1, 2, 3, 4, 5};
  numSet.add(1);
  numSet.add(1);
  numSet.add(1);
  print(numSet);
}
```

### 3. Functions
{: #upj_1678579048307}

```dart
// 1.define function
String sayHello(String potato) {
  return "Hello $potato nice to meet you";
}

num plus(num a, num b) => a + b;

// 2. Named Arguments
String sayHi1(
    {String name = 'anon', int age = 99, String country = 'wakanda'}) {
  return "";
}

String sayHi2(
    {required String name, required int age, required String country}) {
  return "Hello $name, you are $age, and you come from $country";
}

// 3.Optional Positional Parameters
String sayOppa(String name, int age, [String? country = 'cuba']) =>
    "Hello $name, you are $age, and you come from $country";

// 4.QQ Operator
String capitalizeName1(String? name) {
  if (name != null) {
    return name.toUpperCase();
  }
  return 'ANON';
}

String capitalizeName2(String? name) =>
    name != null ? name.toUpperCase() : 'ANON';

String capitalizeName3(String? name) => name?.toUpperCase() ?? 'ANON';

// 5.Typedef
List<int> reverseListOfNumbers1(List<int> list) {
  var reversed = list.reversed;
  return reversed.toList();
}

typedef ListOfInts = List<int>;

ListOfInts reverseListOfNumbers2(ListOfInts list) {
  var reversed = list.reversed;
  return reversed.toList();
}

String sayAnyeong1(Map<String, String> userInfo) {
  return "Hi ${userInfo['name']}";
}

typedef UserInfo = Map<String, String>;

String sayAnyeong2(UserInfo userInfo) {
  return "Hi ${userInfo['name']}";
}

void main() {
  // 1.define function
  print(sayHello('wonjune'));
  print(plus(1, 2));

  // 2.Named Arguments
  print(sayHi1(name: 'nico', country: 'germany', age: 12));
  print(sayHi2(name: 'nico', country: 'germany', age: 12));

  // 3.Optional Positional Parameters
  print(sayOppa('upj53', 12));

  // 4.QQ Operator
  capitalizeName1('WJPark');
  capitalizeName1(null);

  String? name;
  name ??= 'WJPark';
  name = null;
  name ??= 'another';
  print(name);

  // 5.Typedef
  print(reverseListOfNumbers1([1, 2, 3]));
  print(reverseListOfNumbers2([4, 5, 6]));

  print(sayAnyeong1({'asefasdf': 'upj53'}));
  print(sayAnyeong2({'name': 'wjpark'}));
}
```

### 4-①. Classes : define
{: #upj_1678579052640}

```dart
class Player {
  String name = 'wjpark';
  int xp = 1500;

  void sayHello() {
    print('Hi my name is $name');
  }
}

void main() {
  var player = Player();
  print(player.name);
  player.name = 'upj53';
  print(player.name);
  player.sayHello();
}
```

### 4-②. Classes : Constructor
{: #upj_1678579630720}

```dart
class PlayerA {
  late final String name;
  late int xp;

  PlayerA(String name, int xp) {
    this.name = name;
    this.xp = xp;
  }

  void sayHello() {
    print('Hi my name is $name');
  }
}

class PlayerB {
  final String name;
  int xp;

  PlayerB(this.name, this.xp);

  void sayHello() {
    print('Hi my name is $name');
  }
}

void main() {
  var player1 = PlayerA('wjpark', 1500);
  player1.sayHello();
  var player2 = PlayerA('upj53', 3000);
  player2.sayHello();
  var player3 = PlayerB('esther', 5000);
  player3.sayHello();
}
```

### 4-③. Classes : Named Constructor Parameters
{: #upj_1678579655374}

```dart
class PlayerC {
  final String name;
  int xp;
  String team;
  int age;

  PlayerC(
      {required this.name,
      required this.xp,
      required this.team,
      required this.age});

  void sayHello() {
    print('Hi my name is $name');
  }
}

void main() {
  var player3 = PlayerC(name: 'wjpark', xp: 1200, team: 'blue', age: 21);
  player3.sayHello();
}
```

### 4-④. Classes : Named Constructors
{: #upj_1678579663262}

```dart
class PlayerC {
  final String name, team;
  int xp, age;

  PlayerC(
      {required this.name,
      required this.xp,
      required this.team,
      required this.age});

  PlayerC.createRedPlayer({required String name, required int age})
      : this.name = name,
        this.age = age,
        this.team = 'blue',
        this.xp = 0;

  PlayerC.createBluePlayer(String name, int age)
      : this.name = name,
        this.age = age,
        this.team = 'red',
        this.xp = 0;

  void sayHello() {
    print('Hi my name is $name. team:$team, age:$age, xp:$xp');
  }
}

void main() {
  var playerRed = PlayerC.createRedPlayer(name: 'wjRed', age: 21);
  playerRed.sayHello();
  var playerBlue = PlayerC.createBluePlayer('wjBlue', 31);
  playerBlue.sayHello();
}
```

### 4-⑤. Classes : Review
{: #upj_1678579671970}

```dart
class PlayerC {
  final String name, team;
  int xp, age;

  PlayerC(
      {required this.name,
      required this.xp,
      required this.team,
      required this.age});

  PlayerC.createRedPlayer({required String name, required int age})
      : this.name = name,
        this.age = age,
        this.team = 'blue',
        this.xp = 0;

  PlayerC.createBluePlayer(String name, int age)
      : this.name = name,
        this.age = age,
        this.team = 'red',
        this.xp = 0;

  void sayHello() {
    print('Hi my name is $name. team:$team, age:$age, xp:$xp');
  }
}

void main() {
  var playerRed = PlayerC.createRedPlayer(name: 'wjRed', age: 21);
  playerRed.sayHello();
  var playerBlue = PlayerC.createBluePlayer('wjBlue', 31);
  playerBlue.sayHello();
}
```

### 4-⑥. Classes : Cascade Notation
{: #upj_1678579680250}

```dart
class PlayerE {
  String name;
  int xp;
  String team;

  PlayerE({required this.name, required this.xp, required this.team});

  void sayHello() {
    print('Hi my name is $name. team:$team, xp=$xp.');
  }
}

void main() {
  var wjpark = PlayerE(name: 'wjpark', xp: 2000, team: 'pink')
    ..name = 'esther'
    ..xp = 120000
    ..team = 'orange'
    ..sayHello();
}
```

### 4-⑦. Classes : Enums
{: #upj_1678579688586}

```dart
enum Team { red, blue }
enum XPLevel { beginner, medium, pro }

class Player {
  final String name;
  XPLevel xp;
  int age;
  Team team;

  Player(
      {required this.name,
      required this.xp,
      required this.team,
      required this.age});

  Player.createRedPlayer({required String name, required int age})
      : this.name = name,
        this.age = age,
        this.team = Team.red,
        this.xp = XPLevel.medium;

  Player.createBluePlayer(String name, int age)
      : this.name = name,
        this.age = age,
        this.team = Team.blue,
        this.xp = XPLevel.pro;

  void sayHello() {
    print('Hi my name is $name. team:$team, age:$age, xp:$xp');
  }
}

void main() {
  var playerRed = Player.createRedPlayer(name: 'wjRed', age: 21);
  playerRed.sayHello();
  var playerBlue = Player.createBluePlayer('wjBlue', 31);
  playerBlue.sayHello();
}
```

### 4-⑧. Classes : Abstract Classes
{: #upj_1678579694303}

```dart
// blue print
abstract class Human {
  void walk();
}

enum Team { red, blue }
enum XPLevel { beginner, medium, pro }

class Player extends Human {
  final String name;
  XPLevel xp;
  int age;
  Team team;

  Player(
      {required this.name,
      required this.xp,
      required this.team,
      required this.age});

  Player.createRedPlayer({required String name, required int age})
      : this.name = name,
        this.age = age,
        this.team = Team.red,
        this.xp = XPLevel.medium;

  Player.createBluePlayer(String name, int age)
      : this.name = name,
        this.age = age,
        this.team = Team.blue,
        this.xp = XPLevel.pro;

  void sayHello() {
    print('Hi my name is $name. team:$team, age:$age, xp:$xp');
  }

  @override
  void walk() {
    // TODO: implement walk
  }
}

class Coach extends Human {
  @override
  void walk() {
    // TODO: implement walk
  }
}

void main() {
  var playerRed = Player.createRedPlayer(name: 'wjRed', age: 21);
  playerRed.sayHello();
  var playerBlue = Player.createBluePlayer('wjBlue', 31);
  playerBlue.sayHello();
}
```

### 4-⑨. Classes : Inheritance
{: #upj_1678579704032}

```dart
class Human {
  final String name;

  Human({required this.name});

  void sayHello() {
    print("Hi my name is $name");
  }
}

enum Team { blue, red }

class Player extends Human {
  final Team team;

  Player({required this.team, required String name}) : super(name: name);

  @override
  void sayHello() {
    super.sayHello();
    print('and I play for $team');
  }
}

void main() {
  var player = Player(team: Team.red, name: 'wjpark');
  player.sayHello();
}
```

### 4-⑩. Classes : Mixins
{: #upj_1678579709980}

```dart
class Strong {
  final double strenghtLevel = 1500.99;
}

class QuickRunner {
  void runQuick() {
    print('ruuuuuuun!');
  }
}

class Tall {
  final double height = 1.99;
}

enum Team { blue, red }

class Player with Strong, QuickRunner, Tall {
  final Team team;

  Player({required this.team});
}

class Horse with Strong, QuickRunner {}

class Kid with QuickRunner {}

void main() {

}
```

## Udemy: Flutter & Dart
{: #upj_1677548319798}


### 1.Introduction
{: #upj_1677548386174}

[Flutter 와 React Native 차이점](https://academind.com/tutorials/react-native-vs-flutter-vs-ionic-vs-nativescript-vs-pwa)

[DartPad](https://dartpad.dev/)

### 2.Button
{: #upj_1677644455710}

MaterialApp > home

Scaffold > appBar, body

Different Types of Widget (Container)

- Output & Input (Visible)
  - Button, Text, Card
- Layout & Control (Invisible)
  - Row, Column, ListView

[New Button Style](https://docs.flutter.dev/release/breaking-changes/buttons)

- 변경된 버튼
  - TextButton ~~FlatButton~~
  - OutlinedButton ~~OutlineButton~~
  - ElevatedButton ~~RaisedButton~~

```dart
ElevatedButton(
  onPressed: () {}, 
  child: Text(
    '$btntxt',
    style: TextStyle(
      fontSize: 35,
      color: txtcolor
    ),
  ),
  style: ElevatedButton.styleFrom(
    backgroundColor: btncolor,
    shape: RoundedRectangleBorder(
      borderRadius: BorderRadius.circular(20)
    ),
    padding: EdgeInsets.all(20),
  ),
)

TextButton(
  onPressed: () {
      // Respond to button press
  },
  child: Text("TEXT BUTTON"),
)
TextButton.icon(
  onPressed: () {
      // Respond to button press
  },
  icon: Icon(Icons.add, size: 18),
  label: Text("TEXT BUTTON"),
)

OutlinedButton(
  onPressed: () {
      // Respond to button press
  },
  child: Text("OUTLINED BUTTON"),
)
OutlinedButton.icon(
  onPressed: () {
      // Respond to button press
  },
  icon: Icon(Icons.add, size: 18),
  label: Text("OUTLINED BUTTON"),
)
````

- RaisedButton, ElevatedButton
  - child
  - onPressed: 함수 포인터, 익명 함수
    - funName
    - () -> {}
  
[Dart List](https://dart.dev/guides/language/language-tour#lists),
[List Class](https://api.dart.dev/stable/2.3.1/dart-core/List-class.html)

[Widget 카달로그](https://docs.flutter.dev/development/ui/widgets)

RaisedButton and ElevatedButton

```dart
RaisedButton(
  color: Colors.blue,
  child: ...,
  onPressed: ...
)
ElevatedButton(
  style: ButtonStyle(
    backgroundColor: MaterialStateProperty.all(Colors.blue),
  ),
  child: ...,
  onPressed: ...,
),
```

### 3.Debugging & DevTools
{: #upj_1680265008560}

[Flutter Debugging](https://docs.flutter.dev/testing/debugging)

[DevTools](https://docs.flutter.dev/tools/devtools/overview)

### 4.Expense Tracker App
{: #upj_1680265208018}

[intl](https://pub.dev/packages/intl)

[DatFormat](https://pub.dev/documentation/intl/latest/intl/DateFormat-class.html)

- [간단한 계산기, CodeFlutter](https://www.youtube.com/watch?v=s9A2l6Y7GV4) ([코드](https://github.com/bimalkaf/Flutter_Basic_Calculator)) 더 잘 만들었다
- [Calculator, 설명없이](https://www.youtube.com/watch?v=cUxyqztdwwM) ([코드](https://github.com/sanket-kankariya/Calculator-flutter))
- [공학용 계산기](https://www.youtube.com/watch?v=l4bLPfS1uik)
- [Quiz App, Quiz App - Flutter Complete App - Speed Code](https://www.youtube.com/watch?v=Nhy0VWAMsFU) ([코드](https://github.com/abuanwar072/Quiz-App-Flutter))
- [Quiz App, Quiz App Flutter Speed Code 2023](https://www.youtube.com/watch?v=ORDjs-oHJ5Q) ([코드](https://github.com/bimalkaf/Flutter_Simple_Quiz_App))
- [ToDo App, Local List](https://www.youtube.com/watch?v=K4P5DZ9TRns)
- [ToDo Firebase](https://www.youtube.com/watch?v=qFrJ30VFCFc&list=PL9n0l8rSshSnSO4dNTJmKGNa0VNHrCQFR)
- [행맨 게임](https://youtu.be/hY9kNFdmPaE), [계산기](https://youtu.be/hY9kNFdmPaE)
- [CRUD SQLite](https://www.youtube.com/watch?v=jnkItI-0Fn0)
- [Firebase Login-out, 풍성한채널](https://www.youtube.com/watch?v=o_ZeLqpqt90)
- [음식배달앱 Part-1, 풍성한채널](https://www.youtube.com/watch?v=7dAt-JMSCVQ)
- [음식배달앱 Part-2, 풍성한채널](https://www.youtube.com/watch?v=GQJovou6zuE)

플러터 수업
- [플러터기초(오준석)](https://survivalcoding.com/courses/543787/lectures/9871615)
- [FlutterStudio레이아웃 만들기](https://flutterstudio.app/)
- [Material.io 디자인](https://m3.material.io/)
- [Flutter.dev 위젯 인덱스](https://docs.flutter.dev/reference/widgets)
- [iOS 디자인 가이드](https://developer.apple.com/design/human-interface-guidelines/widgets)
- [CodeFlutter, 기초실력 쌓기](https://www.youtube.com/@codeflutter7723/videos)

### 5.Flutter and Nodejs with Chatting
{: #upj_1680265214761}







```text
{: #upj_1680265224089}
{: #upj_1680265228994}
{: #upj_1680265238496}
```

