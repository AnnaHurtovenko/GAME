# Using Python as a base image
FROM python:3.9-slim

RUN apt-get update && apt-get install -y --no-install-recommends \
    build-essential \
    libpq-dev \
    && rm -rf /var/lib/apt/lists/*
    
# Working directory
WORKDIR /app

# Copy the project files
COPY . /app

# Setting up dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Opening the port 
EXPOSE 8000

# Command to launch the application
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
