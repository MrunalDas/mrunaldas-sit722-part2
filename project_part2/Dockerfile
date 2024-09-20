# Dockerfile for book_catalog microservice

FROM python:3.11-alpine

# Set the working directory inside the container
WORKDIR /app/

# Copy the requirements file and install dependencies
COPY book_catalog/requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application code
COPY book_catalog/ .

# Expose the port the app will run on
EXPOSE 9000

# Command to run the application with Uvicorn
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "9000"]
