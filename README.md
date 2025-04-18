# SpecBot

A comprehensive web application for algorithmic performance and complexity analysis.

## Features

- Docker-based deployment with three services:
  - Backend (Flask)
  - Frontend (React)
  - Nginx (Reverse Proxy)
- Algorithm complexity analysis
- Performance visualization
- Dockerized environment for easy setup and deployment
- CI/CD with GitHub Actions
## 🎥 Demo

Watch the video here: [Project Demo]([https://drive.google.com/file/d/YOUR_FILE_ID/view](https://drive.google.com/file/d/1DzUZqjXLK2gpKwB9-nKcmjAap-hBzc51/view?usp=sharing))

## Getting Started

### Prerequisites

- Docker and Docker Compose
- Git
- PowerShell (for Windows users)

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/YOUR_USERNAME/SpecBot.git
   cd SpecBot
   ```

2. Reconstruct the Inputs folder (required for testing with sample data):

   On Windows:

   ```powershell
   .\setup_inputs.ps1
   ```

   On Linux/Mac:

   ```bash
   # Use the instructions in Backend/inputs_parts/README.md
   ```

3. Start the application:

   ```bash
   docker-compose up -d
   ```

4. Access the application at http://localhost:80

5. To stop the application

```bash
docker-compose down
```

## Architecture

- **Backend**: Flask API for algorithm analysis and performance metrics
- **Frontend**: React application for user interface
- **Nginx**: Serves as a reverse proxy for both frontend and backend

## About the Inputs Folder

The original Inputs folder contains large test files that exceed GitHub's file size limits. We've split these files into smaller parts located in `Backend/inputs_parts/`. To reconstruct the original Inputs folder:

1. Run the provided setup script: `.\setup_inputs.ps1` (Windows)
2. For non-Windows users, follow the instructions in `Backend/inputs_parts/README.md`

## CI/CD Workflows

This project includes several GitHub Actions workflows:

1. **Build Workflow**: Triggered on push to main/master branches. Builds both frontend and backend applications.
2. **Test Workflow**: Runs tests for frontend and backend components.
3. **Deploy Workflow**: Builds and pushes Docker images to Docker Hub when code is pushed to the production branch.

## License

[MIT](LICENSE)
