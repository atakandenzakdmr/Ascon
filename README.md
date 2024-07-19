# Ascon

Ascon, kullanıcıların günlük beslenme, uyku ve sağlık verilerini kaydetmelerini ve takip etmelerini sağlayan bir mobil uygulamadır. Uygulama, kullanıcıların sağlıklı yaşam alışkanlıkları geliştirmelerine yardımcı olmayı amaçlamaktadır. Bu proje, Flutter ve Dart kullanılarak geliştirilmiştir ve MVVM (Model-View-ViewModel) mimarisi uygulanmıştır.

## Proje Amacı

Ascon uygulaması, kullanıcıların:
- Günlük besin tüketimlerini kaydetmelerini,
- Yiyeceklerin besin değerlerini hesaplamalarını,
- Uyku saatlerini takip etmelerini,
- Sağlık verilerini düzenli olarak girmelerini ve analiz etmelerini sağlar.

Bu sayede, kullanıcıların sağlık ve beslenme alışkanlıklarını daha iyi yönetmelerine yardımcı olur.

## Kullanılan Mimariler

### MVVM (Model-View-ViewModel)

- **Model:** Uygulamanın veri yapıları ve iş mantığını temsil eder. Veriler ve bu verilere yönelik işlemler burada tanımlanır.
- **View:** Kullanıcı arayüzü bileşenlerini temsil eder. Ekranlar ve widget'lar burada tanımlanır.
- **ViewModel:** Uygulamanın iş mantığını ve veri akışını kontrol eder. Kullanıcı arayüzü ile veri modelleri arasında bağlayıcı rol oynar.

### Clean Code Prensipleri

Proje, kodun okunabilirliğini, bakımını ve sürdürülebilirliğini artırmak amacıyla Clean Code prensiplerine uygun olarak organize edilmiştir.

## Dosya Yapısı

```plaintext
ascon_app/
│
├── android/                # Android platforma özgü dosyalar
│
├── ios/                    # iOS platforma özgü dosyalar
│
├── lib/                    # Uygulama kaynak kodları
│   ├── main.dart           # Uygulamanın giriş noktası
│   ├── src/                # Tüm kaynak kodları içeren ana klasör
│       ├── core/           # Çekirdek bileşenler ve genel kullanım dosyaları
│       │   ├── constants/  # Sabitler ve genel ayarlar
│       │   ├── utils/      # Yardımcı fonksiyonlar ve araçlar
│       │   ├── widgets/    # Ortak kullanılan widget'lar
│       │   ├── theme/      # Tema ve stil dosyaları
│       │
│       ├── data/           # Veri kaynakları ve modeller
│       │   ├── models/     # Veri modelleri
│       │   ├── providers/  # State management dosyaları
│       │   ├── repositories/ # Veri erişim katmanı
│       │
│       ├── ui/             # Kullanıcı arayüzü bileşenleri
│       │   ├── screens/    # Ekranlar ve sayfalar
│       │   ├── components/ # Ekran bileşenleri ve parçaları
│       │
│       ├── services/       # Servisler ve iş mantığı
│
├── assets/                 # Statik varlıklar (görseller, animasyonlar vb.)
│   ├── animations/
│   │   ├── splash_animation.json
│   │   ├── another_animation.riv
│   │
│   ├── images/
│       ├── logo.png
│       ├── example_food.jpg
│
├── pubspec.yaml            # Proje bağımlılıkları ve varlık tanımlamaları
│
├── README.md               # Proje hakkında bilgi
│
├── test/                   # Test dosyaları
│   ├── widget_test.dart
