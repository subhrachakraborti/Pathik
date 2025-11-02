# Pathik (পথিক)
_Rediscover Kolkata, one story at a time._

![Status](https://img.shields.io/badge/Status-In%20Development-yellow)
![Hackathon](https://img.shields.io/badge/Hackathon-Calcutta<Hacks/>%202025-blue)

---

`Pathik` is a gamified mobile-web app for Calcutta Hacks 2025. It transforms exploring Kolkata's heritage from a passive activity into an interactive quest, blending real-world location-based challenges with AI-powered storytelling.

### The Problem

Kolkata's rich history is often trapped in static plaques and forgotten bylaws. For new generations, this heritage can feel inaccessible and disconnected from their digital lives. How do we make exploring the "City of Joy" as engaging as a video game?

### The Solution

`Pathik` is a digital companion for urban explorers. It features an interactive map of Kolkata's iconic locations. When a user visits a location (verified by GPS), two things happen:

1. AI Storyteller: The user unlocks an AI-generated narrative of that location—a short story, a "first-person" account from a historical figure, or a vivid description of a past event.

2. Gamified Collection: The user collects a unique digital "Heritage Card" for that location. By collecting cards, users complete quests, learn the city's stories, and compete on a public leaderboard.

### Core MVP Features (for Calcutta Hacks 2025)

* Interactive Heritage Map: A map of Kolkata (using Mapbox or Leaflet) populated with 15-20 key heritage sites (e.g., Victoria Memorial, Coffee House, Howrah Bridge, Marble Palace).
* User Authentication: Simple email/social login using Supabase Auth.
* AI-Powered Narratives: When a user is at a location, they can request a story. This calls an OpenRouter API (e.g., GPT-4o-mini, Claude 3.5 Sonnet) with a prompt like: "Tell me a short, vivid, 150-word story about the Victoria Memorial from the perspective of a tourist in 1925."
* GPS "Check-in" (Core Gamification):
   * A "Check-in" button is enabled only when the user is on-site.
   * Logic: navigator.geolocation gets the user's lat/long. The backend (Supabase Edge Function or Next.js API route) checks if these coordinates are within a 100m radius of the landmark's coordinates.

* Digital Card Collection: A simple table in Supabase linking user_id to location_id to track collected cards. The UI displays these as a grid of "unlocked" achievements.
* Leaderboard: A public page showing users ranked by the number of heritage cards collected.

### Tech Stack

This project is designed to be built and deployed rapidly using a modern, scalable stack.
* Framework: Next.js (React)
* Styling: TailwindCSS
* Backend & DB: Supabase or Firebase (Auth, Postgres Database for users/places/leaderboard, PostGIS for geo-queries)
* AI: OpenRouter (for access to various LLMs)
* Deployment: Vercel

### Hackathon Tracks

This project is aimed at the following Calcutta Hacks 2025 tracks:
* "Heritage & Culture"
* "AI for Good"
* "Smart Cities & Tourism"

### Future Scope (Post-Hackathon)

1. AR Mode: Overlaying historical photos or 3D models onto the live camera view.
2. Community Submissions: Allowing users to submit their own family stories or photos related to a location.
3. Themed Quests: "The Tagore Trail," "Netaji's Escape Route," "Colonial Architecture" quests that guide users along a specific path.
4. AI Voice Narratives: Integrating a voice API to read the stories aloud.

### Meet the Team: Creo Canvas

* **Subhra Chakraborti (Team Lead)** - [LinkedIn](https://www.linkedin.com/in/subhrachakraborti) | [GitHub](https://github.com/subhrachakraborti)
* **Ishiraj Palchaudhuri** - [LinkedIn](https://www.linkedin.com/in/ishiraj-palchaudhuri-6b77ab389) | [GitHub](https://github.com/totti0126)
* **Ranojoy Chatterjee** - [LinkedIn](https://www.linkedin.com/in/ranojoy-chatterjee) | [GitHub](https://github.com/chatterjeeranojoy98)
