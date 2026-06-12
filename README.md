#  Kentsel Emisyon Sistemi (Green-Audit)

Mevcut şehir kameralarını, çevre sensörlerini ve NASA uydu görüntülerini yapay zeka ile eşzamanlı işleyerek kentsel alanlardaki çevre suçlarını ve özellikle gizlice yapılan kaçak moloz/hafriyat dökümlerini anlık tespit eden otonom kentsel takip platformu.

Bu proje, geleneksel denetim mekanizmalarının ve kameraların yetersiz kaldığı kör noktalarda bile uydu teknolojilerini ve bilgisayarlı görüyü birleştirerek yasadışı dökümleri engellemeyi amaçlar.

---

## Projenin Amacı ve Çözdüğü Problem

Modern şehirlerde kaçak moloz ve hafriyat dökümleri genellikle denetimin az olduğu kırsal alanlarda, orman sınırlarında veya kameraların görmediği kör noktalarda gizlice gerçekleştirilmektedir. 

**Green-Audit**, bu problemi çözmek için çok katmanlı bir hibrit ağ kurar:
1. **Anlık Takip:** Şehir kameralarından gelen canlı yayınlar üzerinden yasadışı döküm yapmaya çalışan araçları ve şüpheli hareketleri bilgisayarlı görüyle saptar.
2. **Emisyon Analizi:** Çevreye yerleştirilen sensör verileriyle hava kalitesindeki ani değişimleri ve kaçak emisyon odaklarını yakalar.
3. **Kör Nokta Denetimi (NASA):** Kameraların tamamen dışında kalan gizli bölgelerdeki topoğrafik değişimleri ve kaçak dolgu alanlarını **NASA uydu görüntüleri** ve zaman serisi analizleriyle otonom olarak tespit eder.

---

##  Teknolojik Mimari ve Stack

Proje, farklı veri kaynaklarını tek bir yapay zeka analitiği altında toplayan hibrit bir boru hattına (pipeline) sahiptir.

| Katman | Kullanılan Teknolojiler / Kütüphaneler |
|---|---|
| **Yapısal Programlama & Veri İşleme** | Python, Pandas, NumPy |
| **Bilgisayarlı Görü (Computer Vision)** | OpenCV |
| **Makine Öğrenmesi & Analitik** | Scikit-learn |
| **Veri Entegrasyonu** | NASA Uydu Veri Havuzları, Çevre Sensör Metrikleri, Kamera Yayın Akışları |
| **Geliştirme Ortamı** | Google Colab / Jupyter Notebook |

---

##  Dosya Yapısı

* `KentselEmisyonDemo02_1.ipynb`: Çoklu veri kaynaklarını (Kamera + Sensör + Uydu) işleyen, anomalileri saptayan ve platform arayüzünü çalıştıran ana notebook dosyası.
* `README.md`: Proje ana dokümantasyonu.

---

##  Nasıl Çalıştırılır?

Sistemi test etmek ve analiz süreçlerini incelemek için aşağıdaki adımları takip edebilirsiniz:

1. Depoda bulunan `KentselEmisyonDemo02_1.ipynb` dosyasını indirin veya doğrudan Google Colab üzerinde açın.
2. Gerekli bağımlılıkların ortamınızda yüklü olduğundan emin olun:
   ```bash
   pip install opencv-python scikit-learn pandas numpy
