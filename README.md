# **Break Tracker PWA**

A simple, mobile-first Progressive Web App (PWA) for tracking work sessions and breaks throughout the day. This app is designed to be hosted statically (e.g., GitHub Pages) and installed on mobile devices.

## **Features**

* **PWA Ready:** Installable on iOS (via Safari Share \> Add to Home Screen), Android, Windows, and macOS.  
* **Offline First:** Uses a Service Worker to cache assets and work without an internet connection.  
* **Local Data:** Data persists in local storage between reloads.  
* **Export/Import:** Save daily logs as JSON files to keep a history or transfer between devices.  
* **Privacy:** All data is stored on the device; nothing is sent to a server unless you manually copy/export it.

## **Repository Structure**

/  
├── index.html         \# Main application logic and UI  
├── manifest.json      \# PWA Configuration (Name, colors, icons)  
├── service-worker.js  \# Offline caching logic  
├── .gitignore         \# Git configuration  
├── README.md          \# This file  
└── icons/             \# Icon assets (Required)  
    ├── icon-192x192.png  (Required)
    └── icon-512x512.png  (Required)

## **How to Deploy on GitHub Pages**

1. **Commit the files:** Ensure index.html, manifest.json, service-worker.js, and the icons/ folder are in your repository.  
2. **Go to Settings:** Navigate to your repository on GitHub \-\> **Settings**.  
3. **Pages:** Click on **Pages** in the left sidebar.  
4. **Build and deployment:** Under "Source", select **Deploy from a branch**.  
5. **Branch:** Select **main** (or master) and **/(root)**, then click **Save**.  
6. **Done:** GitHub will provide a URL (usually https://username.github.io/repo-name/). Open this URL on your mobile device to install the app.

## **Local Development**

To test locally, you cannot simply double-click index.html because Service Workers require HTTPS or localhost context to function for security reasons.  
We recommend using a simple HTTP server:  
**Using Python:**  
python \-m http.server 8000

**Using Node.js:**  
npx http-server .

Then visit http://localhost:8000 in your browser.

## **Icon Requirements**

To ensure the app installs correctly, you must create an icons folder and add two PNG images:

* icons/icon-192x192.png  
* icons/icon-512x512.png
