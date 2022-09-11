# FastAPI tutorial

## Installation

```bash
$ pip install fastapi[all]
```

Create `main.py`:

```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
async def root():
    return {"message": "Hello World!"}
```

Run the server using `uvicorn` with:

```bash
$ uvicorn main:app --reload
```

