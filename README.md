# 🚨 Klasifikasi Aspek & Emosi Respons Bencana (IndoBERT)

Proyek Pemrosesan Bahasa Alami (*Natural Language Processing*) untuk mengklasifikasikan **9 Aspek** dan **6 Kategori Emosi** secara simultan dari respons publik terhadap efektivitas penanganan pemerintah pada situasi krisis (Gempa Bumi M7.7 NTT & Karhutla Kalimantan).

## 🎯 Fokus Penelitian
Penelitian ini bertujuan untuk melampaui analisis sentimen biasa (positif/negatif) dengan memetakan secara presisi "apa yang dibahas" (Aspek) dan "bagaimana perasaannya" (Emosi) dari 2.890 korpus teks komentar X (Twitter) dan TikTok.

## 🛠️ Tech Stack & Metodologi
* **Bahasa:** Python
* **Deep Learning Framework:** PyTorch, Hugging Face Transformers
* **Pre-trained Language Model:** IndoBERT (Fine-Tuning)
* **Machine Learning Baselines:** SVM (TF-IDF), 1D-CNN, BiLSTM, Conv1D+BiLSTM
* **Hyperparameter Tuning:** Optuna (Tree-structured Parzen Estimator / TPE)

## 📈 Temuan & Hasil Utama
* **Evaluasi Model:** **IndoBERT** terbukti sebagai model paling superior dibandingkan arsitektur lainnya, mencapai **Macro-F1 0.359 (Aspek)** dan **Macro-F1 0.384 (Emosi)** dengan Akurasi Emosi sebesar **73.53%**.
* **Analisis Data Krisis (Batch Inference pada 2.890 Data):**
  * **Gempa NTT:** Didominasi oleh opini terkait *Korban dan Dampak Sosial* (Aspek 1) yang sangat berkorelasi dengan emosi *Sadness*.
  * **Karhutla Kalimantan:** Didominasi oleh kritik terhadap *Kebijakan dan Aspek Hukum* (Aspek 7) yang berkorelasi kuat dengan emosi *Anger*.
  * **Mayoritas Absolut:** Aspek *Penanganan dan Respons Pemerintah* (Aspek 5) menjadi topik yang paling disorot secara keseluruhan.
