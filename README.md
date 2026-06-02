# Dünya CO2 ve Sera Gazı Emisyonları — Veri Analizi

**Hazırlayan:** Mehmet Emir Örer  
**Öğrenci No:** 24LITT039  
**Ders:** Veri Analizinde Bilgisayar Programlama 2

📊 **Canlı rapor:** https://KULLANICI_ADIN.github.io/sera-gazi-analizi/

> ⚠️ `KULLANICI_ADIN` kısmını kendi GitHub kullanıcı adınla değiştir.

## Ne yaptım?

Our World in Data tarafından derlenen CO2 ve sera gazı emisyonu veri setini Python ile analiz ettim. 30 büyük ülkenin 1990-2021 arasındaki emisyon verilerini inceledim, görselleştirdim ve yorumladım.

Raporda şunlar var:
- 4 tanımsal istatistik (`describe`, `groupby`, `corr`, `nlargest`)
- 5 farklı grafik tipi (histogram, boxplot, scatter, bar, heatmap)
- Her grafiğin altında yorum
- Sonuç bölümünde 5 bulgu

## Bilgisayara hiçbir şey kurmadan çalıştırmak (Google Colab)

Bilgisayarına Python, pandas, jupyter falan kurmana gerek yok. Google Colab tamamen tarayıcıda çalışıyor ve her şey önceden hazır.

1. https://colab.research.google.com adresine git, Google hesabınla giriş yap.
2. **File → Upload notebook** → bilgisayarındaki `notebook/rapor.ipynb` dosyasını yükle.
3. Sol taraftaki **dosya simgesine** (klasör ikonu) tıkla → **upload** butonuyla `data/owid-co2-data-sample.csv` dosyasını yükle.
4. Notebook'ta CSV okuma satırını şu şekilde değiştir:
   ```python
   df = pd.read_csv("owid-co2-data-sample.csv")
   ```
   (yani `../data/` kısmını sil, sadece dosya adı kalsın)
5. Üst menüden **Runtime → Run all** ile bütün hücreleri çalıştır.

İşte hepsi bu. Hiçbir paket kurmana gerek yok, hepsi Google'ın sunucularında çalışıyor.

## Klasör Yapısı

```
sera-gazi-analizi/
├── data/
│   └── owid-co2-data-sample.csv   ← veri seti
├── notebook/
│   └── rapor.ipynb                ← analiz notebook'u (çıktılar gömülü)
├── docs/
│   └── index.html                 ← GitHub Pages bunu yayınlıyor
├── .gitignore
└── README.md
```

> 💡 `notebook/rapor.ipynb` dosyasını **hiç çalıştırmadan da** açtığında tüm grafikleri ve çıktıları görebilirsin — çünkü içine gömülü.

## GitHub'a yükleme adımları

1. GitHub'a gir, sağ üstten **+ → New repository**.
2. Repo adı: `sera-gazi-analizi`, **Public** seç, README/.gitignore ekleme.
3. Bilgisayarında bu klasörün içinde terminal aç:
   ```bash
   git init
   git add .
   git commit -m "ilk versiyon: veri analizi raporu"
   git branch -M main
   git remote add origin https://github.com/KULLANICI_ADIN/sera-gazi-analizi.git
   git push -u origin main
   ```

## GitHub Pages'i açma

1. Repo'ya gir → **Settings** sekmesi
2. Sol menüden **Pages**
3. **Source:** Deploy from a branch
4. **Branch:** `main` / **Folder:** `/docs`
5. **Save**

2-3 dakika içinde `https://KULLANICI_ADIN.github.io/sera-gazi-analizi/` adresinde rapor yayında olacak.

## Veri Kaynağı

[Global CO2 and Greenhouse Gas Emissions](https://www.kaggle.com/datasets/mexwell/global-co2-and-greenhouse-gas-emissions) — Our World in Data (Kaggle).
