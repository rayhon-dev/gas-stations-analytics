# Gas Stations Analytics

## Loyiha haqida
5 ta zapravkaning tranzaksiya ma'lumotlari asosida to'liq EDA va bandlik darajasini 
bashorat qiluvchi ML model yaratildi.

## Bajarilgan ishlar
- To'liq EDA (5 ta filial): missing values, duplicates, outlier tahlili
- Data quality muammolarini aniqlash (amount hisoblash xatosi, sensor xatoliklari)
- Feature engineering: vaqt-asosli, lag feature'lar (1 kun/hafta oldingi bandlik)
- 6 ta model solishtirildi: CatBoost, Random Forest, XGBoost, LightGBM, 
  Gradient Boosting, Ridge Regression
- Hyperparameter tuning (GridSearchCV/RandomizedSearchCV)
- Baseline (7 kunlik o'rtacha) bilan solishtirish

## Natija
Eng yaxshi model: Random Forest (target_usul_2), Test R²=0.856, MAE=0.089

## Struktura
- notebooks/eda_file1.ipynb — to'liq EDA + modellashtirish (file1)
- notebooks/eda_file2-5.ipynb — EDA (qolgan filiallar)
- data/ — xom ma'lumotlar (.gitignore'da, maxfiylik sababli repo'da yo'q)

## Ishlatilgan texnologiyalar
Python, pandas, scikit-learn, CatBoost, XGBoost, LightGBM, matplotlib, seaborn


## Eslatma
Model training va hyperparameter tuning to'liq faqat file1 uchun bajarildi 
(metodologiyani chuqur sinash maqsadida). Xuddi shu pipeline file2'ga ham 
qisman qo'llanildi (natija past chiqdi - filiallar orasidagi farqni ko'rsatadi). 
Qolgan filiallar uchun EDA to'liq bajarilgan, model training esa loyihaning 
ushbu bosqichida ustuvor emas deb belgilandi.
