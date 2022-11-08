# Network 101 Notlar

### Network ve IP'lerin tanıtımı
1. İnternet genel olarak Ethernet kartlarının birbirleriyle iletişim kurmaları sayesinde çalışır.
2. Ethernet kartları Anakartlara entegre edilen donanım birimlerinden bisidir.
3. Ethernet kartları üzerinde bulundukları cihazların bir ağa bağlanmasını sağlar.
4. Bir Ethernet Port'undan diğerine uzanan kablo CAT6'dır.
5. CAT6'nın Ethernet Port'una giren başlığı RJ45'dir.
6. RJ45 başlığı, CAT6'dan gelen 8 adet bakır telin belli bir düzene göre sıralanmasını sağlayarak cihazlardaki Ethernet portlarına kilitlenerek CAT6 ya da herhangi bir Ethernet kablosunun bağlanmasını sağlar.
7. Ethernet kabloları, UTP ve STP olarak ikiye ayrılır.
8. STP, korumalı yani topraklamalı olan kablodur.
9. STP, ikişerli olarak birbirlerine bakır tellerin aralarında bir plastik çubuğun kablo boyunca uzanması anlamına gelir. Bu parça tellerin zarar görmesini engeller ve tellerin dalga boylarının düşmesini UTP'ye göre daha uzun süre engeller.
10. CAT6, STP tipinde bir kablodur.
11. Ethernet kablolarındaki bakır teller RJ45 başlığı sayesinde "Straigth Through(Düz)" ya da "Crossover Cable(Çapraz)" dizilimlerinde çakılabilirler.
![RJ45, Straight through and Crossover Cable](straight_cross.png)
12. Network'ler genel olarak Straight Through ile karşılaşırız çünkü Straigth Through birbirinden farklı Layer'larda çalışan cihazların iletişimini sağlamak kullanılır. Örneğin bir PC ile bir Switch aynı Layer'da cihazlar değillerdir.
13. İstisnai bir durum olarak PC direkt olarak Ethernet kablosu ile Router'ın Ethernet Port'una bağlanacak ise Crossover Cable çakılmalıdır.
14. Özetlenecek olursa özdeş iki cihaz Crossover Cable, farklı ise Straigth Through RJ45'e ihtiyaç var demektir.

---

### Network oluşturmak
1. Network, içerisinde bir ya da birden fazla Client bulunduran ve bu Client ile iletişime geçilmesinin sağlandığı ortamdır.
2. İki tane Client'in birbiri ile iletişime geçebilmesi için birinin Ethernet Port'undan diğerinin Ethernet Port'una CAT6 kablosunu Crossover RJ45 ile bağlamak yeterlidir.
3. Birden fazla Client'in birbirleri ile iletişimini sağlamak istediğimizde fiziksel bir sınır ile karşı kaşıya kalırız. Bu sınır; Client'lerin, Ethetnet Port'larının yetersiz kalması durumudur. Özetlenecek olursa; Network'teki Client sayısı kadar her bir Client'in üzerinde Ethernet Port'u bulunma şartı bulunur.
4. İkiden fazla Client'in birbirleri ile iletişim kurabilmelerini sağlamak için Layer 2'de çalışan ve Switch adı verilen aracı cihazlar kullanılır.
5. Switch'ler üzerlerinde birden çok Ethernet Port'u barındırabilirler.
6. Network'teki bütün Client'ler sadace o Network'teki Switch'e bağlanarak, diğer Client'ler ile o Switch üzerinden iletişime geçebilirler.
7. Client'ler, iletişime geçmek istedikleri Client'e erişebilmek için önce paketlerini Switch'e gönderirler. Switch bu paketleri alıp hedef Client'e gönderir.
7. Switch MAC adres tablolaması yaparak, Client'lerden gelen paketleri Client'lerin MAC adreslerine göre gönderir.
8. MAC Adresi, Ethernet Kartının "Unique ID"'si ve "Pyscall Address(Fiziksel Adres)"'i anlamına gelir.
9. MAC Adresleri Hexadecimal Sayı Sistemi'nde ifade edilirler. Dolayısıyla MAC Adreslerini ifade eden maksimum karakter "FF"'tir.
10. Her bir paketin içersinde şu bilgiler yer alır; Source, MAC, IP, Destination MAC, Destination IP, CRC, DATA.
11. Switch'lerin; Unicast, Multicast ve Broadcast yayın yapabilme özellikleri vardır.
	- Unicast, paketleri noktadan noktaya(Örneğin PC'den PC'ye) gönderir.
	- Multicast, paketleri aynı anda birden çok Client'e gönderir.
	- Broadcast, paketleri bulunduğu Network üzerindeki herkese aynı anda gönderir.
