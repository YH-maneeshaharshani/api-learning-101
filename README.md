# API Learning 101 🚀

Welcome to API Learning 101! This repository is your comprehensive guide to understanding and working with APIs, complete with a fully functional REST API backend and hands-on learning resources.

![API Learning 101 Banner](images/banner.png)

## 🌐 Live Demo

**Backend API**: [api-learning.nisalgunawardhana.com](https://api-learning.nisalgunawardhana.com)

## 📚 What You'll Learn

This repository provides:

- **Complete API fundamentals** - HTTP methods, status codes, headers, REST principles
- **Working backend API** - Real API you can interact with
- **Postman collection** - Ready-to-use API tests
- **Hands-on examples** - Practical demonstrations
- **Best practices** - Industry-standard approaches

## 📂 Repository Structure

```
api-learning-101/
├── docs/
│   ├── 01-what-is-api.md
│   ├── 02-http-methods.md
│   ├── 03-status-codes.md
│   ├── 04-rest-principles.md
│   ├── 05-postman-guide.md
│   └── screenshots/
├── backend/
│   ├── api/
│   │   └── index.js
│   ├── data/
│   │   └── users.json
│   ├── package.json
│   └── README.md
├── postman/
│   └── API-Learning-101.postman_collection.json
├── .github/
│   ├── ISSUE_TEMPLATE/
│   └── workflows/
└── vercel.json
```

## 🚀 Quick Start

### 1. Access the Public Postman Collection

**🌟 Postman Workspace**: [API Learning 101 Collection](https://www.postman.com/cloudy-water-123799/workspace/api-learning)

1. Open the public Postman workspace link above
2. Fork the collection to your workspace
3. Start testing with the live API at `https://api-learning.nisalgunawardhana.com`

### 2. (Optional) Local Testing

If you want to test locally:

```bash
# Clone the repository
git clone https://github.com/nisalgunawardhana/api-learning-101.git
cd api-learning-101

# Install dependencies
cd backend
npm install

# Run locally
npm start
```

The API will be available at `http://localhost:3000`

## 🎯 API Endpoints

**Base URL**: `https://api-learning.nisalgunawardhana.com`

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/users` | Get all users |
| GET | `/api/users/:id` | Get user by ID |
| POST | `/api/users` | Create new user |
| PUT | `/api/users/:id` | Update user |
| DELETE | `/api/users/:id` | Delete user |
| GET | `/api/reset` | Reset data to initial state |

**💡 Note about Data Persistence:**
- The API uses **in-memory storage** (no database required!)
- Data persists during the serverless function's lifetime
- Changes are temporary and reset periodically on Vercel
- Use `GET /api/reset` to manually reload initial data
- Perfect for learning and testing without worrying about data cleanup!

## 📖 Learning Path

Follow these guides in order:

1. [What is an API?](docs/01-what-is-api.md)
2. [HTTP Methods](docs/02-http-methods.md)
3. [Status Codes](docs/03-status-codes.md)
4. [REST Principles](docs/04-rest-principles.md)
5. [Postman Guide](docs/05-postman-guide.md)

## 🧪 Complete Testing Guide

### Step 1: Access Postman Collection

1. Visit the public workspace: [API Learning 101 Collection](https://www.postman.com/cloudy-water-123799/workspace/api-learning)
2. Click **Fork Collection** to add it to your workspace
3. All requests are pre-configured with the production URL

### Step 2: Test Each Request Type

You must test all request types and capture screenshots for submission:

#### 🔍 **GET Request - Fetch All Users**

1. Select `GET All Users` from the collection
2. Click **Send**
3. Verify status code: `200 OK`
4. **Take a screenshot** showing:
   - Request URL
   - Response status
   - Response body with user data

#### 🔍 **GET Request - Fetch Single User**

1. Select `GET User by ID` from the collection
2. Replace `:id` with `1` in the URL
3. Click **Send**
4. Verify status code: `200 OK`
5. **Take a screenshot**

#### ➕ **POST Request - Create User**

1. Select `POST Create User` from the collection
2. Go to **Body** tab (raw JSON)
3. Use this sample data:
   ```json
   {
     "name": "Your Name",
     "email": "yourname@example.com",
     "age": 25
   }
   ```
4. Click **Send**
5. Verify status code: `201 Created`
6. **Take a screenshot** showing the created user with generated ID

#### ✏️ **PUT Request - Update User**

1. Select `PUT Update User` from the collection
2. Use the ID from your created user
3. Update the data in Body:
   ```json
   {
     "name": "Updated Name",
     "email": "updated@example.com",
     "age": 26
   }
   ```
4. Click **Send**
5. Verify status code: `200 OK`
6. **Take a screenshot** showing the updated user

#### 🗑️ **DELETE Request - Remove User**

1. Select `DELETE User` from the collection
2. Use the ID of the user you created
3. Click **Send**
4. Verify status code: `200 OK`
5. **Take a screenshot** showing successful deletion message

### Step 3: Organize Your Screenshots

Create a folder named `screenshots-[your-github-username]` with all 5 screenshots:
```
screenshots-yourusername/
├── 01-get-all-users.png
├── 02-get-single-user.png
├── 03-post-create-user.png
├── 04-put-update-user.png
└── 05-delete-user.png
```

### Step 4: Submit Your Work

1. Add your screenshots to the `docs/screenshots/` folder
2. Create a Pull Request with your screenshots
3. Go to **Issues** → **New Issue**
4. Select **📝 Submission** template
5. Fill in:
   - Your name
   - Email address (for badges and prize notifications)
   - GitHub username
   - PR number
   - T-shirt size (for winners only)
6. Submit the issue

**Note**: Your submission will be automatically assigned to @nisalgunawardhana for review. Once approved, you'll receive completion badges!

### 🎁 Social Media Bonus!

Increase your chances to win **Postman swags**:
1. Share your completion on Twitter/LinkedIn/Facebook
2. Tag **@NisalGunawardhana** and **@Postman**
3. Use hashtag **#APILearning101**
4. Winners will be selected randomly from all approved submissions!

## 🏆 Rewards & Badges

After successful submission and review:

**Everyone receives:**
- ✅ **Submission Approved Badge**
- 🎓 **API Learning 101 Completion Badge**

**Random winners receive:**
- 👕 **Exclusive T-Shirt** (winners selected randomly)
- 🎁 **Chance for Postman Swags** (share on social media for more chances!)

We've included a comprehensive Postman collection with pre-configured requests:

- ✅ All CRUD operations
- ✅ Pre-request scripts
- ✅ Tests for validation
- ✅ Environment variables

See the [Postman Guide](docs/05-postman-guide.md) for detailed instructions.

## 💻 Backend Technology

- **Runtime**: Node.js
- **Framework**: Express.js
- **Storage**: JSON file (no database needed!)
- **Hosting**: Vercel

## 🤝 Contributing

We welcome contributions! Please submit your work:

1. Fork the repository
2. Create your feature branch
3. Make your changes
4. Submit a pull request
5. Create a submission issue

Your submission will be reviewed and you'll receive contributor badges!

## 📝 Submission Process

1. Complete your work and create a PR
2. Use the **Submission** issue template
3. Fill in all required details
4. Your submission will be automatically tagged and assigned for review
5. Receive your contributor badge upon approval! 🏆

## 🏆 Badges
## 🎊 Congratulations @YH-maneeshaharshani!

Your **API Learning 101** task submission has been **approved** by @nisalgunawardhana!

### 🏆 Achievement Unlocked!

You have successfully completed the API Learning 101 challenge and earned your badges:

- ✅ **Submission Approved Badge**
- 🎓 **API Learning 101 Completion Badge**

![Completion Badge](https://raw.githubusercontent.com/nisalgunawardhana/api-learning-101/main/images/badges/badge.png)



**Thank you for completing API Learning 101!** Keep building amazing things! 🚀

Contributors receive badges based on their submissions:
- 🟡 Pending Review
- ✅ Approved
- 🎉 Closed/Completed

## 📄 License

MIT License - feel free to use this for learning!

## 👨‍💻 Maintainer

**Nisal Gunawardhana** ([@nisalgunawardhana](https://github.com/nisalgunawardhana))

---

Happy Learning! 🎉
