# API Design Forum App
## Requirement/User Stories:
```
As a user, I want to be able to Register
As a user, I want to be able to Log In
As a user, I want to be able to Create new Thread
As a user, I want to be able to Create new Reply (on a Thread)
As a user I want to be able to Update my Personal profile
As a user, I want to be able to Save/Bookmark Threads
As a user, I want to be able to UnSave/UnBM Threads
```
## Core Entities
```
User: (id, username, password, email, avatar, name)
Thread: (id, title, content, created_at, user_id)
Reply: (id, thread_id, content, created_at, user_id)
Bookmark: (id, user_id, thread_id)
```

### Register
- POST /api/register
Request body: { name: string, username: string, email: string, password: string }
Response: { status: number, message: string }
