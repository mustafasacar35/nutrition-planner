# 🍽️ Nutrition Planner - Beslenme Planlayıcısı

Akıllı beslenme planlama sistemi. Genetik algoritma ve çoklu optimizasyon kriterleri ile kişiselleştirilmiş yemek planları oluşturur.

## ✨ Özellikler

### 🧠 Smart Planning Engine v2.0
- **Genetik Algoritma** ile optimizasyon
- **Çoklu kriter skorlama** sistemi
- **Makro hedef** takibi (%40 ağırlık)
- **Yemek çeşitliliği** optimizasyonu (%25 ağırlık)
- **Kural uyumluluğu** kontrolü (%20 ağırlık)
- **Mevsimsellik** desteği (%8 ağırlık)
- **Yemek uyumluluğu** analizi (%7 ağırlık)

### 📊 Gelişmiş Makro Hesaplama
- **Mifflin-St Jeor Equation** ile BMR hesaplama
- **5 seviyeli aktivite** çarpanı
- **Diyet türüne özel** makro dağılımı
- **Hedef odaklı** kalori ayarlaması

### 🎯 Diyet Desteği
- **Keto Diyeti** (25% protein, 5% karb, 70% yağ)
- **Low-Carb** (30% protein, 15% karb, 55% yağ)
- **Balanced** (25% protein, 45% karb, 30% yağ)

### 📁 Modüler Veri Yapısı
- **GitHub entegrasyonu** ile cloud sync
- **JSON tabanlı** esnek veri yapısı
- **Cache sistemi** ile hızlı erişim
- **LocalStorage** ile offline çalışma

## 🚀 Kurulum

### 1. Repository Klonlayın
```bash
git clone https://github.com/kullanici-adiniz/nutrition-planner.git
cd nutrition-planner
```

### 2. GitHub Pages'te Yayınlayın
- Repository Settings > Pages
- Source: Deploy from a branch
- Branch: main / root

### 3. Tarayıcıda Açın
```
https://kullanici-adiniz.github.io/nutrition-planner
```

## 📂 Proje Yapısı

```
nutrition-planner/
├── index.html                    # Ana uygulama
├── js/
│   ├── SmartPlanningEngine.js    # Plan algoritması
│   ├── GitHubDataManager.js      # Veri yöneticisi
│   └── main.js                   # Ana JavaScript
├── data/
│   ├── foods.json               # Yemek veritabanı
│   ├── rules.json               # Sistem kuralları
│   ├── config.json              # Konfigürasyon
│   └── users/
│       └── user_templates.json  # Kullanıcı şablonları
├── css/
│   └── style.css                # Stil dosyaları
└── README.md                    # Bu dosya
```

## ⚙️ Konfigürasyon

`data/config.json` dosyasından sistem ayarlarını düzenleyebilirsiniz:

```json
{
  "algorithms": {
    "smart_v2": {
      "populationSize": 30,     // Aynı anda test edilecek plan sayısı
      "maxGenerations": 50,     // Maksimum iterasyon
      "weights": {
        "macroAccuracy": 0.40,  // Makro doğruluğu ağırlığı
        "varietyScore": 0.25    // Çeşitlilik ağırlığı
      }
    }
  }
}
```

## 🍽️ Yemek Ekleme

`data/foods.json` dosyasına yeni yemekler ekleyebilirsiniz:

```json
{
  "name": "Yeni Yemek",
  "calories": 200,
  "protein": 15,
  "carbs": 5,
  "fat": 12,
  "tags": ["keto", "protein"],
  "role": "mainDish",
  "mealType": ["lunch", "dinner"],
  "keto": true,
  "lowcarb": true,
  "seasonRange": "[1,12]"
}
```

## 🔧 Kullanım

### 1. Algoritma Seçimi
- **Smart Planning v2.0**: Genetik algoritma ile optimize edilmiş planlar
- **Klasik Algoritma**: Hızlı ve basit plan oluşturma

### 2. Plan Oluşturma
1. Kullanıcı profilini ayarlayın
2. Diyet türünü seçin (Keto/Low-carb)
3. "Akıllı Plan" butonuna tıklayın
4. Algoritma seçeneğini belirleyin
5. "Plan Oluştur" butonuna basın

### 3. Sonuçları Değerlendirme
- Makro hedeflerine yakınlık
- Yemek çeşitliliği analizi
- Kural uyumluluğu kontrolleri
- Plan kalite skoru

## 📊 API Kullanımı

```javascript
// Smart Planning Engine kullanımı
const planner = new SmartPlanningEngine({
  populationSize: 30,
  maxGenerations: 50
});

const plan = await planner.generateSmartPlan({
  targetCalories: 2000,
  targetProtein: 150,
  targetCarbs: 50,
  targetFat: 150
});

// GitHub Data Manager kullanımı
const dataManager = new GitHubDataManager({
  owner: 'kullanici-adiniz',
  repo: 'nutrition-planner'
});

const foods = await dataManager.loadFoods();
const rules = await dataManager.loadRules();
```

## 🐛 Hata Ayıklama

### JavaScript Console Logları
```javascript
// Debug modunu açın
localStorage.setItem('debug', 'true');

// İstatistikleri görün
const stats = await githubDataManager.getStats();
console.log(stats);
```

### Yaygın Sorunlar
1. **GitHub bağlantı hatası**: Repository URL'lerini kontrol edin
2. **Plan oluşturmama**: Yemek veritabanını kontrol edin
3. **Yavaş çalışma**: Popülasyon boyutunu azaltın

## 🤝 Katkıda Bulunma

1. Repository'yi fork edin
2. Feature branch oluşturun (`git checkout -b feature/yeni-ozellik`)
3. Değişikliklerinizi commit edin (`git commit -am 'Yeni özellik eklendi'`)
4. Branch'i push edin (`git push origin feature/yeni-ozellik`)
5. Pull Request oluşturun

## 📝 Lisans

Bu proje MIT lisansı altında lisanslanmıştır.

## 📞 İletişim

- GitHub: [kullanici-adiniz](https://github.com/kullanici-adiniz)
- Email: email@example.com

## 🔄 Güncellemeler

### v1.0.0 (2025-08-06)
- ✅ Smart Planning Engine v2.0
- ✅ GitHub entegrasyonu
- ✅ Çoklu kriter optimizasyonu
- ✅ Modüler veri yapısı
- ✅ Keto/Low-carb diyet desteği
