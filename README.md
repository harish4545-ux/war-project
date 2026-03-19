<div align="center">
```
██╗    ██╗ █████╗ ██████╗     ███████╗███████╗███╗   ██╗████████╗██╗███╗   ███╗███████╗███╗   ██╗████████╗
██║    ██║██╔══██╗██╔══██╗    ██╔════╝██╔════╝████╗  ██║╚══██╔══╝██║████╗ ████║██╔════╝████╗  ██║╚══██╔══╝
██║ █╗ ██║███████║██████╔╝    ███████╗█████╗  ██╔██╗ ██║   ██║   ██║██╔████╔██║█████╗  ██╔██╗ ██║   ██║
██║███╗██║██╔══██║██╔══██╗    ╚════██║██╔══╝  ██║╚██╗██║   ██║   ██║██║╚██╔╝██║██╔══╝  ██║╚██╗██║   ██║
╚███╔███╔╝██║  ██║██║  ██║    ███████║███████╗██║ ╚████║   ██║   ██║██║ ╚═╝ ██║███████╗██║ ╚████║   ██║
 ╚══╝╚══╝ ╚═╝  ╚═╝╚═╝  ╚═╝   ╚══════╝╚══════╝╚═╝  ╚═══╝   ╚═╝   ╚═╝╚═╝     ╚═╝╚══════╝╚═╝  ╚═══╝   ╚═╝
```

#  War Social Media Sentiment Analysis
### *When the world tweets about war — what does it really feel?*

