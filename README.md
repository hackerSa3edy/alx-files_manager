# Files Manager

A comprehensive file storage and management platform built with Node.js.

## Overview

This project is a file storage and management platform that combines various backend technologies to create a robust file management system. It implements user authentication, file upload/download capabilities, image processing, and background job processing.

## Features

- User authentication and management
- File upload and storage
- File permission management (public/private)
- Image thumbnail generation
- Background job processing
- Email notifications
- API-first design
- Redis caching
- MongoDB storage

## Technology Stack

- **Runtime**: Node.js
- **Framework**: Express.js
- **Database**: MongoDB
- **Caching**: Redis
- **Job Queue**: Bull
- **Testing**: Mocha
- **Development**: Nodemon
- **Image Processing**: Sharp (for thumbnails)
- **Email**: NodeMailer

## API Endpoints

### Authentication

- `POST /users` - Create new user
- `GET /users/me` - Get current user info
- `GET /connect` - Sign in user
- `GET /disconnect` - Sign out user

### Files

- `POST /files` - Upload new file
- `GET /files/:id` - Get file by ID
- `GET /files` - List all files
- `PUT /files/:id/publish` - Make file public
- `PUT /files/:id/unpublish` - Make file private
- `GET /files/:id/data` - Get file content

## Setup and Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/yourusername/alx-files_manager.git
    cd alx-files_manager
    ```

2. Install dependencies:

    ```bash
    npm install
    ```

3. Configure environment variables:

    ```bash
    cp .env.example .env
    # Edit .env with your configuration
    ```

4. Start required services:

    ```bash
    # Start MongoDB
    mongod

    # Start Redis
    redis-server
    ```

5. Run the application:

    ```bash
    npm start
    ```

## Development

- Run in development mode: `npm run dev`
- Run tests: `npm test`
- Lint code: `npm run lint`

## Environment Variables

- `PORT`: API port (default: 5000)
- `DB_HOST`: MongoDB host
- `DB_PORT`: MongoDB port
- `DB_DATABASE`: MongoDB database name
- `REDIS_HOST`: Redis host
- `REDIS_PORT`: Redis port
- `FOLDER_PATH`: Local storage folder path

## Testing

The project includes comprehensive tests using Mocha:

```bash
npm test
```

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Acknowledgments

- ALX Software Engineering Program
- All contributors and reviewers
