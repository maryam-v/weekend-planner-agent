# Weekend Planner Agent Team

An **AI‑powered weekend itinerary planner** built with **Python** and **Google ADK**.  
This project demonstrates **multi‑agent orchestration**: three specialized agents collaborate to transform a free‑form travel query into a structured, two‑day itinerary.
1. Extracts user travel interests
2. Discovers points of interest (POIs)
3. Builds a structured weekend itinerary

---

## ✨ Features

- **Multi‑agent orchestration**: Sequential delegation across three agents
- **Async workflow handling**: Smooth event streaming with robust error handling
- **Colored logging**: Clear, step‑by‑step outputs using [`rich`](https://github.com/Textualize/rich)
- **Professional documentation**: Diagrams, screenshots, and `.env` secrets management
- **Plug‑and‑play demo**: Run `main.py` once and see the full pipeline in action

---

## 🚀 Setup

Clone the repo and install dependencies:
```bash
git clone https://github.com/yourusername/weekend-planner.git
cd weekend-planner
pip install -r requirements.txt


Create a .env file in the project root with your API keys:

```
GOOGLE_API_KEY=your_google_api_key
OPENAI_API_KEY=your_openai_api_key
ANTHROPIC_API_KEY=your_anthropic_api_key
GOOGLE_GENAI_USE_VERTEXAI=False
```

# ▶️ Run the Demo
```bash
python main.py

# 🎨 Example Output
When you run main.py, you’ll see a colorful step-by-step pipeline:

```
>>> User Query: Plan a two-day weekend in Montreal, Canada focused on hiking trails...

──────────────────────────────
Step 1: Extract Interests (retrieve_user_interest_agent)
{"target_city": "Montreal, Canada", "interest_category": "NATURE_OUTDOORS"}

──────────────────────────────
Step 2: Discover POIs (discovery_agent)
[
  {"name": "Mount Royal Park", "address": "..."},
  {"name": "Parc Jean-Drapeau", "address": "..."},
  {"name": "Parc national des Îles-de-Boucherville", "address": "..."}
]

──────────────────────────────
Step 3: Build Itinerary (plan_itinerary_agent)
Weekend in Montreal, Canada — Urban Nature Escape

Saturday:
  10:00 AM - Explore Mount Royal Park: ...
  1:00 PM - Lunch: ...
Sunday:
  9:30 AM - Day trip to Parc national des Îles-de-Boucherville: ...
Notes: ...
```

Each step is color‑coded:

Blue → User query

Cyan → Intermediate agent outputs

Yellow → JSON outputs

Green → Final itinerary (pretty‑printed)

Red → Errors/escalations


## 🎨 Demo Output
Here’s what the pipeline looks like when you run `python main.py`:

![Weekend Planner Demo Screenshot](docs/demo-output.png)
