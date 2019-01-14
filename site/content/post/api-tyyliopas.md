---
title: 'REST rajapintojen standardointi tyylioppaan avulla - 6 hyötynäkökulmaa'
date: 2019-01-12T15:04:10.000Z
description: >-
  API -tyyliopas on luonnollisesti tärkeä yrityksille, joilla on useita rajapintoja ja niitä suunnittelee sekä toteuttaa useammat ihmiset. Kuitenkin yritys, jolla on jo muutama rajapinta, hyötyy merkittävästi tuottamalla edes perusasiat standardoivan API -tyylioppaan. Mitä ne perusasiat ovat, käsitellään alla. APIt ja alustat kulkevat käsi kädessä ja siksi API -tyyliopas on olennainen osa myös alustojen kehittämistä ja ylläpitoa. Artikkelissa avataan API -tyylioppaan hyötyjä kuudesta eri näkökulmasta.
image: /img/blog-chemex.jpg
---

## Mikä on API -tyyliopas?

Englanninkielessä esiintyy tämän asian yhteydessä termejä kuten “API Style Guide”, “API Design Guide” ja “API Guidelines”. Rakkaalla lapsella on monta nimeä, mutta kyse on samasta asiasta. Tunnetuilla suurilla ja pienillä yrityksillä on omat API -tyylioppaansa.

Tyyliopas ei ota kantaa käytettyyn ohjelmointikieleen, vaan antaa reunaehtoja muotoilulle ja toteutukselle vähän samaan tapaan kuin graafiset ohjeistot yrityksen logon käytöstä. Yhtä lailla yleisesti käytetty Open API spesifikaatio luo kehikon API:n kuvaukselle, mutta jättää yksityiskohdat kuten esimerkiksi  virheenkäsittely ja parametrien nimeämiskäytännöt soveltajan vastuulle. Tunnetusti paholainen asustaa juuri yksityiskohdissa. Lyhyesti sanottuna, API -tyyliopas on keino standardoida APIen suunnittelua, kehittämistä ja käyttäytymistä.(3)

API -tyylioppaita ei juuri ole akateemisesti tutkittu. Vuodelta 2017 löytyy tutkimus(2), jossa on analysoitu 32 API -tyyliopasta. Analyysissä löytyi 27 kategoriaa asioista, joita oppaat sisältävät. Viisi kategoriaa nousi esiin suurimmassa osassa analysoituja API -tyylioppaita:

- Versiointi (Versioning)
- Nimeäminen (Naming)
- Vastausformaatti/rakenne (Response Structure/Format)
- Metodit (Standard Methods)
- Tilakoodit (Status Codes)

Kannattaa tutustua olemassa oleviin oppaisiin, mutta ei välttämättä kopioida niitä suoraan sellaisenaan omaan käyttöön, koska monesti oppaat sisältävät myös organisaatiokohtaisia nyansseja. Tarkastellaan seuraavaksi suppeasti API -tyylioppaan hyötynäkökulmia, joita tähän on valittu 6 kappaletta.

## Arkkitehtuurin näkökulmasta

REST ei ole standardi vaan Roy Fieldingin alkuunlaittama arkkitehtuurityyli (1). Toisin sanoen vapausasteita tehdä eri asiat on niin monta kuin API kehittäjiä. Tästä syystä API -tyylioppaalla pidetään huoli arkkitehtuurin APIen yhtenäisyydestä.

>Liiketoimintasuunnitelman ja -tavoitteiden tulee ohjata arkkitehtuuria

Arkkitehtuuriratkaisut ohjaavat sitä, millaista koodia ja palveluja loppujen lopuksi tehdään. API -tyylioppaan avulla ohjataan käytännössä myös arkkitehtuurin toteutusta. Mikäli tyyliopas määrittää epäsuorasti että yrityksessä on vain datarajapintoja, on vaikea tehdä liiketoimintasuunnitelmia toiminnallisten ja tapahtumapohjaisten rajapintojen varaan.

Liiketoiminta ei saakaan olla alisteinen arkkitehtuurille, niin kuin se nykyään vielä tuntuu olevan. IT -osasto tekee rajapinnat ja liiketoimintajohto yrittää käyttää ratkaisuja osana liiketoimintaa. Liiketoimintasuunnitelman ja -tavoitteiden tulee ohjata arkkitehtuuria. Tämä puolestaan vaatii tiivistä dialogia liiketoimintajohton ja IT -osaston välillä. Niin kauan kuin nämä kaksi ihmisjoukkoa ovat kaukana toisistaan, ei tulos voi olla optimaalinen.

Mikäli yritys käyttää mikropalveluarkkitehtuuria, ovat APIt joka puolella arkkitehtuuria. Siinä vaiheessa API -tyyliopas on kultaakin kalliimpi ja keskeinen osa arkkitehtuurin toteutuksen ohjausta.

On syytä mainita, että mikropalveluarkkitehtuurissa kaikki APIt eivät monestikaan ole REST rajapintoja (vaikka voisi olla). Sisäiset rajapinnat ovat tehokkuusvaatimuksiensa vuoksi ehkä toteutettu muilla tekniikoilla kuten esimerkiksi gRPC teknologialla. Esimerkiksi Google käyttää gRPC rajapintoja paljon ja heidän API -tyylioppaansa sisältää ohjeistuksen myös niiden tuottamiseen. Näin ollen API -tyyliopas ei ole vain REST rajapintojen standardointiin, vaikka niin joskus ajatellaankin.

Sen sijaan hyvin yleisesti asiakkaan suuntaan paljastetut rajapinnat usein ovat nykyään REST tai RESTful. Riippumatta siitä, onko kyseessä sisäiset tai avoimet rajapinnat, on API -tyylioppaalla standardoiva vaikutus organisaation sisällä. APIen lajityyppeihin voit tutustua aiemman artikkelin avulla.
