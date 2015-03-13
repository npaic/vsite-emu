# ApacheInstalacija #

APACHE

> gunzip -d httpd-2\_0\_NN.tar.gz

> tar xvf httpd-2\_0\_NN.tar

Ovo kreira novi direktorij unutar trenutnog direktorija.

Konfiguriranje

Najlakši način za prihvaćanje defaultnih vrijednosti je, upisivanjem:
> ./configure

Ukoliko se ne koristi defaultna opcija instalacije;
Najvažnija opcija je prefix= option.
Ona lokalizira mjesto insatalacije.
Također, mogu se odrediti i specifične varijable okoline i moduli:

mod\_alias - to map different parts of the URL tree
mod\_include - to parse Server Side Includes
mod\_mime - to associate file extensions with its MIME-type
mod\_rewrite - to rewrite URLs on the fly
mod\_speling (sic) - to help your readers who might misspell URLs
mod\_ssl - to allow for strong cryptography using SSL
mod\_userdir - to allow system users to have their own Web page directories
Ovo su samo primjeri modula, nisu svi.

Build

Prvo se radi "build"

> make
> make install

Ukoliko do sad nije bilo problema, slijedi konfiguracija.
Ona se svodi na editiranje httpd.conf file.
Datoteka je smještena u PREFIX/conf direktoriju.
Editira se sa vi:
> vi PREFIX/conf/httpd.conf

Testiranje servera

Otvorite preglednik i upišite http://localhost/ in the address box.
Ukoliko velikim slovima piše "Seeing this instead of the website you expected?",
server je dobro instaliran.

document root:
/var/www/www.vsite.hr