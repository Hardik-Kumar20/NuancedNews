# Nuanced News
Nuanced News is a web application that curates current news stories from various sources across the web. It highlights left-leaning and right-leaning bias and enables readers to gain a comprehensive and balanced understanding of the WHOLE story.  

  NN is open to contributors! Please star the repository if this interests you! 
  
## Features
- User Authentication
- News Aggregation
- Real-time updates
  
## How it Works
Large news publications post their .rss files, which are XML files that contain the latest news articles from the publication. The Nuanced News app fetches these .rss files from various sources, parses the XML to extract article information, and categorizes the articles based on their source's political bias.

## Technologies Used
- ### Frontend:
* React
* Bootstrap
* Vite
* Axios
- ### Backend:
* Flask
* Python
- ### Other:
* Firebase (User Auth)

## Installation and Setup
### MAKEFILE
  A makefile has been added. Now you can run the code by simply using:
```bash
make install
make run
```
  Make sure you run rss_parser.py to populate the JSON before starting the server. 
```bash
python rss_parser.py
```
### 1. Clone the repository
```bash
git clone https://github.com/jackabald/NuancedNews.git
cd NuancedNews
```
### 2. Backend Setup
- Navigate to the backend directory and setup a virtual environment:
```bash
cd Backend
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
```
- Install the required Python packages:
```bash
pip install -r requirements.txt
```
- Parse RSS feeds and start the Flask server:
```bash
python rss_parser.py
python app.py
```
### 3. Frontend Setup
- Navigate to the frontend directory:
```bash
cd Frontend
```
- Install required node packages:
```bash
npm install
```
- Create a .env file in the frontend directory to hold all of your environment variables for Firebase Web SDK:
```
VITE_API_KEY=your_firebase_api_key
VITE_AUTH_DOMAIN=your_firebase_auth_domain
VITE_PROJECT_ID=your_firebase_project_id
VITE_STORAGE_BUCKET=your_firebase_storage_bucket
VITE_MESSAGING_SENDER_ID=your_firebase_messaging_sender_id
VITE_APP_ID=your_firebase_app_id
```
- Start development server:
```bash
npm run dev
```

## Docker Setup

### Prerequisites
- Docker installed
- Docker Compose installed

### Running with Docker

1. Build and run the containers:
```bash
docker-compose up --build
