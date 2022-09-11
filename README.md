---
typora-copy-images-to: ../../../../../home/mhered/fastapi_tutorial/assets/images
---

# FastAPI tutorial

## Installation

```bash
$ pip install fastapi[all]
```

## Hello World in 7 steps

Create `main.py`:

```python
from fastapi import FastAPI # 1) import FastAPI

my_app = FastAPI()  # 2) create a FastAPI instance in the variable my_app

@my_app.get("/")  # 3) define a path operation decorator for GET requests to the URL "/"
async def root():  # 4) write the path operation function
    return {"message": "Hello World!"}  # 5) return the content
```

then 6) run this basic JSON server using `uvicorn` with:

```bash
$ uvicorn main:my_app --reload
INFO:     Will watch for changes in these directories: ['/home/mhered/fastapi_tutorial']
INFO:     Uvicorn running on http://127.0.0.1:8000 (Press CTRL+C to quit)
INFO:     Started reloader process [73948] using watchgod
INFO:     Started server process [73950]
INFO:     Waiting for application startup.
INFO:     Application startup complete.
INFO:     127.0.0.1:41690 - "GET / HTTP/1.1" 200 OK

```

and 7) open your browser at http://127.0.0.1:8000: 

![](/home/mhered/fastapi_tutorial/assets/images/fastapi_helloworld.png)

You also get interactive documentation at http://127.0.0.1:8000/docs:

![fastapi_helloworld_docs](/home/mhered/fastapi_tutorial/assets/images/fastapi_helloworld_docs.png)
