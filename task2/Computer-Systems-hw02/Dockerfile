FROM python:3.12-slim

ENV APP_HOME=/app
WORKDIR $APP_HOME

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

RUN useradd -m myuser
USER myuser

EXPOSE 8000
CMD ["python", "main.py"]
