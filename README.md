# 🚀 MarsBase AI

**Mars üssü hayatta kalma simülasyonu · Mars base survival training experience**

Dört kişilik bir ekibin Mars’taki yedi sol boyunca enerji, oksijen, su ve gıda kaynaklarını yönetmesine yardımcı olan etkileşimli bir eğitim simülasyonu. Plan yap, olaylara karar ver, sistemleri çalıştır ve her solun kaynak hesabını gör.

[🇹🇷 Türkçe](#turkce) · [🇬🇧 English](#english)

<p align="center">
  <img src="docs/screenshots/home-desktop.png" alt="MarsBase AI giriş ekranı" width="900">
</p>

<a id="turkce"></a>
## 🇹🇷 Türkçe

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

### 📄 Lisans

Bu proje paketinde kök dizinde bir lisans dosyası bulunmuyor. Yeniden kullanım ve katkı koşullarını belirlemek için GitHub’a yayımlamadan önce proje sahibi bir <code>LICENSE</code> dosyası eklemelidir.

---

<a id="english"></a>
## 🇬🇧 English

### 🎯 What is this project?

MarsBase AI is an interactive training simulation where you manage Ares, a fictional Mars outpost. Plan each sol, respond to mission events, operate base systems, and keep a four-person crew safe with limited energy, oxygen, water, and food.

The interface is available in Turkish and English. Progress is saved in the current browser.

### ✨ Features

- 🧑‍🚀 Manage a four-person crew across seven sols.
- ⚡ Balance energy, oxygen, water, and food.
- ☀️ Operate solar panels, an oxygen plant, water recovery, a greenhouse, and a shelter.
- 🌪️ Respond to events such as a dust storm, water-filter failure, and radiation alert.
- 📊 Apply a plan and review predicted and actual resource changes.
- 🎯 Complete at least three of five engineering objectives.
- 🌐 Rotate, zoom, and interact with a Three.js Mars base scene.
- 📚 Explore NASA references and science notes linked to the missions.
- 🤖 Use the optional ARES advisor; local rule-based diagnostics work without an API key.

**Mission goal:** Complete all seven sols, keep all four resources and crew health above zero, and complete at least three engineering objectives.

### 🧰 Languages and technology

- **TypeScript:** Main language for the interface and simulation logic.
- **JavaScript (Node.js):** Startup and server-side helper scripts.
- **HTML and CSS:** Page structure, styling, and responsive layout.
- **React:** User-interface components.
- **Vite:** Development server and production build.
- **Three.js:** Interactive 3D base scene.
- **Framer Motion and Lucide:** UI transitions and icons.

### 📋 Requirements

- **Node.js 22.12.0 or newer.** This is the documented project minimum; use a supported LTS release that meets it.
- **npm**, included with the Node.js installer.
- A current browser such as Chrome, Firefox, or Edge. WebGL 2 is recommended for the interactive 3D scene; the game falls back to a static base image if WebGL 2 is unavailable.
- Internet access is needed for the initial dependency install. The game and local diagnostics work offline after installation; live NASA data and external AI require internet access.

Check the installed versions:

    node -v
    npm -v

Install Node.js from the [official download page](https://nodejs.org/en/download/). See the [Node.js release schedule](https://nodejs.org/en/about/previous-releases) and [Vite guide](https://vite.dev/guide/) for current support details.

### 🪟 Quick start on Windows

1. Extract the ZIP into a new folder.
2. Install Node.js, then close and reopen any terminals.
3. Double-click **BAŞLAT.bat** in the project folder.
4. Open [http://127.0.0.1:5173](http://127.0.0.1:5173) in your browser when the app starts.

#### What does BAŞLAT.bat do?

- Changes to the project folder and installs dependencies from the lockfile with <code>npm ci</code>.
- If installation fails, it displays an error and pauses.
- If installation succeeds, it starts <code>a.cmd</code> with Windows administrator approval.
- <code>a.cmd</code> runs <code>node scripts/start.mjs</code>, which starts the local server at <code>127.0.0.1:5173</code> and opens the browser.

**Please note:** <strong>BAŞLAT.bat</strong> runs <code>npm ci</code> every time it is launched. It may take a while and may need internet access when packages are not cached. Windows may also show a User Account Control prompt. To avoid reinstalling packages on every launch or approving elevation, use the manual start steps below.

### ⌨️ Manual start (Windows, macOS, and Linux)

Open a terminal in the project folder:

    npm ci
    npm run dev

Open the local address printed in the terminal. Press **Ctrl+C** in the terminal to stop the server. After dependencies have been installed once, subsequent starts usually only need <code>npm run dev</code>.

### 🤖 Optional AI and NASA connections

The AI advisor is optional; local diagnostics work without an API key. To connect an external model, copy <code>.env.example</code> to <code>.env.local</code>, choose NVIDIA or OpenRouter, add your own API key and model ID, and restart the server.

Windows Command Prompt:

    copy .env.example .env.local

macOS/Linux:

    cp .env.example .env.local

NVIDIA example:

    AI_PROVIDER=nvidia
    NVIDIA_API_KEY=your_nvidia_api_key
    NVIDIA_MODEL=nvidia/nemotron-3.5-super-vl-120b-a12b
    NASA_API_KEY=

For OpenRouter, set <code>AI_PROVIDER=openrouter</code>, <code>OPENROUTER_API_KEY</code>, and <code>OPENROUTER_MODEL</code>. <code>NASA_API_KEY</code> is optional; when empty, the app uses NASA’s public demo key.

🔐 **Never commit API keys to GitHub.** Keep them in <code>.env.local</code>; do not put them in variables prefixed with <code>VITE_</code>. When external AI is enabled, the question, mission state, selected plan, and related context are sent to your configured provider.

### 🧪 Developer commands

    npm run dev          # Local development server
    npm run typecheck    # TypeScript check
    npm test             # Unit and UI tests
    npm run build        # Production build; output is written to dist/
    npm run preview      # Preview the production build locally

For browser end-to-end tests, install Chromium first:

    npx playwright install chromium
    npm run test:e2e

### 📂 Project structure

| Folder / file | Contents |
|---|---|
| <code>src/trainer/</code> | Mission screen, lessons, and local diagnostics |
| <code>src/game/</code> | Resource accounting, mission state, events, and saves |
| <code>src/scene/</code> | 3D scene creation and animation |
| <code>src/components/</code> | UI and 3D scene components |
| <code>server/</code> | Local AI advisor and NASA data endpoints |
| <code>public/</code> | Images and static files |
| <code>docs/</code> | Science references, design notes, and screenshots |
| <code>BAŞLAT.bat</code> / <code>a.cmd</code> | Windows launchers |

### 🔬 Scientific scope

The project uses educational ideas inspired by NASA and other scientific sources. It is **not endorsed by NASA**. Resource values are training points, not real liters, kWh, pressure, or radiation measurements. Do not use this simulation as an operational guide for a real Mars base. See [docs/NASA_KAYNAKLARI.md](docs/NASA_KAYNAKLARI.md) for references.

### 📄 License

The provided project archive does not include a root-level license file. Add a <code>LICENSE</code> file before publishing if you want to define reuse and contribution terms.


