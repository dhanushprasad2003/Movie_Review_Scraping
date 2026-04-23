# 🎬 Movie Review Sentiment Analysis (Rotten Tomatoes)

## 📌 Project Overview

This project scrapes audience reviews for a given movie from Rotten Tomatoes and performs sentiment analysis using a pre-trained NLP model. The final output includes structured review data along with sentiment labels (positive, neutral, negative).

---

## 🚀 Features

* Scrapes **audience reviews** dynamically using Rotten Tomatoes API
* Handles pagination to collect large volumes of reviews
* Cleans and structures review data
* Performs **sentiment analysis** using a transformer-based model
* Exports results into CSV files for further analysis

---

## 🛠️ Tech Stack

* **Python**
* **Requests** – API calls
* **Pandas** – Data manipulation
* **Transformers (Hugging Face)** – Sentiment analysis model
* **CSV** – Data storage

---

## 📂 Project Structure

```
├── scraper.py                  # Main scraping script
├── sentiment_analysis.py       # Sentiment analysis logic
├── iron_man_audience_reviews.csv
├── iron_man_reviews_with_sentiment.csv
├── README.md
```

---

## ⚙️ Installation

1. Clone the repository:

```bash
git clone https://github.com/your-username/movie-review-sentiment.git
cd movie-review-sentiment
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

---

## ▶️ Usage

1. Set the movie name and number of reviews:

```python
MOVIE_NAME = "iron_man"
REVIEW_COUNT = 200
```

2. Run the script:

```bash
python scraper.py
```

3. Output files:

* `iron_man_audience_reviews.csv`
* `iron_man_reviews_with_sentiment.csv`

---

## 📊 Output Example

| display_name | rating | review_text    | sentiment |
| ------------ | ------ | -------------- | --------- |
| John D       | STAR_5 | Amazing movie! | positive  |
| Alex P       | STAR_3 | It was okay    | neutral   |
| Sam K        | STAR_1 | Didn't like it | negative  |

---

## 📈 Sentiment Results (Example)

* **Positive:** 82%
* **Neutral:** 11.5%
* **Negative:** 6.5%

---

## 🧠 Model Used

* `cardiffnlp/twitter-roberta-base-sentiment-latest`

This model is fine-tuned for sentiment classification and performs well on short text such as reviews.

---

## ⚠️ Notes

* Reviews are limited by API pagination
* Some reviews may be empty or missing user details
* Rate limiting is handled using delays between requests

---

## 🔮 Future Improvements

* Add visualization (charts/dashboard)
* Support multiple movies in one run
* Deploy as a web app
* Add advanced NLP (topic modeling, keyword extraction)

---

## 🤝 Contributing

Contributions are welcome! Feel free to fork the repo and submit a pull request.

---

## 📜 License

This project is open-source and available under the MIT License.

---

## 👨‍💻 Author

**Your Name**
GitHub: https://github.com/dhanushprasad2003
