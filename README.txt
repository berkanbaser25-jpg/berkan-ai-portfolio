BERKAN BAŞER — ANGULAR WEB PORTFÖYÜ / PUBLIC SÜRÜM
24 Kasım 2026

1. PROJE VE KAPSAM

Yapay zekâ ve web geliştirme çalışmalarını tanıtan Angular portföyüdür.
Ana sayfa, hakkımda/iletişim, üyelik, yönetici paneli, hesap ayarları,
sipariş talepleri ve site destek asistanı yerelde çalışır.

Ana sayfa beş sahneli üç boyutlu bir sunumdur: Giriş, Market, Kavşak,
Yaklaşım ve İletişim. Bölüm düğmeleri, sağ/sol yön tuşları, Home ve End
ile gezinilir. Fare hareketi üç boyutlu sahnenin bakışını değiştirir.
Hareketi azalt seçeneği animasyonları durdurur. Tam ekran isteğine izin
verilmezse sunum sayfa içinde ekranı kaplar; Esc ile çıkılır.

Market Planlayıcı ve Kavşak Laboratuvarı sayfaları çalışan uygulama için
Netlify bağlantısı gösterir. Bu public pakette bu iki uygulamanın algoritma
kodları, eğitilmiş modelleri, katsayıları, veri setleri, sentetik görüntüleri,
eğitim/test kodları veya kod içeren rapor/defterleri bulunmaz.

Canlı site: https://berkanbaser.netlify.app/
Market: https://berkanbaser.netlify.app/projeler/market
Kavşak: https://berkanbaser.netlify.app/projeler/kavsak
Public depo: https://github.com/berkanbaser25-jpg/berkan-ai-portfolio

2. KURULUM

Gereksinim: Node.js 24.15 veya daha yeni bir 24.x sürümü ve npm.
Depodaki Berkan_Baser_Angular_Kaynak.zip dosyasını indirip açın.
Paket klasöründe terminal açarak şu komutları çalıştırın:

  npm ci
  npm run build
  npm start

Tarayıcı: http://127.0.0.1:4200/
Durdurma: Terminalde Ctrl+C.

İlk çalıştırma yerel yönetici hesabını ve rastgele başlangıç şifresini
oluşturur. Kullanıcı adı berkan'dır. Şifre yalnızca bilgisayarınızda oluşan
.runtime/yonetici-ilk-giris.json dosyasındadır; pakette hazır şifre bulunmaz.
Üyelik ve siparişler .runtime/portal.sqlite dosyasında saklanır. Bu dosyaları
paylaşmayın. Yerel ve canlı site hesapları birbirinden bağımsızdır.

3. KULLANIM

Üyelik: Üye ol / Giriş yap düğmesi formu açar. Zorunlu alanları ve onayları
tamamlayın; yeni üyelik yönetici onayı bekler. Yönetici /yonetim sayfasından
başvuruyu onaylar. Aktif üyeler talep oluşturup sürecini görebilir.

Hesap: Kullanıcı menüsünden iletişim ve şifre bilgileri değiştirilebilir,
üyenin hesabı silinebilir ve oturum kapatılabilir.

Projeler: Market veya Kavşak sayfasını açıp canlı uygulama düğmesine basın.
Yeni sekmede Netlify uygulaması açılır. Yerel üyelik ve sipariş oturumu
bu bilgisayarda kalır; canlı siteyle otomatik birleştirilmez.

Asistan: Sağ alttaki yuvarlak düğmeden projeler, hizmetler, üyelik ve iletişim
hakkında soru sorulabilir. Hazır bilgi havuzundan metin benzerliğiyle yanıt
seçer; haricî büyük dil modeli API'si kullanmaz.

4. TEKNOLOJİLER

Angular 22.3, TypeScript 6, HTML/CSS, Angular Router/Forms, RxJS,
Node.js 24, Animate.css 4.1.1, yerelde SQLite, Netlify Functions ve Netlify Blobs.
Bu public sürüm ONNX Runtime veya yapay zekâ model dosyası gerektirmez.
Animate.css kaynak: https://animate.style/
Lisans: public/third-party/ANIMATE_CSS_LICENSE.txt

5. YAPAY ZEKÂ DESTEĞİ

Geliştiricinin beyanına göre araştırma, kodlama, basit kurulumlar ve Türkçe
dokümantasyon hazırlığında ChatGPT 6 Astra ve ChatGPT Pro planı kullanıldı.
Araştırmada yöntem ve kaynak seçenekleri incelendi; kodlamada Angular
bileşenleri, stiller, API akışları ve hata düzeltmeleri için destek alındı.
Kurulumda bağımlılık komutları, derleme ve yayın ayarları hazırlandı.
Son kapsam, tercihler ve kontroller geliştiricinin değerlendirmesiyle yapıldı.
Model düzeyinin yüksek tutulmasının nedeni aynı ortamda başka projelerin
de yürütülmesidir. Web sitesini çalıştırmak için bu abonelik gerekli değildir.

6. DOSYALAR VE KONTROLLER

src/app/pages/        Portföy, hesap, yönetim, sipariş ve canlı proje bağlantıları.
presentation.component.ts / .css   3D sunum sahneleri ve etkileşimleri.
src/app/core/         Üyelik istemcisi, form doğrulaması ve site asistanı.
src/styles.css        Görünüm, mobil tasarım, kaydırma ve hover efektleri.
server/               Yerel API, yetkilendirme ve kalıcı veri deposu.
netlify/functions/    İsteğe bağlı ayrı yayın için sunucu işlevi.
scripts/              Yerel başlatma ve portal/asistan doğrulamaları.
dokumantasyon/        Görselli teslim belgesi ve iki proje ekran görüntüsü.

  npm run test:registration
  npm run test:portal
  npm run test:support
  npm run build

Testler ayrı deneme veritabanlarında çalışır. Unutulan şifre için otomatik
e-posta hizmeti bağlı değildir; hesap ayarları mevcut şifreyle değişir.

7. YAYIN VE TESLİM

Mevcut çalışan uygulama: https://berkanbaser.netlify.app/
Bu public sürümü ayrıca yayımlamak isterseniz Netlify build komutu
npm run build, publish dist/portfolio/browser, functions netlify/functions
ve Node sürümü 24.x olmalıdır. ADMIN_INITIAL_PASSWORD sunucu ortamında
en az 16 karakterlik güçlü bir başlangıç şifresiyle tanımlanır. Kaynağa
veya tarayıcı dosyalarına gerçek yönetici şifresi yazılmaz.

Teslim formunda public GitHub adresini ve canlı Netlify adresini paylaşın.
Canlı Netlify sürümünde iki uygulama çalışır durumdadır. GitHub dağıtımı
yalnızca bu uygulamalara bağlantı verir; model ve algoritmalar dağıtılmaz.

Ekran görüntüleri: dokumantasyon/gorseller/ana-sayfa.jpg ve
dokumantasyon/gorseller/kavsak-laboratuvari.jpg. İkinci görüntü yerel sürümdeki
Netlify bağlantısını gösterir. İki uygulama canlı siteden kullanılır.
Görselli belge: dokumantasyon/Web_Sitesi_Teslim_Dokumantasyonu.html

İletişim: Berkan Başer | berkanbaser25@gmail.com | +90 532 371 51 05
