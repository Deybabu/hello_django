# Use the official Python image as a parent image
FROM python:3.9

# Set environment variables for Python buffering and Django
ENV PYTHONUNBUFFERED 1
ENV DJANGO_SETTINGS_MODULE=myapp.settings

# Create and set the working directory
WORKDIR /app

# Copy the requirements file into the container
COPY requirements.txt /app/

# Install the project dependencies
RUN pip install -r requirements.txt

# Copy the application code into the container
COPY . /app/

# Expose the port where the Django app will run (change as needed)
EXPOSE 8000

# Start the Django application
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
