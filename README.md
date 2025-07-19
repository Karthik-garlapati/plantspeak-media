# PlantSpeak - Traditional Plant Knowledge Preservation

PlantSpeak is a Streamlit web application designed to help preserve traditional plant knowledge from elders, farmers, and healers.

## Setup

### 1. Install Dependencies
```bash
pip3 install -r requirements.txt
```

### 2. Database and Files
The following files have been created for you:
- `plantspeak.db` - SQLite database with users and submissions tables
- `plantspeak_submissions.csv` - CSV file for backup submissions
- `uploads/` - Directory structure for uploaded files
  - `uploads/photos/` - Plant photos
  - `uploads/voice/` - Voice recordings
  - `uploads/notes/` - Handwritten notes and documents

### 3. Sample User Account
A sample admin account has been created:
- **Username:** admin
- **Password:** admin123

## Running the Application

```bash
streamlit run app.py
```

The application will be available at `http://localhost:8501`

## Features

- **User Registration & Login**: Secure user authentication system
- **Plant Knowledge Entry**: Add detailed information about plants including:
  - Photos and descriptions
  - Local names and scientific names
  - Usage descriptions and preparation methods
  - Location and community information
  - Voice recordings and handwritten notes
- **Browse Submissions**: View all public submissions with filtering options
- **User Profiles**: Manage personal information and view submission history
- **Privacy Controls**: Choose whether to make submissions public or private

## File Structure

```
plantSpeak/
├── app.py                      # Main Streamlit application
├── plantspeak.db              # SQLite database
├── plantspeak_submissions.csv # CSV backup
├── requirements.txt           # Python dependencies
├── uploads/                   # Uploaded files directory
│   ├── photos/               # Plant photos
│   ├── voice/                # Voice recordings
│   └── notes/                # Handwritten notes
└── README.md                 # This file
```

## Database Schema

### Users Table
- id (Primary Key)
- username (Unique)
- password (Hashed)
- name, email, role, community
- registration_date

### Submissions Table
- id (Primary Key)
- user_id (Foreign Key)
- Plant information (name, scientific name, local names)
- Usage and preparation details
- Location and community information
- File paths for photos, voice, and notes
- Consent and privacy settings

## Privacy and Consent

The application includes privacy controls where users can choose to:
- Make their submissions public (visible to all users)
- Keep submissions private (only visible to the submitter)

Public submissions help build a community knowledge base while respecting users' privacy preferences.
