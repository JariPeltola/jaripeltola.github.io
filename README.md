# jaripeltola.github.io

Käyttäjäsivu, oma verkkotunnus **jarippeltola.com** (tiedosto `CNAME`).
Etusivu ohjaa osoitteeseen [/kojelauta/](https://jarippeltola.com/kojelauta/), jonka sisältö tulee repossa `kojelauta`.

## Valvomo – https://jarippeltola.com/valvomo/

Home Assistantin valvontakamerat, näkyvät vain kirjautuneelle. Sivu (`valvomo/index.html`)
on staattinen eikä sisällä mitään salaista: kaikki kuvat haetaan Home Assistantista
(https://ha.jarippeltola.com), joka vaatii kirjautumisen. Kuvat ladataan HA:n
allekirjoittamilla, 30 s voimassa olevilla linkeillä.

**Kirjautuminen HA-tunnuksilla** (HA:n oma kirjautumissivu, myös kaksivaiheinen tunnistus
toimii). Vaatii kerran HA:n `configuration.yaml`iin ja HA:n uudelleenkäynnistyksen:

```yaml
http:
  cors_allowed_origins:
    - https://jarippeltola.com
```

Vaihtoehtona sivulla voi kirjautua myös pitkäikäisellä tunnuksella (HA → profiili →
Suojaus → Pitkäikäiset käyttöoikeustunnukset), joka ei tarvitse yllä olevaa asetusta.
Kirjautuminen muistetaan vain siinä selaimessa. "Kirjaudu ulos" poistaa sen
(ja HA-tunnuksilla kirjautuessa mitätöi tunnuksen myös HA:ssa).
