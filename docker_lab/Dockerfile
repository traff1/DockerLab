FROM python:3.12-alpine

WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY . .
COPY templates/ templates/
COPY static/ static/

RUN adduser -D flaskuser
USER flaskuser

CMD ["flask", "run", "--host=0.0.0.0"]