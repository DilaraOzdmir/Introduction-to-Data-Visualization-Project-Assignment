## Öğrenci Bilgileri

Ad Soyad: Dilara Özdemir  
Okul Numarası: 230205074  
Ders: Veri Görselleştirmeye Giriş


# AI Asistan - Metin İşleme Uygulaması

Bu proje, Ollama API üzerinden çalışan bir yapay zeka destekli metin işleme uygulamasıdır. Kullanıcı seçtiği bir metni F8 kısayolu ile yapay zekaya gönderebilir ve farklı işlemler uygulayabilir.

## Yapılan Geliştirmeler

Bu projede mevcut yapı bozulmadan yeni eğitim odaklı özellikler eklenmiştir.

Eklenen yeni özellikler:

- Kısa Anlat
- Örnekle Anlat
- Mini Quiz Oluştur
- Soru Üret
- Basitleştir

Ayrıca bu uzun eğitim çıktılarının seçili metnin üzerine yazılması yerine yeni bir `.txt` dosyasında açılması sağlanmıştır.

## Eklenen Özelliklerin Açıklaması

### Kısa Anlat
Seçilen konuyu kısa, sade ve öğrenci seviyesinde açıklar.

### Örnekle Anlat
Seçilen konuyu örneklerle daha detaylı açıklar.

### Mini Quiz Oluştur
Seçilen konu hakkında 5 soruluk mini quiz oluşturur ve cevap anahtarını verir.

### Soru Üret
Seçilen metinden kolay, orta veya zor seviyede sorular üretir.

### Basitleştir
Seçilen metni daha anlaşılır ve öğrenci seviyesine uygun şekilde sadeleştirir.

## TXT Dosyasında Açma Özelliği

Eğitim odaklı uzun cevaplar artık doğrudan seçili metnin yerine yazılmaz. Bunun yerine:

1. `ai_sonuclar` adlı klasör oluşturulur.
2. Yapay zeka cevabı `.txt` dosyasına kaydedilir.
3. Oluşturulan dosya otomatik olarak açılır.

Bu sayede kullanıcı orijinal metni kaybetmeden AI çıktısını ayrı bir dosyada saklayabilir.

## Kullanım

1. Ollama çalışır durumda olmalıdır.
2. Proje klasöründe `BASLAT.bat` dosyası çalıştırılır.
3. İşlem yapılacak metin seçilir.
4. F8 tuşuna basılır.
5. Açılan menüden istenen işlem seçilir.

## Kullanılan Teknolojiler

- Python
- Ollama API
- Tkinter
- PyAutoGUI
- Pyperclip
- Pynput

## Akış Şeması

```mermaid
flowchart TD

A[Program Başlatılır] --> B[Ollama Bağlantısı Kontrol Edilir]

B --> C[Kullanıcı Metin Seçer]

C --> D[F8 Tuşuna Basar]

D --> E[İşlem Menüsü Açılır]

E --> F{İşlem Türü Seçilir}

F --> G[Kısa Anlat]
F --> H[Örnekle Anlat]
F --> I[Mini Quiz]
F --> J[Soru Üret]
F --> K[Basitleştir]

G --> L[Prompt Oluştur]
H --> L
I --> L
J --> L
K --> L

L --> M[Ollama API]

M --> N[AI Sonucu Alınır]

N --> O[TXT Dosyasına Kaydedilir]

O --> P[TXT Dosyası Açılır]
```

## Örnek Çalışma

Aşağıda uygulamanın çalışma örneği gösterilmektedir:

![Örnek Çalışma](ornek_calisma.png)<img width="1919" height="1138" alt="ornek_calisma" src="https://github.com/user-attachments/assets/344300a0-999e-44d8-bf7d-32afbfed882a" />
