# Care Opinion – Web Scraping & Tokenization

A university NLP project where I scraped real patient stories from Care Opinion and compared different tokenization techniques on the extracted text.

---

## What I Did

**Step 1 – Web Scraping**  
I scraped 100 patient stories from [careopinion.org.uk](https://www.careopinion.org.uk) using BeautifulSoup and Requests. For each story I collected the title, date, story text, related service, and summary. Results were saved to a CSV file.

**Step 2 – Tokenization**  
I applied and compared three sentence tokenization methods on the extracted stories:
- `sent_tokenize` (NLTK)
- `PunktSentenceTokenizer` (NLTK)
- `RegexpTokenizer` (custom regex pattern)

---

## Files

| File | Description |
|---|---|
| `web_scraping.py` | Scrapes stories from Care Opinion |
| `Tokenization_Code.ipynb` | Applies and compares the three tokenizers |
| `care_opinion_data.csv` | Raw scraped data |
| `tokenization_result.csv` | Tokenization output for all three methods |
| `Comparison_Report.docx` | Analysis and comparison of the three techniques |

---

## Key Finding

`sent_tokenize` handled abbreviations and punctuation the best and was chosen for future work. The Regex tokenizer struggled with cases like "Dr." — splitting mid-sentence where it shouldn't.

---

## How to Run

```bash
pip install requests beautifulsoup4 lxml pandas nltk

# Step 1 - Scrape data
python web_scraping.py

# Step 2 - Run tokenization
jupyter notebook Tokenization_Code.ipynb
```

---

📅 University NLP Project — Abdalrhman Jehad
