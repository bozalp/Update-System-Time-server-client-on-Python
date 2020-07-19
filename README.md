# Update-System-Time-server-client-on-Python
### İstemci(client) saatini sunucu(server) saatine göre ayarlayan program
#### Yazar: Batuhan ÖZALP
#### Program dili: Python3
#### Çalışan platformlar: Linux tabanlı işletim sistemleri
* Sunucu **TCP** 142. portu dinlemektedir.
* İstemci sunucu bağlantısı için sunucunun IP adresini yazarak bağlanabilmektedir.
#### Nasıl Çalışır?
CMD ya da terminal üzerinden önce server.py bulunduğu kısımda **python server.py** yazıp çalıştırılır. Daha sonra client tarafında client.py dosyasının bulunduğu yere gidip **python client.py** komutları çalıştırılır. Linux'ta **sudo python3 server.py-client.py** şeklinde yazılmalıdır. Daha sonra client kısmından server bilgisayarının ip adresi girilerek bağlantı sağlanır. 

Server programı çalıştırıldğında ekrana server zaman dilimi(+5, -3 gibi) ve server zamanı gün, ay, saat ve yıl olarak ekrana bastırılır. Client ekranına ise serverdan gelen milisaniye cinsinden değer, serverın UTC değeri, degisecek zaman dilimi ve ayarlanması gereken zaman ekrana yazdırılır. Client zaman dilimini server.py dosyası üzerinden **zaman_dilimi** isimli değişken ile değiştirilebilir. Saati ayarlamak için milisaniye cinsinden veri gönderilir. Veri gönderirken geçen zamanı ayarlanma isteği geldiği anda client tarafında bir timer kullanılarak zaman bilgisi ulaştığında timer bilgisi de gelen mesajın üstüne eklenip gecikme oluşmaması sağlanmaya çalışılmıştır.
