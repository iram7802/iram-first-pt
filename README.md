# WanderAI — AI-Powered Travel Guide & Itinerary Planner

A full-stack, intelligent, responsive travel guide platform that empowers travelers to discover world destinations, plan personalized multi-day itineraries with AI, explore vetted hotels & restaurants, forecast detailed travel budgets, and manage saved trips.

![WanderAI Banner](https://images.unsplash.com/photo-1488646953014-85cb44e25828?auto=format&fit=crop&w=1600&q=80)

---

## 🚀 Live Services & Architecture

- **Frontend Client**: React 18, Vite, Tailwind CSS, Lucide Icons, Leaflet / React-Leaflet Maps, Canvas Confetti.
  - Running on: `http://localhost:3000`
- **Backend API**: Node.js & Express.js REST API with JWT Auth, Heuristic & OpenAI Synthesis Engine, JSON persistence.
  - Running on: `http://localhost:5000`
  - Automated proxy from client `/api` to `http://localhost:5000`

---

## 🌟 Key Features & Pages

### 1. 🏠 Home Page
- **Hero Section**: Large immersive photography, heading *"Explore the World, One Journey at a Time."*
- **Search Bar with Autocomplete**: Live suggestions as you type with thumbnail preview & category tags.
- **Popular & Trending Destinations**: Card showcases with daily budget index, ratings, and wishlist toggles.
- **Quick Category Filters**: Beaches, Mountains, Historical Places, Culture, Adventure.
- **AI Trip Planner Feature Spotlight**: One-click quick form that pre-populates the AI Planner wizard.
- **Featured Experiences**: Top-rated tours, catamaran cruises, and treks with durations and pricing.
- **Why Choose WanderAI**: Verified metrics and explorer testimonials.

### 2. 🗺️ Explore Destinations (`/explore`)
- Multi-faceted real-time filtering:
  - Text search by name, country, or description
  - Category filter pills (Beaches, Mountains, Historical, Culture, Adventure)
  - Country dropdown
  - Budget tier (Budget <$75/day, Moderate $75-$150/day, Luxury $150+/day)
  - Sorting: Popularity, Rating, Budget (Asc/Desc), Name (A-Z)
  - Layout toggle: Grid vs List view
- Wishlist heart button with optimistic update & toast feedback.

### 3. 📍 Destination Details (`/destination/:id`)
- **High-Definition Gallery**: Hero photo with interactive thumbnail switcher.
- **Quick Facts Ribbon**: Best Season, Daily Budget, Currency, Language, Timezone, Ideal Duration.
- **Interactive OpenStreetMap (Leaflet)**: Custom colored pins for attractions (teal) and hotels (amber) with popups.
- **Live Weather Forecast Widget**: Current temperature, condition, humidity, wind, and 5-day outlook.
- **Curated Attractions**: Admission fees, best visiting hours, and photo cards.
- **Culture & Traditions**: Etiquette, cultural heritage, and local customs.
- **Must-Try Local Food**: Signature delicacies, flavor profiles, and price ranges.
- **Transportation Guide**: Scooters, metros, ferries, rail passes, and tips.
- **Daily Expense Tiers**: Budget vs Mid-Range vs Luxury cost breakdowns.
- **Safety Guidelines**: Scams to avoid, neighborhood tips, and health advice.
- **"Plan AI Trip to [Destination]" Action**: Pre-fills the AI Planner wizard.

### 4. 🤖 AI Trip Planner (`/ai-planner`)
- **6-Step Interactive Form**:
  1. Origin and Destination
  2. Duration (1 to 14 days)
  3. Travelers Count (1 to 8) & Companion Type (Solo, Couple, Family with Kids, Friends)
  4. Budget Style (Budget, Moderate, Luxury) & Target Budget
  5. Styles & Interests (Culture, Nature, Foodie, Adventure, Relaxation, Beaches, Nightlife, Photography)
  6. Pace (Relaxed, Balanced, Packed) & Special Requests
- **Generated Output**:
  - Full Day-by-Day schedule (Morning, Afternoon, Evening, Night) with exact times, costs, and tips.
  - Interactive Day Tabs (`Day 1`, `Day 2`, ...).
  - Curated Hotels and Restaurants for the trip.
  - Interactive Packing Checklist with checkboxes.
  - Action Bar: Save Itinerary to Profile, Share public link, Print / Save PDF.
  - **WanderAI Guide Chat Assistant**: Ask custom follow-up questions right inside the itinerary.

### 5. 🏨 Hotels & Dining Directory (`/hotels-restaurants`)
- Switch between **Recommended Hotels** and **Top Restaurants & Dining**.
- Filter by destination, price category, and minimum rating (★ 4.5+, 4.8+, 4.9+).
- Amenities tags (Infinity Pool, Cliff Views, Spa) and Chef's specialties.

### 6. 💰 Travel Budget Calculator (`/budget-calculator`)
- Dynamic interactive sliders for trip duration, travelers count, flights, hotel room rates, food, activities, local transit, and emergency buffer.
- Visual breakdown progress meters with percentage distribution.
- **Multi-Currency Live Converter**: Instant toggling between USD ($), EUR (€), GBP (£), INR (₹), JPY (¥), AUD (A$), and CAD (C$).
- Smart budget optimization tips.

### 7. 👤 User Authentication & Profile (`/profile`)
- Sign up, login, and instant **"Continue as Demo Traveler (1-Click)"** access.
- User Profile Dashboard:
  - Editable profile details (Name, Home Country).
  - **Saved AI Itineraries**: Open, share, or delete saved trips.
  - **Wishlist**: View and manage bookmarked dream destinations.
  - Explorer statistics.

### 8. ℹ️ About & Contact (`/about-contact`)
- Platform mission and travel values.
- **Interactive Contact Form**: Direct API submission with validation and feedback.
- **Interactive FAQ Accordion**: 8+ comprehensive travel and planning questions with smooth expand/collapse.

---

## 🛠️ Tech Stack

| Layer | Technologies |
|---|---|
| **Frontend** | React 18, Vite, React Router v6, Tailwind CSS, Lucide React, Leaflet, React-Leaflet, Canvas Confetti |
| **Backend** | Node.js, Express.js, CORS, Dotenv, JSON Web Tokens (JWT), Bcrypt.js |
| **AI Planner Engine** | Heuristic Synthesis Engine + OpenAI API client support (`gpt-4o-mini`) |
| **Data & Persistence** | JSON Store with pre-seeded users, itineraries, and 12+ world destinations |

---

## 💻 Getting Started Locally

### 1. Requirements
- Node.js (v18+) & npm

### 2. Quick Launch
To start both backend (port 5000) and frontend (port 3000):
```bash
# In the project root
npm run dev
```

Or run them individually:
```bash
# Terminal 1: Backend
cd server
node server.js

# Terminal 2: Frontend
cd client
npm run dev
```

### 3. Open in Browser
Visit **`http://localhost:3000`**

### 4. Optional: Enable Live OpenAI Generation
In `server/.env`, uncomment and set your OpenAI key:
```env
OPENAI_API_KEY=sk-your-openai-key-here
```
*(If omitted, WanderAI automatically runs on its built-in intelligent heuristic synthesis engine).*
