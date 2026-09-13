# 🛡️ SpamShield AI – AI Spam Email Detection System
An intelligent web-based spam email detection system that uses Machine Learning and Natural Language Processing (NLP) to identify whether an email is **Spam** or **Not Spam**.
The application provides secure user authentication, real-time email prediction, confidence scores, risk analysis, and user-specific prediction history.
## ✨ Features
- 🤖 AI-based Spam Email Detection
- 📧 Classifies emails as **Spam** or **Not Spam**
- 📊 Prediction confidence and probability scores
- ⚠️ Spam risk trigger analysis
- 👤 User Registration and Login
- 🔐 Secure password hashing
- 🚪 Login and Logout functionality
- 🗃️ SQLite database for user accounts
- 📜 User-specific prediction history
- 🔍 Search prediction history
- 🗑️ Clear prediction history
- 📨 Sample email testing
- 📱 Responsive and modern user interface
- 🔒 Session-based authentication
- ⚡ Works locally without any paid API
## 🛠️ Technologies Used
- **Python**– Core programming language
- **Flask** – Web application framework
- **Scikit-learn** – Machine Learning
- **TF-IDF** – Text feature extraction
- **Pandas** – Dataset processing
- **NumPy** – Numerical operations
- **Joblib** – Saving and loading ML models
- **SQLite** – User and prediction database
- **Werkzeug** – Secure password hashing
- **HTML5** – Web page structure
- **CSS3** – UI styling and responsive design
- **JavaScript** – Frontend interactions
## 📁 Project Structure

