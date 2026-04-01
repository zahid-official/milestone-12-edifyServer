<div align="center">

<img src="https://edify-official.vercel.app/assets/fav.svg" alt="Edify Logo" width="60" />

# Edify Server - Scholarship Management API

A robust RESTful API driving the Edify scholarship platform - orchestrating scholarship catalogs, multi-role access control, Stripe payment processing, JWT authentication, and application lifecycle management through Express.js and MongoDB.

[![Live App](https://img.shields.io/badge/▶_Live_App-edify--official.vercel.app-00806D?style=for-the-badge&logo=vercel&logoColor=white)](https://edify-official.vercel.app/)
[![GitHub Repo](https://img.shields.io/badge/GitHub-Repository-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/zahid-official/milestone-12-server)
<img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js" />
<img src="https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white" alt="Express" />
<img src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB" />
<img src="https://img.shields.io/badge/Stripe-6772E5?style=for-the-badge&logo=stripe&logoColor=white" alt="Stripe" />
<img src="https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white" alt="JWT" />
<img src="https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Vercel" />

</div>

<br/>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=gradient&customColorList=14,16,18&height=2&section=header" width="100%" />
</p>

## 🔍 Overview

**Edify Server** is the mission-critical backend powering the [Edify](https://edify-official.vercel.app/) scholarship discovery and management platform. Built with Express.js and backed by MongoDB Atlas, it delivers a comprehensive API surface that enables students to search, apply, and pay for scholarships - while moderators curate listings and admins oversee the entire ecosystem through role-based dashboards. The server handles JWT-secured authentication, Stripe payment intents, multi-collection aggregation pipelines, and granular RBAC middleware, all deployed as a serverless function on Vercel.

> _Empowering academic journeys through intelligent scholarship infrastructure._

<br/>

## ✨ Key Features

### 🎓 Scholarship Management

<table align="center">
<thead>
<tr><th align="left">Feature</th><th align="left">Description</th></tr>
</thead>
<tbody>
<tr><td><b>Full CRUD Operations</b></td><td>Create, read, update, and delete scholarships through dedicated RESTful endpoints</td></tr>
<tr><td><b>Top Scholarships</b></td><td>Aggregation pipeline combining average review ratings with lowest application fees</td></tr>
<tr><td><b>Advanced Search</b></td><td>Regex-powered search across university names, scholarship names, and degree types</td></tr>
<tr><td><b>Server-Side Pagination</b></td><td>Configurable page size and page number for efficient large-catalog browsing</td></tr>
<tr><td><b>Date-Based Sorting</b></td><td>Sort applied scholarships by application date or submission deadline</td></tr>
</tbody>
</table>

### 🔐 Authentication & Role-Based Access

<table align="center">
<thead>
<tr><th align="left">Feature</th><th align="left">Description</th></tr>
</thead>
<tbody>
<tr><td><b>JWT Authentication</b></td><td>Secure token generation with 1-hour expiration via <code>Authorization</code> header</td></tr>
<tr><td><b>Three-Tier RBAC</b></td><td>User, Moderator, and Admin roles with cascading permission middleware</td></tr>
<tr><td><b>Admin Verification</b></td><td>Custom <code>verifyAdmin</code> middleware restricts sensitive endpoints to Admin-only access</td></tr>
<tr><td><b>Moderator Verification</b></td><td>Custom <code>verifyModerator</code> middleware grants access to both Moderator and Admin roles</td></tr>
<tr><td><b>Email-Based Identity</b></td><td>JWT payload validation ensures users can only access their own scoped resources</td></tr>
</tbody>
</table>

### 💳 Payments & Application Workflow

<table align="center">
<thead>
<tr><th align="left">Feature</th><th align="left">Description</th></tr>
</thead>
<tbody>
<tr><td><b>Stripe Integration</b></td><td>Server-side payment intent creation for secure scholarship application fees</td></tr>
<tr><td><b>Application Lifecycle</b></td><td>Full status tracking - Pending, Processing, Approved, Rejected - with feedback</td></tr>
<tr><td><b>Review System</b></td><td>Users submit ratings and comments; moderators can edit or remove reviews</td></tr>
<tr><td><b>User Scoped Records</b></td><td>Fetch personal applications and reviews filtered by authenticated user email</td></tr>
<tr><td><b>Role Filtering</b></td><td>Filter and display users by role for admin management dashboards</td></tr>
</tbody>
</table>

### 🔧 Infrastructure & Deployment

<table align="center">
<thead>
<tr><th align="left">Feature</th><th align="left">Description</th></tr>
</thead>
<tbody>
<tr><td><b>MongoDB Atlas</b></td><td>Cloud-hosted cluster with Stable API v1 for production reliability</td></tr>
<tr><td><b>Serverless Deployment</b></td><td>Vercel-powered serverless functions with automatic scaling</td></tr>
<tr><td><b>Environment Security</b></td><td>All credentials managed via <code>dotenv</code> - never exposed in source</td></tr>
<tr><td><b>CORS Configuration</b></td><td>Cross-origin resource sharing enabled for client-server communication</td></tr>
</tbody>
</table>

<br/>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=gradient&customColorList=14,16,18&height=2&section=header" width="100%" />
</p>

## 🛠️ Tech Stack

<table align="center">
<thead>
<tr><th align="left">Technology</th><th align="center">Version</th><th align="left">Purpose</th></tr>
</thead>
<tbody>
<tr><td><b>Node.js</b></td><td align="center"><code>18+</code></td><td>Server-side JavaScript runtime environment</td></tr>
<tr><td><b>Express</b></td><td align="center"><code>^4.21.2</code></td><td>Minimal and flexible web application framework</td></tr>
<tr><td><b>MongoDB Driver</b></td><td align="center"><code>^6.12.0</code></td><td>Official MongoDB driver for data persistence</td></tr>
<tr><td><b>Stripe</b></td><td align="center"><code>^17.5.0</code></td><td>Payment processing for scholarship application fees</td></tr>
<tr><td><b>jsonwebtoken</b></td><td align="center"><code>^9.0.2</code></td><td>JWT token generation and verification</td></tr>
<tr><td><b>cookie-parser</b></td><td align="center"><code>^1.4.7</code></td><td>Parse and manage HTTP cookies in requests</td></tr>
<tr><td><b>dotenv</b></td><td align="center"><code>^16.4.7</code></td><td>Environment variable management from <code>.env</code> files</td></tr>
<tr><td><b>CORS</b></td><td align="center"><code>^2.8.5</code></td><td>Cross-origin request handling middleware</td></tr>
</tbody>
</table>

<br/>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=gradient&customColorList=14,16,18&height=2&section=header" width="100%" />
</p>

## 🏗️ Architecture

<div align="center">
<pre>
┌──────────────────────────────────────────────────────────────────────┐
│                      Client Application (React)                      │
│                  https://edify-official.vercel.app                    │
└────────────────────────────────┬─────────────────────────────────────┘
                                 │  HTTP Requests (REST + JWT Header)
                                 ▼
┌──────────────────────────────────────────────────────────────────────┐
│                       Express.js API Server                          │
│                                                                      │
│  ┌─────────────────┐  ┌──────────────────┐  ┌────────────────────┐  │
│  │   Middleware     │  │     Routes       │  │  Business Logic    │  │
│  │                  │  │                  │  │                    │  │
│  │  • CORS          │  │  POST /jwt       │  │  • JWT Sign/Verify │  │
│  │  • JSON Parser   │  │  POST /users     │  │  • Role Cascading  │  │
│  │  • verifyJWT     │  │  GET  /users     │  │  • Stripe Intents  │  │
│  │  • verifyAdmin   │  │  POST /stripe    │  │  • Aggregation     │  │
│  │  • verifyMod     │  │  GET  /search    │  │  • Pagination      │  │
│  │                  │  │  PATCH /status   │  │  • Email Scoping   │  │
│  └─────────────────┘  └────────┬─────────┘  └────────────────────┘  │
│                                │                                     │
├────────────────────────────────┼─────────────────────────────────────┤
│                                ▼                                     │
│  ┌──────────────────────────────────────────────────────────────┐    │
│  │                  MongoDB Atlas (Cluster1)                    │    │
│  │                     Database: scholarshipDB                  │    │
│  │                                                              │    │
│  │  ┌────────────────┐ ┌───────────────────┐ ┌──────────────┐  │    │
│  │  │    users       │ │   scholarships    │ │   reviews    │  │    │
│  │  │   Collection   │ │    Collection     │ │  Collection  │  │    │
│  │  └────────────────┘ └───────────────────┘ └──────────────┘  │    │
│  │                  ┌───────────────────────┐                   │    │
│  │                  │  appliedScholarships  │                   │    │
│  │                  │      Collection       │                   │    │
│  │                  └───────────────────────┘                   │    │
│  └──────────────────────────────────────────────────────────────┘    │
│                                                                      │
│  ┌──────────────────────────────────────────────────────────────┐    │
│  │                     Stripe API                               │    │
│  │              Payment Intent Processing                       │    │
│  └──────────────────────────────────────────────────────────────┘    │
└──────────────────────────────────────────────────────────────────────┘
</pre>
</div>

<br/>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=gradient&customColorList=14,16,18&height=2&section=header" width="100%" />
</p>

## 📡 API Endpoints

### 🔑 Authentication

<table align="center">
<thead>
<tr><th align="left">Method</th><th align="left">Endpoint</th><th align="left">Auth</th><th align="left">Description</th></tr>
</thead>
<tbody>
<tr><td><code>POST</code></td><td><code>/jwt</code></td><td>—</td><td>Generate a JWT token from user credentials</td></tr>
</tbody>
</table>

### 👥 Users

<table align="center">
<thead>
<tr><th align="left">Method</th><th align="left">Endpoint</th><th align="left">Auth</th><th align="left">Description</th></tr>
</thead>
<tbody>
<tr><td><code>POST</code></td><td><code>/users</code></td><td>—</td><td>Register a new user with default "User" role</td></tr>
<tr><td><code>GET</code></td><td><code>/users</code></td><td>🔒 Admin</td><td>Fetch all registered users</td></tr>
<tr><td><code>GET</code></td><td><code>/users/role/:email</code></td><td>🔒 JWT</td><td>Get role flags (admin, moderator, user) for an email</td></tr>
<tr><td><code>GET</code></td><td><code>/usersId/:email</code></td><td>—</td><td>Fetch user profile by email</td></tr>
<tr><td><code>GET</code></td><td><code>/filter/:role</code></td><td>—</td><td>Filter users by role name</td></tr>
<tr><td><code>PATCH</code></td><td><code>/users/role/:id</code></td><td>🔒 Admin</td><td>Update a user's role assignment</td></tr>
<tr><td><code>DELETE</code></td><td><code>/users/:id</code></td><td>🔒 Admin</td><td>Delete a user account</td></tr>
</tbody>
</table>

### 🎓 Scholarships

<table align="center">
<thead>
<tr><th align="left">Method</th><th align="left">Endpoint</th><th align="left">Auth</th><th align="left">Description</th></tr>
</thead>
<tbody>
<tr><td><code>GET</code></td><td><code>/</code></td><td>—</td><td>Health check - returns server connection status</td></tr>
<tr><td><code>GET</code></td><td><code>/allScholarships</code></td><td>—</td><td>Fetch all scholarships in the catalog</td></tr>
<tr><td><code>GET</code></td><td><code>/topScholarship</code></td><td>—</td><td>Top 6 scholarships by lowest fees + average ratings</td></tr>
<tr><td><code>GET</code></td><td><code>/scholarshipDetails/:id</code></td><td>—</td><td>Fetch a single scholarship by ObjectId</td></tr>
<tr><td><code>GET</code></td><td><code>/search?searchQuery=...</code></td><td>—</td><td>Search by university name, scholarship name, or degree</td></tr>
<tr><td><code>GET</code></td><td><code>/allScholarshipPagination</code></td><td>—</td><td>Paginated scholarship list with <code>pageNo</code> and <code>pageItems</code></td></tr>
<tr><td><code>GET</code></td><td><code>/total</code></td><td>—</td><td>Get total scholarship count for pagination</td></tr>
<tr><td><code>POST</code></td><td><code>/addScholarship</code></td><td>🔒 Moderator</td><td>Add a new scholarship to the catalog</td></tr>
<tr><td><code>PATCH</code></td><td><code>/editScholarship/:id</code></td><td>—</td><td>Update scholarship details (name, university, fees, etc.)</td></tr>
<tr><td><code>DELETE</code></td><td><code>/deleteScholarship/:id</code></td><td>—</td><td>Remove a scholarship from the catalog</td></tr>
</tbody>
</table>

### 📋 Applications

<table align="center">
<thead>
<tr><th align="left">Method</th><th align="left">Endpoint</th><th align="left">Auth</th><th align="left">Description</th></tr>
</thead>
<tbody>
<tr><td><code>GET</code></td><td><code>/appliedScholarships</code></td><td>—</td><td>Fetch all submitted applications</td></tr>
<tr><td><code>GET</code></td><td><code>/myScholarships/:email</code></td><td>—</td><td>Fetch applications for a specific user</td></tr>
<tr><td><code>GET</code></td><td><code>/filterDate/:date</code></td><td>—</td><td>Sort applications by <code>currentDate</code> or <code>deadline</code></td></tr>
<tr><td><code>POST</code></td><td><code>/appliedScholarship</code></td><td>—</td><td>Submit a new scholarship application</td></tr>
<tr><td><code>PATCH</code></td><td><code>/editApplication/:id</code></td><td>—</td><td>Edit application details (results, degree, location)</td></tr>
<tr><td><code>PATCH</code></td><td><code>/appliedScholarship/status/:id</code></td><td>—</td><td>Update application status (Pending → Approved/Rejected)</td></tr>
<tr><td><code>PATCH</code></td><td><code>/feedback/:id</code></td><td>—</td><td>Add moderator feedback to an application</td></tr>
<tr><td><code>PATCH</code></td><td><code>/deleteAppliedScholarship/:id</code></td><td>—</td><td>Soft-reject an application (sets status to "Rejected")</td></tr>
<tr><td><code>DELETE</code></td><td><code>/deleteMyApplication/:id</code></td><td>—</td><td>Delete a user's own application record</td></tr>
</tbody>
</table>

### ⭐ Reviews

<table align="center">
<thead>
<tr><th align="left">Method</th><th align="left">Endpoint</th><th align="left">Auth</th><th align="left">Description</th></tr>
</thead>
<tbody>
<tr><td><code>GET</code></td><td><code>/allReviews</code></td><td>—</td><td>Fetch all reviews across the platform</td></tr>
<tr><td><code>GET</code></td><td><code>/myReviews/:email</code></td><td>—</td><td>Fetch reviews submitted by a specific user</td></tr>
<tr><td><code>GET</code></td><td><code>/stroies/:id</code></td><td>—</td><td>Fetch reviews for a specific scholarship</td></tr>
<tr><td><code>POST</code></td><td><code>/addReview</code></td><td>—</td><td>Submit a new review with rating and comment</td></tr>
<tr><td><code>PATCH</code></td><td><code>/editReview/:id</code></td><td>—</td><td>Update a review's rating, comment, and date</td></tr>
<tr><td><code>DELETE</code></td><td><code>/deleteMyReview/:id</code></td><td>—</td><td>Delete a review by its ObjectId</td></tr>
</tbody>
</table>

### 💳 Payments

<table align="center">
<thead>
<tr><th align="left">Method</th><th align="left">Endpoint</th><th align="left">Auth</th><th align="left">Description</th></tr>
</thead>
<tbody>
<tr><td><code>POST</code></td><td><code>/stripe</code></td><td>—</td><td>Create a Stripe payment intent for application fees</td></tr>
</tbody>
</table>

<br/>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=gradient&customColorList=14,16,18&height=2&section=header" width="100%" />
</p>

## 🗃️ Database Schema

### 📋 usersCollection

<table align="center">
<thead>
<tr><th align="left">Field</th><th align="left">Type</th><th align="left">Description</th></tr>
</thead>
<tbody>
<tr><td><code>_id</code></td><td>ObjectId</td><td>Auto-generated unique identifier</td></tr>
<tr><td><code>email</code></td><td>String</td><td>User email address (unique)</td></tr>
<tr><td><code>role</code></td><td>String</td><td>Access level - <code>User</code>, <code>Moderator</code>, or <code>Admin</code></td></tr>
</tbody>
</table>

### 📋 scholarshipCollection

<table align="center">
<thead>
<tr><th align="left">Field</th><th align="left">Type</th><th align="left">Description</th></tr>
</thead>
<tbody>
<tr><td><code>_id</code></td><td>ObjectId</td><td>Auto-generated unique identifier</td></tr>
<tr><td><code>scholarshipName</code></td><td>String</td><td>Name of the scholarship program</td></tr>
<tr><td><code>universityName</code></td><td>String</td><td>Offering university name</td></tr>
<tr><td><code>universityCountry</code></td><td>String</td><td>Country of the university</td></tr>
<tr><td><code>universityCity</code></td><td>String</td><td>City where the university is located</td></tr>
<tr><td><code>universityRank</code></td><td>Number</td><td>Global ranking of the university</td></tr>
<tr><td><code>scholarshipCategory</code></td><td>String</td><td>Category of the scholarship</td></tr>
<tr><td><code>subjectCategory</code></td><td>String</td><td>Academic subject area</td></tr>
<tr><td><code>degree</code></td><td>String</td><td>Applicable degree level (Bachelor, Master, etc.)</td></tr>
<tr><td><code>deadline</code></td><td>String</td><td>Application deadline date</td></tr>
<tr><td><code>stipend</code></td><td>Number</td><td>Stipend amount offered</td></tr>
<tr><td><code>tuitionFee</code></td><td>Number</td><td>Tuition fee amount</td></tr>
<tr><td><code>serviceCharge</code></td><td>Number</td><td>Platform service charge</td></tr>
<tr><td><code>applicationFees</code></td><td>Number</td><td>Application processing fee</td></tr>
</tbody>
</table>

### 📋 appliedScholarshipCollection

<table align="center">
<thead>
<tr><th align="left">Field</th><th align="left">Type</th><th align="left">Description</th></tr>
</thead>
<tbody>
<tr><td><code>_id</code></td><td>ObjectId</td><td>Auto-generated unique identifier</td></tr>
<tr><td><code>email</code></td><td>String</td><td>Applicant's email address</td></tr>
<tr><td><code>gender</code></td><td>String</td><td>Applicant's gender</td></tr>
<tr><td><code>sscResult</code></td><td>String</td><td>Secondary school certificate result</td></tr>
<tr><td><code>hscResult</code></td><td>String</td><td>Higher secondary certificate result</td></tr>
<tr><td><code>applyingDegree</code></td><td>String</td><td>Degree the applicant is applying for</td></tr>
<tr><td><code>applicantCountry</code></td><td>String</td><td>Applicant's country of residence</td></tr>
<tr><td><code>applicantDistrict</code></td><td>String</td><td>Applicant's district</td></tr>
<tr><td><code>status</code></td><td>String</td><td>Application status - Pending, Processing, Approved, Rejected</td></tr>
<tr><td><code>feedback</code></td><td>String</td><td>Moderator/admin feedback on the application</td></tr>
<tr><td><code>currentDate</code></td><td>String</td><td>Date of application submission</td></tr>
<tr><td><code>deadline</code></td><td>String</td><td>Scholarship deadline at time of application</td></tr>
</tbody>
</table>

### 📋 reviewCollection

<table align="center">
<thead>
<tr><th align="left">Field</th><th align="left">Type</th><th align="left">Description</th></tr>
</thead>
<tbody>
<tr><td><code>_id</code></td><td>ObjectId</td><td>Auto-generated unique identifier</td></tr>
<tr><td><code>scholarshipId</code></td><td>String</td><td>Reference to the scholarship being reviewed</td></tr>
<tr><td><code>email</code></td><td>String</td><td>Reviewer's email address</td></tr>
<tr><td><code>rating</code></td><td>Number</td><td>Numerical rating score</td></tr>
<tr><td><code>comment</code></td><td>String</td><td>Written review comment</td></tr>
<tr><td><code>reviewDate</code></td><td>String</td><td>Date the review was submitted</td></tr>
</tbody>
</table>

<br/>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=gradient&customColorList=14,16,18&height=2&section=header" width="100%" />
</p>

## 📂 Project Structure

```
milestone-12-server/
├── index.js              # Express server entry point - routes, middleware, DB logic
├── package.json          # Dependencies and npm scripts
├── vercel.json           # Vercel serverless deployment configuration
├── .gitignore            # Ignored files (node_modules, .env, .vercel)
└── .env                  # Environment variables (not committed)
```

<br/>

## 🚀 Getting Started

### Prerequisites

<table align="center">
<thead>
<tr><th align="left">Requirement</th><th align="left">Details</th></tr>
</thead>
<tbody>
<tr><td><b>Node.js</b></td><td>v18 or higher recommended</td></tr>
<tr><td><b>npm</b></td><td>Comes bundled with Node.js</td></tr>
<tr><td><b>MongoDB Atlas</b></td><td>A cloud MongoDB cluster with connection credentials</td></tr>
<tr><td><b>Stripe Account</b></td><td>API keys for payment processing</td></tr>
<tr><td><b>Vercel CLI</b></td><td>Optional - for deployment to Vercel</td></tr>
</tbody>
</table>

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/zahid-official/milestone-12-server.git

# 2. Navigate to the project directory
cd milestone-12-server

# 3. Install dependencies
npm install

# 4. Set up environment variables (see section below)

# 5. Start the server
npm start
```

The server will be available at `http://localhost:5000` by default.

<br/>

## 🔑 Environment Variables

Create a `.env` file in the project root with the following credentials:

```env
DB_USER=your_mongodb_username
DB_PASS=your_mongodb_password
ACCESS_TOKEN=your_jwt_secret_key
STRIPE_KEY=your_stripe_secret_key
```

> **Note:** The `.env` file is included in `.gitignore` and will never be committed to version control. `DB_USER` and `DB_PASS` construct the MongoDB Atlas connection string, `ACCESS_TOKEN` is used for signing and verifying JWT tokens, and `STRIPE_KEY` authenticates server-side Stripe API calls.

<br/>

## 📜 Available Scripts

<table align="center">
<thead>
<tr><th align="left">Command</th><th align="left">Description</th></tr>
</thead>
<tbody>
<tr><td><code>npm start</code></td><td>Start the Express server with <code>node index.js</code></td></tr>
<tr><td><code>npm test</code></td><td>Run the test suite (placeholder)</td></tr>
</tbody>
</table>

<br/>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=gradient&customColorList=14,16,18&height=2&section=header" width="100%" />
</p>

## ⚙️ How It Works

<div align="center">
<pre>
┌──────────────┐        ┌─────────────────┐        ┌──────────────────┐
│    Client     │───────▶│   Express.js    │───────▶│  MongoDB Atlas   │
│    (React)    │  HTTP  │     Server      │  Query │  (scholarshipDB) │
└──────────────┘        └───────┬─────────┘        └────────┬─────────┘
                                │                           │
                  ┌─────────────┼─────────────┐    ┌────────┼────────┐
                  ▼             ▼             ▼    ▼        ▼        ▼
           ┌────────────┐ ┌──────────┐ ┌──────────┐ ┌────────┐ ┌──────┐
           │ Middleware  │ │  Router  │ │  Stripe  │ │  CRUD  │ │Aggre-│
           │            │ │          │ │   API    │ │  Ops   │ │gation│
           │ • CORS     │ │ /jwt     │ │          │ │        │ │      │
           │ • JSON     │ │ /users   │ │ Payment  │ │ Find   │ │ Avg  │
           │ • JWT      │ │ /scholar │ │ Intent   │ │ Insert │ │Rating│
           │   Verify   │ │ /applied │ │ Creation │ │ Update │ │ Sort │
           │ • Admin    │ │ /reviews │ │          │ │ Delete │ │ Skip │
           │   Verify   │ │ /stripe  │ │          │ │ Patch  │ │Limit │
           │ • Mod      │ │ /search  │ │          │ │        │ │      │
           │   Verify   │ │ /filter  │ │          │ │        │ │      │
           └────────────┘ └──────────┘ └──────────┘ └────────┘ └──────┘
                                │
                                ▼
                     JSON Response ──▶ Client Renders Data
</pre>
</div>

1. **Request Arrival** - The React client sends HTTP requests with optional JWT `Authorization` headers to the Express server.
2. **Middleware Chain** - CORS headers are applied, JSON body is parsed, and JWT tokens are verified where protection is required.
3. **Role Verification** - Protected routes pass through `verifyAdmin` or `verifyModerator` middleware to enforce permission boundaries.
4. **Route Matching** - Express matches the HTTP method and URL pattern to the appropriate handler function.
5. **Payment Processing** - For scholarship applications, Stripe payment intents are created server-side before saving application data.
6. **Database Operations** - Handlers execute MongoDB queries including aggregation pipelines, regex searches, and pagination logic.
7. **JSON Response** - Structured JSON data is returned to the client for rendering in the React interface.

<br/>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=gradient&customColorList=14,16,18&height=2&section=header" width="100%" />
</p>

## 🚢 Deployment

This server is deployed on **Vercel** as a serverless function. The `vercel.json` configuration routes all incoming requests to `index.js`:

```json
{
  "version": 2,
  "builds": [{ "src": "/index.js", "use": "@vercel/node" }],
  "routes": [
    {
      "src": "/(.*)",
      "dest": "/index.js",
      "methods": ["GET", "POST", "PUT", "PATCH", "DELETE", "OPTIONS"]
    }
  ]
}
```

> **Tip:** Set your `DB_USER`, `DB_PASS`, `ACCESS_TOKEN`, and `STRIPE_KEY` environment variables in the Vercel dashboard under **Settings → Environment Variables** before deploying.

<br/>

## 🔗 Related Repository

<table align="center">
<thead>
<tr><th align="left">Repository</th><th align="left">Description</th><th align="left">Link</th></tr>
</thead>
<tbody>
<tr><td><b>Edify Client</b></td><td>React frontend - browse scholarships, apply, pay, manage reviews & dashboards</td><td><a href="https://github.com/zahid-official/milestone-12-client">GitHub</a></td></tr>
<tr><td><b>Live App</b></td><td>Deployed full-stack application on Vercel</td><td><a href="https://edify-official.vercel.app/">edify-official.vercel.app</a></td></tr>
</tbody>
</table>

<br/>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=gradient&customColorList=14,16,18&height=2&section=header" width="100%" />
</p>

## 🌟 Author

<div align="center">
  <a href="https://github.com/zahid-official">
    <img src="https://github.com/zahid-official.png" width="100" height="100" style="border-radius: 50%;" alt="Zahid Official" />
  </a>

  <h3>Zahid Official</h3>
  <p><b>Full Stack Developer | Tech Enthusiast</b></p>

[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/zahid-official)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/zahid-web)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:zahid.official8@gmail.com)

  <p>Building scalable backend systems that empower modern web applications</p>
</div>

<br/>

## 🤝 Contributing

Contributions are welcome and appreciated! Here's how you can help improve **Edify Server**:

```bash
# 1. Fork the repository

# 2. Create a feature branch
git checkout -b feature/your-feature-name

# 3. Make your changes and commit
git commit -m "feat: add your feature description"

# 4. Push to your fork
git push origin feature/your-feature-name

# 5. Open a Pull Request against the main branch
```

<br/>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=gradient&customColorList=14,16,18&height=2&section=header" width="100%" />
</p>

<p align="center"><b>Edify Server</b> - <i>Empowering academic journeys through intelligent scholarship infrastructure.</i></p>
