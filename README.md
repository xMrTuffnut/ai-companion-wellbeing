# AI Companions and Psychological Well-being

Group project: How is interaction with AI companions related to users' psychological well-being?

**Dataset:** [SALT-NLP/AI-companionship-well-being](https://github.com/SALT-NLP/AI-companionship-well-being) (`data.csv`, 1,131 participants, 14 variables)

## Who does what

| Notebook | Topic | Owner |
|---|---|---|
| `notebooks/01_cleaning.ipynb` | Preprocessing, creates `data/clean.csv` | Claas |
| `notebooks/02_rq1_companion_vs_others.ipynb` | RQ1: companion users vs. others (t-test) | Person B |
| `notebooks/03_rq2_intensity.ipynb` | RQ2: use intensity and well-being (correlation) | Person C |
| `notebooks/04_rq3_disclosure_network.ipynb` | RQ3: self-disclosure, social network (regression) | Person D |
| `notebooks/05_final.ipynb` | Final results for the presentation | Everyone, at the end |

## How we work

1. Open your notebook in Google Colab: *File → Open notebook → GitHub tab* → paste this repo's URL. Or if you are working with VS Code etc. the usual way.
2. Only edit **your own** notebook. Questions about someone else's: message them.
3. Before saving: *Runtime → Restart and run all* (must run top to bottom without errors).
4. Save: *File → Save a copy in GitHub* → this repo, same file path, short commit message.
5. Figures: `save_fig("name.png")` downloads the image; upload it to `figures/` (*Add file → Upload files*).
6. Never edit data by hand. All changes happen in `01_cleaning`.

## Folders

- `data/` – cleaned data (`clean.csv`)
- `notebooks/` – one notebook per person
- `figures/` – exported plots for the slides

## Notes on the data

- `intensity`, `self_disclosure`, `social_network_scale`, `tenure_of_activity` are already standardized (mean 0, SD 1).
- `well_being` is on a 1–7 scale.
- `companionship_chat` only exists for the 237 participants who donated chat logs.
- Only 134 participants use the chatbot primarily as a companion (`companionship_prim = 1`), so use Welch's t-test.
- Cross-sectional survey: results show associations, not causes.
