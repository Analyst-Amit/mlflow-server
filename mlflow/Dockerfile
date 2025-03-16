# Start with the official Python slim image
FROM python:3.9.5-slim

# Install MLflow
RUN pip install --no-cache-dir psycopg2-binary==2.9.10
RUN pip install --no-cache-dir mlflow==2.17.2
RUN pip install --no-cache-dir boto3


# Expose the port that MLflow will use
EXPOSE 5000

# Set the command to run the MLflow server
CMD ["mlflow", "server", "--host", "0.0.0.0", "--port", "5000"]

# # Set the command to run the MLflow server with the desired parameters
# CMD ["mlflow", "server", "--backend-store-uri", "postgresql://user:password@postgres:5432/mlflowdb", "--artifacts-destination", "s3://mlops-aws-windoutput-staging", "--host", "0.0.0.0", "--port", "5000"]
