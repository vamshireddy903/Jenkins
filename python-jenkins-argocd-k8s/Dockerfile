FROM python:3.11-slim

# Set working directory
WORKDIR /app

# Install Django
RUN pip install --no-cache-dir django==3.2

# Copy project files
COPY . .

# Expose Django development server port
EXPOSE 8000

# Run migrations and start server when container runs (not at build time)
CMD ["sh", "-c", "python manage.py migrate && python manage.py runserver 0.0.0.0:8000"]
