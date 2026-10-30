# 🎯 AI-Powered Internship Recommendation System

An intelligent, machine learning-based web application that helps students discover relevant internship opportunities based on their educational background, technical skills, interests, and preferences.

The system uses the **Nearest Neighbors algorithm** to identify and recommend internships that closely match a student's profile from a database containing 10,000+ internship records.

## 🚀 Project Overview

Finding suitable internships can be challenging for students because they often need to manually search through thousands of opportunities.

This project addresses that problem by providing personalized internship recommendations through a machine learning-based recommendation engine.

Users enter their profile information, and the system analyzes their details to identify the most relevant internship opportunities.

## ✨ Key Features

- **Personalized Recommendations:** Suggests internships based on education, technical skills, interests, and preferences.
- **Machine Learning Integration:** Uses the Nearest Neighbors algorithm to identify similar internship profiles.
- **Large Internship Dataset:** Processes and retrieves recommendations from 10,000+ internship records.
- **MySQL Database:** Stores and manages structured internship information.
- **REST API Integration:** Connects the React frontend with the Flask backend.
- **Interactive User Interface:** Provides an easy-to-use interface for entering profile details and viewing recommendations.
- **Ranked Results:** Displays the nearest matching internship opportunities.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Backend development and ML implementation |
| Flask | Backend framework and REST APIs |
| React.js | Frontend development |
| HTML5 | Web page structure |
| CSS3 | Styling and responsive design |
| JavaScript | Frontend functionality |
| MySQL | Internship data storage |
| Scikit-learn | Nearest Neighbors implementation |
| NumPy / Pandas | Data preprocessing and manipulation |

## 🏗️ System Architecture

The application follows a frontend-backend-database architecture.

```text
              USER
                |
                ▼
        REACT FRONTEND
                |
                ▼
          HTTP POST
           REQUEST
                |
                ▼
         FLASK BACKEND
                |
                ▼
       INPUT PREPROCESSING
                |
                ▼
        MYSQL DATABASE
       (10,000+ Records)
                |
                ▼
       FEATURE EXTRACTION
                |
                ▼
       NEAREST NEIGHBORS
           ALGORITHM
                |
                ▼
       DISTANCE CALCULATION
                |
                ▼
       TOP MATCHING INTERNSHIPS
                |
                ▼
         JSON RESPONSE
                |
                ▼
        REACT FRONTEND
                |
                ▼
       DISPLAY RECOMMENDATIONS
```

## ⚙️ How It Works

**1. User Profile Input**

Users provide information such as:
- Educational qualification
- Technical skills
- Areas of interest
- Preferred location
- Experience level

**2. Frontend Communication**

The React application collects the user's information and sends it to the Flask backend through an HTTP POST request.

**3. Backend Processing**

Flask receives the user profile, validates the input, and performs the necessary preprocessing.

**4. Database Integration**

The backend connects to MySQL and retrieves the available internship records.

**5. Feature Representation**

The user profile and internship records are converted into numerical feature representations so that they can be compared mathematically.

**6. Machine Learning Recommendation**

The Nearest Neighbors algorithm compares the user profile with internship records using a configured distance metric.

**7. Recommendation Ranking**

The algorithm identifies the nearest internship records and retrieves the top matching opportunities.

**8. Display Results**

The Flask backend returns the recommendations in JSON format, and React displays the results to the user.

## 🤖 Machine Learning Algorithm

### Nearest Neighbors

The project uses the `NearestNeighbors` implementation from Scikit-learn.

It is a distance-based neighbor-search technique used to identify data points that are closest to a given input.

**Working principle:**

1. Represent internship records as numerical feature vectors.
2. Convert the user's profile into the same feature representation.
3. Calculate distances between the user profile and internship profiles.
4. Identify the nearest data points.
5. Return the top matching internship opportunities.

### Euclidean Distance

When configured with Euclidean distance, the algorithm measures the straight-line distance between two feature vectors.

Formula:

\[
d(A,B)=\sqrt{\sum_{i=1}^{n}(A_i-B_i)^2}
\]

A smaller distance indicates that two feature vectors are closer in the feature space.

## 🗄️ Database Design

**Database:** MySQL

**Table:** `internships`

The internship database contains more than 10,000 records.

Example fields:

| Column | Description |
|---|---|
| internship_id | Unique internship identifier |
| company_name | Company offering the internship |
| role | Internship position |
| skills | Required technical skills |
| location | Internship location |
| domain | Internship domain |
| eligibility | Educational eligibility |

*Adjust these fields to match your actual MySQL table schema.*

## 🔌 API Integration

The Flask backend exposes REST API endpoints for communication with the React frontend.

Example recommendation request:

**HTTP Method:** POST

**Endpoint:** `/recommend` (example route; replace with your actual endpoint)

Example request body:

```json
{
  "education": "B.Tech CSE",
  "skills": ["Python", "SQL", "Machine Learning"],
  "interest": "Artificial Intelligence",
  "location": "Hyderabad"
}
```

The backend processes the request and returns internship recommendations in JSON format.

## 💻 Installation and Setup

### Prerequisites

- Python 3.x
- Node.js and npm
- MySQL Server
- Git

### 1. Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd YOUR_PROJECT_FOLDER
```

### 2. Set Up the Backend

Create and activate a virtual environment:

```bash
python -m venv .venv
```

Windows PowerShell:

```powershell
.venv\Scripts\Activate.ps1
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

### 3. Configure MySQL

Create the database:

```sql
CREATE DATABASE internship_db;
```

Create the required internship table and import your internship records.

Configure your MySQL connection details using environment variables or your application's configuration file.

Example configuration:

```text
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=your_password
DB_NAME=internship_db
```

Do not upload actual database passwords or credentials to GitHub.

### 4. Run the Flask Backend

Use your backend entry point and configured Flask command to start the server.

Example:

```bash
python app.py
```

### 5. Set Up the Frontend

Navigate to the frontend directory:

```bash
cd frontend
```

Install dependencies:

```bash
npm install
```

Start the React application:

```bash
npm run dev
```

Open the local URL displayed in your terminal to access the application.

## 📊 Expected Outcome

The application provides students with a list of internship opportunities ranked according to their similarity to the submitted profile.

Instead of manually browsing thousands of listings, users can discover relevant opportunities through an automated recommendation process.

## 🔮 Future Enhancements

- Resume parsing and automatic skill extraction.
- Skill-gap analysis and learning recommendations.
- Integration with live internship data sources.
- Hybrid recommendation techniques.
- User feedback-based recommendation improvement.
- Internship application tracking.
- Admin dashboard for managing internship records.

## 🎓 Learning Outcomes

Through this project, I gained practical experience in:

- Integrating machine learning algorithms into web applications.
- Developing REST APIs using Flask.
- Connecting Python applications with MySQL.
- Building frontend applications using React.js.
- Data preprocessing and feature engineering.
- Implementing distance-based recommendation techniques.
- Integrating frontend, backend, database, and ML components.

## 👩‍💻 Author

**Prathiba Akkinapelly**

BE – Computer Science and Engineering (AI & ML)

GitHub: [Your GitHub Profile](YOUR_GITHUB_PROFILE_URL)

---

⭐ If you find this project interesting, consider giving the repository a star!
