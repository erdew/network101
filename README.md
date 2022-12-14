# Packet Tracer ToDo List

1. [x] (1) 2 adet PC oluştur, Ethernet'ten direkt bağla ve PC'lere Static IP ver. PC'lerin Command Prompt'undan Ping at.
2. [x] (2) 1 PC ve 1 Router'ı direkt Ethernet'ten birbirlerine bağlayıp
    PC'nin Command Promt'undan Ping at.
3. [x] (3) 3 adet PC'nin olduğu bir Network kurup her bir PC'nin bir
    diğerine Switch aracılığı ile Ping atabilmesini sağla.
4. [x] (4) Farklı 1 adet daha Network oluştur.
5. [x] (5) İki Network için de iki adet Router oluştur. Router'larını birbirlerine bağla ve
    Configuration'larını yap. Yaptığın Configuration'ları yedekle. Oluşturduğun Network'lerin iletişimi için Router'lara Static IP Routing yap.
```
    ==show history== (Yazılan tüm komutları gösterir)
    ==show ip interface== (Interface hakkında detaylı bilgi verir)
    ==show ip interface brief== (Intereface hakkında özet bilgi verir)
    ==show run== (Çalışan Interface'leri gösterir)
    ==no ip address== (Verilmiş olan IP'yi siler)
```
6. [x] (6) Basic Router Configuration'ları yap ve yaptığın tüm Configuration'ları yedekle.
7. [x] (7) Yeni bir Router oluşturup mevcut Router'lardan birisine kablo ile bağla. Yeni eklediğin Router'a mevcuttaki Router'lardan birisi üzerinden TelNet ile bağlantı kur, Basic Configuration'ları yap ve yaptığın tüm Configuration'ları yedekle.
8. [x] (8) Herhangi bir Router için IP Routing'i 0.0.0.0 0.0.0.0 ile yap.
9. [x] (9) Yeni bir Router oluştur. Bu Router'ın Console ve Enable Port'larına Random Password'lar ata. Bilmediğimiz bir Password atanmış olacağından bu Router'a bağlanabilmek için Password Resetleme sürecini uygula.
```
     ==show version== (Router hakkında bilgi verir, Router'ın hangi Conf modunda açıldığını gösterir)
     ==show flash== (Kullandığımız cihazı IOS'unun adını gösterir)
```
10. [x] (10) 1 adet Server oluştur. Bu Server'ın DHCP Protokol'ü ile bir Network'e otomatik olarak IP dağıtmasını sağla.
11. [ ] (11) Router'lardan herhangi birinin NVRAM'ine yedekleme sürecini uygula.
12. [ ] (12) Router'lardan herhangi birinde Flash'ı sil. IOS yüklenememe sorunu ile karşılaşılacağından bunun çözüme giden süreci uygula.
```
     ==delete== (Router'ların CLI'ında silme komutudur) delete flash
    (Router'daki Flash bölümünü komple siler)
    
    ==show ip route== (Router'a yapılan IP Routing'leri ve Router'a Directly Connected olan Network'leri gösterir)    
```
13. [x] (13) Router'lara Serial Port'tan bağlantı kur.(Eski, güncel olarak sektörde kullanılmaz. Fakat CCNA sınavlarında çıkar.)
```
    ==show sessions== (Router üzerinden kaç tane Router'a bağlı olunduğunu yani kaç tane "oturum" olduğunu gösterir.)
```
14. [ ] (14) Birden fazla Router'a TelNet ile bağlan, TelNet'ler arasındaki Session'ları düzenle.
```
    ==show hosts== (Router'ların IP'lerini ve isimlerini listeler.)
    ==show cdp neighbors== (Komşu Network cihazlarını gösterir, bazı durumlarda IP'leri bilemez ve Directly Connected IP'ler görüntülenir.)
```
15. [x] (15) DNS sürecini uygula.
16. [ ] (16) 4 şubeli ödevi yap.(Network'lerden en az birini TelNet bağlantısı ile konfigüre et. En az bir Network'e Serial Port ile bağlantı kur. Tüm Network'ler için DNS ve DHCP kullan. Dynamic Routing Protokollerinden birisini kullanarak Network'ler arasındaki iletişimleri düzenle. Yaptığın tüm konfigürasyonları ve işlemleri yedekle.)



