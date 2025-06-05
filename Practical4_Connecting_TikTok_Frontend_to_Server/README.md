## NOTE: The actual practical work implementation is done in practical1-tiktok folder. This folder is just for README.md and Reflection.md.

# Practical 4: Connecting TikTok Frontend to Server

## Overview
This practical demonstrates how to connect a Next.js frontend to an Express.js backend, implementing user authentication, video display, and social interactions for a TikTok-like application.

## Prerequisites
- Node.js installed
- Next.js frontend project
- Express.js backend server
- Basic understanding of React, API integration, and JWT authentication

## Installation

### Required Packages
Install the necessary dependencies:

```bash
npm install axios jwt-decode react-hot-toast
```

## Implementation Steps

### Step 1: API Client Configuration

Create a centralized API client for backend communication.

**File: src/lib/api-config.js**
- Sets up Axios instance with base URL
- Configures request interceptors for authentication tokens
- Handles API error responses globally

**File: .env.local**
```
NEXT_PUBLIC_API_URL=http://localhost:8000/api
```

### Step 2: Authentication Context

Implement authentication state management across the application.

**File: src/contexts/authContext.jsx**
- Creates React context for user authentication state
- Manages login/logout functionality
- Provides JWT token handling

**Update: src/app/layout.js**
- Wraps application with AuthProvider
- Makes authentication state available globally

### Step 3: Authentication UI Components

Build reusable authentication interface components.

**File: src/components/ui/Modal.jsx**
- Reusable modal component for popup displays
- Handles overlay and content positioning

**File: src/components/auth/AuthForms.jsx**
- Login and signup form components
- Form validation and error handling
- API integration for authentication

**File: src/components/auth/AuthModal.jsx**
- Combines modal and forms
- Complete authentication user interface

### Step 4: Main Layout Updates

**File: src/components/layout/MainLayout.jsx**
- Conditional rendering based on authentication status
- Login/logout button integration
- Protected navigation items

### Step 5: Video Service

**File: src/services/videoService.js**
- Abstracts video-related API calls
- Functions for fetching, liking, and commenting on videos
- Centralized video data management

### Step 6: User Service

**File: src/services/userService.js**
- Handles user-related API operations
- Profile management and following functionality
- User discovery and search features

### Step 7: VideoCard Component Updates

**File: src/components/ui/VideoCard.jsx**
- Displays individual videos with user information
- Real-time interaction handling (likes, comments)
- Video playback controls integration

### Step 8: VideoFeed Component Updates

**File: src/components/ui/VideoFeed.jsx**
- Fetches and displays video feeds from backend
- Supports both "For You" and "Following" feeds
- Loading states and error handling

### Step 9: Following Page

**File: src/app/following/page.jsx**
- Personalized feed showing videos from followed users
- Empty state handling for users with no follows
- Social connection-based content filtering

### Step 10: User Discovery Page

**File: src/app/explore-users/page.jsx**
- User discovery and exploration interface
- Follow/unfollow functionality
- User search and browsing capabilities

### Step 11: Dynamic Profile Page

**File: src/app/profile/[userId]/page.jsx**
- Dynamic user profile pages
- User-specific video displays
- Profile information and statistics

### Step 12: Video Upload

**File: src/app/upload/page.jsx**
- Video upload form interface
- File handling and validation
- Caption and thumbnail management

## Key Features Implemented

### Authentication System
- JWT-based authentication
- Secure token storage
- Login/logout functionality
- Protected routes

### Video Management
- Video feed display
- Like/unlike functionality
- Comment system
- Video upload capabilities

### Social Features
- User following/unfollowing
- Personalized feeds
- User discovery
- Profile viewing

### API Integration
- Centralized API client
- Error handling
- Loading states
- Request interceptors

## Testing Instructions

### 1. User Registration and Authentication
- Create multiple user accounts (2-3 recommended)
- Test login/logout functionality
- Verify token persistence and authentication state

### 2. Video Operations
- Upload videos with different accounts
- Add captions and thumbnails
- Test video playback and controls

### 3. Social Interactions
- Follow/unfollow users between accounts
- Verify following feed shows correct content
- Test user discovery and profile viewing

### 4. Video Interactions
- Like and unlike videos
- Test comment functionality
- Verify real-time updates

### 5. Navigation and UI
- Test protected route access
- Verify authentication-based UI changes
- Check responsive design and user experience

## Project Structure

```
src/
├── app/
│   ├── explore-users/
│   ├── following/
│   ├── profile/[userId]/
│   ├── upload/
│   └── layout.js
├── components/
│   ├── auth/
│   ├── layout/
│   └── ui/
├── contexts/
├── lib/
└── services/
```

## Environment Variables

```
NEXT_PUBLIC_API_URL=http://localhost:8000/api
```

## Resources

- [Next.js Documentation](https://nextjs.org/docs)
- [React Hook Form](https://react-hook-form.com/)
- [Axios Request Library](https://axios-http.com/)
- [JWT Authentication](https://jwt.io/)
- [Express.js Documentation](https://expressjs.com/)
- [Prisma ORM Documentation](https://www.prisma.io/docs)

## Troubleshooting

### Common Issues
1. **CORS Errors**: Ensure backend CORS is configured for frontend URL
2. **Authentication Failures**: Check JWT token format and expiration
3. **API Connection Issues**: Verify backend server is running and API URL is correct
4. **File Upload Problems**: Check file size limits and supported formats

### Debug Tips
- Use browser developer tools to inspect network requests
- Check console for JavaScript errors
- Verify environment variables are loaded correctly
- Test API endpoints directly using tools like Postman




