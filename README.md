# Flask CI/CD Project

A simple Flask web application with automated testing and deployment using GitHub Actions.

## What it does

This is a basic Flask app that shows a welcome page. Pretty straightforward - just wanted to practice setting up CI/CD pipelines.

## Running locally

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

2. Run the app:
   ```bash
   python app.py
   ```

3. Open your browser and go to `http://localhost:5000`

## Testing

Run tests with:
```bash
pytest
```

The tests check if the home page loads correctly and returns the right content.

## Docker

Build and run with Docker:
```bash
docker build -t my-flask-app .
docker run -p 5000:5000 my-flask-app
```

## CI/CD

This project uses GitHub Actions to:
- Run tests automatically when code is pushed
- Build a Docker image
- Push the image to Docker Hub

The workflow runs on every push to the main branch.

## Project Structure

```
├── app.py              # Main Flask application
├── test_app.py         # Tests
├── requirements.txt    # Python dependencies
├── Dockerfile         # Docker configuration
├── templates/
│   └── index.html     # HTML template
└── .github/workflows/
    └── main.yaml      # CI/CD pipeline
```

## Notes

This was mainly a learning project to understand how CI/CD works with Flask and Docker. Nothing too fancy, just the basics working together.
