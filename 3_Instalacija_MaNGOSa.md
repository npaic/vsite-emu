# Instalacija MaNGos-a #

Nakon kompajliranja, datoteke potrebne za pokretanje MaNGOS-a se nalaze u trentnom radnom direktoriju. Pokretanje MaNGOS-a se vrši u tom direktoriju (inače MaNGOS ne može čitati konfiguracijske datoteke).
Potrebno je namjestiti i konfigurirati MaNGOS prije pokretanja servera.

# Binaries i konfiguracija #

Potrebno je pribaviti .conf datoteke koje sadrže sve konfiguracije.
Postoje dvije .conf datoteke, u direktoriju `src/mangosd/mangosd.conf.dist.in` i u direktoriju `src/realmd/realmd.conf.dist.in.` Nakon što ih kopirate u MaNGOS direktorij `home/opt/mangos` trebate pobtisati `.dist.in` na kraju imena obje datoteke.
Kada su kompajlirane binari datoteke i konfiguracijske datoteke u istom direktoriju, `bin/win32_release`, možete ih tamo ostaviti radi lašeg update-a jezgre, ili staviti u drugi direktorij radi lakšeg pristupa.
Ukoliko server želite maknuti u drugi direktorij, treba kopirati sve .dll, .exe i .pdb datoteke u novi direktorij zajedno sa .conf datotekama.