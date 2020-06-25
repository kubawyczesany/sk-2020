# Zadanie 2

Projekt sieci spełnił oczekiwania, organizacja po uwzględnieniu nowych wymogów chce podzielić dotychczasowe sieci na kilka podsieci.

1. Zaprojektuj oraz udokumentuj prototyp rozwiązania z wykorzystaniem oprogramowania ``CISCO Packet Tracer``, ``VirtualBox`` lub podobnego. 

## Schemat

![zadanie 2](stage-02.svg)

## Charakterystyka
  * LAN 1 pozostaje bez zmian
  * LAN 2 zostaje podzielony na 3 równe podsieci
  * LAN 3 zostaje podzielony na 3 podsieci z uwzględnieniem
    * podsieć 1 ma obsłużyć do 512 hostów
    * podsieć 2 ma obsłużyć do 10 hostów
    * podsieć 3 ma obsłużyć do 32 hostów
  * Usunięty został również link pomiędzy Routerem (LAN 1) a Routerem (LAN 2)
  * Uwzględnij zmiany w tablicy routingów

## Zawartość

 ## Adresy poszczególnych sieci IP
 
  * LAN 1: 192.107.0.0/22 : dostępne adresy: od 192.107.0.1 do 192.107.3.254

  * LAN 2: (podział na 3 równe)
  * SUBNET_1: 192.109.0.0/24 : dostępne adresy: od 192.109.0.1 do 192.109.0.254 
  * SUBNET_2: 192.109.1.0/24 : dostępne adresy: od 192.109.1.1 do 192.109.1.254 
  * SUBNET_3: 192.109.2.0/24 : dostępne adresy: od 192.109.2.1 do 192.109.2.254

  * LAN 3: (podział ze względy na różną ilość hostów)
  * SUBNET_1: 192.108.0.0/23 : dostępne adresy: od 192.108.0.1 do 192.108.1.255 
  * SUBNET_2: 192.108.3.128/26 : dostępne adresy: od 192.108.3.129 do 192.108.3.191 
  * SUBNET_3: 192.108.3.224/28 : dostępne adresy: od 192.108.3.225 do 192.108.3.239

 ## Adresacja linków pomiędzy routerami
  * LAN1 <=> LAN3 192.207.4.1 <=> 192.207.0.2 \
  * LAN3 <=> LAN2 192.207.4.2 <=> 192.207.4.3


 ## Tablice routingów na poszczególnych routerach
  * Router 1:
  * 192.108.0.0/22 via 192.207.0.2  192.109.0.0/22 via 192.207.4.2
  * Router 2:
  * 192.107.0.0/22 via 192.207.0.2 192.108.0.0/22 via 192.207.4.2
  * Router 3:
  * 192.107.0.0/22 via 192.207.4.1  192.109.0.0/22 via 192.207.4.3
 
 
# MODYFIKACJA!
 podsieć 1 ma obsłużyć do **512** hostów
 powinno być **510**
 
