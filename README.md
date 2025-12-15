# Genetik Algoritma ile Optimizasyon  
## Senaryo 2 – Endüstriyel Boya Karışımı

Bu projede, iki farklı pigment kullanılarak elde edilen boya karışımının
renk kalitesini maksimize etmek amacıyla Genetik Algoritma uygulanmıştır.

Çalışma, yapay zeka dersi proje ödevi kapsamında bireysel olarak gerçekleştirilmiştir.

---

## Problem Tanımı

Bir fabrikada iki pigment karıştırılarak ideal renk yoğunluğu elde edilmek istenmektedir.

Amaç fonksiyonu:

y = 5x1 + 2x2 - x1*x2

Burada:
- x1: Pigment A oranı (%)
- x2: Pigment B oranı (%)

---

## Kısıtlar

- x1 + x2 = 100  
- x1 ≥ 30  
- x1 ve x2 değerleri 0 ile 100 arasındadır

---

## Kısıtların Ele Alınışı

Toplam karışımın %100 olması gerektiği için:

x2 = 100 - x1

şeklinde bir dönüşüm yapılmıştır.

Bu sayede problem tek değişkenli hale getirilmiş ve
Genetik Algoritma yalnızca x1 değişkeni üzerinden uygulanmıştır.

Arama aralığı:
- [30, 100]

---

## Genetik Algoritma Yaklaşımı

Projede kullanılan genetik algoritma şu adımlardan oluşmaktadır:

1. Rastgele x1 değerlerinden oluşan başlangıç popülasyonu oluşturulmuştur.
2. Her birey için kalite puanı (fitness) hesaplanmıştır.
3. Popülasyon kalite puanına göre sıralanmıştır.
4. En iyi bireyler elitizm yöntemiyle korunmuştur.
5. Yeni bireyler, çaprazlama (ortalama alma) yöntemiyle üretilmiştir.
6. Küçük rastgele değişimler (mutasyon) uygulanmıştır.
7. Bu işlemler belirli sayıda nesil boyunca tekrar edilmiştir.

---

## Kullanılan Parametreler

- Popülasyon boyutu: 30  
- Nesil sayısı: 100  
- Elit birey sayısı: 5  
- Mutasyon oranı: 0.1  
- Çaprazlama yöntemi: İki ebeveynin ortalaması  
- Kromozom yapısı: Tek değişken (x1)

---

## Elde Edilen Sonuç

Genetik algoritma çalıştırıldıktan sonra elde edilen en iyi çözüm:

- x1 = 100  
- x2 = 0  

Bu durumda amaç fonksiyonu değeri:

y = 5*100 + 2*0 - (100*0) = 500

olarak hesaplanmıştır.

---