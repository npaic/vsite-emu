## Opis ##

Nakon što znamo korisničko ime, šifru, ime baze podataka te imamo osnovni sadržaj baze podataka, u sljedećoj naredbi umjesto username upišemo korisničko ime, umjesto password šifru, umjesto data-base-name ime baze podataka te umjesto data.sql lokaciju i ime datoteke s osnovnim sadržajem baze podataka

## Naredbe i primjeri ##

Osnovna naredba izgleda ovako:
```
$ mysql -uusername -ppassword -hlocalhost data-base-name < data.sql
```

a za sljedeće podatke
```
Korisničko ime = vsite 
Šifra = emu 
Ime baze podataka = vsite_emu
Lokacija osnovnog sadržaja baze podataka = ~/vsiteEmu/dbStart.sql
```

naredba izgleda ovako:
```
$ mysql -uvsite -pemu -hlocalhost vsite_emu < ~/vsiteEmu/dbStart.sql
```