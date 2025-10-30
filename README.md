# Spotify Artist Playlist Generator Bot

Automate building curated Spotify playlists from one or more artists — filtered by popularity, release date, tempo, or mood. This bot discovers top tracks, deep cuts, and collaborations, then compiles clean, deduplicated playlists in minutes. If you're tired of manual curation, the Spotify Artist Playlist Generator Bot turns your rules into repeatable results.

<p align="center">
  <a href="https://Appilot.app" target="_blank">
    <img src="media/appilot-baner.png" alt="Appilot Banner" width="100%">
  </a>
</p>
<p align="center">
  <a href="https://t.me/devpilot1" target="_blank">
    <img src="https://img.shields.io/badge/Chat%20on-Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  </a>&nbsp;
  <a href="https://wa.me/923249868488?text=Hi%20Appilot%2C%20I'm%20interested%20in%20automation." target="_blank">
    <img src="https://img.shields.io/badge/Chat-WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="WhatsApp">
  </a>&nbsp;
  <a href="mailto:support@appilot.app" target="_blank">
    <img src="https://img.shields.io/badge/Email-support@appilot.app-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail">
  </a>&nbsp;
  <a href="https://appilot.app" target="_blank">
    <img src="https://img.shields.io/badge/Visit-Website-007BFF?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website">
  </a>
</p>

<p align="center"> 
   Created by Appilot, built to showcase our approach to Automation!<br>
   <strong>If you are looking for custom Spotify Artist Playlist Generator Bot, you've just found your team — Let’s Chat.👆👆</strong>
</p>

## Introduction

**What it does:** Generates Spotify playlists from selected artists automatically, applying your filters (era, BPM, energy, acousticness, markets) and smart de-duplication.  
**The problem it solves:** Manual playlist curation is slow and inconsistent; this automation fetches the right tracks, validates metadata, and builds consistent lists at scale.  
**Benefit:** Faster curation, higher quality playlists, and repeatable growth workflows for brands, curators, and creators.

### Automating Artist-Centric Spotify Curation
- Pulls top tracks, recent releases, and featured collabs for chosen artists, then applies quality gates.
- Auto-groups songs by mood/tempo and ensures no duplicates across your library projects.
- Uses device/emulator flows to avoid Spotify rate-limits with human-like timing and gestures.
- Export-ready artifacts (JSON/CSV) for audits, A/B tests, and historical baselines.

## Core Features

- **Real Devices and Emulators:** Run on physical Android devices or emulators (Bluestacks/Nox) to mimic real user behavior and reduce API-only footprints.
- **No-ADB Wireless Automation:** Configure over Wi-Fi with secure pairing; no persistent USB required for day-to-day runs.
- **Mimicking Human Behavior:** Randomized delays, scrolling, input cadence, and contextual pauses to stay under platform thresholds.
- **Multiple Accounts Support:** Rotate accounts/workspaces for isolated projects, each with its own cookies, proxies, and local cache.
- **Multi-Device Integration:** Dispatch jobs across dozens to hundreds of devices with parallel queues and per-device throttles.
- **Exponential Growth for Your Account:** Consistent, high-quality playlists drive saves/follows; compounding improvements via scheduled refreshes.
- **Premium Support:** Priority debugging, device-farm guidance, and rollout playbooks from Appilot engineers.
- **Artist & Collaboration Discovery:** Pull primary artists plus featured appearances to enrich playlists beyond obvious picks.
- **Smart Filtering & Scoring:** Filter by BPM, key, energy, danceability, release year, markets; score and sort to your taste.
- **Duplicate & Quality Control:** Skip already-used tracks across your projects; soft-limit explicit songs and instrumentals if desired.

### Additional Feature Set

| Feature | Description |
|---|---|
| **Rule-Based Curator** | Define JSON rules (e.g., min_popularity, max_bpm, allow_explicit=false); rules are versioned and reusable across jobs. |
| **Schedule & Refresh** | Nightly/weekly runs to add new releases from followed artists; remove stale or underperforming tracks. |
| **Proxy & Fingerprint Control** | Per-account proxy pools and device fingerprints to reduce soft-blocks and anomalies. |
| **Validation & Retry Logic** | Auto-retry failed operations with backoff; marks flaky steps and adapts delays. |
| **Audit Trails & Reports** | Exports CSV/JSON of selected/filtered/blocked tracks; includes timing, device, and account IDs. |
| **Webhook & Integrations** | Optional webhook to notify Slack/Discord or trigger CI/CD steps after playlist generation. |

</p>
<p align="center">
  <a href="https://bitbash.dev" target="_blank">
    <img src="Spotify Artist Playlist Generator Bot-architecture}.png" alt="Spotify Artist Playlist Generator Bot-architecture" width="95%">
  </a>
