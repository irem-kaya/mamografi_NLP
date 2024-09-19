# Mamografi Radyoloji Raporlarından Varlık İsmi Çıkarımı ve BIRADS Kategori Tahmini

Bu proje, mamografi radyoloji raporlarından varlık ismi çıkarımı (VİÇ) ve BIRADS (Breast Imaging-Reporting and Data System) kategori tahmini yapmayı hedeflemektedir. Proje kapsamında iki temel görev gerçekleştirilmiştir: birincisi BIRADS kategori tahmini, ikincisi ise varlık ismi çıkarımıdır.

## Proje İçeriği

- **BIRADS Kategori Tahmini**: BIRADS kategorilerinin tahmini için BERT modeli kullanılmıştır.
  - BIRADS-1 sınıfı için veri dengesizliği olduğu tespit edilmiş ve artırma (augmentation) yöntemleri uygulanarak denge sağlanmıştır.
  - Model eğitimi sonrasında test işlemi gerçekleştirilmiş ve sonuçlar `precision`, `recall`, `f1-score` ve `accuracy` metrikleri ile değerlendirilmiştir.
  
- **Varlık İsmi Çıkarımı (VİÇ)**: Varlık ismi çıkarımı işlemi için Spacy kütüphanesi kullanılmıştır.
  - Modelin performansı `F1-score`, `precision` ve `recall` metrikleri ile değerlendirilmiştir.
  - Çıktı dosyası, yarışma için istenilen JSON formatında sunulmuştur.

## Proje Yapısı

Proje aşağıdaki ana klasör ve dosyalardan oluşmaktadır:

- `Birads-viç/`
  - **ikinciAsama**: Jupyter Notebook kaynaklı dosyalar ve proje boyunca gerçekleştirilen tüm aşamaları içerir.
  - **NLPdemo**: İkinci aşama için yapılan deneme kodlarını içerir.
  - **öznitelik**: Projede kullanılan öznitelik çıkartma işlemlerine ait kodları içerir.
  - **VİÇ**: Varlık ismi çıkarımı için yapılan deneme kodlarını içerir.
  
## Kullanılan Modeller ve Teknolojiler

### BIRADS Kategori Tahmini
- **Model**: BERT (Bidirectional Encoder Representations from Transformers)
- **Veri Artırma**: BIRADS 1 için veri dengesizliğini gidermek amacıyla veri artırma (data augmentation) teknikleri kullanılmıştır.
- **Metrikler**: Precision, Recall, F1-Score, Accuracy

### Varlık İsmi Çıkarımı (VİÇ)
- **Model**: Spacy NER (Named Entity Recognition)
- **Metrikler**: Precision, Recall, F1-Score

## Kurulum

Bu projeyi kendi bilgisayarınızda çalıştırmak için aşağıdaki adımları izleyebilirsiniz.

1. **Python Gereksinimleri**: Proje, Python 3.x ile uyumludur. Gerekli kütüphaneleri yüklemek için aşağıdaki komutu çalıştırın:
   ```bash
   pip install -r requirements.txt