[![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org)
[![VADER](https://img.shields.io/badge/VADER-NLP%20Sentiment-FF6B35?style=for-the-badge&logo=python&logoColor=white)]()
[![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557C?style=for-the-badge&logo=python&logoColor=white)]()
[![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)]()

> **"In the digital age, every war is fought twice — once on the battlefield, once on social media."**
>
> This project decodes the emotional pulse of the world during active war conflicts using real Twitter data, NLP sentiment analysis, and data visualization.

</div>

---

##  What Is This Project?

When wars break out — Russia-Ukraine, Israel-Palestine — **millions of people take to Twitter** to express fear, anger, solidarity, and grief. But what does the *data* actually say?

This project answers:
-  Are people more **negative or positive** about war on social media?
-  Which **countries** are most vocal — and what sentiment do they carry?
-  **When** do people tweet the most? (Spoiler: it's 8–11 PM)
-  Do **emotional tweets** get more retweets than calm ones?
-  Which **hashtags** dominate the conversation?

---

##  Key Features

| Feature | Description |
|---|---|
|  **Smart Preprocessing** | Auto-detects CSV columns, cleans text, extracts hashtags, tags countries |
|  **VADER Sentiment Engine** | NLP model built for social media — handles slang, CAPS, emojis |
|  **8 Professional Charts** | Dark-themed, insight-annotated visualizations |
|  **3 Word Clouds** | All tweets / Positive only / Negative only |
|  **Country Comparison** | Sentiment breakdown across 12+ nations |
|  **Peak Hour Heatmap** | Discover when the world reacts to war news |
|  **Power BI Export** | Clean CSV output ready for interactive dashboards |
|  **Auto Sample Mode** | No dataset? It generates realistic demo data instantly |

---

## Output Gallery
```
sentiment_output/
├── 01_pie_sentiment.png          → Positive / Negative / Neutral split
├── 02_line_sentiment_time.png    → Sentiment trend over weeks
├── 03_bar_hashtags.png           → Top 20 most used hashtags
├── 04_wordcloud_all.png          → All tweets word cloud
├── 04_wordcloud_positive.png     → Positive tweets word cloud
├── 04_wordcloud_negative.png     → Negative tweets word cloud
├── 05_bar_country.png            → Country-wise sentiment comparison
├── 06_heatmap_hours.png          → Peak hour heatmap + line chart
├── 07_engagement_sentiment.png   → Retweets & likes by sentiment
├── 08_dashboard.png              → Full summary dashboard
└── war_sentiment_clean.csv       → Power BI ready export
```

---

##  How Sentiment Is Classified
```python
VADER Compound Score → Label

score >= +0.05   →    Positive
score <= -0.05   →    Negative
in between       →    Neutral
```

VADER understands social media language — it handles CAPS, punctuation, and emojis correctly, making it perfect for tweet analysis.

---

##  Key Insights Discovered
```
 Peak Hour     →  People tweet most between 8–11 PM
                    (Post-work news consumption cycle)

 Hashtag Split →  #Ukraine & #Russia equally trending
                    → Divided global attention

 Engagement    →  Negative/emotional tweets get 3–4×
                    more retweets than neutral ones

 Country Split →  Western nations → higher negative sentiment
                    Global South    → more neutral stance
```

---

##  Tech Stack
```
Language      →  Python 3.8+
NLP           →  vaderSentiment
Data          →  Pandas, NumPy
Visualization →  Matplotlib, Seaborn, WordCloud
Dashboard     →  Power BI (via CSV export)
Dataset       →  Kaggle (Twitter / War datasets)
```

---

##  Getting Started

### 1. Clone the repo
```bash
git clone https://github.com/harishkumarv/war-sentiment-analysis.git
cd war-sentiment-analysis
```

### 2. Create virtual environment
```bash
python -m venv .venv

# Windows
.\.venv\Scripts\Activate

# Mac/Linux
source .venv/bin/activate
```

### 3. Install dependencies
```bash
pip install pandas numpy matplotlib seaborn wordcloud vaderSentiment
```

### 4. Add your dataset *(optional)*
```
Place your Kaggle CSV in the project folder.

Recommended datasets:
→ "Ukraine Russia Crisis Twitter Dataset" — Kaggle
→ "Gaza Palestine Israel Tweets" — Kaggle

Then edit this line in the script:
CSV_FILE = 'your_dataset.csv'
```

### 5. Run
```bash
python "war sentiment analysis.py"
```

### 6. View outputs
```
Charts  →  sentiment_output/ folder
Power BI →  sentiment_output/war_sentiment_clean.csv
```

---

##  Project Structure
```
war-sentiment-analysis/
│
├── war sentiment analysis.py    # Main script
├── README.md                    # You are here
│
└── sentiment_output/            # Auto-generated on run
    ├── *.png                    # 8 visualization charts
    └── war_sentiment_clean.csv  # Power BI export
```

---

##  Countries Supported

`🇺🇦 Ukraine` · `🇷🇺 Russia` · `🇺🇸 USA` · `🇬🇧 UK` · `🇩🇪 Germany` · `🇫🇷 France` · `🇵🇱 Poland` · `🇮🇱 Israel` · `🇵🇸 Palestine` · `🇹🇷 Turkey` · `🇮🇳 India` · `🇦🇺 Australia`

---

##  Why This Project Matters

> The Russia-Ukraine war generated **over 200 million tweets** in the first month alone.
> The Israel-Palestine conflict trended globally for **weeks without interruption**.

Social media sentiment analysis helps researchers, journalists, and NGOs to understand public opinion shifts, detect misinformation spikes, and track emotional fatigue during prolonged conflicts.

---

##  Future Improvements

- [ ] Multilingual support (Arabic, Russian, Ukrainian tweets)
- [ ] Real-time Twitter API streaming with Tweepy
- [ ] BERT/RoBERTa model for higher accuracy
- [ ] Interactive web dashboard with Streamlit
- [ ] Geospatial map of tweet origins
- [ ] Bot detection to filter non-human accounts

---

##  Author

<div align="center">

### **Harish Kumar V**
*Data Analytics Enthusiast · NLP Explorer · Fresher*

[![GitHub](https://img.shields.io/badge/GitHub-harishkumarv-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/harishkumarv)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Harish%20Kumar%20V-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/harishkumarv)

> *"Built this project to understand how the world speaks during its darkest moments."*

</div>

---

##  License

MIT License — free to use, modify, and distribute.
If you found this useful, a  star would mean a lot!

---

<div align="center">

** Star this repo if you found it useful!**

*Made with  and lots of data by Harish Kumar V*

</div>

