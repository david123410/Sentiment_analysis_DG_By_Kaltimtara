# Sentiment Analysis - DG by Bankaltimtara

Project pribadi buat belajar NLP/sentiment analysis, pakai data review aplikasi mobile banking **DG by Bankaltimtara** dari Google Play Store.

Tujuannya nyoba klasifikasi review jadi positif/negatif, sekaligus lihat masalah apa aja yang paling sering dikeluhkan user.

> Data yang dipakai adalah review publik dari Play Store. Ini project belajar pribadi, bukan analisis/laporan resmi dari Bankaltimtara.

## Apa yang dilakukan

- Scraping review dari Google Play Store
- Cleaning data & bikin label sentiment dari rating
- Sempat coba 3 kelas (positif/netral/negatif), tapi kelas netral ternyata labelnya tidak akurat (banyak review rating 3 bintang isinya komplain jelas) jadi dibuat hanya negatif dan positif
- Coba 2 cara representasi teks: TF-IDF vs Sentence Transformer, terus dibandingkan
- Modeling pakai Logistic Regression, Random Forest, XGBoost + hyperparameter tuning
- Word cloud & kategorisasi masalah yang paling sering muncul di review negatif

## Hasil

Model terbaik: **TF-IDF + Logistic Regression**, accuracy ~88%, macro F1 ~0.87

## Cara jalanin

```bash
pip install -r requirements.txt
jupyter notebook notebook/sentiment_analysis.ipynb
```

Run cell dari atas ke bawah.

## Tools yang dipakai

pandas, scikit-learn, sentence-transformers, xgboost, google-play-scraper, wordcloud, matplotlib, seaborn
