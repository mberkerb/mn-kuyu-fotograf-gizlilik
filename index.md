# MN Kuyu Fotoğraf — Gizlilik Politikası

**Yürürlük tarihi:** 19 Ağustos 2026
**Uygulama:** MN Kuyu Fotoğraf (`com.mnkuyufotograf.app`)
**Veri sorumlusu:** Mavi Nokta Su Mühendisliği
**İletişim:** mberkerb@gmail.com

## 1. Bu uygulama ne yapar

MN Kuyu Fotoğraf, saha personelinin su kuyularını fotoğraflayıp konumlarını
belgelemesi için geliştirilmiş kurumsal bir araçtır. Kamuya açık bir tüketici
uygulaması değildir ve yalnızca davet edilen kullanıcılara dağıtılır.

## 2. Topladığımız veriler

### 2.1 Konum bilgisi (hassas konum)

Fotoğraf çekildiğinde şunlar kaydedilir:

- Enlem ve boylam
- Varsa irtifa
- Cihazın bildirdiği konum doğruluğu (metre)
- Ölçüm dağılımı, %65 hassasiyet yarıçapı ve DRMS değeri
- Konumun hangi kuralla sabitlendiği (otomatik veya kullanıcı onayıyla)
- Konum sabitlenirken alınan son ölçümlerin koordinatları ve zaman damgaları
- GPS zaman damgası

Konum yalnızca uygulama ekranda açıkken ve fotoğraf çekimi amacıyla kullanılır.
**Arka planda konum toplanmaz.** Kullanıcı ekrana 60 saniye dokunmazsa konum
güncellemeleri tamamen durdurulur.

### 2.2 Fotoğraflar

Kamerayla çekilen fotoğraflar. Fotoğrafın EXIF üst verisine yukarıdaki konum
bilgileri ve aşağıdaki kimlikler gömülür. **Cihazın galerisindeki mevcut
fotoğraflara erişilmez**; yalnızca uygulama içinde çekilen kareler işlenir.

### 2.3 Kimlikler

- **Kurulum kimliği (UUID):** Uygulama ilk açıldığında üretilen rastgele bir
  numaradır. Kişiyi değil kurulumu tanımlar. Uygulama silinip yeniden
  kurulduğunda yenisi üretilir.
- **Anonim oturum kimliği:** Firebase Anonymous Authentication tarafından
  atanır. E-posta, telefon numarası veya parola istenmez; kişisel hesap
  oluşturulmaz.
- **İsim (isteğe bağlı):** İlk açılışta isim girmeniz istenir, atlayabilirsiniz.
  İsim girilirse kurulum kimliğiyle ilişkilendirilerek saklanır.

### 2.4 Toplamadıklarımız

Reklam kimliği, kişi listesi, çağrı kaydı, mikrofon kaydı, cihaz galerisi,
tarayıcı geçmişi, sağlık verisi ve ödeme bilgisi **toplanmaz**. Uygulamada
reklam ve üçüncü taraf analitik bulunmaz.

## 3. Verinin nereye gittiği

Fotoğraflar ve konum kayıtları, internet bağlantısı olduğunda Google Firebase
altyapısına yüklenir:

- **Google Cloud Storage** — fotoğraf dosyaları
- **Google Cloud Firestore** — konum ve üst veri kayıtları

Sunucular **europe-west8 (Milano, İtalya)** bölgesinde barındırılmaktadır. Veri
aktarımı HTTPS ile şifrelenir.

Google, bu hizmetler bakımından **veri işleyen** konumundadır. Veriler pazarlama
veya reklam amacıyla üçüncü taraflara satılmaz, kiralanmaz veya devredilmez.

## 4. Erişim ve güvenlik

Buluttaki kayıtlara yalnızca kaydı oluşturan anonim oturum sahibi yazabilir.
Uygulama içinden bulut verisi okunamaz, listelenemez ve silinemez; bu kısıtlar
sunucu tarafı güvenlik kurallarıyla zorunlu kılınmıştır.

Yönetici erişimi Mavi Nokta Su Mühendisliği'nin Firebase konsolu üzerinden
yapılır ve şirket personeliyle sınırlıdır.

## 5. Saklama

**Cihazdaki fotoğraflar:** Uygulamanın Ayarlar ekranındaki "Senkronize
fotoğrafları cihazdan sil" seçeneğiyle, yalnızca buluta yüklendiği doğrulanmış
fotoğraflar cihazdan silinebilir. Bu işlem buluttaki kopyayı etkilemez.

**Buluttaki kayıtlar:** Kuyu kayıtları belge niteliği taşıdığı için, hizmetin
amacı devam ettiği sürece saklanır. Kayıtlar zaman zaman şirket sistemlerine
arşivlenerek bulut ortamından kaldırılabilir; bu bir silme değil, saklama
ortamının değişmesidir.

Silme talepleri aşağıdaki bölümde açıklandığı şekilde karşılanır.

## 6. Haklarınız

Kayıtlarınızın silinmesini veya bir kopyasını talep etmek için
**mberkerb@gmail.com** adresine yazabilirsiniz.

Talebinizi işleyebilmemiz için uygulamanın **Ayarlar** ekranında görünen
**kurulum kimliğini** bildirmeniz gerekir; kayıtlar bu numarayla
ilişkilendirilmiştir ve başka bir kimlik bilgisi tutulmadığı için tespitin tek
yolu budur.

KVKK ve GDPR kapsamındaki erişim, düzeltme, silme ve işlemeye itiraz haklarınız
saklıdır.

## 7. Çocuklar

Uygulama kurumsal saha kullanımı içindir ve 18 yaş altındaki kişilere yönelik
değildir.

## 8. Değişiklikler

Bu politika değiştirilirse güncel sürüm bu adreste yayınlanır ve yürürlük tarihi
güncellenir.

## 9. İletişim

**Mavi Nokta Su Mühendisliği**
E-posta: mberkerb@gmail.com