```text
AI-Spam-Email-Detection/
│
├── dataset/
│   └── spam_email_dataset.csv
│
├── model/
│   ├── spam_classifier.pkl
│   └── tfidf_vectorizer.pkl
│
├── database/
│   └── users.db
│
├── templates/
│   ├── login.html
│   ├── register.html
│   ├── index.html
│   └── history.html
│
├── static/
│   ├── css/
│   │   └── style.css
│   └── js/
│       └── script.js
│
├── app.py
├── train_model.py
├── requirements.txt
├── README.md
└── .gitignore
File Description
app.py – Main Flask application containing authentication, prediction, database operations, and API routes.
train_model.py – Trains the Machine Learning spam classification model.
spam_email_dataset.csv – Dataset containing spam and legitimate email samples.
spam_classifier.pkl – Trained Machine Learning classification model.
tfidf_vectorizer.pkl – TF-IDF vectorizer used to convert email text into numerical features.
users.db – SQLite database containing user accounts and prediction records.
login.html – Login page.
register.html – User registration page.
index.html – Main email detection interface.
history.html – Displays the logged-in user's prediction history.
style.css – Application UI and responsive styling.
script.js – Handles frontend interactions and API communication.
requirements.txt – Required Python dependencies.
.gitignore – Prevents sensitive and unnecessary files from being uploaded to GitHub.
How SpamShield AI Works
**The application follows this workflow:
Email Text
    ↓
Text Preprocessing
    ↓
TF-IDF Feature Extraction
    ↓
Trained Machine Learning Model
    ↓
Spam / Not Spam Prediction
    ↓
Confidence & Probability Analysis
    ↓
Risk Trigger Detection
    ↓
Prediction History
User Authentication
SpamShield AI includes a complete authentication system.
Registration
Users can create an account using:
Full Name
Email
Password
Confirm Password
The application validates:
Required fields
Valid email format
Minimum password length
Password confirmation
Duplicate email prevention
Passwords are securely stored using Werkzeug password hashing.
Login
Registered users can log in using their email and password.
Invalid credentials display:
Invalid email or password.
Logout
Users can securely log out of their account.
🗃️ Database
SpamShield AI uses SQLite for storing application data.
Users Table
Stores:
User ID
Full Name
Email
Hashed Password
Account Creation Date
Predictions Table
Stores:
Prediction ID
User ID
Email Text
Prediction Result
Confidence
Spam Probability
Ham Probability
Risk Triggers
Word Count
Prediction Date
Each user can access only their own prediction history.
🔄 Application Workflow
User Registration
        ↓
User Login
        ↓
SpamShield AI Dashboard
        ↓
Enter Email
        ↓
AI Spam Detection
        ↓
Display Prediction
        ↓
Save Result to Database
        ↓
View Prediction History
        ↓
Logout
📊 Prediction Analysis
For every analyzed email, SpamShield AI provides information such as:
Prediction result
Confidence score
Spam probability
Not-Spam probability
Detected risk triggers
Email word count
This makes the prediction easier to understand instead of displaying only a simple Spam/Not Spam result.
📨 Sample Emails
The application provides sample emails that can be used to quickly test the spam detection system.
Example:
Congratulations! You have won a free prize.
Click the link below to claim your reward.
The system analyzes the email and returns the prediction.
📜 Prediction History
After analyzing an email, the prediction can be stored in the database.
Users can:
View previous predictions
Search their history
Review prediction results
View confidence information
Clear their prediction history
Prediction data is isolated between users.
🔒 Security
SpamShield AI implements several security practices:
Password hashing using Werkzeug
Flask session-based authentication
Protected application routes
User-specific database queries
Duplicate account prevention
Secure session cookie configuration
SQLite foreign-key relationships
Sensitive database files excluded using .gitignore
💻 Installation
1. Clone the Repository
git clone YOUR_GITHUB_REPOSITORY_URL
2. Navigate to the Project
cd AI-Spam-Email-Detection
3. Create a Virtual Environment
Windows:
python -m venv venv
Activate it:
venv\Scripts\activate
📦 Install Dependencies
pip install -r requirements.txt
🧠 Train the Model
If you want to retrain the Machine Learning model:
python train_model.py
The trained model files will be saved inside:
model/
▶️ Run the Application
Start the Flask server:
python app.py
Then open:
http://127.0.0.1:5000
👤 Using the Application
Step 1 – Register
Create a new account using your name, email, and password.
Step 2 – Login
Log in with your registered credentials.
Step 3 – Detect Spam
Enter an email message into the detector.
Step 4 – View Result
The AI model displays:
Spam / Not Spam
Confidence
Probability scores
Risk information
Step 5 – View History
Open the History page to see your previous predictions.
Step 6 – Logout
Click Logout when finished.
🧪 Testing
The project can be tested using the following authentication flow:
✅ Register a new user
✅ Register with duplicate email
✅ Login with valid credentials
✅ Login with invalid credentials
✅ Access protected dashboard
✅ Detect spam email
✅ Save prediction
✅ View prediction history
✅ Verify user-specific history
✅ Clear history
✅ Logout
✅ Verify unauthenticated users are redirected to Login
🌟 Main Advantages
🤖 Automated AI-based spam detection
⚡ Fast real-time predictions
🔐 Secure user authentication
👤 Personalized prediction history
📊 Detailed prediction analysis
💻 Runs locally without paid APIs
📱 Responsive web interface
🗃️ Persistent SQLite storage
🎯 Objective
The main objective of SpamShield AI is to provide an easy-to-use and intelligent system for detecting potentially harmful or unwanted emails using Machine Learning and Natural Language Processing.
The system combines AI-based email classification, secure authentication, prediction analysis, and history management into a single web application.
🔮 Future Enhancements
📧 Gmail/Outlook integration
🧠 Advanced NLP models
🔄 Continuous model retraining
📈 Advanced analytics dashboard
🚨 Phishing URL detection
🔗 Malicious link analysis
📱 Mobile application
☁️ Cloud deployment
🛡️ Explainable AI for prediction decisions
👩‍💻 Author
Baddili Hema Kumari
CSE Student
Interested in AI/ML, Python, Software Development and Full Stack Development
GitHub:-https://github.com/BaddiliHemaKumari
⭐ Support
If you find SpamShield AI useful, consider giving the repository a ⭐ on GitHub!
GitHub Repository :https://github.com/BaddiliHemaKumari/AI-Spam-Email-Detection.git
