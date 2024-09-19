# Dockerfile for book_catalog microservice

FROM python:3.11-alpine
WORKDIR /app/
COPY book_catalog/requirements.txt .
RUN pip install --nocache-dir -r requirements.txt
COPY /book_catalog .
EXPOSE 9000
CMD [ "uvicorn", "main:app","0.0.0.0","--port","9000" ]