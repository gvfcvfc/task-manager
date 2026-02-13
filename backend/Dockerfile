# 1. Base image: Python installed
FROM python:3.11-slim

# 2. Set working directory inside container
WORKDIR /app


# Copy requirements from backend folder
COPY backend/requirements.txt ./requirements.txt

# 4. Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# 5. Copy the rest of the project files
COPY . .

# 6. Expose Flask port
EXPOSE 5000

# 7. Command to run the app
CMD ["gunicorn","-b" ,"0.0.0.0:5000","main:app"]

