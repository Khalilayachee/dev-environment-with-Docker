FROM python:3.11-slim

# Set work directory
WORKDIR /code

# Copy requirements and install dependencies
COPY ../requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the app code
COPY ./src ./src



# Command to run the app with Uvicorn
CMD ["uvicorn", "src.main:app", "--host", "0.0.0.0", "--port", "80", "--reload"]
