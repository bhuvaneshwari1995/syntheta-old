# Python base image
FROM python:3.9

# working directory
WORKDIR /app

COPY requirements.txt .

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Install MkDocs
RUN pip install --no-cache-dir mkdocs

# MkDocs project files to the container
COPY . .

# Expose port
EXPOSE 8486

# Run MkDocs server
CMD ["mkdocs", "serve", "--dev-addr=0.0.0.0:8486"]
