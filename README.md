# KGM Avrupa Otoyolu (Mahmutbey - Edirne Kesimi) Geçiş Ücretleri Hesaplama

Bu proje, Karayolları Genel Müdürlüğü'nün (KGM) Avrupa Otoyolu'nun Mahmutbey ile Edirne arasındaki geçiş ücretlerini hesaplayan bir Python programını içerir. Bu program, istasyonlar arasında geçiş ücretlerini otomatik olarak hesaplamak için belirli bir ücret tablosunu kullanır.

## İçerik

- [Genel Bilgi](#genel-bilgi)
- [Kurulum](#kurulum)
- [Kullanım](#kullanım)
- [Katkıda Bulunma](#katkıda-bulunma)
- [Lisans](#lisans)

## Genel Bilgi

Bu uygulama, Avrupa Otoyolu'ndaki 18 farklı istasyon arasında geçiş ücretlerini hesaplamak için `numpy` kütüphanesini kullanır. Ücret tablosu, her istasyon çifti için sınıf bazlı ücretleri içermektedir. Kullanıcılar, belirli iki istasyon arasında bir geçiş ücreti hesaplayabilir ve ücret bilgilerini görüntüleyebilirler.

## Kurulum

Projeyi klonladıktan sonra, gerekli Python kütüphanelerini yüklemek için aşağıdaki adımları izleyin:

```bash
git clone https://github.com/kullaniciadi/kgm-avrupa-otoyolu-gecis-ucretleri.git
cd kgm-avrupa-otoyolu-gecis-ucretleri
pip install -r requirements.txt
```

## Kullanım
Aşağıdaki gibi iki istasyon arasındaki geçiş ücretini hesaplayabilirsiniz:

```
import numpy as np

istasyonlar = [
    "MAHMUTBEY", "ISPARTAKULE", "AVCILAR", "ESENYURT", "HADIMKÖY", 
    "ÇATALCA", "K.BURGAZ", "SELİMPAŞA", "SİLİVRİ", "KINALI", 
    "KÜÇÜKKILIÇLI", "ÇERKEZKÖY", "ÇORLU", "SARAY", "LÜLEBURGAZ", 
    "BABAESKİ", "HAVSA", "EDİRNE"
]

ucretler = {
    1: np.array([...])  # Ücret tablosu burada tanımlıdır
}

guzergah_1 = ucretler[1][11][17]  # ÇERKEZKÖY'den EDİRNE'ye
guzergah_2 = ucretler[1][17][11]  # EDİRNE'den ÇERKEZKÖY'e

print(guzergah_1)
print(guzergah_2)
```

## Katkıda Bulunma
Katkıda bulunmak isterseniz, lütfen bir pull request gönderin veya bir issue açın. Geri bildirimleriniz bizim için değerlidir!

## Lisans
Bu proje MIT Lisansı altında lisanslanmıştır. Daha fazla bilgi için LICENSE dosyasına bakın.
