# 🛍️ SleekRoad — Campus Marketplace

**SleekRoad** is a campus-focused online marketplace that enables students to buy, sell, and rent products within their university community. It simplifies campus trading by providing a centralized platform for product discovery, listing management, and direct student-to-student communication.

Built with **Next.js, TypeScript, Node.js, PostgreSQL, Prisma ORM, and AWS IAM**, SleekRoad aims to make campus transactions more accessible, convenient, and efficient.

<p align="center">
  <a href="YOUR_LIVE_DEMO_URL">
    <img src="https://img.shields.io/badge/Live%20Demo-Visit%20Website-blue?style=for-the-badge" alt="Live Demo" />
  </a>
  <img src="https://img.shields.io/badge/Next.js-TypeScript-black?style=for-the-badge&logo=next.js" alt="Next.js and TypeScript" />
  <img src="https://img.shields.io/badge/Database-PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/ORM-Prisma-2D3748?style=for-the-badge" alt="Prisma ORM" />
</p>

---

## 📸 Project Preview

<!-- Save your homepage screenshot as assets/sleekroad-homepage.png -->

<p align="center">
  <img src="apps/sleek-fe/public/Screenshot 2026-10-11 210013.png" alt="SleekRoad Homepage" width="100%" />
</p>

<p align="center">
  <em>SleekRoad — Buy, sell, and rent within your campus community.</em>
</p>

---

## 🌐 Live Application

- **Frontend:** Next.js, React, TypeScript, Tailwind CSS
- **Backend:** Node.js, Express.js, TypeScript
- **Database:** PostgreSQL
- **ORM:** Prisma ORM
- **Cloud & Access Management:** AWS IAM
- **Deployment:** Configure according to your actual hosting setup

---

## ✨ Key Features

### 🛒 Buy & Sell Products
- Browse products listed by other students.
- Discover useful products available within the campus community.
- Create and manage product listings.
- Facilitate direct student-to-student transactions.
- Make second-hand products easier to discover and reuse.

### 🏠 Product Rental
- Support rental listings for frequently used campus essentials.
- Help students access products without purchasing them permanently.
- Encourage affordable and resource-efficient campus living.

### 📝 Listing Management
- Create product listings with relevant information.
- Organize products to improve browsing and discovery.
- Simplify the process of publishing and managing marketplace listings.
- Maintain structured product information using PostgreSQL and Prisma ORM.

### 💬 Student Communication
- Provide a centralized place for students to discover listings and connect with sellers.
- Support communication between buyers, sellers, and renters.
- Make campus trading more convenient and accessible.

### ⚡ Performance & Scalability
- Type-safe development using TypeScript.
- Component-based frontend architecture with Next.js.
- Structured database operations through Prisma ORM.
- PostgreSQL for reliable relational data storage.
- Modular application architecture for easier maintenance and future expansion.

---

## 🛠️ Tech Stack

| Category | Technologies |
|---|---|
| Frontend | Next.js, React, TypeScript |
| Styling | Tailwind CSS |
| Backend | Node.js, Express.js, TypeScript |
| Database | PostgreSQL |
| ORM | Prisma ORM |
| Cloud & Security | AWS IAM |
| Authentication | Application authentication; Google OAuth if configured |
| Package Management | npm / pnpm, depending on the repository |
| Version Control | Git, GitHub |

---

## 🏗️ System Architecture

SleekRoad follows a client-server architecture that separates the user interface, backend application logic, and database operations.

```text
                 ┌──────────────────────┐
                 │       Students       │
                 │ Buyers / Sellers     │
                 │       Renters        │
                 └──────────┬───────────┘
                            │
                            ▼
                 ┌──────────────────────┐
                 │      Next.js App     │
                 │  React + TypeScript  │
                 └──────────┬───────────┘
                            │ HTTPS / API
                            ▼
                 ┌──────────────────────┐
                 │     Node.js API      │
                 │  Express + TypeScript│
                 └──────────┬───────────┘
                            │
                            ▼
                 ┌──────────────────────┐
                 │    Prisma ORM       │
                 │ Database Access     │
                 └──────────┬───────────┘
                            │
                            ▼
                 ┌──────────────────────┐
                 │     PostgreSQL       │
                 │ Listings & User Data │
                 └──────────────────────┘

                 AWS IAM: Access Control
                 for Supported AWS Resources
```

### Architecture Overview

1. **Frontend:** Displays marketplace listings and provides the student-facing interface.
2. **Backend API:** Handles listing operations, application logic, and communication between the frontend and database.
3. **Prisma ORM:** Provides structured, type-safe access to database records.
4. **PostgreSQL:** Stores relational marketplace data.
5. **AWS IAM:** Manages permissions for AWS resources used by the application, according to the configured deployment.

---

## 📂 Project Structure

The following is a representative structure for a Next.js and Node.js marketplace project. Adapt it to match your actual repository.

```text
sleekroad/
│
├── apps/
│   ├── sleekroad-fe/            # Next.js frontend
│   │   ├── app/                 # Pages and layouts
│   │   ├── components/          # Reusable UI components
│   │   ├── public/              # Static assets
│   │   ├── package.json
│   │   └── ...
│   │
│   └── sleekroad-be/            # Node.js backend
│       ├── src/                 # API and application logic
│       ├── prisma/              # Prisma schema and migrations
│       ├── package.json
│       └── ...
│
├── assets/
│   └── sleekroad-homepage.png   # Homepage screenshot
│
├── package.json
├── .gitignore
└── README.md
```

