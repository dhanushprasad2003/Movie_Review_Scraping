# Movie Review Webscraping Project

## Overview

This repository contains a Jupyter notebook **`scrap_movie_review.ipynb`** that:

1. **Scrapes audience reviews** from Rotten Tomatoes for a given movie.
2. **Saves** the raw review data to a CSV file.
3. **Loads** the CSV into a pandas DataFrame.
4. **Performs sentiment analysis** on each review using the HuggingFace model `cardiffnlp/twitter-roberta-base-sentiment-latest`.
5. **Outputs** a final CSV that includes the sentiment label for every review.

The notebook is fully self‑contained and walks you through each step with clear headings and code cells.

---

## Directory Structure

```
Movie_Review_webscraping_Project/
│   scrap_movie_review.ipynb   # Main notebook
│   README.md                  # <--- this file
└───data/                     # (optional) place to store CSVs
```

---

## Prerequisites

- **Python 3.12+** (the notebook was developed with Python 3.12).
- **pip** (for installing packages).
- An internet connection (to download the Rotten Tomatoes page and the HuggingFace model).

---

## Installation

Open a terminal in the project folder and run:

```bash
# Install required libraries (including tqdm & ipywidgets to silence warnings)
pip install -q requests transformers torch pandas tqdm ipywidgets
```

If you plan to run many requests or larger batches, consider setting a HuggingFace token to avoid rate‑limit warnings:

```bash
# Replace <YOUR_TOKEN> with your actual HF token
echo "HF_TOKEN=hf_<YOUR_TOKEN>" >> .env
```

---

## Usage

1. **Open the notebook** in Jupyter Lab / VS Code:
   ```bash
   jupyter notebook scrap_movie_review.ipynb
   ```
2. **Install dependencies** – run the first cell (the `!pip install …` line) if you haven’t already.
3. **Configure the scraper** – edit the `MOVIE_NAME` and `REVIEW_COUNT` variables in the *Run the Scraper* cell.
4. **Execute each cell sequentially**. The notebook prints progress information and saves:
   - `iron_man_audience_reviews.csv` (raw data)
   - `iron_man_reviews_with_sentiment.csv` (final data with sentiment)
5. **Explore the results** – the notebook includes cells to display a preview, sentiment distribution, and to save the final CSV.

---

## Troubleshooting

| Issue | Suggested Fix |
|-------|---------------|
| `TqdmWarning: IProgress not found` | Ensure `ipywidgets` is installed (included in the install command). |
| "Unauthenticated requests" warning from HuggingFace | Set `HF_TOKEN` as described above, then re‑run the model‑loading cell. |
| No reviews collected | Verify the movie slug matches the Rotten Tomatoes URL (e.g., `iron_man` → `https://www.rottentomatoes.com/m/iron_man`). |
| Kernel dies during sentiment analysis | Reduce `REVIEW_COUNT` or process reviews in batches. |

---

## 👤 Author

**Dhanush Prasad**  
[GitHub](https://github.com/dhanushprasad2003)

---

## 📄 License

This project is for educational purposes.
