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
12. TCP, paketlerin tamamının gönderilme zorunluluğu olan protokoldür. UDP'ye göre bazı bağlantılarda daha yavaş olabilir fakat ne gönderildiyse hedef gönderilenlerin tamamına ulaşır.
13. Network'ler arasında bağlantı kurmak istediğimizde artık Switch yeterli olmamaktadır. Çünkü Network'ler arası bağlantı demek Layer 3 cihazların ihtiyaç duyulduğu bir bağlantı demektir.
14. Router'lar Layer 3'te çalışan cihazlardır.
15. Bir Router'ın her bir Interface'i yani Ethernet Port'u başka bir Network'e bağlanır.
16. Router'ın Interface'lerinden birisine bağlı olan bir Switch ile ona bağlı olan Client'lerin tamamı bir Network'un içinde demektir.
17. Client'lerden, Router'ın başka bir Interface'inde bulunan diğer Client'lere paket göndermek istendiğinde bu paketlerin Router'a gönderilebiliyor olması gerekmektedir.
18. Router'ların Interface'lerine atadığımız IP adresleri o Interface'e bağlı olan Network'teki tüm Client'ler için "Default Gateway"'dir.
19. Default Gateway Network'ün çıkış kapısıdır.
20. Default Gateway genellikle tercihen o Network'teki atanabilir ilk IP adresidir.
21. Client'ler paketleri kendi sahip oldukları IP ve Subnet Mask bilgisine göre gönderirler. Çünkü sahip oldukları tek bilgi kendi üzerlerine yazılmış olan, kendileri hakkındaki bilgilerden ibarettir. O Client'e sadece hedef IP adresi bilgisi verilir ve IP adresinin hangi Subnet Mask'a sahip olduğunu bilmediği için kendi sahip olduğu Subnet Mask'la karşılaştırarak hangi Network'e gideceğini anlar. Yani hedefin Subnet Mask'ı ile Client'in kendi Subnet Mask'ı aynı ise bu hedefin Client'in kendisi ile aynı Network'te olduğu anlamına gelir ve bu paketi Switch'e gönderir. Fakat hedefin Subnet Mask'ı farklı ise kendisinin hedef ile aynı Network'te olmadığını anlayıp direkt olarak Gateway'e gönderir.
22. Bu bağlamda bir Network'te yapılacak olan Broadcast maksimum o Network'ün Gateway'ine yani Router'ın içerideki Interface'ine kadar gidebilir.
23. Bir Network'ün ilk IP'si o Network'ın ID'si anlamına gelir.
24. Bir Network'ün en son IP'si ise o Network'ün Broadcast ID'si anlamına gelir.
25. İlk ve son IP'ler hiç bir cihaza IP olarak atanamazlar. Çünkü bu IP'lerin yukarıdaki maddelerde bahsedilen özel anlamları vardır.
26. Bir Network'te toplamda ne kadar IP atanabileceğini "Subnet Mask" belirler.
27. Network'ün toplamda kaç Client içereceğini ifade eden sayıya Host denir.
28. Subnet Mask'ın evrensel ve standart olarak IP'lerin yanına "/x"(192.168.1.0/24) ile beraber yazılan versiyonuna "Prefix" adıverilmiştir.
29. Bir önceki maddedeli /24 sayısı Subnet Mask'ın Binary cinsinden hesaplandığında soldan kaç adet 1 içerdiğini belirtir.
30. IP'ler 2^32 üzerinden hesaplandıkları için, Subnet Mask'ta maksimum 32 adet 1 veya 0 olabilir.
31. Prefix'in 24 olması, soldan ilk 24 Bit'lik Binary cinsinden 1 sayısının Network'ü ifade ettiği anlamına gelir.
31. 24 tane 1 var ise her Octed'in 8 bit'ten oluştuğunu hesaba kattığımızda soldan 3 Octed'in Network'ü ifade ettiğini anlayabiliriz.
32. Yukarıdaki senaryoya göre 192.168.1.0 bu Network'ün ID'sidir. 192.168.1.255 ise Broadcast'dir.
33. Host olarak son Octed'in tamamı kaldığı için 2 üzeri 8'e eşit Host sayımız var demektir. 2 üzeri 8 = 256'dır. İlk ve son IP'leri atayamadığımız için 256 - 2 = 254 toplam atanabilir IP sonucuna erişebiliriz. Yukarıdaki senaryoya göre IP ve Subnet Mask'ın Binary karşılıkları;
```
-------------------------------------
| 	   192.168.1.40/24          |
|11000000.10101000.00000001.00101000|
-------------------------------------
---------------------------
|	    /24		  |
|	255.255.255.0	  |
---------------------------
```
34. Subnet Mask'ların maksimum değeri 255 olabilir çünkü; Binary olarak Octed üzerinden soldan sağa ilerledikleri için sadece Binary 1 olanların değerlerinin toplamına eşit olan sayıları alabilirler.
35. IP'ler maksimum 2 üzeri 32'den verilmek zorunda olduğu için gerçek dünyada IP'lerin yetersiz kalması gibi bir tehlike söz konusudur.
36. Muhtemelen internetin ilk geliştirildiği dönemlerde bu denli bir trafik oluşacağı öngörülmemişti.
Ayrıca teknik olarak IP'ler üzerinde yapılan bir hata yüzünden de çok ciddi sayıda IP gerçek dünyada kullanılamaz durumdadır.
37. IP'ler A, B, C, D, E Class'larına ayrılırlar;
```
A)  0.0.0.0  - 127.255.255.255 /8, 16, 24(Subnetting yapılmamış)
B) 128.0.0.0 - 192.255.255.255
C) 192.0.0.0 - 223.255.255.255
D) 224.0.0.0 - 239.255.255.255
E) 240.0.0.0 - 255.255.255.255
```
38. 127 Octed'i ile başlayan hiç bir IP kullanılamaz.
39. Bu adrese "Loopback Address" denir. Fakat herhangi bir makinede 127 ile başlayan herhangi bir IP Ping attığımızda bu kendi Ethernet Port'unu Ping'lediği anlamına gelir. Cevap gelmesi Ethernet Port'unun çalışır durumda olduğunu gösterir. Cevap gelmemesi bozuk olabileceği anlamına gelebilir.
40. Loopback Address olarak 127'nin belirlenmesi aslında teknik bir hatadır.
Çünkü 127'lik IP bloklarının tamamını içerdiği için 2^24 farklı IP adresinin kullanılamamasına sebep olur.
41. D Class IP'ler(224.0.0.0 - 239.255.255.255) sadece Multicast yayınlar için kullanılır.
42. E Class IP'ler(240.0.0.0 - 255.255.255.255) geliştirici kurullarının çalışmaları için ayrılmıştır.
43. Modemin dış bacağına A, B, C Class'larından başka bir IP atanmaz. Bu IP'lerin internete çıkma yeteneği olduğu için ve bir IP'yi sadece bir modem kullanabileceği için bu IP'ler ücretlidir. Fakat yukarıdaki durum sadece modemin dış bacağı yani internete çıkan Interface'i ile alakalıdır. Yani modemin öteki yüzünde yani bizim cihazlarımızı modeme bağladığımız kendi Network'ümüzde bu IP'leri kullanmamız hem çok mantıksız hem de mümkün değildir. Çünkü durum böyle olsaydı biz her internete bağlanmak için kullandığımız cihaz için ekstra IP kiralamak zorunda kalırdık. Bunun yerine kendi Network'lerimizde Private olarak ayrılmış IP'leri kullanırız. Zaten evlerimizdeki modemler de bu şekilde yapılandırılmıştır. Örneğin, telefonunuza modemden bağlandığınızda muhtemelen telefonunuza atanan IP adresi 192.168.0.x'li bir IP adresi olacaktır.
44. Private IP adresleri şunlardır;
```
10.0.0.0 - 10.255.255.255
172.16.0.0 - 172.31.255.255
192.168.0.0 - 192.168.255.255
```
45. Eğer çok büyük bir şirket tipolojisine sahipsek 10.0 Network'ünü kullanmak daha maktıklıdır.
Çünkü diğerine göre 2^8 daha fazla IP tanımlanabilir.
46. IP'lerin dağıtımını ISP(Internet Sevice Provider) yapar. ISP Private IP'leri yukarıda anlattığımız sebeplerden dolayı ayırmıştır. Sonuç olarak A, B, C Class'larından başka hiç bir IP internete çıkamaz. Bir Network'ün tamamının internete çıkabilmesi için gerçek IP'ye sahip bir dış bacağa bağlı olması yeterlidir. Private IP'ler ücretsizdir. ISP size atadığı Static IP'yi başkasına veremez.
47. Aslında ISP direkt olarak sizin Modem'inize gerçek IP atamaz. Sadece sizin Servis Sağlayıcı'nıza gerçek bir IP verir. Servis Sağlayıcı'lar tıpkı kendi evlerimizde kullandığımız Modem'in bağladığımız her cihaz için yapılandırıldığı gibi Private IP'ler ile mahallelere caddelere, sokaklara, binalara yerleştirdiği kablolar aracılığı ile kendi merkezleri ve apartmanlardaki ağları birbirlerine bağlarlar. Evdeki bir bilgisayardan Modem'e CAT6 kablo çekmekten tek farkı mesafenin çok uzak olmasıdır. Dolayısıyla Servis Sağlayıcı da bizim Modem'imizden kendi merkez HOP'una kadar gerçek IP atamak zorunda değildir. Onlar da aynı şekilde Private IP'lerle Daire, Apartman, Sokak, Cadde, Mahalle, Semt, Şehir, Ülke tipolojisini oluştururlar. Servis Sağlayıcının internete çıkan dış bacakların gerçek IP olmak zorundadır. Yani örneğin Türk Telekom, müşterilerini kendisine bağlı aylarındaki tüm Network'leri ISP'den aldığı bu gerçek IP üzerinden internete çıkartıyor.



















	
	
	
	
	
