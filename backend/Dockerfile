# Use an official Python runtime based on Debian Bullseye
FROM python:3.10-bullseye

# Set the working directory in the container
WORKDIR /app

# Copy the requirements.txt into the container at /app
COPY requirements.txt /app/

RUN pip3 install NumPy==1.21.0

# Install Python dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the current directory contents into the container at /app
COPY . .

# Expose the backend port
EXPOSE 5500

# Define environment variable
ENV FLASK_APP=app.py

# Run app.py when the container launches
CMD [python3, FLASK_APP]