*Note: The folder names above are examples. Keep the structure consistent with your actual project.*

---

## ⚙️ Getting Started

Follow these steps to set up SleekRoad locally.

### Prerequisites

Install the following tools:

- Node.js (LTS recommended)
- npm or pnpm
- Git
- PostgreSQL
- AWS account and IAM permissions, if required by your implementation

### 1. Clone the Repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd sleekroad
```

Replace the placeholder with your actual GitHub repository URL.

### 2. Install Dependencies

For a project using npm:

```bash
npm install
```

For a project using pnpm:

```bash
pnpm install
```

If your project is a monorepo, run the command from the repository root.

### 3. Configure Environment Variables

Create the environment files required by your application.

Example backend configuration:

**`.env`**

```env
PORT=5000
DATABASE_URL="postgresql://USER:PASSWORD@HOST:5432/DATABASE?sslmode=require"
```

If your implementation uses additional services, configure their required environment variables as well.

**Security best practices:**
- Never commit `.env` files or database credentials.
- Do not expose private keys in frontend environment variables.
- Use least-privilege IAM policies for AWS resources.
- Keep development and production credentials separate.

### 4. Set Up Prisma

Generate the Prisma Client:

```bash
npx prisma generate
```

Apply existing database migrations:

```bash
npx prisma migrate deploy
```

For local development, create a migration after modifying your Prisma schema:

```bash
npx prisma migrate dev --name init
```

If your Prisma schema is in a custom location, pass the appropriate `--schema` path.

### 5. Run the Application

Start the backend using the scripts configured in its `package.json`.

```bash
npm run dev
```

Start the frontend in a separate terminal:

```bash
cd apps/sleekroad-fe
npm run dev
```

If your project uses different directories or scripts, replace these commands with the ones defined in your repository.

### 6. Open the Application

- **Frontend:** http://localhost:3000
- **Backend API:** http://localhost:5000

These are example local URLs; actual ports depend on your configuration.

---

## 🗄️ Database & Prisma ORM

SleekRoad uses PostgreSQL and Prisma ORM to manage structured application data.

Depending on the implemented schema, database entities may include:

- Users and student profiles.
- Product listings.
- Product categories.
- Buying, selling, and rental information.
- Listing availability and status.

Prisma helps maintain a structured data-access layer and provides generated TypeScript types for database queries.

Useful commands:

```bash
# Generate Prisma Client
npx prisma generate

# Open Prisma Studio
npx prisma studio

# Apply development migrations
npx prisma migrate dev
```

---

## ☁️ Security & AWS IAM

AWS IAM supports secure access management for AWS resources used by the application.

Security considerations include:

- Follow the principle of least privilege.
- Assign only the permissions required by each application component.
- Prefer IAM roles for workloads running on AWS compute services.
- Avoid storing AWS access keys in source code.
- Review resource policies and access permissions regularly.

The exact AWS services and permissions depend on the deployed architecture.

---

## 🚀 Deployment

Deploy the frontend and backend according to your configured hosting environment.

### Frontend

For a Next.js deployment:

1. Connect the repository to your hosting provider.
2. Configure the frontend root directory and build command.
3. Add the required environment variables.
4. Configure the production domain.
5. Build and deploy the application.

### Backend

For a Node.js backend hosted on a cloud server:

1. Provision the required compute resources.
2. Configure the Node.js runtime and application environment.
3. Set the PostgreSQL connection string.
4. Configure the process manager and reverse proxy if required.
5. Enable HTTPS and restrict network access.
6. Verify API endpoints and database connectivity.

### Database

Ensure that the PostgreSQL database is reachable from the backend and that production migrations are applied safely.

---

## 🔮 Future Improvements

Potential enhancements include:

- Advanced search and filtering.
- Product categories and sorting.
- Wishlist and saved listings.
- In-app messaging between students.
- Rental availability and booking management.
- Student verification and trust mechanisms.
- Reviews and seller ratings.
- Listing moderation and reporting.
- Notifications for new listings and messages.
- Automated testing and CI/CD workflows.

---

## 🎯 What I Learned

Developing SleekRoad provided practical experience with:

- Building a full-stack marketplace using Next.js and Node.js.
- Designing and developing API-driven applications.
- Managing relational data with PostgreSQL.
- Using Prisma ORM for type-safe database access.
- Implementing structured listing and marketplace workflows.
- Applying cloud access-management principles through AWS IAM.
- Organizing frontend and backend application code.
- Designing a platform around the needs of a specific user community.

---

## 🤝 Contributing

Contributions, suggestions, and bug reports are welcome.

1. Fork the repository.
2. Create a feature branch.
3. Commit your changes.
4. Push the branch to GitHub.
5. Open a pull request.

```bash
git checkout -b feature/your-feature
git add .
git commit -m "feat: add your feature"
git push origin feature/your-feature
```

---

## 📄 License

Add a `LICENSE` file if you intend to distribute SleekRoad under an open-source license. Specify the license here once selected.

---

## 👨‍💻 Author

**SleekRoad — Campus Marketplace**

- 🌐 Live Website: [YOUR_LIVE_DEMO_URL](YOUR_LIVE_DEMO_URL)
- 💻 GitHub: [Your GitHub Profile](https://github.com/YOUR_GITHUB_USERNAME)
- 📧 Contact: [Your Email](mailto:YOUR_EMAIL@example.com)

---

<p align="center">
  If you find SleekRoad interesting, consider giving the repository a ⭐ on GitHub!
</p>