12. Anakart ve buna benzer Network ya da Bilgisayar sistemlerine ait donanım birimlerinin Fiziksel Adresleri vardır ve bu adresleri GUID(Global Unique Identifier-Eşsiz Referans Numarası Tanımlayıcısı)  belirler.
13. ARP Protokolü ile IP'sini bilgidiğimiz bir makinenin MAC adresini öğrenebiliriz.
14. IP'ler Anakart'lara değil direkt olarak Ethernet Port'larına atanan bir Unique Number'dır. Dolayısıyla kullanacağımız tüm Ethernet Port'larına IP atamak zorundayız.
15. 5651 Loglama Kanunu'dur. Şirketler kendi Network'lerine bağlanan cihazları Log'layarak kullanıcıların o cihazlar üzerinden bir siber suç işlemeleri durumunda arkalarında bir kanıt bırakmaları ve şirketlerin kendilerini aklayabilmeleri için zorunlu hale getirilmiştir. Log'lama yapılmıyorsa bu gibi bir durumda şirket sorumlu tutulur.

---

### IP Adresleri
1. IP adresleri bilgisayarların CPU'larının çalışma prensiplerine göre şekillenmiştir. CPU(Central Processing Unit)'lar ikilik sayı sistemine göre çözümleme yaparlar. Elektrik akımı, sürekli olarak 0 veya 1 değerine çevirilerek işlem yapılır.
2. Bir anlamda her bir 0 ya da her bir 1, 1 Bit'e kaşılık gelirler.
3. IP'ler 2 üzeri 32 üzerinden belirlenirler ve toplamda 4 Octed'ten oluşurlar.
4. Her bir Octed toplam 8 Bit'ten oluşur. Octed'ler soldan sağa okunurlar ve soldaki Bit, en yüksek değere sahip Bit'tir.
5. Her bir IP toplam 4 Octed'ten oluşur.
```
------------------------
| 128 64 32 16 8 4 2 1 |
|  1  1  1  1  1 1 1 1 |
------------------------
```
6. Soldan sağa bütün Bit'ler toplandığında 255 değeri elde edilir.
7. Bu değer bir IP adresinin alabileceği maksimum Octed değerini ifade eder.
8. IP adreslerinin hangi Network'e ait olduklarını sadece IP adreslerine bakarak bilmem mümkün değildir. Bunu belirten bir adrese Subnet Mask denir. Her IP'nin Subnet Mask'ı olmak zorundadır.
9. Network'teki bir cihazın IP Adresini öğrenmek istediğimizde aşağıdaki komutları uygularız.
```
ip config
ipconfig /all	
ARP -a
arp /?
ping x.x.x.x
```
10. UDP ve TCP adında gönderilen paketlerin gidip gitmediğini ya da cevap gelip gelmediği kontrol eden iki farklı İletişim Protokol'ü vardır.
11. UDP, paketlerin tamamının gönderilme zorunluluğunun olmadığı protokoldür ve TCP'ye göre daha hızlı bir bağlantı sağlar fakat kesintiler, kayıplar vs. yaşanabilir. 
12. 


























	
	
	
	
	
