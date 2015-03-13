Downloadi

samo MPQE
http://filebeam.com/9512c5cc36ca9223183bdeec5a4b5c65

AD.exe + MPQE

http://www.megaupload.com/?d=MJ9ZOEEJ

VMAP

http://filebeam.com/0fa2b9b14812d70f953cce099609f92b

Tutoriali

http://mangos-debian.blogspot.com/2009/03/compiling-mangos-on-debian-4050.html
http://wowps.org/forum/t52-guide_setting_up_mangos_server.html
http://wowps.org/forum/t69-mangos_upgrade_latest_revision.html
http://www.maxcheaters.com/forum/index.php?topic=25216.0;wap2

http://www.mmowned.com/forums/mangos-guides/154004-guide-how-create-make-vmaps-your-mangos-server-1-2-3-user-friendly.html

Upute

<b>1. u MySql-u napraviti sve potrebne baze</b>

  * Kreirati dvije baze, prva se treba zvati "realmd",druga "mangos", treća "characters".

  * Nakon toga je potrebno baze restorati iz sql-dumpa "realmd.sql" restorati realmd bazu.
  * Bazu "mangos" ćemo restorati iz YTDB za mangos.
  * Characters iz characters.sql



<b>2. Podešavanje konfiguracije</b>

  * U mangos direktoriju u folderu se nalaze dvije konfiguracijske datoteke        "Mangod.conf" i "Realmd.conf", tu treba biti i "ScriptDev2.conf".


Pr.

<i>

#####################################<br>
# MaNGOS Configuration file #<br>
#####################################<br>
ConfVersion=2008022901<br>
<br>
RealmID = 1<br>
DataDir = "data"<br>
LogsDir = "Logs"<br>
LoginDatabaseInfo = "127.0.0.1;3306;root;password;realmd"<br>
WorldDatabaseInfo = "127.0.0.1;3306;root;password;mangos"<br>
CharacterDatabaseInfo = "127.0.0.1;3306;root;password;characters"<br>
MaxPingTime = 30<br>
WorldServerPort = 8085<br>
BindIP = "0.0.0.0"<br>
<br>
<br>
<br>
############################################<br>
# MaNGOS realmd configuration file #<br>
############################################<br>
ConfVersion=2007062001<br>
<br>
LoginDatabaseInfo = "127.0.0.1;3306;root;password;realmd"<br>
LogsDir = "logs"<br>
MaxPingTime = 30<br>
RealmServerPort = 3724<br>
BindIP = "0.0.0.0"<br>
PidFile = "./realmd.pid"<br>
LogLevel = 0<br>
LogTime = 0<br>
LogFile = "Realmd.log"<br>
LogTimestamp = 0<br>
LogFileLevel = 0<br>
LogColors = ""<br>
UseProcessors = 0<br>
ProcessPriority = 1<br>
RealmsStateUpdateDelay = 20<br>
<br>
############################################<br>
# ScriptDev2 Configuration file<br>
############################################<br>
# This file must be placed within the directory which holds mangosd.conf and realmd.conf<br>
ConfVersion=2008011901<br>
<br>
ScriptDev2DatabaseInfo = "127.0.0.1;3306;root;password;scriptdev2"<br>
<br>
</i>

<b>3.Extractanje mapa iz World of Warcraft instalacije</b>

  * Stavite ad.exe u WoW instalacijski direktorij
  * Tamo kreirajte novi direktorij zvan "maps"
  * Pokrenite "ad.exe" i pričekajte
  * Kada je gotovo kopirajte "maps" direktorij u ManGOS folder.
  * Obrišite maps direktorij iz WoW foldera
  * U maps folderu bi trebalo biti 3000+ mapa


<b>4. Extrakcija Virtualnih mapa</b>

  * Odzipajte VMAPS.zip u WoW instalacijski direktorij.
  * Pokrenite "makevmaps\_simple.bat" batch file.
  * Nakon što završi kreirati će se folder "vmaps".
  * Kopirajte "vmaps" direktorij u ManGOS folder.


<b>5. Extractiranje DBC</b>


  * U ManGos direktoriju kreirajte folder "dbc"
  * Stavite "mpqe.exe" u {WoW instalacijski direktorij}\Data\enUS (ili euro ovisi o verziji)
  * Pokrenite mpqe sa parametrima

> mpqe /p locale-enUS.MPQ DBFilesClient\**.dbc**

  * mpqe će početi extractirati dbc datoteke u folder MPQOUT\DBFilesClient


  * Trebao bi extractirati iz ovih datoteka:


  * Kada je extractiranje gotovo kopirajte dbc datoteke u "dbc-folder" u ManGos direktoriju.

  * Nakon toga obrišite dbc datoteke iz WoW foldera (trebalo bi biti oko 176 file-ova).