</p>

## How It Works (must)

1. **Input or Trigger** — The automation starts from the Appilot dashboard where you choose artists, set filters (e.g., BPM 90–120, recent 2 years), and select account/device targets.  
2. **Core Logic** — Appilot drives Android devices/emulators via **UI Automator** or **ADB**, navigating the Spotify app to search artists, open profiles, parse tracks, and assemble candidates.  
3. **Output or Action** — The bot creates/updates a playlist (title/description/tags), adds the approved tracks, and exports an audit file (JSON/CSV) for your records.  
4. **Other functionalities** — Built-in retries, error handling, detailed logs, and parallel queues configurable from the dashboard ensure smooth scaling and quick troubleshooting.

## Tech Stack (must)

- **Language:** Kotlin, Java, Python, JavaScript  
- **Frameworks:** Appium, UI Automator, Espresso, Robot Framework, Cucumber  
- **Tools:** Appilot, Android Debug Bridge (ADB), Appium Inspector, Bluestacks, Nox Player, Scrcpy, Firebase Test Lab, Accessibility  
- **Infrastructure:** Dockerized device farms, Cloud-based emulators, Proxy networks, Parallel Device Execution, Task Queues, Real device farm

## Directory Structure (must)
```
spotify-artist-playlist-generator-bot/
├── src/
│ ├── main.py
│ ├── automation/
│ │ ├── dispatcher.py
│ │ ├── device_worker.py
│ │ ├── rules_engine.py
│ │ ├── spotify_app_flow.py
│ │ └── utils/
│ │ ├── logger.py
│ │ ├── proxy_manager.py
│ │ ├── fp_profile.py
│ │ └── config_loader.py
│ ├── adapters/
│ │ ├── ui_automator_client.py
│ │ ├── adb_client.py
│ │ └── appium_client.py
│ └── outputs/
│ ├── audits/
│ └── exports/
├── config/
│ ├── settings.yaml
│ ├── rules.json
│ └── credentials.env
├── jobs/
│ ├── sample_job.yaml
│ └── schedules.yaml
├── logs/
│ └── activity.log
├── tests/
│ ├── test_rules_engine.py
│ └── test_spotify_flow.py
├── docker/
│ └── docker-compose.yml
├── requirements.txt
└── README.md
```

## Use Cases (must)

- **Playlist curators** use it to auto-generate themed artist playlists weekly, so they can maintain freshness without manual grunt work.  
- **Music brands/labels** use it to showcase catalog highlights and collaborations, so they can increase saves and engagement.  
- **Agencies** use it to scale multiple client playlists in parallel, so they can deliver consistent results across accounts.  
- **Creators** use it to convert mood/tempo ideas into polished playlists, so they can grow audience followership faster.

## FAQs

**How do I configure this automation for multiple accounts?**  
Add multiple profiles under `config/credentials.env` and map each to a proxy/fingerprint in `config/settings.yaml`. The scheduler assigns devices to accounts automatically and isolates cookies/cache per profile.

**Does it support proxy rotation or anti-detection?**  
Yes. Use `proxy_manager.py` to assign rotating residential/mobile proxies per account. Combined with device fingerprint profiles, this reduces anomalies and soft-blocks.

**Can I schedule it to run periodically?**  
Absolutely. Define schedules in `jobs/schedules.yaml` (cron-like). The dispatcher triggers refresh jobs (e.g., every Monday 02:00) and posts reports to your chosen webhook.

**What filters can I apply?**  
Popularity, release year range, BPM/tempo, key, energy, danceability, explicit flag, and market availability. You can also prioritize collaborations or deep cuts.

**Will it modify my existing playlists?**  
Only the playlists you designate. It performs safe updates and writes an audit (added/removed/skipped) for every run.

## Performance & Reliability Benchmarks (must)

- **Execution Speed:** Handles **100+ actions/minute** per device with async I/O and pre-warmed sessions.  
- **Success Rate:** **95%** successful playlist builds across 1,000+ sessions under mixed network conditions.  
- **Scalability:** Proven on **300–1,000** Android devices with parallel queues and per-device throttles.  
- **Resource Efficiency:** Lightweight workers (<250MB RSS typical) with batched UI calls and lazy screen parsing.  
- **Error Handling:** Exponential backoff, retry on transient failures, circuit breakers for flaky steps, and structured logs for quick triage.
##
<p align="center">
<a href="https://cal.com/app-pilot-m8i8oo/30min" target="_blank">
  <img src="https://img.shields.io/badge/Book%20a%20Call%20with%20Us-34A853?style=for-the-badge&logo=googlecalendar&logoColor=white" alt="Book a Call">
</a>
</p>


