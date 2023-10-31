# Cisco LAN(Local Area Network) Router Config

Bu yazımız da yerel ağlarda nasıl yönlendirme yapılır onu öğreneceğiz.

İlk önce çalışma mantıklarından bahsedelim.

## Router

Routerlar, ağları ağ geçitlerine göre tanımlar. Örneğin, iki farklı ağ düşünelim. Birincisi 1.1.1.1, diğeri ise 1.1.1.2 IP adresine sahip olsun. Her iki IP adresi de aynı IP bloğuna ait gibi görünse de, routerlar aslında bu iki IP adresini farklı ağlarda yönlendirir. Örnek olarak, bir LAN ağı düşünelim. İlk ağda cihazlar 192.168.10.10 IP adreslerine sahipken, ikinci ağdaki cihazlar 192.168.20.10 IP adreslerini kullanıyor. Routerlar, bu iki farklı ağı ve ağ geçitlerini kullanarak paketleri doğru bir şekilde yönlendirirler, böylece cihazlar arasında iletişim sağlarlar.

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


# Simulasyon

## 10'lu blok IP ye sahip bilgisayarın yapılandırması:

![image](https://github.com/ugurcomptech/CiscoLANRouterConfig/assets/133202238/ce0827bd-29d0-4304-a321-48d92c54c704)


## 20'lu blok IP ye sahip bilgisayarın yapılandırması:

![image](https://github.com/ugurcomptech/CiscoLANRouterConfig/assets/133202238/d500cb8f-de10-4d42-8ba5-42cd0ad9e3dc)


## Router Yapılandırması:

![image](https://github.com/ugurcomptech/CiscoLANRouterConfig/assets/133202238/99bce4de-a3f2-4c77-9abf-fa4d59fa77d5)


Yapılandırmalarımızı Bitirdik şimdi paketin nasıl gittiğini görelim:



https://github.com/ugurcomptech/CiscoLANRouterConfig/assets/133202238/b02b46f4-e70e-4667-8cc6-5aa0d62a93bd


  
