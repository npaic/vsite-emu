## Dobava odgovoarajuće verzije MaNGos-a ##

Za pocetak treba instalirati sljedeće pakete:

-- GCC 4.1.X ( gcc / g++ / cpp / fort77 / g77 / gpp)

-- automake

-- autoconf

-- glibc & glibc-dev(glibc headers) [libc6 ](.md)

-- make

-- mysql-server 4.1 or mysql-server 5.0 && libmysql++-dev

-- libtool

-- OpenSSL (libssl-dev)

-- subversion and patch

-- git

-- zlibc

Ovo radimo pomoću sljedeće naredbe sa konzole

_sudo apt-get install gcc g++ automake autoconf make libmysql++-dev libtool libssl-dev subversion patch zlibc libc6 git git-core pkg-config_

**Nakon ovog konfiguriramo git.**

Prvo upisujemo _/usr/bin/git-scm_

Sada treba zapisati prikazane informacije i unijeti ogovarajuće kada će se to od nas tražiti

_update-alternatives –config git_

**Nabavljanje izvora**

Kloniramo zadnju verziju MaNGos-a pomoću narebe

_git clone git://github.com/mangos/mangos.git mangos_

Nakon ovog koraka se može prijeći na kompajliranje izvora.