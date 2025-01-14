
# **YouTube Comment Summarization Plugin**

This project is a Python-based tool that scrapes YouTube comments from a given video, categorizes them into meaningful themes, and generates constructive summaries using LangChain. The tool can be extended into a plugin or web application.

---

## **Features**
- Scrape YouTube comments using the YouTube Data API.
- Categorize comments into themes (e.g., sentiment, relevance, or topics).
- Generate summaries for each category using LangChain's summarization techniques.
- Provide an easy-to-use interface for users to input YouTube video URLs.

---

## **Technologies Used**
- **Python**: Core programming language.
- **YouTube Data API**: For fetching comments from YouTube videos.
- **LangChain**: For text classification and summarization.
- **Hugging Face Transformers**: For text classification models.
- **Streamlit/Flask**: Optional frontend for user interaction.

---

## **Folder Structure**

```
youtube-summarization-plugin/
│
├── main.py                  # Main script to run the backend logic
├── app.py                   # Frontend application (e.g., Streamlit or Flask)
├── requirements.txt         # List of dependencies
├── .env                     # Environment variables (e.g., API keys)
│
├── data/                    # Directory for storing scraped data and outputs
│   ├── raw_comments.csv     # Raw scraped comments from YouTube
│   ├── categorized.json     # Categorized comments (JSON format)
│   └── summaries.txt        # Final generated summaries
│
├── src/                     # Source code directory for modular components
│   ├── scraper.py           # Script for scraping YouTube comments
│   ├── categorizer.py       # Script for categorizing comments
│   ├── summarizer.py        # Script for summarizing categorized comments
│   └── utils.py             # Utility functions (e.g., text processing)
│
├── models/                  # Pre-trained or fine-tuned models (if needed)
│   └── custom_model/        # Directory to store custom Hugging Face models
│
├── tests/                   # Unit tests for each module
│   ├── test_scraper.py      # Tests for scraper module
│   ├── test_categorizer.py  # Tests for categorizer module
│   └── test_summarizer.py   # Tests for summarizer module
│
└── README.md                # Project documentation (this file)
```

---

## **How It Works**

### **1. Scraping Comments**
The `scraper.py` module uses the YouTube Data API to fetch comments from a given video ID. Comments are saved in `data/raw_comments.csv`.

### **2. Categorizing Comments**
The `categorizer.py` module uses Hugging Face Transformers or LangChain's classification tools to categorize comments into themes like sentiment or relevance. Results are saved in `data/categorized.json`.

### **3. Summarizing Comments**
The `summarizer.py` module uses LangChain's map-reduce or iterative refinement techniques to generate summaries for each category. Final summaries are saved in `data/summaries.txt`.

### **4. Frontend Interface**
The optional frontend (`app.py`) provides an easy way for users to input video URLs and view results interactively.

---

## **Future Enhancements**
- Fine-tune custom models for domain-specific categorization.
- Deploy as a browser extension or web app.
