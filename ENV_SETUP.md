# Environment Variable Configuration

This project has been updated to use environment variables for important configuration settings to improve security and flexibility.

## Backend Configuration

The backend now uses a `.env` file with the following variables:

```plaintext
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
PORT=5000
NODE_ENV=development
API_URL=http://localhost:5000
```

## Frontend Configuration

The frontend now uses a `.env` file with the following variables:

```plaintext
REACT_APP_API_URL=http://localhost:5000
```

## Security Benefits

1. **Credential Security**: Sensitive credentials are no longer hardcoded in the source code
2. **Environment Separation**: Easy to configure different settings for development, testing, and production
3. **Simplified Deployment**: Makes it easier to deploy to different environments

## How to Use

1. Make sure the `.env` files are properly configured in both backend and frontend directories
2. Never commit the `.env` files to version control (they are now included in `.gitignore`)
3. For production deployment, set up environment variables on your hosting platform

## Files Updated

1. Backend:

   - `app.js` (added dotenv configuration)
   - `config/keys.js` (now uses environment variables)
   - `config/jwtConfig.js` (now uses environment variables)
   - `auth/auth.js` (now uses environment variables)
   - `routes/login.js` (now uses environment variables)

2. Frontend:
   - `components/API/api.js` (now uses environment variables)
   - `.env` file created with API URL configuration
