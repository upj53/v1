---
title: Web
layout: upj_design
permalink: /resource/web/
---

#### Table Of Contents

- TOC
{:toc}

## 사용팁
{: #upj_1703483602407}

### Bootstrap 5
{: #upj_1703483627304}

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title></title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-T3c6CoIi6uLrA9TneNEoa7RxnatzjcDSCmG1MXxSR1GAsXEV/Dwwykc2MPK8M2HN" crossorigin="anonymous">
</head>
<body>


<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js" integrity="sha384-C6RzsynM9kWDrMNeT87bh95OGNyZPhcTNXj1NW7RuBCsyN/o0jlpcV8Qyq46cDfL" crossorigin="anonymous"></script>
</body>
</html>
```

<!--

### JS fetch
{: #upj_1703824233619}

```javascript
```

## Snippets
{: #upj_1703496180623}

### Headers
{: #upj_1703496259873}

### Heros
{: #upj_1703496283059}

### Features
{: #upj_1703496299485}

### Sidebars
{: #upj_1703496317663}

## Custom Components
{: #upj_1703496336538}

### Album
{: #upj_1703496349725}

### Pricing
{: #upj_1703496359293}

### Checkout
{: #upj_1703496370341}

### Product
{: #upj_1703496379625}

### Cover
{: #upj_1703496390463}

### Carousel
{: #upj_1703496404221}

### Blog
{: #upj_1703496418926}

### Dashboard
{: #upj_1703496431806}

### Sign-in
{: #upj_1703496443803}

### Sticky footer
{: #upj_1703496454759}

### Sticky footer navbar
{: #upj_1703496471844}

### Jumbotron
{: #upj_1703496483764}

## Framework
{: #upj_1703496502036}

-->

### Starter template
{: #upj_1703496516531}

[Starter template](https://getbootstrap.kr/docs/5.0/examples/starter-template/){:target="_blank"}

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta name="description" content="">
    <meta name="author" content="Mark Otto, Jacob Thornton, and Bootstrap contributors">
    <meta name="generator" content="Hugo 0.84.0">
    <title>Starter Template · Bootstrap v5.0</title>

    <link rel="canonical" href="https://getbootstrap.com/docs/5.0/examples/starter-template/">

    

    <!-- Bootstrap core CSS -->
<link href="../assets/dist/css/bootstrap.min.css" rel="stylesheet">

    <style>
      .bd-placeholder-img {
        font-size: 1.125rem;
        text-anchor: middle;
        -webkit-user-select: none;
        -moz-user-select: none;
        user-select: none;
      }

      @media (min-width: 768px) {
        .bd-placeholder-img-lg {
          font-size: 3.5rem;
        }
      }
    </style>

    
    <!-- Custom styles for this template -->
    <link href="starter-template.css" rel="stylesheet">
  </head>
  <body>
    
<div class="col-lg-8 mx-auto p-3 py-md-5">
  <header class="d-flex align-items-center pb-3 mb-5 border-bottom">
    <a href="/" class="d-flex align-items-center text-dark text-decoration-none">
      <svg xmlns="http://www.w3.org/2000/svg" width="40" height="32" class="me-2" viewBox="0 0 118 94" role="img"><title>Bootstrap</title><path fill-rule="evenodd" clip-rule="evenodd" d="M24.509 0c-6.733 0-11.715 5.893-11.492 12.284.214 6.14-.064 14.092-2.066 20.577C8.943 39.365 5.547 43.485 0 44.014v5.972c5.547.529 8.943 4.649 10.951 11.153 2.002 6.485 2.28 14.437 2.066 20.577C12.794 88.106 17.776 94 24.51 94H93.5c6.733 0 11.714-5.893 11.491-12.284-.214-6.14.064-14.092 2.066-20.577 2.009-6.504 5.396-10.624 10.943-11.153v-5.972c-5.547-.529-8.934-4.649-10.943-11.153-2.002-6.484-2.28-14.437-2.066-20.577C105.214 5.894 100.233 0 93.5 0H24.508zM80 57.863C80 66.663 73.436 72 62.543 72H44a2 2 0 01-2-2V24a2 2 0 012-2h18.437c9.083 0 15.044 4.92 15.044 12.474 0 5.302-4.01 10.049-9.119 10.88v.277C75.317 46.394 80 51.21 80 57.863zM60.521 28.34H49.948v14.934h8.905c6.884 0 10.68-2.772 10.68-7.727 0-4.643-3.264-7.207-9.012-7.207zM49.948 49.2v16.458H60.91c7.167 0 10.964-2.876 10.964-8.281 0-5.406-3.903-8.178-11.425-8.178H49.948z" fill="currentColor"></path></svg>
      <span class="fs-4">Starter template</span>
    </a>
  </header>

  <main>
    <h1>Get started with Bootstrap</h1>
    <p class="fs-5 col-md-8">Quickly and easily get started with Bootstrap's compiled, production-ready files with this barebones example featuring some basic HTML and helpful links. Download all our examples to get started.</p>

    <div class="mb-5">
      <a href="../examples/" class="btn btn-primary btn-lg px-4">Download examples</a>
    </div>

    <hr class="col-3 col-md-2 mb-5">

    <div class="row g-5">
      <div class="col-md-6">
        <h2>Starter projects</h2>
        <p>Ready to beyond the starter template? Check out these open source projects that you can quickly duplicate to a new GitHub repository.</p>
        <ul class="icon-list">
          <li><a href="https://github.com/twbs/bootstrap-npm-starter" rel="noopener" target="_blank">Bootstrap npm starter</a></li>
          <li class="text-muted">Bootstrap Parcel starter (coming soon!)</li>
        </ul>
      </div>

      <div class="col-md-6">
        <h2>Guides</h2>
        <p>Read more detailed instructions and documentation on using or contributing to Bootstrap.</p>
        <ul class="icon-list">
          <li><a href="../getting-started/introduction/">Bootstrap quick start guide</a></li>
          <li><a href="../getting-started/webpack/">Bootstrap Webpack guide</a></li>
          <li><a href="../getting-started/parcel/">Bootstrap Parcel guide</a></li>
          <li><a href="../getting-started/build-tools/">Contributing to Bootstrap</a></li>
        </ul>
      </div>
    </div>
  </main>
  <footer class="pt-5 my-5 text-muted border-top">
    Created by the Bootstrap team &middot; &copy; 2021
  </footer>
</div>


    <script src="../assets/dist/js/bootstrap.bundle.min.js"></script>

      
  </body>
</html>
```

```css
.icon-list {
  padding-left: 0;
  list-style: none;
}
.icon-list li {
  display: flex;
  align-items: flex-start;
  margin-bottom: .25rem;
}
.icon-list li::before {
  display: block;
  flex-shrink: 0;
  width: 1.5em;
  height: 1.5em;
  margin-right: .5rem;
  content: "";
  background: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' fill='%23212529' viewBox='0 0 16 16'%3E%3Cpath d='M8 0a8 8 0 1 1 0 16A8 8 0 0 1 8 0zM4.5 7.5a.5.5 0 0 0 0 1h5.793l-2.147 2.146a.5.5 0 0 0 .708.708l3-3a.5.5 0 0 0 0-.708l-3-3a.5.5 0 1 0-.708.708L10.293 7.5H4.5z'/%3E%3C/svg%3E") no-repeat center center / 100% auto;
}
```

### Grid
{: #upj_1703496529233}

[Grid](https://getbootstrap.kr/docs/5.0/examples/grid/){:target="_blank"}


### Cheatsheet
{: #upj_1703496548880}

[Cheatsheet](https://getbootstrap.kr/docs/5.0/examples/cheatsheet/){:target="_blank"}

### Navbars
{: #upj_1703496691955}

**Default**

![navbar-default](https://github.com/upj53/upj53.github.io/assets/27456270/ac80981f-0cfe-4223-a229-4724c231f8f6)

```html
<nav class="navbar navbar-expand-lg bg-body-tertiary">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Navbar</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Link</a>
        </li>
        <li class="nav-item dropdown">
          <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
            Dropdown
          </a>
          <ul class="dropdown-menu">
            <li><a class="dropdown-item" href="#">Action</a></li>
            <li><a class="dropdown-item" href="#">Another action</a></li>
            <li><hr class="dropdown-divider"></li>
            <li><a class="dropdown-item" href="#">Something else here</a></li>
          </ul>
        </li>
        <li class="nav-item">
          <a class="nav-link disabled" aria-disabled="true">Disabled</a>
        </li>
      </ul>
      <form class="d-flex" role="search">
        <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
        <button class="btn btn-outline-success" type="submit">Search</button>
      </form>
    </div>
  </div>
</nav>
```

**오른쪽 정렬**

```html
<!--네비게이션 바-->
<nav class="navbar navbar-expand-lg bg-body-tertiary">
  <div class="container-fluid">
    <a class="navbar-brand" use:link href="/">HOME</a>
    <button
      class="navbar-toggler"
      type="button"
      data-bs-toggle="collapse"
      data-bs-target="#navbarNavDropdown"
      aria-controls="navbarNavDropdown"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <div
      class="collapse navbar-collapse justify-content-end"
      id="navbarNavDropdown"
    >
      <ul class="navbar-nav">
        <li class="nav-item" style="width:30px;"></li>
        <li class="nav-item">
          <a
            class="nav-link"
            use:link
            href="/"
            on:click={() => {
              $access_token = "";
              $userid = "";
              $is_student_login = false;
              $is_teacher_login = false;
            }}>관리자 로그아웃 ({$userid})</a
          >
        </li>
        <li class="nav-item" style="width:30px;"></li>
      </ul>
    </div>
  </div>
</nav>
```

<!--

## Navbars
{: #upj_1703496680627}

### Navbar static
{: #upj_1703496702041}

### Navbar fixed
{: #upj_1703496716050}

### Navbar bottom
{: #upj_1703496724618}

### Offcanvas navbar
{: #upj_1703496739375}

-->

## FastAPI 공식 튜토리얼
{: #upj_1703307119262}

```text
Declare Request Example Data
Extra Data Types
Cookie Parameters
Header Parameters
Response Model - Return Type
Extra Models
Response Status Code
Form Data
Request Files
Request Forms and Files
Handling Errors
Path Operation Configuration
JSON Compatible Encoder
Body - Updates
Dependencies
Dependencies
Classes as Dependencies
Sub-dependencies
Dependencies in path operation decorators
Global Dependencies
Dependencies with yield
Security
Security
Security - First Steps
Get Current User
Simple OAuth2 with Password and Bearer
OAuth2 with Password (and hashing), Bearer with JWT tokens
Middleware
CORS (Cross-Origin Resource Sharing)
SQL (Relational) Databases
Bigger Applications - Multiple Files
Background Tasks
Metadata and Docs URLs
Static Files
Testing
```

### Path Parameters
{: #upj_1703246882823}

Path Parameters

```python
from fastapi import FastAPI
from enum import Enum

class ModelName(str, Enum):
    alexnet = 'alexnet'
    resnet = 'resnet'
    lenet = 'lenet'

@app.get('/models/{model_name}')
async def get_model(model_name: ModelName):
    if model_name is ModelName.alexnet:
        return {'model_name': model_name, 'message': 'Deep Leaning FTW!'}
    if model_name.value == 'lenet':
        return {'model_name': model_name, 'message': 'LeCNN all the images'}
    return {'model_name': model_name, 'message': 'Have some residuals'}

# Path convertor
@app.get('/files/{file_path:path}')
async def read_file(file_path: str):
    return {'file_path': file_path}
```

### Query Parameters
{: #upj_1703306703367}

```python
from fastapi import FastAPI
app = FastAPI()

fake_items_db = [
    {'item_name': 'foo'}, {'item_name': 'bar'}, {'item_name': 'baz'}
]

@app.get('/items/')
async def read_item(skip: int = 0, limit: int = 1):
    return fake_items_db[skip: skip + limit]

# https://upj53api-test.run.goorm.io/items/?limit=2
```

### Request Body
{: #upj_1703309283645}

Pydantic 베이스모델

```python
from typing import Union
from pydantic import BaseModel

class Item(BaseModel):
    name: str
    description: Union[str, None] = None
    price: float
    tax: Union[float, None] = None

@app.post('/items')
async def create_item(item: Item):
    return item
```

Union을 사용하여 정수 또는 문자열을 받는 간단한 엔드포인트

```python
from fastapi import FastAPI
from typing import Union

app = FastAPI()

@app.post("/items/")
async def create_item(item: Union[int, str]):
    return {"item": item}
```

HTML Post 예제

main.py
```python
from fastapi import FastAPI, Form, Request
from typing import Union
from pydantic import BaseModel
from fastapi.templating import Jinja2Templates
app = FastAPI()
templates = Jinja2Templates(directory='./templates')

@app.get('/login')
def get_login_form(request: Request):
    return templates.TemplateResponse(
        'test.html', context={'request': request, 'id': 2}
    )

@app.post('/login')
def login(username:str=Form(...), password:str=Form(...)):
    return {'username': username, 'password': password}
```

test.html
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
<form method="post">
<input type="string" name="username" value="{{username}}" />
<input type="password" name="password" value="{{password}}" />

<input type="text" value="{{id}}" disabled />
<input type="submit" value="Submit" />
</form>
</body>
</html>
```

파일 업로드 예제

main.py

```python
from fastapi import FastAPI, Form, Request, File, UploadFile
from typing import Union, List
from pydantic import BaseModel
from fastapi.templating import Jinja2Templates
app = FastAPI()
templates = Jinja2Templates(directory='./templates')

@app.get('/files')
def get_login_form(request: Request):
    return templates.TemplateResponse(
        'test1.html', context={'request': request}
    )

@app.post('/files')
def create(files: List[bytes]=File(...)):
    return  {'file_sizes': [len(file) for file in files]}

@app.get('/uploadedfiles')
def get_login_form(request: Request):
    return templates.TemplateResponse(
        'test2.html', context={'request': request}
    )

@app.post('/uploadedfiles')
def create_uploaded(files: List[UploadFile]=File(...)):
    return {'file_sizes': [file.filename for file in files]}
```

test1.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
<form method="post" enctype="multipart/form-data">
<input type="file" multiple name="files" />
<input type="submit" value="Submit" />
</form>
</body>
</html>
```

test2.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
<form method="post" enctype="multipart/form-data">
<input type="file" multiple name="files" />
<input type="submit" value="Submit" />
</form>
</body>
</html>
```

### Body - Multiple Parameters
{: #upj_1703329290140}

```python
from fastapi import FastAPI, Form, Request, File, UploadFile
from typing import Union, List
from pydantic import BaseModel
app = FastAPI()

class Item(BaseModel):
    name: str 
    description: Union[str, None] = None
    price: float 
    tax: Union[float, None] = None 

class User(BaseModel):
    username: str 
    full_name: Union[str, None] = None

@app.put('/items/{item_id}')
async def update_item(item_id: int, item: Item, user: User):
    results = {
        'item_id': item_id,
        'item': item,
        'user': user
    }
    return results
```

### Body - Nested Models
{: #upj_1703332157947}

main.py

```python
from fastapi import FastAPI, Form, Request, File, UploadFile
from typing import Union, List, Set
from pydantic import BaseModel, HttpUrl
app = FastAPI()

class Image(BaseModel):
    url: HttpUrl
    name: str

class Item(BaseModel):
    name: str 
    description: Union[str, None] = None
    price: float 
    tax: Union[float, None] = None 
    tags: Set[str] = set()
    images: Union[List[Image], None] = None

@app.put('/items/{item_id}')
async def update_item(item_id: int, item: Item):
    results = {
        'item_id': item_id,
        'item': item
    }
    return results
```

Bodies of pure lists

```python
from fastapi import FastAPI, Form, Request, File, UploadFile
from typing import Union, List, Set
from pydantic import BaseModel, HttpUrl
app = FastAPI()

class Image(BaseModel):
    url: HttpUrl
    name: str

@app.post('/images/multiple/')
async def create_multiple_images(images: List[Image]):
    return images
```

## FastAPI + Svelte
{: #upj_1705753377209}

### 문법
{: #upj_1705753410367}

```html
1. 분기문
{#if 조건문1}
    <p>조건문1에 해당하면 실행</p>
{:else if 조건문2}
    <p>조건문2에 해당하면 실행</p>
{:else}
    <p>조건문1, 2 모두 해당하지 않으면 실행</p>
{/if}

2. 반복문
{#each list as item, index}
    <p>순서: {index} </p>
    <p>{item}</p>
{/each}
index는 반복순서를 의미하고 0부터 1씩 증가한다.
(index는 each문에서 생략 가능하다.)

3. 객체 표시
{객체}
{객체.속성}
```

### 파일 시스템 구조
{: #upj_1705714728884}

**FRONT Svelt 폴더 구조**

```text
┳(assets)
┃  └ svelte.svg
┠(components)
┃  ├ Error.svelte
┃  └ Navigation.svelte
┠(lib)
┃  ├ app.js
┃  └ store.js
┠(routes)
┃  ├ Home.svelte
┃  └ 
┠ App.svelte
┠ app.css
┠ main.js
┖ .env
```

**BACK FastAPI 폴더 구조**

```text
┳(frontend)
┃  └ (assets)
┠(models)
┃  ├ __init__.pyp
┃  └ 
┠(modules)
┃  ├ __init__.pyp
┃  └ 
┠(routers)
┃  ├ __init__.pyp
┃  └ 
┠(schemas)
┃  ├ __init__.pyp
┃  └ 
┠ main.py
┠ 
┖ .env
```

<details>
<summary>**FRONT /App.svelte**
</summary>

```html
<script>
  import Router from "svelte-spa-router";
  import Home from "./routes/Home.svelte";
  import Detail from "./routes/Detail.svelte";
  import QuestionCreate from "./routes/QuestionCreate.svelte";
  import Navigation from "./components/Navigation.svelte";
  import UserCreate from "./routes/UserCreate.svelte";
  import UserLogin from "./routes/UserLogin.svelte";
  import QuestionModify from "./routes/QuestionModify.svelte";
  import AnswerModify from "./routes/AnswerModify.svelte";

  const routes = {
    "/": Home,
    "/detail/:question_idx": Detail,
    "/question-create": QuestionCreate,
    "/user-create": UserCreate,
    "/user-login": UserLogin,
    "/question-modify/:question_id": QuestionModify,
    "/answer-modify/:answer_id": AnswerModify,
  };
</script>

<Navigation />
<Router {routes} />
```
</details>

<details>
<summary>**FRONT /app.css**
</summary>

```html
:root {
  font-family: Inter, system-ui, Avenir, Helvetica, Arial, sans-serif;
  line-height: 1.5;
  font-weight: 400;

  color-scheme: light dark;

  font-synthesis: none;
  text-rendering: optimizeLegibility;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
```
</details>

<details>
<summary>**FRONT /main.js**
</summary>
```javascript
import './app.css'
import 'bootstrap/dist/css/bootstrap.min.css'
import 'bootstrap/dist/js/bootstrap.js'
import App from './App.svelte'

const app = new App({
  target: document.getElementById('app'),
})

export default app
```
</details>

### Mysql 데이터베이스 세팅
{: #upj_1705714728883}

<details>
<summary>**BACK /modules/db.py**
</summary>

```python
from dotenv import dotenv_values
from sqlalchemy import create_engine
from sqlalchemy.ext.declarative import declarative_base
from sqlalchemy.orm import sessionmaker, scoped_session

config = dotenv_values('.env')

user_name = config['DB_USER_NAME']
user_pwd = config['DB_USER_PWD']
db_host = config['DB_HOST']
db_name = config['DB_NAME']

DATABASE = f'mysql://{user_name}:{user_pwd}@{db_host}/{db_name}?charset=utf8'

ENGINE = create_engine(
  DATABASE,
  echo=True
)

session = scoped_session(
  sessionmaker(
    autocommit=False,
    autoflush=False,
    bind=ENGINE
  )
)

Base = declarative_base()
Base.query = session.query_property()

def get_db():
  db = session()
  try:
    yield db
  finally:
    db.close()
```
</details>


### 회원가입 CRUD
{: #upj_1705714728886}

<details>
<summary>**FRONT /routes/UserCreate.svelte**
</summary>

```html
<script>
  import { push } from "svelte-spa-router";
  import fastapi from "../lib/api";
  import Error from "../components/Error.svelte";

  let error = { detail: [] };
  let username = "";
  let password1 = "";
  let password2 = "";
  let email = "";

  function post_user(event) {
    event.preventDefault();
    let url = "/pybo/user/create";
    let params = {
      username: username,
      password1: password1,
      password2: password2,
      email: email,
    };
    fastapi(
      "post",
      url,
      params,
      (json) => {
        push("/user-login");
      },
      (json_error) => {
        error = json_error;
      },
    );
  }
</script>

<div class="container">
  <h5 class="my-3 border-bottom pb-2">회원가입</h5>
  <Error {error} />
  <form method="post">
    <div class="mb-3">
      <label for="username">사용자 이름</label>
      <input
        type="text"
        class="form-control"
        id="username"
        bind:value={username}
      />
    </div>
    <div class="mb-3">
      <label for="password1">비밀번호</label>
      <input
        type="password"
        class="form-control"
        id="password1"
        bind:value={password1}
      />
    </div>
    <div class="mb-3">
      <label for="password2">비밀번호 확인</label>
      <input
        type="password"
        class="form-control"
        id="password2"
        bind:value={password2}
      />
    </div>
    <div class="mb-3">
      <label for="email">이메일</label>
      <input type="email" class="form-control" id="email" bind:value={email} />
    </div>
    <button class="btn btn-primary" type="submit" on:click={post_user}
      >생성하기</button
    >
  </form>
</div>
```
</details>

<details>
<summary>**FRONT /components/Error.svelte**
</summary>

```html
<script>
  export let error;
</script>

{#if typeof error.detail === "string"}
  <div class="alert alert-danger">{error.detail}</div>
{:else if typeof error.detail === "object" && error.detail.length > 0}
  <div class="alert alert-danger">
    {#each error.detail as err, i}
      <div>
        <string>{err.loc[1]}</string> : {err.msg}
      </div>
    {/each}
  </div>
{/if}
```
</details>

<details>
<summary>**FRONT /lib/api.js**
</summary>

```javascript
import qs from "qs"
import { access_token, username, is_login } from "./store"
import { get } from 'svelte/store'
import { push } from 'svelte-spa-router'

const fastapi = (operation, url, params, success_callback, failure_callback) => {
  let method = operation
  let content_type = 'application/json'
  let body = JSON.stringify(params)

  if (operation === 'login') {
    method = 'post'
    content_type = 'application/x-www-form-urlencoded'
    body = qs.stringify(params)
  }

  let _url = import.meta.env.VITE_SERVER_URL + url
  if (method === 'get') {
    _url += '?' + new URLSearchParams(params)
  }

  let options = {
    method: method,
    headers: {
      'Content-Type': content_type
    }
  }

  const _access_token = get(access_token)
  // console.log(`_access_token=${_access_token}`)
  if (_access_token) {
    // console.log(`_access_token=${_access_token}`)
    // 'Bearer ' Bearer뒤에 띄어쓰기를 꼭 해야한다.
    options.headers['Authorization'] = 'Bearer ' + _access_token 
  }

  if (method !== 'get') {
    options['body'] = body
  }

  fetch(_url, options)
    .then(response => {
      if (response.status === 204) { // No content
        if (success_callback) {
          // console.log(`response.status === 204`)
          success_callback()
        }
        return
      }
      response.json()
        .then(json => {
          if (response.status >= 200 && response.status < 300) { // 200~299
            if (success_callback) {
              success_callback(json)
            }
          } else if (operation !== 'login' && response.status === 401) { // token time out
            access_token.set('')
            username.set('')
            is_login.set(false)
            alert('로그인이 필요합니다')
            push('/user-login')
          } else {
            if (failure_callback) {
              failure_callback(json)
            } else {
              console.log(json)
            }
          }
        })
        .catch(error => {
          console.log(error)
        })
    }
    )
}

export default fastapi
```
</details>

<details>
<summary>**BACK /main.py**
</summary>

```python
# python libraries
from dotenv import dotenv_values
from fastapi import FastAPI, Form, Request, File, UploadFile, Depends, Body
from fastapi.responses import HTMLResponse, FileResponse
from fastapi.templating import Jinja2Templates
from fastapi.staticfiles import StaticFiles
from starlette.middleware.cors import CORSMiddleware
from starlette.responses import RedirectResponse
from typing import Union, List, Set, Annotated, Dict, Any
from pydantic import BaseModel, HttpUrl
import os
import time
import requests

# user libraries
from modules.db import session
from routers import *
from models import *

app = FastAPI(dependencies=[Depends(get_query_token)])
app.include_router(router_pybo.router)

config = dotenv_values('.env')
domain = config['DOMAIN_URL']
app.add_middleware(
    CORSMiddleware,
    allow_origins=['*'],
    allow_credentials=True,
    allow_methods=['*'],
    allow_headers=['*']
)
app.mount('/static', StaticFiles(directory='./static'), name='static')
app.mount('/assets', StaticFiles(directory='./frontend/assets'))

@app.get('/test-pybo-svelte')
async def test_pybo_index():
    return FileResponse('./frontend/index-pybo.html')
```
</details>

<details>
<summary>**BACK /routers/router_pybo.py**
</summary>

**__init__.py**

```pytyon
import routers.router_pybo
import routers.router_edu
```

```python
# python libraries
from fastapi import FastAPI, Form, Request, File, UploadFile, Depends, Body
from fastapi import APIRouter, Depends, HTTPException, Body
from fastapi.responses import HTMLResponse, FileResponse
from fastapi.security import OAuth2PasswordBearer, OAuth2PasswordRequestForm
from jose import jwt, JWTError
from datetime import timedelta, datetime
from pydantic import BaseModel
from fastapi.templating import Jinja2Templates
from dotenv import dotenv_values
from typing import Annotated
from sqlalchemy.orm import Session
from starlette import status

# user libraries
from modules.db import get_db
from models import *
from schemas import *
from modules import *

# import secrets
# secrets.token_hex(32)
router = APIRouter(prefix="/pybo", tags=["pybo"])
config = dotenv_values(".env")

ACCESS_TOKEN_EXPIRE_MINUTES = 60*24
SECRET_KEY = 'f9d2b97ee5c112796127fc6af1b1d19b0d80d97142b80f5bbb635665f85f1c6f'
ALGORITHM = 'HS256'
oauth2_scheme = OAuth2PasswordBearer(tokenUrl='/pybo/user/login')


def get_current_user(
        token: str = Depends(oauth2_scheme),
        db: Session = Depends(get_db)):
    credentials_exception = HTTPException(
        status_code=status.HTTP_401_UNAUTHORIZED,
        detail='Could not validate credentials',
        headers={'WWW-Authenticate': 'Bearer'},
    )
    try:
        payload = jwt.decode(token, SECRET_KEY, algorithms=[ALGORITHM])
        username: str = payload.get('sub')
        if username is None:
            raise credentials_exception
    except JWTError:
        raise credentials_exception
    else:
        user = pybo_get_user(db, username)
        if user is None:
            raise credentials_exception
        return user


@router.post('/user/create', status_code=status.HTTP_204_NO_CONTENT)
async def user_create(
        _user_create: PyboUserCreateSchema,
        db: Session = Depends(get_db)):
    user = pybo_get_existing_user(db, _user_create)
    if user:
        raise HTTPException(
            status_code=status.HTTP_409_CONFLICT,
            detail='이미 존재하는 사용자 아이디 또는 이메일입니다.'
        )
    pybo_create_user(db, _user_create)


@router.post('/user/login', response_model=PyboTokenSchema)
async def login_for_access_token(
        form_data: OAuth2PasswordRequestForm = Depends(),
        db: Session = Depends(get_db)):
    # check user and password
    user = pybo_get_user(db, form_data.username)
    print(f'{form_data.username}, {form_data.password}')
    print(f'{user.username}, {user.password}')
    if not user or not pwd_context.verify(form_data.password, user.password):
        raise HTTPException(
            status_code=status.HTTP_401_UNAUTHORIZED,
            detail='Incorrect username or password',
            headers={'WWW-Authenticate': 'Bearer'}
        )

    # make access token
    data = {
        'sub': user.username,
        'exp': datetime.utcnow()+timedelta(minutes=ACCESS_TOKEN_EXPIRE_MINUTES)
    }
    access_token = jwt.encode(data, SECRET_KEY, algorithm=ALGORITHM)

    return {
        'access_token': access_token,
        'token_type': 'bearer',
        'username': user.username
    }
```
</details>

<details>
<summary>**BACK /models/pybo_models.py**
</summary>

```python
# python libraries
from sqlalchemy import Column, Integer, String, Text, DateTime, ForeignKey, Table
from sqlalchemy.orm import relationship
from pydantic import BaseModel

# user libraries
from modules.db import Base
from modules.db import ENGINE

class PyboUserModel(Base):
    __tablename__ = 'pybo_user'
    idx = Column(Integer, primary_key=True)
    username = Column(String(30), unique=True, nullable=False)
    password = Column(String(100), nullable=False)
    email = Column(String(50), unique=True, nullable=False)


Base.metadata.create_all(bind=ENGINE)
```
</details>

<details>
<summary>**BACK /schemas/pybo_schemas.py**
</summary>

```python
# python libraries
import datetime
from pydantic import BaseModel, EmailStr
from pydantic import field_validator
from pydantic_core.core_schema import FieldValidationInfo


class PyboUserSchema(BaseModel):
    idx: int
    username: str
    email: str


class PyboUserCreateSchema(BaseModel):
    username: str
    password1: str
    password2: str
    email: EmailStr

    @field_validator('username', 'password1', 'password2', 'email')
    def not_empty(cls, v):
        if not v or not v.strip():
            raise ValueError('빈 값은 허용되지 않습니다')
        return v

    @field_validator('password2')
    def passwords_match(cls, v, info: FieldValidationInfo):
        if 'password1' in info.data and v != info.data['password1']:
            raise ValueError('비밀번호가 일치하지 않습니다')
        return v
```
</details>

<details>
<summary>**BACK /modules/pybo_crud.py**
</summary>

```python
# python libraries
from sqlalchemy.orm import Session
from sqlalchemy import and_
from datetime import datetime
from passlib.context import CryptContext

# user libraries
from models import *
from schemas import *

pwd_context = CryptContext(schemes=['bcrypt'], deprecated='auto')


def pybo_create_user(db: Session, user_create: PyboUserCreateSchema):
    db_user = PyboUserModel(
        username=user_create.username,
        password=pwd_context.hash(user_create.password1),
        email=user_create.email
    )
    db.add(db_user)
    db.commit()


def pybo_get_existing_user(db: Session, user_create: PyboUserCreateSchema):
    return db.query(PyboUserModel).filter(
        (PyboUserModel.username == user_create.username) |
        (PyboUserModel.email == user_create.email)
    ).first()


def pybo_get_user(db: Session, username: str):
    return db.query(PyboUserModel).filter(PyboUserModel.username == username).first()


def pybo_make_db(db: Session):
    user1 = pybo_get_user(db, 'test1')
    user2 = pybo_get_user(db, 'test2')
    for i in range(5):
        # subject = f'테스트 데이터 {i+1:03d}'
        # print(subject)
        if i < 3:
            q = PyboQuestionModel(
                subject=f'테스트 데이터 {i+1:03d}',
                content=f'내용없음 {i+1:03d}',
                create_date=datetime.now(),
                user=user1)
            db.add(q)
        else:
            q = PyboQuestionModel(
                subject=f'테스트 데이터 {i+1:03d}',
                content=f'내용없음 {i+1:03d}',
                create_date=datetime.now(),
                user=user2)
            db.add(q)
    db.commit()
```
</details>

### 게시판 CRUD
{: #upj_1705714728887}

<details>
<summary>**FRONT /lib/store.js**
</summary>

```javascript
import { writable } from 'svelte/store'

const persist_storage = (key, initValue) => {
  const storedValueStr = localStorage.getItem(key)
  const store = writable(storedValueStr != null ? JSON.parse(storedValueStr) : initValue)  //JSON.parse(storedValueStr)
  store.subscribe((val) => {
    localStorage.setItem(key, JSON.stringify(val))
  })
  return store
}

export const page = persist_storage('page', 0)
export const keyword = persist_storage('keyword', '')
export const access_token = persist_storage('access_token', '')
export const username = persist_storage('username', '')
export const is_login = persist_storage('is_login', false)
```
</details>

<details>
<summary>**FRONT /routes/Home.svelte**
</summary>

```html
<script>
  import fastapi from "../lib/api";
  import { link } from "svelte-spa-router";
  import { page, keyword, is_login } from "../lib/store";
  import moment from "moment/min/moment-with-locales";
  moment.locale("ko");

  let question_list = [];
  let size = 10;
  let total = 0;
  let kw = "";
  $: total_page = Math.ceil(total / size);

  function get_question_list() {
    let params = {
      page: $page,
      size: size,
      keyword: $keyword,
    };
    fastapi("get", "/pybo/list", params, (json) => {
      question_list = json.question_list;
      total = json.total;
      kw = $keyword;
    });
  }

  $: $page, $keyword, get_question_list();
</script>

<div class="container my-3">
  <div class="row my-3">
    <div class="col-6">
      <a
        use:link
        href="/question-create"
        class="btn btn-primary {$is_login ? '' : 'disabled'}">질문 등록하기</a
      >
    </div>
    <div class="col-6">
      <div class="input-group">
        <input type="text" class="form-control" bind:value={kw} />
        <button
          class="btn btn-outline-secondary"
          on:click={() => {
            $keyword = kw;
            $page = 0;
          }}>찾기</button
        >
      </div>
    </div>
  </div>
  <table class="table">
    <thead>
      <tr class="text-center table-dark">
        <th>번호</th>
        <th style="width:50%;">제목</th>
        <th>글쓴이</th>
        <th>작성일시</th>
      </tr>
    </thead>
    <tbody>
      {#each question_list as question, i}
        <tr class="text-center">
          <td>{total - $page * size - i}</td>
          <td class="text-start">
            <a use:link href="/detail/{question.idx}">{question.subject}</a>
            {#if question.answers.length > 0}
              <span class="text-danger small mx-2"
                >{question.answers.length}</span
              >
            {/if}
          </td>
          <td>{question.user ? question.user.username : ""}</td>
          <td
            >{moment(question.create_date).format(
              "YYYY년 MM월 DD일 hh:mm a",
            )}</td
          >
        </tr>
      {/each}
    </tbody>
  </table>
  <!--페이징 처리-->
  <ul class="pagination justify-content-center">
    <!--이전 페이지-->
    <li class="page-item {$page <= 0 && 'disabled'}">
      <button
        class="page-link"
        on:click={() => {
          $page--;
        }}>이전</button
      >
    </li>
    <!--페이지 번호-->
    {#each Array(total_page) as _, loop_page}
      {#if loop_page >= $page - 5 && loop_page <= $page + 5}
        <li class="page-item {loop_page === $page && 'active'}">
          <button
            class="page-link"
            on:click={() => {
              $page = loop_page;
            }}>{loop_page + 1}</button
          >
        </li>
      {/if}
    {/each}
    <!--다음 페이지-->
    <li class="page-item {$page >= total_page - 1 && 'disabled'}">
      <button
        class="page-link"
        on:click={() => {
          $page++;
        }}>다음</button
      >
    </li>
  </ul>
</div>
```
</details>

<details>
<summary>**FRONT /routes/Detail.svelte**
</summary>

```html
<script>
  import fastapi from "../lib/api";
  import Error from "../components/Error.svelte";
  import { link, push } from "svelte-spa-router";
  import { page, access_token, is_login, username } from "../lib/store";
  import { marked } from "marked";
  import moment from "moment/min/moment-with-locales";
  moment.locale("ko");

  export let params = {};
  let question_idx = params.question_idx;
  let question = { answers: [], voter: [], content: "" };
  let content = "";
  let error = { detail: [] };

  function get_question() {
    fastapi("get", `/pybo/detail/${question_idx}`, {}, (json) => {
      question = json;
    });
  }

  get_question();

  function post_answer(event) {
    event.preventDefault();
    let url = "/pybo/answer/create/" + question_idx;
    // console.log(url);
    // if (content.trim() == "") {
    // return;
    // }
    let params = {};
    params["content"] = content;
    fastapi(
      "post",
      url,
      params,
      (json) => {
        content = "";
        error = { detail: [] };
        get_question();
      },
      (err_json) => {
        error = err_json;
      },
    );
  }

  function delete_question(_question_id) {
    if (window.confirm("정말로 삭제하시겠습니까?")) {
      let url = "/pybo/question/delete";
      let params = {
        question_id: _question_id,
      };
      fastapi(
        "delete",
        url,
        params,
        (json) => {
          push("/");
        },
        (json_error) => {
          error = json_error;
        },
      );
    }
  }

  function delete_answer(answer_id) {
    if (window.confirm("정말로 삭제하시겠습니까?")) {
      let url = "/pybo/answer/delete";
      let params = {
        answer_idx: answer_id,
      };
      fastapi(
        "delete",
        url,
        params,
        (json) => {
          get_question();
        },
        (json_error) => {
          error = json_error;
        },
      );
    }
  }

  function vote_question(_question_id) {
    if (window.confirm("정말로 추천하시겠습니까?")) {
      let url = "/pybo/question/vote";
      let params = {
        question_idx: _question_id,
      };
      fastapi(
        "post",
        url,
        params,
        (json) => {
          get_question();
        },
        (json_error) => {
          error = json_error;
        },
      );
    }
  }

  function vote_answer(_answer_id) {
    if (window.confirm("정말로 추천하시겠습니까?")) {
      let url = "/pybo/answer/vote";
      let params = {
        answer_idx: _answer_id,
      };
      fastapi(
        "post",
        url,
        params,
        (json) => {
          get_question();
        },
        (json_error) => {
          error = json_error;
        },
      );
    }
  }
</script>

<div class="container my-3">
  <!--질문-->
  <h2 class="border-bottom py-2">{question.subject}</h2>
  <div class="card my-3">
    <div class="card-body">
      <div class="card-text">
        {@html marked.parse(question.content)}
      </div>
      <div class="d-flex justify-content-end">
        {#if question.modify_date}
          <div class="badge bg-light text-dark p-2 text-start mx-3">
            <div class="mb-2">modified at</div>
            <div>
              {moment(question.modify_date).format("YYYY년 MM월 DD일 hh:mm a")}
            </div>
          </div>
        {/if}
        <div class="badge bg-light text-dark p-2 text-start">
          <div class="mb-2">
            {question.user ? question.user.username : ""}
          </div>
          <div>
            {moment(question.create_date).format("YYYY년 MM월 DD일 hh:mm a")}
          </div>
        </div>
      </div>
      <div class="my-3">
        <button
          class="btn btn-sm btn-outline-secondary {$is_login ? '' : 'disabled'}"
          on:click={vote_question(question.idx)}
        >
          추천
          <span class="badge rounded-pill bg-success"
            >{question.voter.length}</span
          ></button
        >
        {#if question.user && $username === question.user.username}
          <a
            use:link
            href="/question-modify/{question.idx}"
            class="btn btn-sm btn-outline-secondary">수정</a
          >
          <button
            class="btn btn-sm btn-outline-secondary"
            on:click={() => {
              delete_question(question.idx);
            }}>삭제</button
          >
        {/if}
      </div>
    </div>
  </div>

  <button
    class="btn btn-secondary"
    on:click={() => {
      push("/");
    }}>목록으로</button
  >

  <!--답변 목록-->
  <h5 class="border-bottom my-3 py-2">
    {question.answers.length}개의 답변이 있습니다.
  </h5>
  {#each question.answers as answer}
    <div class="card my-3">
      <div class="card-body">
        <div class="card-text">
          {@html marked.parse(answer.content)}
        </div>
        <div class="d-flex justify-content-end">
          {#if answer.modify_date}
            <div class="badge bg-light text-dark p-2 text-start mx-3">
              <div class="mb-2">modified at</div>
              <div>
                {moment(answer.modify_date).format("YYYY년 MM월 DD일 hh:mm a")}
              </div>
            </div>
          {/if}
          <div class="badge bg-light text-dark p-2">
            <div class="mb-2">
              {answer.user ? answer.user.username : ""}
            </div>
            <div>
              {moment(answer.create_date).format("YYYY년 MM월 DD일 hh:mm a")}
            </div>
          </div>
        </div>
        <div class="my-3">
          <button
            class="btn btn-sm btn-outline-secondary {$is_login
              ? ''
              : 'disabled'}"
            on:click={vote_answer(answer.idx)}
          >
            추천
            <span class="badge rounded-pill bg-success"
              >{answer.voter.length}</span
            ></button
          >
          {#if answer.user && $username === answer.user.username}
            <a
              use:link
              href="/answer-modify/{answer.idx}"
              class="btn btn-sm btn-outline-secondary">수정</a
            >
            <button
              class="btn btn-sm btn-outline-secondary"
              on:click={() => {
                delete_answer(answer.idx);
              }}>삭제</button
            >
          {/if}
        </div>
      </div>
    </div>
  {/each}
  <!--답변 등록-->
  <Error {error} />
  <form method="post" class="my-3">
    <div class="mb-3">
      <textarea
        rows="10"
        bind:value={content}
        class="form-control"
        disabled={$is_login ? "" : "disabled"}
      ></textarea>
    </div>
    <input
      type="submit"
      value="답변등록"
      class="btn btn-primary {$is_login ? '' : 'disabled'}"
      on:click={post_answer}
    />
  </form>
</div>
```
</details>

<details>
<summary>**FRONT /routes/QuestionCreate.svelte**
</summary>

```html
<script>
  import { push } from "svelte-spa-router";
  import fastapi from "../lib/api";
  import { page, access_token, is_login, username } from "../lib/store";
  import Error from "../components/Error.svelte";

  let error = { detail: [] };
  let subject = "";
  let content = "";

  function post_question(event) {
    event.preventDefault();
    let url = "/pybo/question/create";
    let params = {
      subject: subject,
      content: content,
    };
    fastapi(
      "post",
      url,
      params,
      (json) => {
        push("/");
      },
      (json_error) => {
        error = json_error;
      },
    );
  }
</script>

<div class="container">
  <h5 class="my-3 border-bottom pb-2">질문 등록</h5>
  <Error {error} />
  <form method="post" class="my-3">
    <div class="mb-3">
      <label for="subject">제목</label>
      <input type="text" class="form-control" bind:value={subject} />
    </div>
    <div class="mb-3">
      <label for="content">내용</label>
      <textarea class="form-control" rows="10" bind:value={content}></textarea>
    </div>
    <button class="btn btn-primary" on:click={post_question}>저장하기</button>
  </form>
</div>
```
</details>

<details>
<summary>**FRONT /routes/QuestionModify.svelte**
</summary>

```html
<script>
  import { push } from "svelte-spa-router";
  import fastapi from "../lib/api";
  import { page, access_token, is_login, username } from "../lib/store";
  import Error from "../components/Error.svelte";

  export let params = {};
  const question_id = params.question_id;

  let error = { detail: [] };
  // let question = { answers: [] };
  let subject = "";
  let content = "";

  fastapi("get", `/pybo/detail/${question_id}`, {}, (json) => {
    subject = json.subject;
    content = json.content;
    // question = json;
  });

  function update_question(event) {
    event.preventDefault();
    let url = "/pybo/question/update";
    let params = {
      question_idx: question_id,
      subject: subject,
      content: content,
    };
    fastapi(
      "put",
      url,
      params,
      (json) => {
        push("/detail/" + question_id);
      },
      (json_error) => {
        error = json_error;
      },
    );
  }
</script>

<div class="container">
  <h5 class="my-3 border-bottom pb-2">질문 수정</h5>
  <Error {error} />
  <form method="post" class="my-3">
    <div class="mb-3">
      <label for="subject">제목</label>
      <input type="text" class="form-control" bind:value={subject} />
    </div>
    <div class="mb-3">
      <label for="content">내용</label>
      <textarea rows="10" class="form-control" bind:value={content}></textarea>
    </div>
    <button class="btn btn-primary" on:click={update_question}>수정하기</button>
  </form>
</div>
```
</details>

<details>
<summary>**FRONT /routes/AnswerModify.svelte**
</summary>

```html
<script>
  import fastapi from "../lib/api";
  import Error from "../components/Error.svelte";
  import { push } from "svelte-spa-router";

  export let params = {};
  const answer_id = params.answer_id;

  let error = { detail: [] };
  let question_id = 0;
  let content = "";

  fastapi("get", "/pybo/answer/detail/" + answer_id, {}, (json) => {
    question_id = json.question_idx;
    content = json.content;
  });

  function update_answer(event) {
    event.preventDefault();
    let url = "/pybo/answer/update";
    let params = {
      answer_idx: answer_id,
      content: content,
    };
    fastapi(
      "put",
      url,
      params,
      (json) => {
        push("/detail/" + question_id);
      },
      (json_error) => {
        error = json_error;
      },
    );
  }
</script>

<div class="container">
  <h5 class="my-3 border-bottom pb-2">답변 수정</h5>
  <Error {error} />
  <form class="my-3" method="post">
    <div class="mb-3">
      <label for="content">내용</label>
      <textarea rows="10" class="form-control" bind:value={content}></textarea>
      <button class="btn btn-primary" on:click={update_answer}>수정하기</button>
    </div>
  </form>
</div>
```
</details>

<details>
<summary>**BACK /routers/router_pybo.py**
</summary>

```python
# python libraries
from fastapi import FastAPI, Form, Request, File, UploadFile, Depends, Body
from fastapi import APIRouter, Depends, HTTPException, Body
from fastapi.responses import HTMLResponse, FileResponse
from fastapi.security import OAuth2PasswordBearer, OAuth2PasswordRequestForm
from jose import jwt, JWTError
from datetime import timedelta, datetime
from pydantic import BaseModel
from fastapi.templating import Jinja2Templates
from dotenv import dotenv_values
from typing import Annotated
from sqlalchemy.orm import Session
from starlette import status

# user libraries
from modules.db import get_db
from models import *
from schemas import *
from modules import *

router = APIRouter(prefix="/pybo", tags=["pybo"])
config = dotenv_values(".env")

ACCESS_TOKEN_EXPIRE_MINUTES = 60*24
SECRET_KEY = 'f9d2b97ee5c112796127fc6af1b1d19b0d80d97142b80f5bbb635665f85f1c6f'
ALGORITHM = 'HS256'
oauth2_scheme = OAuth2PasswordBearer(tokenUrl='/pybo/user/login')


@router.get("/list", response_model=PyboQuestionListSchema)
async def question_list(
        db: Session = Depends(get_db),
        page: int = 0, size: int = 10, keyword:str=''):
    # total, _question_list = pybo_get_question_list(
        # db, skip=page*size, limit=size)
    total, _question_list = pybo_get_search_list(
        db, page*size, size, keyword)
    return {
        'total': total,
        'question_list': _question_list
    }


@router.get("/detail/{question_idx}", response_model=PyboQuestionSchema)
async def question_detail(question_idx: int, db: Session = Depends(get_db)):
    question = pybo_get_question(db, question_idx)
    return question


def get_current_user(
        token: str = Depends(oauth2_scheme),
        db: Session = Depends(get_db)):
    credentials_exception = HTTPException(
        status_code=status.HTTP_401_UNAUTHORIZED,
        detail='Could not validate credentials',
        headers={'WWW-Authenticate': 'Bearer'},
    )
    try:
        payload = jwt.decode(token, SECRET_KEY, algorithms=[ALGORITHM])
        username: str = payload.get('sub')
        if username is None:
            raise credentials_exception
    except JWTError:
        raise credentials_exception
    else:
        user = pybo_get_user(db, username)
        if user is None:
            raise credentials_exception
        return user


@router.post('/answer/create/{question_idx}', status_code=status.HTTP_204_NO_CONTENT)
async def answer_create(
        question_idx: int,
        _answer_create: PyboAnswerCreateSchema = Body(...),
        db: Session = Depends(get_db),
        current_user: PyboUserModel = Depends(get_current_user)):
    # create answer
    question = pybo_get_question(db, question_idx)
    if not question:
        raise HTTPException(status_code=404, detail='Question not found')
    pybo_create_answer(
        db,
        question,
        _answer_create,
        current_user)


@router.post('/question/create', status_code=status.HTTP_204_NO_CONTENT)
async def question_create(
        _question_create: PyboQuestionCreateSchema,
        db: Session = Depends(get_db),
        current_user: PyboUserModel = Depends(get_current_user)):
    pybo_create_question(
        db,
        _question_create,
        current_user)


@router.get('/make-db')
async def make_db(db: Session = Depends(get_db)):
    pybo_make_db(db)


@router.put('/question/update', status_code=status.HTTP_204_NO_CONTENT)
async def question_update(
        _question_update: PyboQuestionUpdateSchema,
        db: Session = Depends(get_db),
        current_user: PyboUserModel = Depends(get_current_user)):
    db_question = pybo_get_question(db, _question_update.question_idx)
    if not db_question:
        raise HTTPException(
            status_code=status.HTTP_400_BAD_REQUEST,
            detail='데이터를 찾을 수 없습니다.')
    if current_user.idx != db_question.user.idx:
        raise HTTPException(
            status_code=status.HTTP_400_BAD_REQUEST,
            detail='수정 권한이 없습니다.')
    pybo_update_question(db, db_question, _question_update)


@router.delete('/question/delete', status_code=status.HTTP_204_NO_CONTENT)
async def question_delete(
        _question_delete: PyboQuestionDeleteSchema,
        db: Session = Depends(get_db),
        current_user: PyboUserModel = Depends(get_current_user)):
    db_question = pybo_get_question(db, _question_delete.question_idx)
    if not db_question:
        raise HTTPException(
            status_code=status.HTTP_400_BAD_REQUEST,
            detail='데이터를 찾을 수 없습니다.')
    if current_user.idx != db_question.user.idx:
        raise HTTPException(
            status_code=status.HTTP_400_BAD_REQUEST,
            detail='삭제 권한이 없습니다.')
    pybo_delete_question(db, db_question)


@router.get('/answer/detail/{answer_idx}', response_model=PyboAnswerSchema)
async def answer_detail(answer_idx: int, db: Session = Depends(get_db)):
    answer = pybo_get_answer(db, answer_idx)
    return answer


@router.put('/answer/update', status_code=status.HTTP_204_NO_CONTENT)
async def answer_update(
        _answer_update: PyboAnswerUpdateSchema,
        db: Session = Depends(get_db),
        current_user: PyboUserModel = Depends(get_current_user)):
    db_answer = pybo_get_answer(db, _answer_update.answer_idx)
    if not db_answer:
        raise HTTPException(
            status_code=status.HTTP_400_BAD_REQUEST,
            detail='데이터를 찾을 수 없습니다.')
    if current_user.idx != db_answer.user.idx:
        raise HTTPException(
            status_code=status.HTTP_400_BAD_REQUEST,
            detail='수정 권한이 없습니다.')
    pybo_update_answer(db, db_answer, _answer_update)


@router.delete('/answer/delete', status_code=status.HTTP_204_NO_CONTENT)
async def answer_delete(
        _answer_delete: PyboAnswerDeleteScheme,
        db: Session = Depends(get_db),
        current_user: PyboUserModel = Depends(get_current_user)):
    db_answer = pybo_get_answer(db, _answer_delete.answer_idx)
    if not db_answer:
        raise HTTPException(
            status_code=status.HTTP_400_BAD_REQUEST,
            detail='데이터를 찾을 수 없습니다.')
    if current_user.idx != db_answer.user.idx:
        raise HTTPException(
            status_code=status.HTTP_400_BAD_REQUEST,
            detail='삭제 권한이 없습니다.')
    pybo_delete_answer(db, db_answer)


@router.post('/question/vote', status_code=status.HTTP_204_NO_CONTENT)
async def question_vote(
        _question_vote: PyboQuestionVoteSchema,
        db: Session = Depends(get_db),
        current_user: PyboUserModel = Depends(get_current_user)):
    db_question = pybo_get_question(db, _question_vote.question_idx)
    if not db_question:
        raise HTTPException(
            status_code=status.HTTP_400_BAD_REQUEST,
            detail='데이터를 찾을 수 없습니다.')
    pybo_vote_question(db, db_question, current_user)


@router.post('/answer/vote', status_code=status.HTTP_204_NO_CONTENT)
async def answer_vote(
        _answer_vote: PyboAnswerVoteSchema,
        db: Session = Depends(get_db),
        current_user: PyboUserModel = Depends(get_current_user)):
    db_answer = pybo_get_answer(db, _answer_vote.answer_idx)
    if not db_answer:
        raise HTTPException(
            status_code=status.HTTP_400_BAD_REQUEST,
            detail='데이터를 찾을 수 없습니다')
    pybo_vote_answer(db, db_answer, current_user)
```
</details>

<details>
<summary>**BACK /models/pybo_models.py**
</summary>

```python
# python libraries
from sqlalchemy.orm import Session
from sqlalchemy import and_
from datetime import datetime
from passlib.context import CryptContext

# user libraries
from models import *
from schemas import *

def pybo_get_question_list(db: Session, skip: int = 0, limit: int = 10):
    _question_list = db.query(PyboQuestionModel)\
        .order_by(PyboQuestionModel.create_date.desc())\
        .order_by(PyboQuestionModel.subject.desc())

    total = _question_list.count()
    question_list = _question_list.offset(skip).limit(limit).all()
    return total, question_list  # 전체 개수, 페이징 적용된 질문 목록


def pybo_get_question(db: Session, question_idx: int):
    question = db.query(PyboQuestionModel).get(question_idx)
    return question


def pybo_create_answer(
        db: Session,
        question: PyboQuestionModel,
        answer_create: PyboAnswerCreateSchema,
        user: PyboUserModel):
    db_answer = PyboAnswerModel(
        question=question,
        content=answer_create.content,
        create_date=datetime.now(),
        user=user)
    db.add(db_answer)
    db.commit()


def pybo_create_question(
        db: Session,
        question_create: PyboQuestionCreateSchema,
        user: PyboUserModel):
    db_question = PyboQuestionModel(
        subject=question_create.subject,
        content=question_create.content,
        create_date=datetime.now(),
        user=user)
    db.add(db_question)
    db.commit()


def pybo_make_db(db: Session):
    user1 = pybo_get_user(db, 'test1')
    user2 = pybo_get_user(db, 'test2')
    for i in range(5):
        # subject = f'테스트 데이터 {i+1:03d}'
        # print(subject)
        if i < 3:
            q = PyboQuestionModel(
                subject=f'테스트 데이터 {i+1:03d}',
                content=f'내용없음 {i+1:03d}',
                create_date=datetime.now(),
                user=user1)
            db.add(q)
        else:
            q = PyboQuestionModel(
                subject=f'테스트 데이터 {i+1:03d}',
                content=f'내용없음 {i+1:03d}',
                create_date=datetime.now(),
                user=user2)
            db.add(q)
    db.commit()


pwd_context = CryptContext(schemes=['bcrypt'], deprecated='auto')


def pybo_get_existing_user(db: Session, user_create: PyboUserCreateSchema):
    return db.query(PyboUserModel).filter(
        (PyboUserModel.username == user_create.username) |
        (PyboUserModel.email == user_create.email)
    ).first()


def pybo_get_user(db: Session, username: str):
    return db.query(PyboUserModel).filter(PyboUserModel.username == username).first()


def pybo_update_question(
        db: Session,
        db_question: PyboQuestionModel,
        question_update: PyboQuestionUpdateSchema):
    db_question.subject = question_update.subject
    db_question.content = question_update.content
    db_question.modify_date = datetime.now()
    # db.add(db_question)
    db.commit()


def pybo_delete_question(db: Session, db_question: PyboQuestionModel):
    db.delete(db_question)
    db.commit()


def pybo_get_answer(db: Session, answer_idx: int):
    return db.query(PyboAnswerModel).get(answer_idx)


def pybo_update_answer(
        db: Session,
        db_answer: PyboAnswerModel,
        answer_update: PyboAnswerUpdateSchema):
    db_answer.content = answer_update.content
    db_answer.modify_date = datetime.now()
    db.commit()


def pybo_delete_answer(db: Session, db_answer: PyboAnswerModel):
    db.delete(db_answer)
    db.commit()


def pybo_vote_question(
        db: Session, db_question: PyboQuestionModel, db_user: PyboUserModel):
    db_question.voter.append(db_user)
    db.commit()


def pybo_vote_answer(
        db: Session, db_answer: PyboAnswerModel, db_user: PyboUserModel):
    db_answer.voter.append(db_user)
    db.commit()


def pybo_get_search_list(db: Session, skip: int = 0, limit: int = 0, keyword: str = ''):
    search_list = db.query(PyboQuestionModel)
    if keyword:
        search = f'%%{keyword}%%'
        sub_query = db.query(PyboAnswerModel.question_idx, PyboAnswerModel.content, PyboUserModel.username)\
            .outerjoin(PyboUserModel, and_(PyboAnswerModel.user_idx == PyboUserModel.idx)).subquery()
        search_list = search_list\
            .outerjoin(PyboUserModel)\
            .outerjoin(sub_query, and_(sub_query.c.question_idx == PyboQuestionModel.idx))\
            .filter(
                PyboQuestionModel.subject.ilike(search) |  # 질문제목
                PyboQuestionModel.content.ilike(search) |  # 질문내용
                PyboUserModel.username.ilike(search) |  # 질문작성자
                sub_query.c.content.ilike(search) |  # 답변내용
                sub_query.c.username.ilike(search)  # 답변작성자
            )
    total = search_list.distinct().count()
    search_list = search_list.order_by(PyboQuestionModel.create_date.desc())\
        .offset(skip).limit(limit).distinct().all()
    return total, search_list
```
</details>

<details>
<summary>**BACK /schemas/pybo_schemas.py**
</summary>

```python
# python libraries
import datetime
from pydantic import BaseModel, EmailStr
from pydantic import field_validator
from pydantic_core.core_schema import FieldValidationInfo


class PyboAnswerSchema(BaseModel):
    idx: int
    content: str
    create_date: datetime.datetime
    user: PyboUserSchema | None
    question_idx: int
    modify_date: datetime.datetime | None = None
    voter: list[PyboUserSchema]

    class Config:
        orm_mode = True


class PyboQuestionSchema(BaseModel):
    idx: int
    subject: str | None = None
    content: str | None = None
    create_date: datetime.datetime
    answers: list[PyboAnswerSchema] = []
    user: PyboUserSchema | None
    modify_date: datetime.datetime | None = None
    voter: list[PyboUserSchema]

    class Config:
        orm_mode = True


class PyboAnswerCreateSchema(BaseModel):
    content: str

    @field_validator('content')
    def not_empty(cls, v):
        if not v or not v.strip():
            raise ValueError('빈 값은 허용되지 않습니다.')
        return v

    class Config:
        orm_mode = True


class PyboQuestionCreateSchema(BaseModel):
    subject: str
    content: str

    @field_validator('subject', 'content')
    def not_empty(cls, v):
        if not v or not v.strip():
            raise ValueError('빈 값은 허용되지 않습니다.')
        return v

    class Config:
        orm_mode = True


class PyboQuestionListSchema(BaseModel):
    total: int = 0
    question_list: list[PyboQuestionSchema] = []


class PyboTokenSchema(BaseModel):
    access_token: str
    token_type: str
    username: str


class PyboQuestionUpdateSchema(PyboQuestionCreateSchema):
    question_idx: int


class PyboQuestionDeleteSchema(BaseModel):
    question_idx: int


class PyboAnswerUpdateSchema(PyboAnswerCreateSchema):
    answer_idx: int


class PyboAnswerDeleteScheme(BaseModel):
    answer_idx: int


class PyboQuestionVoteSchema(BaseModel):
    question_idx: int


class PyboAnswerVoteSchema(BaseModel):
    answer_idx: int
```
</details>

<details>
<summary>**BACK /modules/pybo_crud.py**
</summary>

```python
# python libraries
from sqlalchemy.orm import Session
from sqlalchemy import and_
from datetime import datetime
from passlib.context import CryptContext

# user libraries
from models import *
from schemas import *

def pybo_get_question_list(db: Session, skip: int = 0, limit: int = 10):
    _question_list = db.query(PyboQuestionModel)\
        .order_by(PyboQuestionModel.create_date.desc())\
        .order_by(PyboQuestionModel.subject.desc())

    total = _question_list.count()
    question_list = _question_list.offset(skip).limit(limit).all()
    return total, question_list  # 전체 개수, 페이징 적용된 질문 목록


def pybo_get_question(db: Session, question_idx: int):
    question = db.query(PyboQuestionModel).get(question_idx)
    return question


def pybo_create_answer(
        db: Session,
        question: PyboQuestionModel,
        answer_create: PyboAnswerCreateSchema,
        user: PyboUserModel):
    db_answer = PyboAnswerModel(
        question=question,
        content=answer_create.content,
        create_date=datetime.now(),
        user=user)
    db.add(db_answer)
    db.commit()


def pybo_create_question(
        db: Session,
        question_create: PyboQuestionCreateSchema,
        user: PyboUserModel):
    db_question = PyboQuestionModel(
        subject=question_create.subject,
        content=question_create.content,
        create_date=datetime.now(),
        user=user)
    db.add(db_question)
    db.commit()


def pybo_make_db(db: Session):
    user1 = pybo_get_user(db, 'test1')
    user2 = pybo_get_user(db, 'test2')
    for i in range(5):
        # subject = f'테스트 데이터 {i+1:03d}'
        # print(subject)
        if i < 3:
            q = PyboQuestionModel(
                subject=f'테스트 데이터 {i+1:03d}',
                content=f'내용없음 {i+1:03d}',
                create_date=datetime.now(),
                user=user1)
            db.add(q)
        else:
            q = PyboQuestionModel(
                subject=f'테스트 데이터 {i+1:03d}',
                content=f'내용없음 {i+1:03d}',
                create_date=datetime.now(),
                user=user2)
            db.add(q)
    db.commit()


pwd_context = CryptContext(schemes=['bcrypt'], deprecated='auto')


def pybo_get_existing_user(db: Session, user_create: PyboUserCreateSchema):
    return db.query(PyboUserModel).filter(
        (PyboUserModel.username == user_create.username) |
        (PyboUserModel.email == user_create.email)
    ).first()


def pybo_get_user(db: Session, username: str):
    return db.query(PyboUserModel).filter(PyboUserModel.username == username).first()


def pybo_update_question(
        db: Session,
        db_question: PyboQuestionModel,
        question_update: PyboQuestionUpdateSchema):
    db_question.subject = question_update.subject
    db_question.content = question_update.content
    db_question.modify_date = datetime.now()
    # db.add(db_question)
    db.commit()


def pybo_delete_question(db: Session, db_question: PyboQuestionModel):
    db.delete(db_question)
    db.commit()


def pybo_get_answer(db: Session, answer_idx: int):
    return db.query(PyboAnswerModel).get(answer_idx)


def pybo_update_answer(
        db: Session,
        db_answer: PyboAnswerModel,
        answer_update: PyboAnswerUpdateSchema):
    db_answer.content = answer_update.content
    db_answer.modify_date = datetime.now()
    db.commit()


def pybo_delete_answer(db: Session, db_answer: PyboAnswerModel):
    db.delete(db_answer)
    db.commit()


def pybo_vote_question(
        db: Session, db_question: PyboQuestionModel, db_user: PyboUserModel):
    db_question.voter.append(db_user)
    db.commit()


def pybo_vote_answer(
        db: Session, db_answer: PyboAnswerModel, db_user: PyboUserModel):
    db_answer.voter.append(db_user)
    db.commit()


def pybo_get_search_list(db: Session, skip: int = 0, limit: int = 0, keyword: str = ''):
    search_list = db.query(PyboQuestionModel)
    if keyword:
        search = f'%%{keyword}%%'
        sub_query = db.query(PyboAnswerModel.question_idx, PyboAnswerModel.content, PyboUserModel.username)\
            .outerjoin(PyboUserModel, and_(PyboAnswerModel.user_idx == PyboUserModel.idx)).subquery()
        search_list = search_list\
            .outerjoin(PyboUserModel)\
            .outerjoin(sub_query, and_(sub_query.c.question_idx == PyboQuestionModel.idx))\
            .filter(
                PyboQuestionModel.subject.ilike(search) |  # 질문제목
                PyboQuestionModel.content.ilike(search) |  # 질문내용
                PyboUserModel.username.ilike(search) |  # 질문작성자
                sub_query.c.content.ilike(search) |  # 답변내용
                sub_query.c.username.ilike(search)  # 답변작성자
            )
    total = search_list.distinct().count()
    search_list = search_list.order_by(PyboQuestionModel.create_date.desc())\
        .offset(skip).limit(limit).distinct().all()
    return total, search_list
```
</details>

### 로그인, 로그아웃
{: #upj_1705714728888}

<details>
<summary>**FRONT /components/Error.svelte**
</summary>

```html
<script>
  export let error;
</script>

{#if typeof error.detail === "string"}
  <div class="alert alert-danger">{error.detail}</div>
{:else if typeof error.detail === "object" && error.detail.length > 0}
  <div class="alert alert-danger">
    {#each error.detail as err, i}
      <div>
        <string>{err.loc[1]}</string> : {err.msg}
      </div>
    {/each}
  </div>
{/if}
```
</details>

<details>
<summary>**FRONT /components/Navigation.svelte**
</summary>

```html
<script>
  import { link } from "svelte-spa-router";
  import {
    page,
    keyword,
    access_token,
    username,
    is_login,
  } from "../lib/store";
</script>

<!--네비게이션바-->
<nav class="navbar navbar-expand-lg navbar-light bg-light border-bottom">
  <div class="container-fluid">
    <a
      use:link
      href="/"
      class="navbar-brand"
      on:click={() => {
        $keyword = "";
        $page = 0;
      }}>Pybo</a
    >
    <button
      class="navbar-toggler"
      type="button"
      data-bs-toggle="collapse"
      data-bs-target="#navbarSupportedContent"
      aria-controls="navbarSupportedContent"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon" />
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        {#if $is_login}
          <li class="nav-item">
            <a
              use:link
              href="/user-login"
              class="nav-link"
              on:click={() => {
                $access_token = "";
                $username = "";
                $is_login = false;
              }}>로그아웃 ({$username})</a
            >
          </li>
        {:else}
          <li class="nav-item">
            <a use:link href="/user-create" class="nav-link">회원가입</a>
          </li>
          <li class="nav-item">
            <a use:link href="/user-login" class="nav-link">로그인</a>
          </li>
        {/if}
      </ul>
    </div>
  </div>
</nav>
```
</details>

<details>
<summary>**FRONT /lib/api.js**
</summary>

```javascript
import qs from "qs"
import { access_token, username, is_login } from "./store"
import { get } from 'svelte/store'
import { push } from 'svelte-spa-router'

const fastapi = (operation, url, params, success_callback, failure_callback) => {
  let method = operation
  let content_type = 'application/json'
  let body = JSON.stringify(params)

  if (operation === 'login') {
    method = 'post'
    content_type = 'application/x-www-form-urlencoded'
    body = qs.stringify(params)
  }

  let _url = import.meta.env.VITE_SERVER_URL + url
  if (method === 'get') {
    _url += '?' + new URLSearchParams(params)
  }

  let options = {
    method: method,
    headers: {
      'Content-Type': content_type
    }
  }

  const _access_token = get(access_token)
  // console.log(`_access_token=${_access_token}`)
  if (_access_token) {
    // console.log(`_access_token=${_access_token}`)
    // 'Bearer ' Bearer뒤에 띄어쓰기를 꼭 해야한다.
    options.headers['Authorization'] = 'Bearer ' + _access_token 
  }

  if (method !== 'get') {
    options['body'] = body
  }

  fetch(_url, options)
    .then(response => {
      if (response.status === 204) { // No content
        if (success_callback) {
          // console.log(`response.status === 204`)
          success_callback()
        }
        return
      }
      response.json()
        .then(json => {
          if (response.status >= 200 && response.status < 300) { // 200~299
            if (success_callback) {
              success_callback(json)
            }
          } else if (operation !== 'login' && response.status === 401) { // token time out
            access_token.set('')
            username.set('')
            is_login.set(false)
            alert('로그인이 필요합니다')
            push('/user-login')
          } else {
            if (failure_callback) {
              failure_callback(json)
            } else {
              console.log(json)
            }
          }
        })
        .catch(error => {
          console.log(error)
        })
    }
    )
}

export default fastapi
```
</details>

<details>
<summary>**FRONT /lib/store.js**
</summary>

```javascript
import { writable } from 'svelte/store'

// export const page = writable(0)

/* */
const persist_storage = (key, initValue) => {
  const storedValueStr = localStorage.getItem(key)
  const store = writable(storedValueStr != null ? JSON.parse(storedValueStr) : initValue)  //JSON.parse(storedValueStr)
  store.subscribe((val) => {
    localStorage.setItem(key, JSON.stringify(val))
  })
  return store
}

export const page = persist_storage('page', 0)
export const keyword = persist_storage('keyword', '')
export const access_token = persist_storage('access_token', '')
export const username = persist_storage('username', '')
export const is_login = persist_storage('is_login', false)
```
</details>

<details>
<summary>**FRONT /routes/UserLogin.svelte**
</summary>

```html
<script>
  import { push } from "svelte-spa-router";
  import fastapi from "../lib/api";
  import Error from "../components/Error.svelte";
  import { access_token, username, is_login } from "../lib/store";

  let error = { detail: [] };
  let login_username = "";
  let login_password = "";

  function login(event) {
    event.preventDefault();
    let url = "/pybo/user/login";
    let params = {
      username: login_username,
      password: login_password,
    };
    fastapi(
      "login",
      url,
      params,
      (json) => {
        $access_token = json.access_token;
        $username = json.username;
        $is_login = true;
        push("/");
      },
      (json_error) => {
        error = json_error;
      },
    );
  }
</script>

<div class="container">
  <h5 class="my-3 border-bottom pb-2">로그인</h5>
  <Error {error} />
  <form method="post">
    <div class="mb-3">
      <label for="username">사용자 이름</label>
      <input
        type="text"
        class="form-control"
        id="username"
        bind:value={login_username}
      />
    </div>
    <div class="mb-3">
      <label for="password">비밀번호</label>
      <input
        type="password"
        class="form-control"
        id="password"
        bind:value={login_password}
      />
    </div>
    <button class="btn btn-primary" on:click={login}>로그인</button>
  </form>
</div>
```
</details>

<details>
<summary>**FRONT /routes/Detail.svelte**
</summary>

```html
<script>
  import fastapi from "../lib/api";
  import Error from "../components/Error.svelte";
  import { link, push } from "svelte-spa-router";
  import { page, access_token, is_login, username } from "../lib/store";
  import { marked } from "marked";
  import moment from "moment/min/moment-with-locales";
  moment.locale("ko");

  export let params = {};
  let question_idx = params.question_idx;
  let question = { answers: [], voter: [], content: "" };
  let content = "";
  let error = { detail: [] };

  function get_question() {
    fastapi("get", `/pybo/detail/${question_idx}`, {}, (json) => {
      question = json;
    });
  }

  get_question();

  function post_answer(event) {
    event.preventDefault();
    let url = "/pybo/answer/create/" + question_idx;
    // console.log(url);
    // if (content.trim() == "") {
    // return;
    // }
    let params = {};
    params["content"] = content;
    fastapi(
      "post",
      url,
      params,
      (json) => {
        content = "";
        error = { detail: [] };
        get_question();
      },
      (err_json) => {
        error = err_json;
      },
    );
  }

  function delete_question(_question_id) {
    if (window.confirm("정말로 삭제하시겠습니까?")) {
      let url = "/pybo/question/delete";
      let params = {
        question_id: _question_id,
      };
      fastapi(
        "delete",
        url,
        params,
        (json) => {
          push("/");
        },
        (json_error) => {
          error = json_error;
        },
      );
    }
  }

  function delete_answer(answer_id) {
    if (window.confirm("정말로 삭제하시겠습니까?")) {
      let url = "/pybo/answer/delete";
      let params = {
        answer_idx: answer_id,
      };
      fastapi(
        "delete",
        url,
        params,
        (json) => {
          get_question();
        },
        (json_error) => {
          error = json_error;
        },
      );
    }
  }

  function vote_question(_question_id) {
    if (window.confirm("정말로 추천하시겠습니까?")) {
      let url = "/pybo/question/vote";
      let params = {
        question_idx: _question_id,
      };
      fastapi(
        "post",
        url,
        params,
        (json) => {
          get_question();
        },
        (json_error) => {
          error = json_error;
        },
      );
    }
  }

  function vote_answer(_answer_id) {
    if (window.confirm("정말로 추천하시겠습니까?")) {
      let url = "/pybo/answer/vote";
      let params = {
        answer_idx: _answer_id,
      };
      fastapi(
        "post",
        url,
        params,
        (json) => {
          get_question();
        },
        (json_error) => {
          error = json_error;
        },
      );
    }
  }
</script>

<div class="container my-3">
  <!--질문-->
  <h2 class="border-bottom py-2">{question.subject}</h2>
  <div class="card my-3">
    <div class="card-body">
      <div class="card-text">
        {@html marked.parse(question.content)}
      </div>
      <div class="d-flex justify-content-end">
        {#if question.modify_date}
          <div class="badge bg-light text-dark p-2 text-start mx-3">
            <div class="mb-2">modified at</div>
            <div>
              {moment(question.modify_date).format("YYYY년 MM월 DD일 hh:mm a")}
            </div>
          </div>
        {/if}
        <div class="badge bg-light text-dark p-2 text-start">
          <div class="mb-2">
            {question.user ? question.user.username : ""}
          </div>
          <div>
            {moment(question.create_date).format("YYYY년 MM월 DD일 hh:mm a")}
          </div>
        </div>
      </div>
      <div class="my-3">
        <button
          class="btn btn-sm btn-outline-secondary {$is_login ? '' : 'disabled'}"
          on:click={vote_question(question.idx)}
        >
          추천
          <span class="badge rounded-pill bg-success"
            >{question.voter.length}</span
          ></button
        >
        {#if question.user && $username === question.user.username}
          <a
            use:link
            href="/question-modify/{question.idx}"
            class="btn btn-sm btn-outline-secondary">수정</a
          >
          <button
            class="btn btn-sm btn-outline-secondary"
            on:click={() => {
              delete_question(question.idx);
            }}>삭제</button
          >
        {/if}
      </div>
    </div>
  </div>

  <button
    class="btn btn-secondary"
    on:click={() => {
      push("/");
    }}>목록으로</button
  >

  <!--답변 목록-->
  <h5 class="border-bottom my-3 py-2">
    {question.answers.length}개의 답변이 있습니다.
  </h5>
  {#each question.answers as answer}
    <div class="card my-3">
      <div class="card-body">
        <div class="card-text">
          {@html marked.parse(answer.content)}
        </div>
        <div class="d-flex justify-content-end">
          {#if answer.modify_date}
            <div class="badge bg-light text-dark p-2 text-start mx-3">
              <div class="mb-2">modified at</div>
              <div>
                {moment(answer.modify_date).format("YYYY년 MM월 DD일 hh:mm a")}
              </div>
            </div>
          {/if}
          <div class="badge bg-light text-dark p-2">
            <div class="mb-2">
              {answer.user ? answer.user.username : ""}
            </div>
            <div>
              {moment(answer.create_date).format("YYYY년 MM월 DD일 hh:mm a")}
            </div>
          </div>
        </div>
        <div class="my-3">
          <button
            class="btn btn-sm btn-outline-secondary {$is_login
              ? ''
              : 'disabled'}"
            on:click={vote_answer(answer.idx)}
          >
            추천
            <span class="badge rounded-pill bg-success"
              >{answer.voter.length}</span
            ></button
          >
          {#if answer.user && $username === answer.user.username}
            <a
              use:link
              href="/answer-modify/{answer.idx}"
              class="btn btn-sm btn-outline-secondary">수정</a
            >
            <button
              class="btn btn-sm btn-outline-secondary"
              on:click={() => {
                delete_answer(answer.idx);
              }}>삭제</button
            >
          {/if}
        </div>
      </div>
    </div>
  {/each}
  <!--답변 등록-->
  <Error {error} />
  <form method="post" class="my-3">
    <div class="mb-3">
      <textarea
        rows="10"
        bind:value={content}
        class="form-control"
        disabled={$is_login ? "" : "disabled"}
      ></textarea>
    </div>
    <input
      type="submit"
      value="답변등록"
      class="btn btn-primary {$is_login ? '' : 'disabled'}"
      on:click={post_answer}
    />
  </form>
</div>
```
</details>

<details>
<summary>**BACK /routers/router_pybo.py**
</summary>

```python
from datetime import timedelta, datetime
from jose import jwt, JWTError

router = APIRouter(prefix="/pybo", tags=["pybo"])
config = dotenv_values(".env")

ACCESS_TOKEN_EXPIRE_MINUTES = 60*24
SECRET_KEY = 'f9d2b97ee5c112796127fc6af1b1d19b0d80d97142b80f5bbb635665f85f1c6f'
ALGORITHM = 'HS256'
oauth2_scheme = OAuth2PasswordBearer(tokenUrl='/pybo/user/login')

@router.post('/user/login', response_model=PyboTokenSchema)
async def login_for_access_token(
        form_data: OAuth2PasswordRequestForm = Depends(),
        db: Session = Depends(get_db)):
    # check user and password
    # form_data은 OAuth2PasswordRequestForm  의 username 과 password 를 사용함
    user = pybo_get_user(db, form_data.username)
    print(f'{form_data.username}, {form_data.password}')
    print(f'{user.username}, {user.password}')
    if not user or not pwd_context.verify(form_data.password, user.password):
        raise HTTPException(
            status_code=status.HTTP_401_UNAUTHORIZED,
            detail='Incorrect username or password',
            headers={'WWW-Authenticate': 'Bearer'}
        )
    # make access token
    data = {
        'sub': user.username,
        'exp': datetime.utcnow()+timedelta(minutes=ACCESS_TOKEN_EXPIRE_MINUTES)
    }
    access_token = jwt.encode(data, SECRET_KEY, algorithm=ALGORITHM)

    return {
        'access_token': access_token,
        'token_type': 'bearer',
        'username': user.username
    }        
```
</details>

<details>
<summary>**BACK /modules/pybo_crud.py**
</summary>

```python
def pybo_get_user(db: Session, username: str):
    return db.query(PyboUserModel).filter(PyboUserModel.username == username).first()
```
</details>

<details>
<summary>**BACK /models/pybo_models.py**
</summary>

```python
class PyboUserModel(Base):
    __tablename__ = 'pybo_user'
    idx = Column(Integer, primary_key=True)
    username = Column(String(30), unique=True, nullable=False)
    password = Column(String(100), nullable=False)
    email = Column(String(50), unique=True, nullable=False)
```
</details>

<details>
<summary>**BACK /schemas/pybo_schemas.py**
</summary>

```python
class PyboTokenSchema(BaseModel):
    access_token: str
    token_type: str
    username: str
```
</details>

<!--
### **D**elete
{: #upj_1705714728889}

### 로그인 & 로그아웃
{: #upj_1705714728890}
-->

