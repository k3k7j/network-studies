#  My Cybersecurity Learning Journey

**Turkish Notes:**

Öncelikle kendimi tanıtarak başlamak istiyorum. Ben **Batuhan Kömürcügil**. Marmara Üniversitesi Yönetim Bilişim Sistemleri (Almanca) öğrencisiyim ve şu an Almanca hazırlık eğitimi alıyorum.

İlgim olan **Siber Güvenlik** alanında kendimi geliştirmek istiyorum. Bu repodaki amacım; hem kendi gelişimimi takip etmek hem de teknik bir arşiv oluşturmak. Birkaç yıl sonra geriye dönüp buradaki çalışmalarımı incelemenin beni motive edeceğine eminim.

**Cyber Security** dünyasına giriş yapmak isteyen herkes için şüphesiz ilk durak **Network** (Ağ) eğitimidir. Ben de bu aşamada hangi kaynağı kullanacağımı araştırdım ve literatür taramasından sonra başlangıç için **Charles Severance**'ın **"Introduction to Networking"** kitabıyla yola çıkmaya karar verdim. Günümüzdeki en büyük sorun olan "kaynak seçimi kararsızlığını" hallettiğimize göre kitabı incelemeye başlayabiliriz.

###  Yol Haritası (Roadmap)
Kitap toplam 9 Chapter ve bir "Wrap up" bölümünden oluşuyor:

* **Chapter 1:** Introduction
* **Chapter 2:** Network Architecture
* **Chapter 3:** Link Layer
* **Chapter 4:** Internetworking Layer
* **Chapter 5:** The Domain Name System
* **Chapter 6:** Transport Layer
* **Chapter 7:** Application Layer
* **Chapter 8:** Secure Transport Layer
* **Chapter 9:** The OSI Model
* **Chapter 10:** Wrap up

---

##  Chapter 1: Introduction
Kitap bu bölümde bizi internet öncesi dönemle karşılıyor. Özellikle günümüzdeki internet kullanımının kolaylığına ve arka planda bu kolaylığı sağlayan karmaşık **Software (Yazılım)** ve **Hardware (Donanım)** yapılarına dikkat çekiyor. Günümüzde network'ün nasıl çalıştığını anlamak istiyorsak, geçmişte insanların ve bilgisayarların uzak mesafelerden nasıl iletişim kurduğunu incelememiz gerektiğini vurguluyor.

###  Temel Kavramlar

* **Hardware (Donanım):** Bilgisayarın fiziksel parçalarıdır. Elle tutulabilir, gözle görülebilir.
    * *Örnek:* Router, Modem, Ethernet Kabloları (Wires), İşlemci.
* **Software (Yazılım):** Hardware'in (Donanımın) ne yapması gerektiğini söyleyen komutlar ve programlardır.
    * *Örnek:* Windows, Android, Tarayıcılar, Protokoller.

###  Hacker Mindset

* **Hardware Hacking:** Bir donanımı fiziksel olarak ele geçirmektir.
    * *Örnek:* Bir sunucu odasına girip bilgisayara USB takmak. Unutma: *"Eğer bir saldırganın donanıma fiziksel erişimi (Hardware Access) varsa, o bilgisayar artık senin değildir."*
* **Software Hacking:** Yazılım kodlarındaki hataları bulup sistemi sömürmektir.
    * *Örnek:* **Web Exploitation** bu alana girer. Bir web sitesine sızmak için kod açıklarını kullanmak buna örnektir.
 
#  Chapter 1.1: Communicating at a Distance

İnsanlar aynı odadayken iletişim kurmak kolaydır; ancak farklı odalara, şehirlere veya ülkelere dağıldıklarında işler değişir. Network'ün varoluş amacı, mesafeler arasındaki bu iletişim sorununu çözmektir. Kitapta, birbirinden ayrı odalardaki beş insanın iletişim kurma problemi örneklenir. Herkesin birbirine tek tek kablo çekmesi (**Full Mesh Topology**) inanılmaz maliyetli ve karmaşık olacağından, çözüm olarak **"Merkezi Sistemler" (Central Offices)** tasarlanmıştır.

Fiber optik teknolojisinden önce, bakır tellerdeki fiziksel sınırlamalar nedeniyle bir telde aynı anda sadece bir görüşme yapılabiliyordu. Bu da kapasiteyi sınırlı yapıyordu. Günümüzde ise fiber optik ve gelişmiş tekniklerle tek bir kablodan binlerce veri akışı sağlanabilmektedir.

###  Hacker Mindset

**1. Denial-of-Service (DoS) Attack & Circuit Switching:**
Hacker bakış açısıyla eski telefon sistemlerine (veya bugünün devre anahtarlamalı yapılarına) bakıldığında ilk göze çarpan zafiyet **Kapasite Sınırlaması**dır.
* **Mekanizma:** Uzaktan iletişimin ilk yöntemi olan **Circuit Switching (Devre Anahtarlama)**, bir hattın görüşme süresince sadece o görüşme için tahsis edilmesidir bu hat meşguldür ve başkası kullanamaz.
* **Saldırı Vektörü:** Bir saldırgan, mevcut tüm hatları arayarak meşgul ederse (Resource Exhaustion / Kaynak Tüketimi), meşru kullanıcılar iletişim kuramaz. Bu mantık, günümüzdeki **DoS (Denial-of-Service)** saldırılarının temelidir. Bir sunucunun kapasitesini "overloading" yaparak doldurmak, o hattı kullanıma kapatmak demektir. Bu verimsizlik, ileride göreceğimiz **Packet Switching** (Paket Anahtarlama) teknolojisine geçişin ana nedenlerinden biridir.

**2. Man-in-the-Middle (MitM) & Sniffing:**
Literatürdeki **Man-in-the-Middle (Ortadaki Adam)** saldırısının fiziksel karşılığı, iki kişiyi birbirine bağlayan "Santral Operatörü"dür.
* **Gizlilik İhlali:** İletişim, merkezi bir ofis (Central Office) üzerinden geçtiği için, buradaki operatör (veya sisteme sızan bir saldırgan) geçen veriyi/sesi, uçtaki kullanıcıların haberi olmadan dinleyebilir (**Sniffing**).
* **Single Point of Failure:** Ayrıca bu merkezi ofis, ağın "Tek Hata Noktası"dır. Ofisin elektriğinin kesilmesi veya saldırıya uğraması, ona bağlı tüm kullanıcıların iletişiminin (Availability) kopmasına neden olur.


