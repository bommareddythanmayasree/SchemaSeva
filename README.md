# SchemeSeva – Government Scheme Eligibility Checker

A complete full-stack web application that helps Indian citizens discover which government welfare schemes they are eligible for based on personal information such as age, income, occupation, gender, and state.

## 🚀 Features

- **Eligibility Checker**: Quick eligibility verification based on user profile
- **100+ Schemes**: Comprehensive database of government welfare schemes
- **Search Functionality**: Search schemes by name or category
- **Direct Apply Links**: Get direct links to official application portals
- **Modern UI**: Beautiful, responsive design with TailwindCSS
- **Real-time Results**: Instant eligibility matching

## 🛠️ Tech Stack

### Frontend
- React 18
- Vite
- TailwindCSS
- Axios
- React Router

### Backend
- Python 3.8+
- FastAPI
- Uvicorn
- Pydantic

## 📁 Project Structure

```
scheme-seva/
├── backend/
│   ├── app/
│   │   ├── main.py
│   │   ├── routes/
│   │   │   └── scheme_routes.py
│   │   ├── services/
│   │   │   └── eligibility_engine.py
│   │   ├── models/
│   │   │   └── user_model.py
│   │   └── data/
│   │       └── schemes.json
│   └── requirements.txt
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   │   ├── Navbar.jsx
│   │   │   ├── Footer.jsx
│   │   │   ├── SchemeCard.jsx
│   │   │   ├── EligibilityForm.jsx
│   │   │   └── Loader.jsx
│   │   ├── pages/
│   │   │   ├── Home.jsx
│   │   │   ├── Results.jsx
│   │   │   ├── Schemes.jsx
│   │   │   └── About.jsx
│   │   ├── services/
│   │   │   └── api.js
│   │   ├── App.jsx
│   │   └── main.jsx
│   ├── package.json
│   └── vite.config.js
└── README.md
```

## 🚦 Getting Started

### Prerequisites

- Python 3.8 or higher
- Node.js 16 or higher
- npm or yarn

### Backend Setup

1. Navigate to the backend directory:
```bash
cd backend
```

2. Create a virtual environment (recommended):
```bash
python -m venv venv
```

3. Activate the virtual environment:
   - On Windows:
   ```bash
   venv\Scripts\activate
   ```
   - On macOS/Linux:
   ```bash
   source venv/bin/activate
   ```

4. Install dependencies:
```bash
pip install -r requirements.txt
```

5. Run the server:
```bash
uvicorn app.main:app --reload
```

The backend will be available at `http://localhost:8000`

### Frontend Setup

1. Navigate to the frontend directory:
```bash
cd frontend
```

2. Install dependencies:
```bash
npm install
```

3. Run the development server:
```bash
npm run dev
```

The frontend will be available at `http://localhost:5173`

## 📡 API Endpoints

### POST /api/check-eligibility
Check user eligibility for schemes.

**Request Body:**
```json
{
  "age": 25,
  "income": 200000,
  "occupation": "student",
  "gender": "male",
  "state": "Maharashtra"
}
```

**Response:**
```json
{
  "eligible_schemes": [...],
  "total_count": 10
}
```

### GET /api/schemes
Get all available schemes.

### GET /api/search?query=education
Search schemes by name or category.

## 🎨 Usage

1. **Check Eligibility**: 
   - Go to the homepage
   - Fill in your details (age, income, occupation, gender, state)
   - Click "Check Eligible Schemes"
   - View your eligible schemes

2. **Browse All Schemes**:
   - Navigate to "All Schemes" page
   - Browse through all available schemes
   - Use the search bar to find specific schemes

3. **Apply for Schemes**:
   - Click "Apply Now" on any scheme card
   - You'll be redirected to the official government portal

## 📝 Notes

- This platform is for informational purposes only
- Please verify all details on official government portals before applying
- Eligibility criteria may change, always check the official sources

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is open source and available under the MIT License.
