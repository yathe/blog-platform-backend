# TODO List for Blog Platform Backend

## 1. Project Initialization

- [x] Initialize Node.js project with package.json
- [x] Install dependencies: express, pg (PostgreSQL), bcryptjs, jsonwebtoken, cors, dotenv, express-validator

## 2. Database Setup

- [x] Install mongoose for MongoDB
- [x] Set up MongoDB database connection
- [x] Create Mongoose schemas for users, posts, comments

## 3. Models

- [x] Create User model with roles (Writer, Reader, Admin)
- [x] Create Post model with title, content, tags, status
- [x] Create Comment model linked to posts and users

## 4. Authentication

- [x] Implement user registration with password hashing
- [x] Implement user login with JWT token generation
- [x] Create JWT middleware for protected routes
- [x] Add role-based access control

## 5. Post Routes

- [x] Create post CRUD routes (create, read, update, delete)
- [x] Implement permissions: writers edit own posts, readers view published, admins manage all
- [x] Add pagination and search functionality (by title, content, tags)

## 6. Comment Routes

- [x] Create comment routes for adding comments on published posts
- [x] Implement delete own comments functionality

## 7. Frontend

- [x] Create simple HTML page to fetch and display published blog posts
- [x] Ensure API integration works

## 8. Documentation and Deployment

- [x] Write README with setup instructions, API endpoints, and deployment guides
- [x] Prepare for deployment on Render (backend) and Vercel (frontend)

## 9. Fixes for Full Functionality

- [ ] Update server.js to serve static files from 'frontend/public'
- [ ] Modify routes/posts.js to make GET /api/posts public (no auth required for fetching published posts)
- [ ] Update postController.js getPosts and getPostById to handle unauthenticated requests (treat as Reader)
- [ ] Add authenticateToken middleware only to protected routes (create, update, delete)
- [ ] Test the application: run server, seed sample published posts, verify frontend displays posts without auth
- [ ] Add favicon.ico to frontend/public/ to fix 404 error
- [ ] Ensure all CRUD operations work with proper auth for writers/admins
