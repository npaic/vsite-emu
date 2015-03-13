# instalacija mwEnhanced-a #
Instalacija unrar-a

```
sudo apt-get install unrar
```

raspakiravanje source coda u document root direktoriju

```
cd /var/www/www.vsite.hr
unrar e /home/mangos/mw/MangosWebEnhanced_Rev45_Patch3.3.3a.rar
```

omogucavanje instalacije

```
mv install/DISABLE_INSTALLER.php install/DISABLE_INSTALLER.php.moved
```

u web pregledniku odite a adresu:

localhost/install/

Kada se pruzi prilika kliknuti na "full install sql injection"

Unijeti sve trazene informacije o realm-u, likovima i bazi podataka o svijetu

napraviti super Admin account

### mwEnhanced ostala instalacija ###
ima jos puno lipih stvari koje se mogu podesiti unutar mwEnhanced-a kao sto je forum, news system i sl. ali nisam siguran sto rade sve te stvari i koje nam od njih trebaju.
