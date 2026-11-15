# 🚀 MarsBase AI

**Mars üssü hayatta kalma simülasyonu · Mars base survival training experience**

Dört kişilik bir ekibin Mars’taki yedi sol boyunca enerji, oksijen, su ve gıda kaynaklarını yönetmesine yardımcı olan etkileşimli bir eğitim simülasyonu. Plan yap, olaylara karar ver, sistemleri çalıştır ve her solun kaynak hesabını gör.

<p align="center">
  <img src="docs/screenshots/home-desktop.png" alt="MarsBase AI giriş ekranı" width="900">
</p>

### 🎯 Proje ne yapıyor?

MarsBase AI, oyuncuyu Ares adlı kurgusal bir Mars üssünün görev sorumlusu yapar. Oyuncu her sol için olayları değerlendirir, üssün sistemlerini ayarlar ve sınırlı kaynaklarla ekibin güvenliğini sağlamaya çalışır. Uygulama hem oynanabilir bir simülasyon hem de Mars keşfi hakkında bilgi veren bir eğitim prototipidir.

Arayüz Türkçe ve İngilizce kullanılabilir. Görev ilerlemesi aynı tarayıcıda saklanır.

### ✨ Öne çıkanlar

- 🧑‍🚀 Dört kişilik mürettebatı yedi sol (görev) boyunca yönet.
- ⚡ Enerji, oksijen, su ve gıda rezervlerini dengede tut.
- ☀️ Güneş panelleri, oksijen tesisi, su geri kazanımı, sera ve sığınağı planına göre çalıştır.
- 🌪️ Fırtına, su filtresi arızası ve radyasyon alarmı gibi olaylarda karar ver.
- 📊 Planını uygula; tahmini ve gerçekleşen kaynak değişimlerini incele.
- 🎯 Beş mühendislik hedefinden en az üçünü tamamlamaya çalış.
- 🌐 Three.js ile oluşturulan etkileşimli Mars üssünü döndür, yakınlaştır ve sistemlerle etkileş.
- 📚 Görevlerle bağlantılı NASA kaynaklarını ve bilimsel açıklamaları incele.
- 🤖 İsteğe bağlı ARES danışmanını kullan; API anahtarı yoksa yerel, kural tabanlı teşhisler çalışır.

**Görev başarısı:** Yedi solu tamamla, dört kaynağı ve ekip sağlığını sıfırın üzerinde tut, en az üç mühendislik hedefini tamamla.

### 🧰 Hangi diller ve teknolojiler kullanıldı?

- **TypeScript:** Arayüzün ve oyun/simülasyon mantığının ana dili.
- **JavaScript (Node.js):** Başlatma ve sunucu yardımcı betikleri.
- **HTML ve CSS:** Sayfa yapısı, görünüm ve uyarlanabilir düzen.
- **React:** Arayüz bileşenleri.
- **Vite:** Geliştirme sunucusu ve üretim derlemesi.
- **Three.js:** Etkileşimli 3B üs sahnesi.
- **Framer Motion ve Lucide:** Arayüz geçişleri ve simgeler.

### 📋 Gereksinimler

- **Node.js 22.12.0 veya üzeri.** Projenin belgelenmiş alt sınırıdır. Yeni kurulumlarda bu alt sınırı karşılayan desteklenen bir LTS sürümü tercih edin.
- **npm.** Node.js kurucusuyla birlikte gelir.
- Güncel Chrome, Firefox veya Edge gibi WebGL 2 destekleyen bir tarayıcı önerilir. WebGL 2 kullanılamazsa oyun sabit üs görseliyle çalışmaya devam eder.
- Bağımlılıkları ilk kez kurmak için internet gerekir. Oyun ve yerel teşhisler kurulumdan sonra çevrimdışı kullanılabilir; çevrimiçi NASA verileri ve harici AI için internet gerekir.

Sürümleri kontrol edin:

    node -v
    npm -v

