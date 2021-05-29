---
layout: post
title:  "fastapi-1"
summary: "fastapi-1"
author: noah
date: '2021-05-13 23:47:23 +0900'
category: framework
thumbnail: /assets/img/posts/uvicorn/uvicorn.png
keywords: framework, fastapi
permalink: /blog/fastapi-1/
---

fastapi로 실습을 해보기로 한다.

### 가상환경 구성

- `poetry`를 사용하여 가상환경을 구성한다.

    ```bash
    $ poetry init
    ```

- `fastapi` package 설치한다. 추가적으로 `uvicorn` 패키지도 설치해 준다.

    ```bash
    $ poetry add fastapi
    $ poetry add uvicorn
    ```

    - what is uvicorn?

- `main.py` 작성

    ```python
    from fastapi import FastAPI

    app = FastAPI()

    @app.get("/")
    def main():
        return {"Hello": "World"}
    ```

- 확인

    ![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/248da601-fcce-4856-9d7d-8496121429dc/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/248da601-fcce-4856-9d7d-8496121429dc/Untitled.png)