FROM python:3.10-slim-bullseye

WORKDIR /app

COPY requirements/backend.in .

RUN pip install --n0-cache-dir -r requirements/backend.in

COPY . .

CMD ["uvicorn", "spaceship.main:app", "--host=0.0.0.0", "--port=8080"]