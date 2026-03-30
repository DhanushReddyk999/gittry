# gittry

A simple Node.js web application.

## Running Locally

1. Install dependencies: `npm install`
2. Start the server: `npm start`
3. Open `http://localhost:8080` in your browser.

## Docker

Build the Docker image:
```bash
docker build -t my-node-app .
```

Run the container:
```bash
docker run -p 8080:8080 my-node-app
```

## Jenkins CI/CD

This project includes a Jenkinsfile for automated builds and deployments. Ensure Jenkins has the Docker plugin installed and configured.

The pipeline:
- Checks out the code
- Builds the Docker image
- Runs tests
- Deploys the application in a Docker container