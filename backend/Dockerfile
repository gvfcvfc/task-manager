FROM python:3.11-slim

WORKDIR /app

# Copy requirements correctly
COPY backend/requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

# Copy ONLY backend code
COPY backend/ .

EXPOSE 5000

CMD ["gunicorn", "-b", "0.0.0.0:5000", "main:app"]
