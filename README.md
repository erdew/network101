# Packet Tracer ToDo List

1. [x] 2 adet PC oluştur, Ethernet'ten direkt bağla ve PC'lere Static IP ver. PC'lerin Command Prompt'undan Ping at.
2. [x]  1 PC ve 1 Router'ı direkt Ethernet'ten birbirlerine bağlayıp
    PC'nin Command Promt'undan Ping at.
3. [x] 3 adet PC'nin olduğu bir Network kurup her bir PC'nin bir
    diğerine Switch aracılığı ile Ping atabilmesini sağla.
4. [x] Farklı 1 adet daha Network oluştur.
5. [x] İki Network için de iki adet Router oluştur. Router'larını birbirlerine bağla ve
    Configuration'larını yap. Yaptığın Configuration'ları yedekle. Oluşturduğun Network'lerin iletişimi için Router'lara Static IP Routing yap.

```
    ==show history== (Yazılan tüm komutları gösterir)
    ==show ip interface== (Interface hakkında detaylı bilgi verir)
    ==show ip interface brief== (Intereface hakkında özet bilgi verir)
    ==show run== (Çalışan Interface'leri gösterir)
    ==no ip address== (Verilmiş olan IP'yi siler)
```


6. [x] Basic Router Configuration'ları yap ve yaptığın tüm Configuration'ları yedekle.
7. [x] Yeni bir Router oluşturup mevcut Router'lardan birisine kablo ile bağla. Yeni eklediğin Router'a mevcuttaki Router'lardan birisi üzerinden TelNet ile bağlantı kur, Basic Configuration'ları yap ve yaptığın tüm Configuration'ları yedekle.
8. [ ] Yeni bir Router oluştur. Bu Router'ın Console ve Enable Port'larına Random Password'lar ata. Bilmediğimiz bir Password atanmış olacağından bu Router'a bağlanabilmek için Password Resetleme sürecini uygula.

```
     ==show version== (Router hakkında bilgi verir, Router'ın hangi Conf modunda açıldığını gösterir)
     ==show flash== (Kullandığımız cihazı IOS'unun adını gösterir)
```

9. [ ] 1 adet Server oluştur. Bu Server'ı TFTP trafiğini yönetebilir hale getiren süreci uygula.

10. [ ] Router'lardan herhangi birinin NVRAM'ine yedekleme sürecini uygula.
11. [ ] Router'lardan herhangi birinde Flash'ı sil. IOS yüklenememe sorunu ile karşılaşılacağından bunun çözüme giden süreci uygula.


```
     ==delete== (Router'ların CLI'ında silme komutudur) delete flash
    (Router'daki Flash bölümünü komple siler)
    
    ==show ip route== (Router'a yapılan IP Routing'leri ve Router'a Directly Connected olan Network'leri gösterir)    
```

12. [ ] IP Routing'i 0.0.0.0 0.0.0.0 ile yap.
13. [ ] Router'lara Serial Port'tan bağlantı kur.(Eski, güncel olarak sektörde kullanılmaz. Fakat CCNA sınavlarında çıkar.)
14. [ ] Birden fazla Router'a TelNet ile bağlan, TelNet'ler arasındaki Session'ları düzenle.


```
    ==show sessions== (Router üzerinden kaç tane Router'a bağlı olunduğunu yani kaç tane "oturum" olduğunu gösterir.)
```

15. [ ] Router'lara isim ata.

```
    ==show hosts== (Router'ların IP'lerini ve isimlerini listeler.)
    ==show cdp neighbors== (Komşu Network cihazlarını gösterir, bazı durumlarda IP'leri bilemez ve Directly Connected IP'ler görüntülenir.)
```

16. [ ] DNS sürecini uygula.
17. [ ] DHCP sürecini uygula.
18. [ ] 4 şubeli ödevi yap.
19. [ ] Dynamic Routing sürecini uygula.


