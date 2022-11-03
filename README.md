# Packet Tracer ToDo List

1. 2 adet PC oluştur, Ethernet'ten direkt bağla ve PC'lere IP ver. Terminal'den Ping at.
2. 1 PC ve 1 Router'ı direkt Ethernet'ten birbirlerine bağlayıp
    PC'denTerminal'den Ping at.
3. 3 adet PC'nin olduğu bir Network kurup her bir PC'nin bir
    diğerine Switch aracılığı ile Ping atabilmesini sağla.
4. Aynı Network'ten bir tane daha oluştur.
5. İki Network'ün Router'larını birbirlerine bağla ve
    Configuration'larını yap. Yaptığın Configuration'ları yedekle.

```
    **show history** (Yazılan tüm komutları gösterir)
    **show ip interface** (Interface hakkında detaylı bilgi verir)
    **show ip interface brief** (Intereface hakkında özet bilgi verir)
    **show run** (Çalışan Interface'leri gösterir)
    **no ip address** (Verilmiş olan IP'yi siler)
```


6. Basic Router Configuration'ları yapıp kaydet.
7. Yeni bir Router oluşturup mevcut Router'lardan birisine bağla. Bağladığın Router'a mevcuttaki Router'lardan birisinden TelNet ile Configuration'larını yap.
8. Başka bir Router daha oluştur. Bu Router'a TelNet ile Random Password'lar ata. Daha sonra bu Router'a bağlanılamayacağı için Password Resetleme sürecini uygula.

```
     **show version** (Router hakkında bilgi verir, Router'ın hangi Conf modunda açıldığını gösterir)
     **show flash** (Kullandığımız cihazı IOS'unun adını gösterir)
```

9. 1 adet Server oluştur. Bu server'ı TFTP trafiğini sağlayabilecek hale getiren süreci uygula.

10. Router'lardan herhangi birinin NVRAM'ine yedekleme sürecini uygula.
11. Router'lardan herhangi birinde Flash'ı sil. IOS yüklenememe sorunu ile karşılaşıp çözüme giden süreci uygula.


```
     **delete** (Router'ların CLI'ında silme komutudur) delete flash
    (Router'daki Flash bölümünü komple siler)
    
    **show ip route** (Router'a yapılan IP Routing'leri ve Router'a Directly Connected olan Network'leri gösterir)    
```

12. IP Routing'i 0.0.0.0 0.0.0.0 ile yap.
13. Router'lara Serial Port'tan bağlantı kur.(Eski, güncel olarak sektörde kullanılmaz. Fakat CCNA Sınavlarında çıkar.)
14. Birden çok Router'a TelNet ile bağlan, TelNet'ler arasındaki Session'ları düzenle.


```
    **show sessions** (Router üzerinden kaç tane Router'a bağlı olunduğunu yani kaç tane "oturum" olduğunu gösterir.)
```

15. Router'lara isim ata.

```
    **show hosts** (Router'ların IP'lerini ve isimlerini listeler.)
    **show cdp neighbors** (Komşu Network cihazlarını gösterir, bazı durumlarda IP'leri bilemez ve Directly Connected IP'ler görüntülenir.)
```

16. DNS sürecini uygula.
17. DHCP sürecini uygula.
18. 4 şubeli ödevi yap.
19. Dynamic Routing sürecini uygula.


