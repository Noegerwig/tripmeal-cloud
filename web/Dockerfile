# Use a minimal python 3.7 base image
FROM python:3.7-slim

# Set the working directory in the container
WORKDIR /app

# Copy only the requirements file first to leverage docker cache
COPY requirements.txt .

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application code
COPY . .

# Make app.py executable
RUN chmod +x /app/app.py

EXPOSE 5000

# Command to run the application
CMD ["python", "app.py"]
