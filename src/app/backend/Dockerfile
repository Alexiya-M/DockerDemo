FROM python:3.10-alpine

WORKDIR /usr/src/app

COPY src/ .

RUN if ( -f requirements.txt ); then pip install --no-cache-dir -r requirements.txt

EXPOSE 8000

CMD ["python", "src/main.py"]
