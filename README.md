# Cisco LAN(Local Area Network) Router Config

Bu yazımız da yerel ağlarda nasıl yönlendirme yapılır onu öğreneceğiz.

İlk önce çalışma mantıklarından bahsedelim.

## Router

Routerlar ağ geçitlerine göre ağları tanımlar örnek olarak iki tane networkümüz olduğunu düşünelim bunlardan birisi **1.1.1.1** diğeri ise **1.1.1.2** olsun. İkisi de aynı IP bloğuna sahip ve bu iki IP adresi kendi arasında konuşur.
Router da böylediir örneğin LAN da 2 tane networkünüz olduğunu düşünün bunlardan bir tanesi **192.168.10.10** diğeri ise **192.168.20.10** olarak atayalım. Bunların ağ geçitlerine göre routerlar yönlendirme yapar. 

Madde madde bunların IP yapılandırmalarını yazalım:

- 10'lu Bloğun IP Yapılandırmaları:
  - **Ip Adresi:** 192.168.10.10
  - **Ağ Maskesi:** 255.255.255.0
  - **Ağ Geçidi:** 192.168.10.1

- 20'li Bloğun IP Yapılandırmaları:
  - **Ip Adresi:** 192.168.20.10
  - **Ağ Maskesi:** 255.255.255.0
  - **Ağ Geçidi:** 192.168.20.1


Ip yapılandırmalarını yaptığımıza göre Routera gelip orada ki yapılandırmalarımızı da yapalım:

- Ethernet 0/0 Kartın IP Yapılandırması:
  - **Ip Adresi:** 192.168.10.1
  - **Ağ Maskesi:** 255.255.255.0
 

- Ethernet 1/0 Kartın IP Yapılandırması:
  - **Ip Adresi:** 192.168.20.1
  - **Ağ Maskesi:** 255.255.255.0
 

  Artık Local de olan iki farklı blok konuşabiliyor duruma gelmiştir. Bunun aynısını şimdi Cisco Packet Tracer'da yapalım:


  
