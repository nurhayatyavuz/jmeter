<h1 align="center"><img src="https://jmeter.apache.org/images/logo.svg" alt="Apache JMeter logo" /></h1>

Performansı ölçmek ve uygulamaların yük testini yapmak için tasarlanmış açık kaynak kodlu bir Java uygulaması.

Apache Yazılım Vakfı Tarafından

[![Build Status](https://api.travis-ci.com/apache/jmeter.svg?branch=master)](https://travis-ci.com/apache/jmeter/)
[![codecov](https://codecov.io/gh/apache/jmeter/branch/master/graph/badge.svg)](https://codecov.io/gh/apache/jmeter)
[![License](https://img.shields.io/:license-apache-brightgreen.svg)](https://www.apache.org/licenses/LICENSE-2.0.html)
[![Stack Overflow](https://img.shields.io/:stack%20overflow-jmeter-brightgreen.svg)](https://stackoverflow.com/questions/tagged/jmeter)
[![Maven Central](https://maven-badges.herokuapp.com/maven-central/org.apache.jmeter/ApacheJMeter/badge.svg)](https://maven-badges.herokuapp.com/maven-central/org.apache.jmeter/ApacheJMeter)
[![Javadocs](https://www.javadoc.io/badge/org.apache.jmeter/ApacheJMeter_core.svg)](https://www.javadoc.io/doc/org.apache.jmeter/ApacheJMeter_core)
[![Twitter](https://img.shields.io/twitter/url/https/github.com/apache/jmeter.svg?style=social)](https://twitter.com/intent/tweet?text=Powerful%20load%20testing%20with%20Apache%20JMeter:&url=https://jmeter.apache.org)

## Nedir?

Apache JMeter, performansı ölçebilir ve statik ve dinamik web uygulamalarının yük testini yapabilir.

Bir sunucu, sunucu grubu, ağ veya nesne üzerindeki ağır yükü simüle etmek, gücünü test etmek veya farklı yük türleri
altında genel performansı analiz etmek için kullanılabilir.

![JMeter screen](https://raw.githubusercontent.com/apache/jmeter/master/xdocs/images/screenshots/jmeter_screen.png)

## Özellikler

Tam taşınabilirlik ve %100 Java.

Çoklu iş parçacığı, birçok iş parçacığı tarafından eş zamanlı örneklemeye ve
ayrı iş parçacığı grupları tarafından farklı işlevlerin eş zamanlı örneklemesine olanak tanır.

### Protokoller

Birçok uygulama/sunucu/protokol türünü yükleme ve performans testi yapma yeteneği:

- Web - HTTP, HTTPS (Java, NodeJS, PHP, ASP.NET,...)
- SOAP / REST Web servisleri
- FTP
- JDBC aracılığıyla veritabanı
- LDAP
- JMS aracılığıyla mesaj odaklı ara yazılım (MOM)
- Posta - SMTP(S), POP3(S) ve IMAP(S)
- Yerel komutlar veya kabuk betikleri
- TCP
- Java Nesneleri

### IDE

Tam özellikli Test IDE'si, hızlı Test Planı **kaydı** (Tarayıcılardan veya yerel uygulamalardan), 
**oluşturma** ve **hata ayıklama** olanağı sağlar.

### Komut Satırı

[Komut satırı modu (GUI olmayan / başsız mod)](https://jmeter.apache.org/usermanual/get-started.html#non_gui)
Herhangi bir Java uyumlu işletim sisteminden (Linux, Windows, Mac OSX, ...) test yüklemek için

### Raporlama

Tamamlanmış ve sunulmaya hazır [dinamik HTML raporu](https://jmeter.apache.org/usermanual/generating-dashboard.html)

![Pano ekran görüntüsü](https://raw.githubusercontent.com/apache/jmeter/master/xdocs/images/screenshots/dashboard/response_time_percentiles_over_time.png)

[Canlı raporlama](https://jmeter.apache.org/usermanual/realtime-results.html)
into 3rd party databases like InfluxDB or Graphite

![Canlı rapor](https://raw.githubusercontent.com/apache/jmeter/master/xdocs/images/screenshots/grafana_dashboard.png)

### Korelasyon

En popüler yanıt formatlarından veri çıkarma yeteneği sayesinde kolay korelasyon,
[HTML](https://jmeter.apache.org/usermanual/component_reference.html#CSS/JQuery_Extractor),
[JSON](https://jmeter.apache.org/usermanual/component_reference.html#JSON_Extractor),
[XML](https://jmeter.apache.org/usermanual/component_reference.html#XPath_Extractor) or
[any textual format](https://jmeter.apache.org/usermanual/component_reference.html#Regular_Expression_Extractor)

### Son Derece Genişletilebilir Çekirdek

- Takılabilir Örnekleyiciler sınırsız test yeteneklerine izin verir.
- **Komut Dosyası Oluşturulabilir Örnekleyiciler** (Groovy gibi JSR223 uyumlu diller).
- **Takılabilir katmanlar** ile çeşitli yük istatistikleri seçilebilir.
- Veri analizi ve **görselleştirme eklentileri** büyük genişletilebilirlik ve kişiselleştirme sağlar.
- Fonksiyonlar bir teste dinamik girdi sağlamak veya veri manipülasyonu sağlamak için kullanılabilir.
- Maven, Gradle ve Jenkins için 3. taraf Açık Kaynaklı kütüphaneler aracılığıyla Kolay Sürekli Entegrasyon.

## En Son Sürüm

En son sürümün ayrıntıları şu adreste bulunabilir:
[JMeter Apache Projesi web sitesi](https://jmeter.apache.org/)

## Gereksinimler

Apache JMeter'ı çalıştırmak için aşağıdaki gereksinimler mevcuttur:

- Java Yorumlayıcısı:

Apache JMeter'ın çalışması için tamamen uyumlu bir Java 17 Çalışma Ortamı gereklidir. 
`keytool` yardımcı programına sahip bir JDK, HTTPS web sitelerini kaydetmek için daha uygundur.

- İsteğe bağlı jar'lar:

Bazı jar'lar JMeter'a dahil değildir.
Gerekirse, bunlar indirilmeli ve lib dizinine yerleştirilmelidir
- JDBC - veritabanı tedarikçisinden edinilebilir
- JMS - JMS sağlayıcısından edinilebilir
  - [Bouncy Castle](https://www.bouncycastle.org/) -
  sadece SMIME Assertion için gereklidir

- Java Derleyicisi (*İSTEĞE BAĞLI*):

Dağıtım önceden derlenmiş bir Java ikili arşivi içerdiğinden bir Java derleyicisine gerek yoktur.
> **Not** Apache JMeter için eklentiler oluşturmak için bir derleyicinin gerekli olduğunu unutmayın.

## Kurulum Talimatları

> **Not** dizin adlarındaki boşluklar sorunlara neden olabilir.

- Sürüm derlemeleri

İkili arşivi uygun bir dizin yapısına açın.

## JMeter'ı Çalıştırma

1. `bin` dizinine geçin
2. `jmeter` (Un\*x) veya `jmeter.bat` (Windows) dosyasını çalıştırın.

### Windows

Windows için, bir JMX dosyasını sürükleyip bırakabileceğiniz
başka bazı betikler de vardır:

- `jmeter-n.cmd` - dosyayı GUI olmayan bir test olarak çalıştırır
- `jmeter-n-r.cmd` - dosyayı GUI olmayan bir uzak (istemci-sunucu) test olarak çalıştırır
- `jmeter-t.cmd` - dosyayı GUI testi olarak çalıştırmaya hazır şekilde yükler

## Belgeler

Bu sürümün tarihi itibariyle mevcut olan belgeler, 
[printable_docs](printable_docs) dizininde HTML biçiminde de yer almaktadır
ve [index.html](printable_docs/index.html) adlı dosyadan başlayarak taranabilir.

## Bir hata/geliştirme bildirme

[Sorun Takibi] bölümüne bakın
(https://jmeter.apache.org/issues.html).

## Yapım talimatları

### Yapıları yayınla

Kaynak arşivini uygun bir dizin yapısına açın.
3. parti kütüphane dosyalarının çoğu ikili arşivden aynı dizin yapısına açılarak çıkarılabilir.

İsteğe bağlı jar'lar (yukarıya bakın) `lib/opt` ve/veya `lib` içine yerleştirilmelidir.

`lib/opt` içindeki jar'lar JMeter'ı derlemek ve birim testlerini çalıştırmak için kullanılacaktır,
ancak çalışma zamanında kullanılmayacaktır.

_Bu, isteğe bağlı jar'ların diğer JMeter kullanıcıları tarafından indirilmemesi durumunda ne olacağını test etmek için yararlıdır._

Bir proxy'nin arkasındaysanız, Gradle'ın proxy'yi kullanması için 
`~/.gradle/gradle.properties` dizininde birkaç yapı özelliği ayarlayabilirsiniz:

```properties
systemProp.http.proxyHost=proxy.example.invalid
systemProp.http.proxyPort=8080
systemProp.http.proxyUser=your_user_name
systemProp.http.proxyPassword=your_password
systemProp.https.proxyHost=proxy.example.invalid
systemProp.https.proxyPort=8080
systemProp.https.proxyUser=your_user_name
systemProp.https.proxyPassword=your_password
```

### Test yapıları

JMeter, Gradle kullanılarak oluşturulmuştur ve [JVM projeleri için Gradle'ın Araç Zincirlerini] kullanır 
(https://docs.gradle.org/current/userguide/toolchains.html)
JDK'ları sağlamak için. Bu, kodun ihtiyaç duyulan JDK'ları yerel olarak arayacağı veya
bulunmazsa indireceği anlamına gelir.

Varsayılan olarak, kod derleme amaçları için JDK 17'yi kullanır, ancak hedef sürümü 8 olarak ayarlar,
bu nedenle ortaya çıkan eserler Java 8 ile uyumlu olur.

Aşağıdaki komut JMeter'ı derler ve test eder:

```sh
./gradlew build
```

Derleme için özel bir JDK kullanmak istiyorsanız `-PjdkBuildVersion=11` ayarlayabilirsiniz,
ve test için farklı bir JDK kullanmak istiyorsanız `-PjdkTestVersion=21` seçebilirsiniz.

Mevcut yapı parametrelerini şu komutu çalıştırarak listeleyebilirsiniz:

```sh
./gradlew parametreleri
```

Sistemin bir GUI ekranı yoksa:

```sh
./gradlew build -Djava.awt.headless=true
```

Çıktı eserleri (jar'lar, raporlar) `build` klasörüne yerleştirilir.

Örneğin, ikili eserler `src/dist/build/distributions` altında bulunabilir.

Aşağıdaki komut uygulamayı derler ve `jmeter`'ı `bin` dizininden çalıştırmanızı sağlar.

> **Not** `lib/` içeriklerini tamamen yeniler,
bu nedenle `lib/` dizinine yüklediyseniz özel eklentileri kaldırır. Ancak `lib/ext/` eklentilerini olduğu gibi korur.

```sh
./gradlew createDist
```

Alternatif olarak, Gradle'ın GUI'yi başlatmasını sağlayabilirsiniz:

```sh
./gradlew runGui
```

## Geliştirici Bilgileri

İnşa etme ve katkıda bulunma ayrıntılı olarak şu adreste açıklanmaktadır:
[JMeter'ı inşa etmek](https://jmeter.apache.org/building.html)
ve [KATKIDA BULUNMAK.md](CONTRIBUTING.md). Mevcut görevler hakkında daha fazla bilgi
JMeter'ı Gradle ile derlemek şu şekilde mevcuttur: [gradle.md](gradle.md).

Kod şuradan alınabilir:

- https://github.com/apache/jmeter
- https://gitbox.apache.org/repos/asf/jmeter.git

## Lisanslama ve Yasal Bilgiler

Yasal ve lisanslama bilgileri için lütfen aşağıdaki dosyalara bakın:

- [Lisans](LICENSE)
- [Bildirim](NOTICE)

## Kriptografik Yazılım Bildirimi

Bu dağıtım, kriptografik yazılımla birlikte kullanılmak üzere tasarlanmış yazılımları içerebilir. Şu anda ikamet ettiğiniz ülkede, şifreleme yazılımının ithalatı, bulundurulması, kullanımı ve/veya başka bir ülkeye yeniden ihraç edilmesi konusunda kısıtlamalar olabilir. Herhangi bir şifreleme
yazılımını kullanmadan ÖNCE, lütfen şifreleme yazılımının ithalatı, bulundurulması veya kullanımı ve yeniden ihraç edilmesiyle ilgili ülkenizin yasalarını, yönetmeliklerini ve politikalarını kontrol edin. Daha fazla bilgi için <https://www.wassenaar.org/> adresine bakın.

ABD Ticaret Bakanlığı, Sanayi ve
Güvenlik Bürosu (BIS), bu yazılımı, asimetrik algoritmalarla kriptografik işlevleri kullanan veya gerçekleştiren bilgi güvenliği
yazılımlarını içeren İhracat Emtia
Kontrol Numarası (ECCN) 5D002.C.1 olarak sınıflandırmıştır. Bu Apache Yazılım Vakfı
dağıtımının biçimi ve tarzı, hem nesne kodu hem de kaynak kodu için Lisans İstisnası
ENC Teknoloji Yazılımı Sınırsız (TSU) istisnası (bkz. BIS
İhracat İdaresi Yönetmelikleri, Bölüm 740.13) kapsamında ihraç edilmeye uygun hale getirir.

Aşağıda, kriptografik yazılımlarda ihracat kontrollerine tabi olabilecek dahil edilen yazılım hakkında daha fazla ayrıntı verilmektedir:

Apache JMeter, HTTPS desteği sağlamak için Java Secure Socket Extension (JSSE) API'siyle arayüz oluşturur

- NTLM kimlik doğrulaması sağlamak için Apache JMeter (Apache HttpClient4 aracılığıyla) Java Cryptography Extension (JCE) API'siyle arayüz oluşturur

- Apache JMeter, JSSE veya JCE'nin hiçbir uygulamasını içermez.

## Teşekkürler

**Apache JMeter'ı kullandığınız için teşekkür ederiz.**

### Üçüncü taraf bildirimleri

* mxparser için bildirim:

> Bu ürün, Indiana Üniversitesi Extreme! Lab tarafından geliştirilen
> yazılımı içerir. Daha fazla bilgi için lütfen şu adresi ziyaret edin
> http://www.extreme.indiana.edu/
