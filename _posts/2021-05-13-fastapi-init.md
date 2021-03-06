---
layout: post
title:  "fastapi init"
summary: "fastapi init"
author: noah
date: '2021-05-29 23:47:23 +0900'
category: framework
thumbnail: /assets/img/posts/fastapi-init/fastapi.png
keywords: framework, fastapi
permalink: /blog/fastapi-init/
---

# fastapi로 실습을 해보기로 한다.

## <br>가상환경 구성

- `poetry`를 사용하여 가상환경을 구성한다.

    ```bash
    $ poetry init
    ```

- `fastapi` package 설치한다. 추가적으로 `uvicorn` 패키지도 설치해 준다.

    ```bash
    $ poetry add fastapi
    $ poetry add uvicorn
    ```

- what is uvicorn? [링크](https://noahnam.github.io/blog/uvicorn/#/)

- `main.py` 작성

    ```python
    from fastapi import FastAPI

    app = FastAPI()

    @app.get("/")
    def main():
        return {"Hello": "World"}
    ```
- uvicorn 실행
    
    ```bash
    $ uvicorn main:app --reload

    ```    

- 확인

<img src="/../../assets/img/posts/fastapi-init/1.png" style="zoom:65%;" />