# **Mamografi Radyoloji Raporlarından Varlık İsmi Çıkarımı ve BIRADS Kategori Tahmini**

Bu proje, mamografi radyoloji raporlarından varlık ismi çıkarımı (VİÇ) ve BIRADS (Breast Imaging-Reporting and Data System) kategori tahmini yapmayı hedeflemektedir. Proje kapsamında iki ana görev gerçekleştirilmiştir: birincisi BIRADS kategori tahmini, ikincisi ise varlık ismi çıkarımıdır (NER - Named Entity Recognition).

## **Proje İçeriği**

### **1. BIRADS Kategori Tahmini**
- BIRADS kategorilerinin tahmini için **BERT** (Bidirectional Encoder Representations from Transformers) modeli kullanılmıştır.
- BIRADS-1 sınıfı için veri dengesizliği tespit edilmiştir. Bu dengesizlik, **veri artırma (augmentation)** teknikleri ile giderilmiştir.
- Modelin eğitimi sonrası test işlemi gerçekleştirilmiş ve sonuçlar, aşağıdaki metriklerle değerlendirilmiştir:
  - **Precision**
  - **Recall**
  - **F1-Score**
  - **Accuracy**

### **2. Varlık İsmi Çıkarımı (VİÇ)**
- Varlık ismi çıkarımı işlemi için **SpaCy** kütüphanesinin Named Entity Recognition (NER) modeli kullanılmıştır.
- Modelin performansı aşağıdaki metriklerle değerlendirilmiştir:
  - **Precision**
  - **Recall**
  - **F1-Score**
- Çıktılar, yarışma gereksinimlerine uygun olarak **JSON formatında** hazırlanmıştır.

---

## **Proje Yapısı**

Proje aşağıdaki klasör ve dosyaları içerir:

- `Birads-viç/`
  - **ikinciAsama**: Jupyter Notebook dosyaları ve proje süresince gerçekleştirilen tüm aşamaları içerir.
  - **NLPdemo**: İkinci aşama için yapılan deneysel deneme kodlarını içerir.
  - **öznitelik**: Projede kullanılan öznitelik çıkarma işlemleri için geliştirilmiş kodları içerir.
  - **VİÇ**: Varlık ismi çıkarımı (NER) için yapılan deneme kodlarını içerir.

---

## **Kullanılan Modeller ve Teknolojiler**

### **BIRADS Kategori Tahmini**
- **Model**: BERT (Transformer tabanlı bir dil modeli)
- **Veri Artırma**: BIRADS-1 için veri dengesizliğini gidermek amacıyla veri artırma (data augmentation) yöntemleri kullanılmıştır.
- **Değerlendirme Metrikleri**:
  - Precision
  - Recall
  - F1-Score
  - Accuracy

### **Varlık İsmi Çıkarımı (VİÇ)**
- **Model**: SpaCy NER (Named Entity Recognition)
- **Değerlendirme Metrikleri**:
  - Precision
  - Recall
  - F1-Score

---

## **Kurulum Talimatları**

Projenin yerel bir bilgisayarda çalıştırılması için aşağıdaki adımları izleyebilirsiniz:

1. **Python Gereksinimleri**: Bu proje Python 3.x sürümü ile uyumludur. Gerekli bağımlılıkları yüklemek için proje klasöründe aşağıdaki komutu çalıştırın:
   ```bash
   pip install -r requirements.txt
