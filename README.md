# Forsa

#Problem
Students often choose majors without reliable, contextual guidance. Traditional advice is generic and ignores psychological readiness and local constraints.

# Solution
FORSA provides AI-guided career recommendations that combine student interests, psycho-cognitive signals, environmental constraints, and grounded data sources.

# AI Usage
The recommendation pipeline uses:
- Interest assessment results
- Psycho-cognitive indicators (stress, focus, resilience, social tolerance)
- Environmental constraints (internet, location stability, crisis exposure)
- Retrieved contextual data (university programs, labor market, workshops)

AI logic is deterministic within this prototype to ensure explainability and consistent outputs for review.

# RAG Explanation
RAG (Retrieval Augmented Generation) is implemented as a local retrieval layer:
1) **Data source**: internal datasets for university programs, labor market, workshops, and psychological mapping rules.
2) **Retrieval step**: the system retrieves relevant programs, market signals, and workshops for each major.
3) **Generation step**: retrieved context adjusts fit/risk/adaptability scores and produces grounded explanations.

This keeps recommendations contextual, localized, and crisis-aware.

# Project Structure
This prototype keeps a single runtime file for simplicity but follows explicit module boundaries:
- **Data**: static datasets and constants
- **RAG**: retrieval helpers + explanation builder
- **Logic**: scoring and recommendations
- **UI**: render/bind only
- **Core**: routing and persistence

These boundaries are documented in code via `AppModules` to support future file-level modularization.

# Development
Open `index.html` in a browser. No build step required.
