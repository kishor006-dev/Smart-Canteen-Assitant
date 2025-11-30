# smart-canteen-assitant-
AI-based Smart Canteen Assistant Project
# 🍴 Smart Canteen AI Assistant
**Subtitle:** AI-powered Smart Canteen Assistant for students and staff with real-time chat, menu management, and order tracking.  

![Thumbnail](assets/canteen.jpg)  

---

## Overview
**Smart Canteen AI** is a web-based application that allows students to interact with a virtual canteen assistant powered by AI (Groq + LLaMA 3.1 70B). Students can view the menu, place orders, receive recommendations, and manage order history. Staff can manage the menu, set daily specials, and track pending orders.

**Features:**  
- **Student Panel:** Login/Signup, chat with AI assistant, place/cancel orders, view order history.  
- **Staff Panel:** Login/Signup, manage menu items, set daily specials, mark orders as ready.  
- AI-powered recommendations & conversational interface.  
- Real-time notifications via WebSockets.  

---

## Project Structure

Smart-Canteen-AI/
  backend/
    -> main.py             # FastAPI backend
    -> requirements.txt    # Python dependencies
├─ student/
    ├─ student.html        # Student frontend
    ├─ student.css
    └─ student.js
├─ staff/
    ├─ staff.html          # Staff frontend
    ├─ staff.css
    └─ staff.js
├─ assets/
    ├─ canteen.jpg         # Student background image
    └─ staffside.jpg       # Staff background image
│
└─ README.md


## Prerequisites
- Python 3.10+  
- Node.js (optional, for running frontend via server)  
- MongoDB running locally on default port `27017`  
- Groq API Key for AI functionality (set as environment variable `GROQ_API_KEY`)  

---

## Backend Setup
1. Create and activate a virtual environment:

``bash
python -m venv venv
# Linux/Mac
source venv/bin/activate
# Windows
venv\Scripts\activate

2. Install dependencies:

pip install -r backend/requirements.txt

3. Start the backend server:

uvicorn backend.main:app --reload

## Frontend Setup

Open `student/student.html` and `staff/staff.html` in your browser.

Ensure backend server is running at `http://localhost:8000` for API calls.

**Student Panel:**

* Login with seeded user: `student1 / 123`
* Interact with AI assistant, view menu, place orders

**Staff Panel:**

* Login with seeded user: `staff1 / admin`
* Manage menu, set daily specials, view pending orders

## Environment Variables

GROQ_API_KEY – API key for Groq AI.

**Linux/Mac:**

export GROQ_API_KEY="your_api_key_here"

**Windows PowerShell:**

setx GROQ_API_KEY "your_api_key_here"

 **command prompt**
 set GROQ_API_KEY="your_api_key_here"

## Notes

* Student chat uses WebSockets for real-time notifications.
* Daily specials and combo suggestions are AI-powered.
* Orders are stored in MongoDB and persist across sessions.


## Future Improvements

* Integrate payment gateway for online orders.
* Add analytics dashboard for staff.
* Improve AI recommendations with personalized history.


## License

MIT License



