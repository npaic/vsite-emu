# 20. POSTAVLJANJE POSTAVKI MySQL-a #


Potrebno je odkomentirati (maknuti #) sljedeću liniju u konfiguracijskoj datoteci Apache-a:

<b># extension=php_mysql.so</b>

Konfiguracijska datoteka mysql-a (<b>my.cnf</b>) je obično pod: <i>/etc/mysql/my.conf</i>
<br>

MySql po defaultu  kreira korisnika koji radi bez lozinke. Za promjenu root lozinke koristiti:<br>
<br>
mysql> USE mysql;<br>
mysql> UPDATE user SET Password=PASSWORD('new-password') WHERE user='root';<br>
mysql> FLUSH PRIVILEGES;<br>


<h2>Kreiranje korisnika</h2>

Korištenje root lozinke se ne bi smjelo koristiti, pa je potrebno kreirati korisnika za spajanje baze za PhP script. Jedan od načina dodavanja korisnika u bazu je korištenje panela poput webmin ili PhpMyAdmin za jednostavnu dodjelu pristupa bazi pojedinim korisnicima.<br>
<br>
<b>1.način: Instalacija PhpMyAdmin</b> - može se obaviti naredbom:<br>
<i>apt-get install phpmyadmin</i>

Ako se koristi uz Apache, dodati sljedecu liniju u konfiguraciju datoteku Apache-a:<br>
Include /etc/phpmyadmin/apache.conf<br>
<br><br>
<b>2.način: Instalacija Webmin-a</b>  - downloadom sa službenih stranica: <a href='http://www.webmin.com'>http://www.webmin.com</a>