# Dockerfile for book_catalog microservice
# Use an official Python runtime as a parent image
FROM python:3.9-slim

# Set the working directory in the container
WORKDIR /app

# Copy the requirements file into the container
COPY book_catalog/requirements.txt .

# Install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Copy the application code into the container
COPY book_catalog/ .

# Expose the port that the FastAPI app runs on
EXPOSE 8000

# Define environment variables
ENV DATABASE_URL=postgresql://postgresql_week06_user:5DfKE50nVJ3Wsbdb2NpvzeHlLPjVJIIU@dpg-cr9f5b3v2p9s73b6nmhg-a.oregon-postgres.render.com/postgresql_week06

# Command to run the FastAPI application
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