Node.js’i [resmî indirme sayfasından](https://nodejs.org/en/download/) kurun. Desteklenen sürüm çizgileri için [Node.js sürüm takvimine](https://nodejs.org/en/about/previous-releases), Vite gereksinimleri için [Vite rehberine](https://vite.dev/guide/) bakın.

### 🪟 Windows’ta hızlı başlatma

1. ZIP dosyasını yeni bir klasöre çıkarın.
2. Node.js’i kurduktan sonra açık terminalleri kapatıp yeniden açın.
3. Proje klasöründeki **BAŞLAT.bat** dosyasına çift tıklayın.
4. Uygulama açılınca [http://127.0.0.1:5173](http://127.0.0.1:5173) adresini tarayıcıda açın.

#### BAŞLAT.bat ne yapıyor?

- Proje klasörüne geçer ve <code>npm ci</code> ile kilit dosyasındaki bağımlılıkları kurar.
- Kurulum başarısız olursa hata mesajını gösterip pencereyi açık tutar.
- Başarılı olursa <code>a.cmd</code> dosyasını Windows’un yönetici onayıyla başlatır.
- <code>a.cmd</code>, <code>node scripts/start.mjs</code> komutunu çalıştırır. Bu betik yerel sunucuyu <code>127.0.0.1:5173</code> adresinde açar ve tarayıcıyı başlatır.

**Bilmeniz gereken:** <strong>BAŞLAT.bat</strong>, <code>npm ci</code> komutunu her çalıştırmada yeniden çağırır. Paketler önbellekte değilse internet gerekir ve başlangıç biraz zaman alabilir. Ayrıca Windows UAC yönetici onayı gösterebilir. Tekrar tekrar kurulum yapmadan veya yönetici onayı vermeden başlatmak için elle başlatma yöntemini kullanın.

### ⌨️ Elle başlatma (Windows, macOS ve Linux)

Terminali proje klasöründe açın:

    npm ci
    npm run dev

Terminalde görünen yerel adresi tarayıcıda açın. Sunucuyu durdurmak için terminalde **Ctrl+C** tuşlarına basın. Bağımlılıklar kurulduktan sonraki açılışlarda genellikle yalnızca <code>npm run dev</code> yeterlidir.

### 🤖 İsteğe bağlı AI ve NASA bağlantıları

AI danışmanı zorunlu değildir; API anahtarı olmadan yerel teşhisler kullanılabilir. Harici model bağlamak için <code>.env.example</code> dosyasını <code>.env.local</code> adıyla kopyalayın, NVIDIA veya OpenRouter sağlayıcısını seçip kendi anahtarınızı ve model kimliğinizi yazın, ardından sunucuyu yeniden başlatın.

Windows Komut İstemi:

    copy .env.example .env.local

macOS/Linux:

    cp .env.example .env.local

NVIDIA örneği:

    AI_PROVIDER=nvidia
    NVIDIA_API_KEY=kendi_nvidia_anahtariniz
    NVIDIA_MODEL=nvidia/nemotron-3.5-super-vl-120b-a12b
    NASA_API_KEY=

OpenRouter için <code>AI_PROVIDER=openrouter</code>, <code>OPENROUTER_API_KEY</code> ve <code>OPENROUTER_MODEL</code> değerlerini kullanın. <code>NASA_API_KEY</code> isteğe bağlıdır; boş bırakıldığında NASA’nın genel demo anahtarı kullanılır.

🔐 **API anahtarlarını GitHub’a yüklemeyin.** Anahtarları yalnızca <code>.env.local</code> içinde tutun; <code>VITE_</code> ile başlayan değişkenlere yazmayın. Harici AI açıldığında soru, görev durumu, seçili plan ve ilgili görev bağlamı seçtiğiniz sağlayıcıya gönderilir.

### 🧪 Geliştirici komutları

    npm run dev          # Yerel geliştirme sunucusu
    npm run typecheck    # TypeScript kontrolü
    npm test             # Birim ve arayüz testleri
    npm run build        # Üretim derlemesi; çıktı dist/ klasörüne yazılır
    npm run preview      # Üretim derlemesini yerel sunucuda önizle

Tarayıcı uçtan uca testleri için önce Chromium’u kurun:

    npx playwright install chromium
    npm run test:e2e

### 📂 Proje yapısı

| Klasör / dosya | İçerik |
|---|---|
| <code>src/trainer/</code> | Görev ekranı, dersler ve yerel teşhisler |
| <code>src/game/</code> | Kaynak hesabı, görev durumları, olaylar ve kayıt |
| <code>src/scene/</code> | 3B sahnenin oluşturulması ve animasyon yönetimi |
| <code>src/components/</code> | Arayüz ve 3B sahne bileşenleri |
| <code>server/</code> | Yerel AI danışmanı ve NASA veri uç noktaları |
| <code>public/</code> | Görseller ve statik dosyalar |
| <code>docs/</code> | Bilim kaynakları, tasarım notları ve ekran görüntüleri |
| <code>BAŞLAT.bat</code> / <code>a.cmd</code> | Windows başlatıcıları |

### 🔬 Bilimsel kapsam

Proje, NASA ve diğer bilimsel kaynaklardan esinlenen eğitim ilkeleri kullanır; **NASA tarafından onaylanmış bir ürün değildir**. Kaynak değerleri eğitim puanlarıdır; gerçek litre, kWh, basınç veya radyasyon ölçümü değildir. Gerçek bir Mars üssünün işletim prosedürü olarak kullanılmamalıdır. Kaynaklar için [docs/NASA_KAYNAKLARI.md](docs/NASA_KAYNAKLARI.md) dosyasına bakın.
