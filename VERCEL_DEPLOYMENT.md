# Vercel Deployment Configuration

## Environment Variables Required

When deploying to Vercel, make sure to set these environment variables in your Vercel dashboard:

### Required Variables:
1. **MONGODB_URI** - Your MongoDB connection string
2. **JWT_SECRET** - Your JWT secret for authentication
3. **NEXT_PUBLIC_BASE_URL** - Your production domain (e.g., https://your-app.vercel.app)

### Optional Variables (if using Cloudinary):
4. **CLOUDINARY_CLOUD_NAME** - Your Cloudinary cloud name
5. **CLOUDINARY_API_KEY** - Your Cloudinary API key
6. **CLOUDINARY_API_SECRET** - Your Cloudinary API secret

## How to set environment variables in Vercel:

1. Go to your Vercel dashboard
2. Select your project
3. Go to Settings > Environment Variables
4. Add each variable with the appropriate values

## Important Notes:

- The blog routing now uses direct database queries instead of HTTP requests for better reliability
- Make sure your MongoDB connection string is correct and accessible from Vercel
- The routing will work with both slug and ID parameters for backward compatibility

## Troubleshooting:

If blog posts still don't load:
1. Check the Vercel function logs for any errors
2. Verify your MongoDB connection string is correct
3. Ensure all required environment variables are set
4. Check that your blog documents have valid slugs in the database
