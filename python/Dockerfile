FROM python:3.13.0a4-bullseye

WORKDIR /app

COPY main.py .
COPY requirements.txt .
COPY run.sh .
COPY utils.py .

COPY public public
COPY templates templates

RUN pip install --no-cache-dir -r requirements.txt

CMD ["python", "main.py"]