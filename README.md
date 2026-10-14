# A Python-Based Skill Assessment and Gap Analysis System for Students

SkillGap is a Python-based web application developed to help students assess their technical skills and identify the skills they need to improve for a selected job role.

The system evaluates students through objective questions, calculates skill levels, compares them with the required levels for a job role, and generates a learning roadmap based on skill gaps and priorities.

## 🎯 Objectives

1. To create a structured dataset of job roles, skills, and required skill levels.
2. To assess student knowledge through objective questions and determine their current skill levels.
3. To compare assessed skill levels with the required levels and identify skill gaps.
4. To provide priority-based recommendations for improving identified skill gaps.
   

## ✨ Features

- **Multiple Job Roles:** Supports Python Developer, Data Analyst, Software Tester, and Network Engineer.
- **Randomized Quiz:** Selects random questions for each skill and shuffles answer options.
- **Skill Assessment:** Classifies skills as Basic, Intermediate, or Advanced based on scores.
- **Gap Analysis:** Compares assessed skill levels with the required levels for the selected job role.
- **Priority-Based Learning Roadmap:** Highlights High- and Medium-priority skill gaps.
- **Data Visualization:** Displays skill comparisons and overall job readiness using charts.
- **User Authentication:** Provides registration and login functionality.
- **Assessment History:** Allows students to view previous results and track progress.
- **Multiple Storage Formats:** Stores assessment results in JSON, CSV, and MySQL.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Streamlit | Web application interface |
| Pandas | Reading and processing CSV data |
| Matplotlib | Creating charts and visualizations |
| MySQL | Storing user accounts and assessment results |
| XAMPP | Running the local MySQL database |
| MySQL Connector/Python | Connecting Python with MySQL |
| CSV | Storing job roles, skills, and questions |
| JSON | Storing assessment results |
| hashlib | Hashing passwords using SHA-256 |

## 💼 Supported Job Roles

The application currently supports four job roles:

1. **Python Developer:** Python Basics, OOP, and Data Structures.
2. **Data Analyst:** SQL, Statistics, and Pandas.
3. **Software Tester:** Testing Basics, Bug Reporting, and Test Automation.
4. **Network Engineer:** Networking Basics, IP Addressing, and Network Security.

Each job role has three skills with predefined required proficiency levels.

## 📊 Skill Level Classification

The system converts assessment scores into skill levels using the following rules:

| Score | Skill Level |
|---|---|
| Below 40% | Basic |
| 40%–79% | Intermediate |
| 80% and above | Advanced |

### Skill Gap Priority

The system compares the assessed level with the required level for each skill.

- **High Priority:** The required level is two levels higher than the assessed level.
- **Medium Priority:** The required level is one level higher than the assessed level.
- **No Gap:** The assessed level meets or exceeds the required level.

The results help students identify which skills require more attention.

## 🏗️ Project Workflow

1. Analyze project requirements.
2. Prepare job-role, skill, and question datasets.
3. Configure the MySQL database.
4. Design the web interface using Streamlit.
5. Generate quizzes and evaluate submitted answers.
6. Calculate skill levels and analyze gaps.
7. Display results, charts, and learning priorities.
8. Save assessment results and test the application.

## 📁 Project Structure

The project includes Python modules, CSV datasets, application pages, and data-storage files. The exact structure may vary depending on the final version of the code.

```text
SkillGap/
├── app.py
├── analyzer.py
├── auth.py
├── charts.py
├── roles_skills.csv
├── questions.csv
├── requirements.txt
├── .gitignore
└── README.md
```

Additional Python modules, configuration files, and application pages may also be present in the project.

## ⚙️ Installation and Setup

### Prerequisites

Install or configure the following:

- Python 3.10 or a compatible version supported by the project dependencies.
- MySQL database server.
- XAMPP, if you are using it to run MySQL.
- Git (optional, for cloning the repository).

### Step 1: Clone the Repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
```

Move into the project directory:

```bash
cd <YOUR_PROJECT_FOLDER>
```

Replace the placeholders with your actual GitHub repository URL and folder name.

### Step 2: Create a Virtual Environment

```bash
python -m venv .venv
```

Activate it on Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

### Step 3: Install Dependencies

If the repository contains a `requirements.txt` file, run:

```bash
python -m pip install -r requirements.txt
```

### Step 4: Configure MySQL

1. Start MySQL using XAMPP or your configured MySQL server.
2. Create the database required by the application.
3. Configure the database connection settings according to your local setup.
4. Ensure that the required tables are available: `users`, `results`, and `skill_results`.

Use the database name and connection settings expected by your application code.

### Step 5: Run the Application

Run the main Streamlit application file:

```bash
python -m streamlit run app.py
```

Open the local URL displayed in the terminal to access the application.

**Note:** The application may require additional configuration, database initialization, or Python packages depending on the version of the source code.

## 🔐 Security Note

The application uses SHA-256 hashing for passwords before storing them. This demonstrates basic password hashing; however, SHA-256 alone is not recommended for production password storage. A dedicated password-hashing algorithm such as Argon2 or bcrypt is preferable for a production application.

Do not upload database passwords, API keys, personal student information, or other confidential data to GitHub.

## 🚀 Future Scope

- Add more job roles, including Cloud Engineer, AI/ML Engineer, Cybersecurity Analyst, and Web Developer.
- Recommend learning resources based on identified skill gaps.
- Integrate AI-based personalized learning recommendations.
- Update skill requirements using current industry expectations.
- Improve progress tracking with additional charts and reports.
- Deploy the application on a cloud platform for online access.


## 📚 References

- [Python Documentation](https://docs.python.org/3/)
- [Streamlit Documentation](https://docs.streamlit.io/)
- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [Matplotlib Documentation](https://matplotlib.org/stable/)
- [MySQL Documentation](https://dev.mysql.com/doc/)
- [MySQL Connector/Python Documentation](https://dev.mysql.com/doc/connector-python/en/)

---

*SkillGap is an academic micro project developed to demonstrate Python programming, data processing, database connectivity, web application development, and skill gap analysis.*
