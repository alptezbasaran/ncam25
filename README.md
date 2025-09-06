# Spiral Graph: Cluster Buster

**Pairing Citizen Scientists with A.I. to Identify Individual Arms in Spiral Galaxies**

A Quarto + Reveal.js presentation for the North Carolina Astronomers' Meeting 2025.

## Authors

- **Alp Tezbasaran** - alptezbasaran@ncsu.edu
- **Dr. Patrick Treuthardt** - patrick.treuthardt@naturalsciences.org  
- **Ian Hewitt** - ihewitt@coastal.edu

## Project Structure

- `_quarto.yml` — Quarto project configuration with NCSU theme and reveal options
- `slides/index.qmd` — Main slide deck with presentation content
- `slides/theme/ncsu.scss` — Custom NCSU-themed stylesheet
- `assets/` — Images and logos (NCSU, NCMNS, Coastal Carolina)
- `Dockerfile` — Docker configuration for Quarto environment
- `compose.yaml` — Docker Compose setup
- `.gitignore` — Ignores build artifacts and generated files

## Running with Docker

This project includes Docker setup for consistent rendering across different environments.

### Prerequisites

- Docker and Docker Compose installed on your system

### Build and Run

1. **Start the Docker container:**
   ```bash
   docker compose up -d
   ```

2. **Render the slides:**
   ```bash
   docker compose exec slides bash -lc "quarto render slides/index.qmd"
   ```

3. **View the slides:**
   - Open `slides/index.html` in your browser
   - Or serve locally with: `docker compose exec slides bash -lc "quarto preview slides/index.qmd"`

### Alternative: Local Development

If you prefer to run Quarto locally:

1. Install Quarto: https://quarto.org/docs/get-started/
2. From the project root:
   ```bash
   quarto preview slides/index.qmd
   # or
   quarto render slides/index.qmd && open slides/index.html
   ```

## Customize

- Edit `slides/index.qmd` front matter (title, author, logo, etc.)
- Add or remove slides with `---` separators
- Tweak theme in `slides/theme/ncsu.scss`


