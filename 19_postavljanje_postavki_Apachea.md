# 19. POSTAVLJANJE POSTAVKI APACHE-a #

Konfiguracijska datoteka Apache poslužitelja je <b>httpd.conf</b> i defaultno se nalazi u <i>/etc/httpd/conf</i> direktoriju. Njenim sadržajem se definira ponašanje instaliranog Apache poslužitelja. Sadrži mnostvo opcija koje su već inicijalizirane prilikom instalacije, a moguće je promijeniti njihove postavke.

Prije samog postupka konfiguracije, potrebno je odrediti ime poslužitelja, mrežno sučelje koje će primati zahtjeve, gdje će se nalaziti konfiguracijske i log datoteke, te u kojem će direktoriju biti smješteni korišteni dokumenti.

<br><br>
<b>Sintaksa</b>:<br>
<br>
- Jedna direktiva po retku (dodati “\” ako direktiva prelazi u novi red)<br>
<br>
- Directive nisu case sensitive<br>
<br>
- Direktive smještene u glavnoj konfiguracijskoj datoteci se primjenjuju na cijeli server; opseg direktive se može ograničiti “zatvaranjem” u sekcije, npr: <br>
<br>
<Directory><br>
<br>
 <br>
<br>
<Files><br>
<br>
 <br>
<br>
<Location><br>
<br>
<br>
<br>
- Direktivom include se uključuju druge konfiguracijske datoteke ako je to potrebno<br>
<br>
- Komentari: <b>#</b> ispred linije<br>
<br>
- Moguće provjeriti sintaksne greške korištenjem naredbe <b>apachectl configtest</b>


Moguće je prepisati (override) direktive u httpd.conf datoteci upisivanjem u <b>.htaccess</b> datoteci (sintaksna pravila su jednaka), čije izmjene odmah stupaju na snagu, bez potrebe za resetiranjem.  Njene izmjene se odnose na direktorij u kojem se nalazi, te sve poddirektorije. U tom slučaju u httpd.conf datoteci ne smije postojati linija <b>AllowOverride None</b>.<br>
<br>
<br><br>
Neke od osnovnih opcija:<br>
<br>
- <b>ServerTokens</b> određuje što će se staviti u server odgovor HTTP zaglavlja (postavljanje na Prod postavlja zaglavlje HTTP odgovora u oblik “Server: Apache”)<br>
<br>
- <b>Listen</b> direktiva određuje port koji se sluša<br>
<br>
- Moguće je pojednostavniti rad isključenjem nepotrebnih modula koji su uključeni u Apache instalaciju. Pretraži se httpd.conf i zakomentira (#) svaka linija koja sadrži <b>LoadModule</b>.<br>
<br>
- Ograničavanje veličine zahtjeva se obavlja preko <b>LimitRequestBody</b> directive<br>
<br>
- Ograničavanje broja child procesa preko <b>MaxClients</b> (u slučaju nedovoljne količine memorije za obradu istodibnih zahtjeva)<br>
<br>
- Korištenjem modula <b>mod_security</b> se podešavaju dodatne opcije (filtriranje, granica uploada, maskiranje server identiteta, prevencija napada, …)<br>
<br>
<br><br>
Za kompletnu dokumentaciju posjetiti<br>
<br>
<b><a href='http://httpd.apache.org/docs/2.0'>http://httpd.apache.org/docs/2.0</a></b>

gdje su detaljno objašnjeni svi parametri konfiguracijske datoteke.