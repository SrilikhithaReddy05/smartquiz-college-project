# SmartQuiz - Interactive Quiz Website with Live Countdown Timer

> **College Mini Project** for 2-1 Semester B.Tech (Computer Science & Engineering / Information Technology).  
> Features a synchronized real-time countdown timer, dynamic question navigation palette, instant evaluation, circular score gauge, and full Java Servlet / MySQL database backend architecture.

---

## 🚀 Live Demo & Deployment

This project is fully configured for deployment on **Netlify** with zero configuration required.

### Quick Deploy to Netlify (Via Git)
1. Initialize Git and push this repository to GitHub:
   ```bash
   git init
   git add .
   git commit -m "Initial commit of SmartQuiz project"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/smartquiz.git
   git push -u origin main
   ```
2. Log in to [Netlify](https://app.netlify.com/).
3. Click **"Add new site"** > **"Import an existing project"** > Choose **GitHub**.
4. Select your `smartquiz` repository.
5. Netlify will automatically detect the settings from `netlify.toml`:
   - **Build command**: `npm run build`
   - **Publish directory**: `dist`
6. Click **"Deploy site"** — your live website will be live in ~30 seconds!

### Alternative: Netlify Manual Drag & Drop Deploy
1. Build the project locally:
   ```bash
   npm install
   npm run build
   ```
2. Open Netlify Dashboard > **Sites** > drag and drop the generated `dist` folder directly onto the screen.

---

## 🛠️ Local Development Setup

### Prerequisites
- **Node.js**: v18.0.0 or higher
- **npm**: v9.0.0 or higher

### Steps to Run Locally
1. Clone or unzip the project folder.
2. Open terminal in the project directory and install dependencies:
   ```bash
   npm install
   ```
3. Start the local development server:
   ```bash
   npm run dev
   ```
4. Open your browser and navigate to:
   ```text
   http://localhost:3000
   ```

---

## 📁 Complete Project Structure

```text
smartquiz/
├── public/
│   └── _redirects              # Netlify SPA routing rewrite rule
├── src/
│   ├── components/
│   │   ├── Navbar.tsx          # Top Bar with brand mark and role switches
│   │   ├── LandingPage.tsx     # Hero banner, feature cards, and catalog
│   │   ├── AuthModal.tsx       # Student login, registration, and admin login
│   │   ├── StudentDashboard.tsx# Personal score analytics & test launcher
│   │   ├── QuizExamView.tsx    # Live MM:SS timer, question palette & auto-submit
│   │   ├── ResultView.tsx      # Circular SVG score gauge & answer review
│   │   ├── AdminDashboard.tsx  # Question bank CRUD & student results ledger
│   │   └── ProjectHubModal.tsx # In-app Java/SQL source code & Viva prep center
│   ├── data/
│   │   ├── initialData.ts      # 5 subject question banks (Java, Web, SQL, DSA, CN)
│   │   └── javaProjectCode.ts  # Authentic Java Servlets, JDBC, SQL scripts & Viva
│   ├── services/
│   │   └── dbService.ts        # Simulated MySQL & JDBC persistence engine
│   ├── types/
│   │   └── quiz.ts             # TypeScript interfaces for Students, Quizzes, Questions
│   ├── App.tsx                 # Root layout & view controller
│   ├── index.css               # Tailwind CSS v4 design tokens
│   └── main.tsx                # React 19 application entry point
├── index.html                  # HTML5 template with typography links
├── netlify.toml                # Netlify CI/CD build & security configuration
├── package.json                # Project dependencies and npm scripts
├── tsconfig.json               # TypeScript ES2022 configuration
└── vite.config.ts              # Vite bundler & Tailwind plugin setup
```

---

## 🎓 College Mini Project Java & MySQL Backend Suite

For your 2-1 semester B.Tech mini project submission and viva voce examination, all backend Java and SQL files are provided inside `src/data/javaProjectCode.ts` and viewable directly via the **"Java & SQL Source Code"** button in the website header:

| File Name | Purpose |
| :--- | :--- |
| `smartquiz.sql` | Complete MySQL DDL & DML script creating 6 normalized tables (`students`, `admins`, `quizzes`, `questions`, `quiz_results`, `student_answers`) with seed records. |
| `DBConnection.java` | JDBC Singleton database connection manager using `com.mysql.cj.jdbc.Driver`. |
| `LoginServlet.java` | HttpServlet managing student and admin logins with `HttpSession` session tracking. |
| `RegisterServlet.java` | HttpServlet storing new student registrations into MySQL. |
| `SubmitQuizServlet.java` | HttpServlet evaluating candidate answers, computing percentages, and managing ACID transactions. |
| `AdminQuestionServlet.java`| HttpServlet executing CRUD operations on the MySQL question bank. |
| `web.xml` | Apache Tomcat deployment descriptor with URL patterns and session timeout rules. |
| `Tomcat_Setup_Guide.md` | Step-by-step local setup guide for Eclipse IDE and Tomcat 9/10. |
| `Viva_Voce_QA.md` | 15 high-frequency viva voce questions and answers for your project review. |

---

## 🔑 Demo Credentials

- **Student 1**: Roll No `21A91A0501` / Password `password123` (Aarav Sharma)
- **Student 2**: Roll No `21A91A0542` / Password `password123` (Priya Patel)
- **Admin**: Email `admin@smartquiz.edu` / Password `admin123` (Exam Controller)

---

## 📜 License
Developed for educational and academic mini project presentation purposes.
