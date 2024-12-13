# Reverse Proxy Basemaps Planet Project

This README file is part of the reverse_proxy_basemaps_planet project. The project aims to set up a reverse proxy server to handle requests for basemaps from the Planet API. The reverse proxy server acts as an intermediary, forwarding client requests to the Planet API and returning the responses to the clients. This setup can help manage API rate limits, provide caching mechanisms, and enhance security by hiding the API key from the clients.

## Key Features

- Reverse proxy server configuration
- API request forwarding
- Response caching
- API key management and security

## Prerequisites

- Basic understanding of reverse proxy servers
- Access to the Planet API
- Required software and dependencies installed (e.g., Nginx, Apache, etc.)

## Setup Instructions

1. Clone the repository to your local machine.
2. Configure the reverse proxy server with the provided configuration files.
3. Set up the API key and other necessary credentials.
4. Deploy the application on Render.com using Uvicorn.

For detailed instructions, refer to the sections below.

## Detailed Instructions

### Cloning the Repository

```sh
git clone https://github.com/yourusername/reverse_proxy_basemaps_planet.git
cd reverse_proxy_basemaps_planet
```

### Configuring the Reverse Proxy Server

Follow the instructions in the `config/` directory to set up your reverse proxy server. Ensure you have the necessary software installed (e.g., Nginx, Apache).

### Setting Up API Key and Credentials
Create a `.env` file in the root directory and add your Planet API key and other credentials:

```env
PLANET_API_KEY=your_api_key_here
```

### Deploying on Render.com

1. Log in to your Render.com account.
2. Create a new Web Service and connect it to your GitHub repository.
3. In the "Build Command" field, enter the command to build your project (if applicable).
4. In the "Start Command" field, enter the command to start your reverse proxy server using Uvicorn. For example:

```sh
uvicorn reverse_proxy:app --host 0.0.0.0 --port 8000
```

5. Set up environment variables in Render.com with your API key and other credentials.
6. Deploy the service and monitor the logs to ensure everything is working correctly.

### Testing the Setup

Make a request to the basemaps endpoint to ensure everything is working correctly:

```sh
curl https://your-render-app-url/basemaps
```

## Troubleshooting

If you encounter any issues, refer to the `docs/troubleshooting.md` file for common problems and solutions.

## Contributing

Contributions are welcome! Please read the `CONTRIBUTING.md` file for guidelines on how to contribute to this project.

## License

This project is licensed under the Apache 2.0 License. See the `LICENSE` file for more details.