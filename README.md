# SonicSleuth 🔍🎶

> Nothing implement yet

**SonicSleuth** is a lightweight music exploration tool that recommends YouTube tracks based on a user‑input genre.  
This is the MVP prototype — front‑end + API only, no server‑side database yet.

## Motivation
As a daily Spotify user, I’ve found that the “Discover” and “Release Radar” features rarely surprise me—those tracks that truly wow me seldom surface. Even shuffle on my own playlists ends up cycling through the same familiar songs, while others never get a chance. YouTube’s recommendations aren’t any better—they’re not designed for music discovery, and I often feel stuck within the mainstream echo chamber.

That’s why I decided to build **SonicSleuth**: a tool that helps me (and others) uncover fresh, unexpected music—voices and sounds you might never encounter otherwise. Rather than relying on popularity or chart trends, **SonicSleuth** is about **serendipity**—surfacing hidden gems guided by your taste but beyond your usual orbit.

## 🚀 Features (MVP)
- Input mood or genre (e.g. `dreamy lo-fi jazz`)
- Fetch 10 YouTube videos via YouTube Data API
- Display thumbnail, title, channel, view count
- Open video in embedded iframe
- Like / Skip buttons (stored locally)

## 🧩 Tech Stack
- **Frontend**: React + Fetch/Axios  
- **Backend**: FastAPI + `google-api-python-client`  
- **No Database Yet** (feedback saved in browser localStorage)

## ⚙️ Setup Instructions

### 1. Clone & Backends
```bash
git clone https://github.com/yourname/sonicsleuth.git
cd sonicsleuth/backend
python3 -m venv venv
source venv/bin/activate
pip install fastapi uvicorn google-api-python-client
export YT_API_KEY=your_key_here
uvicorn main:app --reload
````

### 2. Frontend

```bash
cd ../frontend
npm install
npm start
```

### 3. Usage

* Open [http://localhost:3000](http://localhost:3000)
* Enter a genre (e.g., `"dreamy jazz"`)
* Click **Recommend** to fetch suggestions
* Browse and play embedded videos, click **Like** or **Skip**

## 🔭 Next Steps

* Persist user feedback with a database (MongoDB / SQLite)
* Develop a ranking algorithm combining semantic similarity and popularity
* Explore embedding-based ranking or GPT semantic analysis
* Improve UI/UX and deploy a public demo

## 🤝 Contributing

Contributions welcome!

* Open an issue for discussion or feature request
* Submit a pull request to add functionality or improve docs
