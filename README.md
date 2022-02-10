# obdelava-podatkov
Projekt je nastal v okviru predmeta programiranje 1 (študijsko leto 2021/2022) na Fakulteti za matematiko in fiziko v Ljubljani.<br>
V mapi so zbrane datoteke potrebne za obdelavo. Zajem podatkov je narejen prek python datoteke v mapi, ki ima tudi temu primerno ime. Html datoteke, prek katerih bo le-ta uspel prejeti podatke, je prav tako shranjen v mapi, podatki pa so urejeni v obliki slovarja ({leto : html}). V mapi sta potem še dva csv datoteki (razlika opisana spodaj), prek katerih je nato storjena analiza v istoimenski datoteki.

# Avtor 
Matej Novoselec

# IGRALCI LIGE NBA
Analiziral bom statistiko/podatke o igralcih iz ameriške lige NBA, v sezonah, ko je dostop do podatkov mogoč (1996/97-2020/21). Te podatke, ki ji bom po letih dobil na povezavi: https://www.nba.com/stats/players/traditional/?SeasonType=Regular%20Season&sort=PTS&dir=-1&Season=2020-21, bom nato še dopolnil s podatki, ki jih bom dobil iz širše baze, ki jo prav tako vodi NBA in je na povezavi: https://www.nba.com/players, če omogočimo "show historic"

# OPOMBA
Po posvetu z asistentom, sem se odločil spletno stran iz katere bom zajemal podatke spremeniti (zajem je bil prek prejsne strani pretežek - potrebno bi bilo znanje zajemanja s pomočjo JavaScripta). Glavni podatki, ki sem jih imel namen zajeti na novo izbrani strani/straneh se na določenih mestih prekrivajo, zato ne bo potrebno spremeniti vseh hipotez. <br>
Url novih strani: od let https://www.basketball-reference.com/leagues/NBA_1980_per_game.html do https://www.basketball-reference.com/leagues/NBA_2020_per_game.html<br>

# CSV DATOTEKI
V projektu sta priloženi 2 csv datoteki, obe vsebujeta iste tipe podatkov (smiselno navedeni spodaj- podatki, ki jih bom zajel za vsakega igralca, njihov pomen pa je naveden tudi v prvi vrstici vsake izmed csv datotek).<br>
players_repeat.csv datoteka ima zajete podatke po igralcih, podatki pa se lahko v tej datoteki večkrat ponovijo (število ponovitev je odvisno od števila let, ko je igralec igral v ligi), druga datoteka, players.csv pa predstavlja datoteko na kateri bo analiza izvedena in imamo podatke za posameznega igralca smiselno "združene" (poračuna se povprečje vsake izmed kategorij glede na podatke po vsakem letu), tako je ponovitev za vsakega igralca le ena sama.

# Za vsakega igralca bom zajel:
Najbolj smiselni in primerni podatki za obdelavo so sledeči/navedeni spodaj, ki jih bom tudi analiziral: <br>

-ime, priimek<br>
-pozicijo (obstaja 5 pozicij PG, SG, PF, SF, C - poziciji, ki se končata na G predstvaljata igralce pozicije G, poziciji ki se končata z F predstavljata pozicijo forward, črka C pa predstavlja igralca pozicije center)<br>
-povprečje metov (iz igre, tako metov za 3 kot tudi za 2 točke)<br>
-povprečni odstotek meta za 2
-povprečni odstotek meta za 3
-povprečni odstotek prostih metov<br>
-povprečje točk<br>
-povprečno število asistenc<br>
-povprečno število skokov

# Delovne hipoteze:
-HIPOTEZA 1: Vsaka pozicija je v ligi številčno enakomerno zastopana (igralcev posamezne pozicije je okvirno enako)<br>

-HIPOTEZA 2: Igralci pozicij G (guards) dosežejo povprečno več točk na tekmo kot igralci pozicij F (forwards)<br>

-HIPOTEZA 3: Igralci pozicij G (guards) dosežejo povprečno več asistenc na tekmo kot igralci pozicij F (forwards) in igralci pozicije C (center) skupaj<br>

-HIPOTEZA 4: igralci pozicije C (center), dosežejo povprečno več skokov, kot igralci pozicij F (forwards) in G (guards) skupaj<br>

-HIPOTEZA 5: Igralci pozicij G (guards) imajo največji odstotek meta (povsod-skupni odstotek), sledijo jih igralci pozicij F (forwards) in nato igralci pozicije C (center)<br>

-HIPOTEZA 6: Igralec z boljših odstotkom meta za 3 ima tudi boljši odstotek meta za 2 (obstaja korelacija med odstotkom meta za 2 in odstotkom meta za 3)<br>
