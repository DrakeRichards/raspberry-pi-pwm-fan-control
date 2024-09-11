# Use an official Python runtime as a parent image
FROM python:3

# Set the working directory in the container
WORKDIR /usr/src/app

# Copy the current directory contents into the container at /usr/src/app
COPY . .

# Install any required packages
RUN pip install --root-user-action=ignore --no-cache-dir -r requirements.txt

# Make the Python script executable
RUN chmod +x /usr/src/app/fan_control.py

# Define environment variable
ENV PATH="/usr/local/bin:/usr/bin:/bin"

# Run the Python script when the container launches
CMD ["python", "./fan_control.py"]
