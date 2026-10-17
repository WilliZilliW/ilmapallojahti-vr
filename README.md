# 🎈 Ilmapallojahti VR

Yksinkertainen selaimessa toimiva 3D-peli: ilmapalloja ilmestyy satunnaisesti ympärillesi, ja niitä puhkotaan heittämällä tikkoja katseen suuntaan peliohjaimen napilla. Tehty pelattavaksi Android-puhelimella VR-laseissa (Cardboard-tyyppiset lasit).

**Pelaa:** https://willizilliw.github.io/ilmapallojahti-vr/

## Näin pelaat

1. Yhdistä Bluetooth-peliohjain puhelimeen.
2. Avaa sivu Chromella ja paina jotain ohjaimen nappia, jotta selain tunnistaa ohjaimen.
3. Valitse **VR-lasit (Cardboard)**. Peli siirtyy koko näytön vaakatilaan ja näyttää kuvan erikseen kummallekin silmälle.
4. Laita puhelin laseihin ja aloita painamalla A.

Jos selain tukee WebXR:ää, valikossa näkyy myös **WebXR VR-tila** -nappi.

## Ohjaimet

| Toiminto | Peliohjain | Muut |
|---|---|---|
| Tähtää | katse (pään liike) | hiirellä vetämällä tietokoneella |
| Heitä tikka / aloita | A, B, X, olkanapit, liipaisimet | näytön napautus, välilyönti |
| Käänny | tatti vasen–oikea, ristiohjain vasen/oikea (45°) | nuolinäppäimet |
| Keskitä näkymä | Y tai Select/Back | R |

Sinulla on 100 tikkaa. Jokainen painallus heittää tikan, osui se tai ei. Tähtäin muuttuu punaiseksi, kun pallo on kohdalla. Kultainen pallo antaa 5 pistettä. Kierros päättyy 60 sekunnin jälkeen tai kun tikat loppuvat, ja ennätys tallentuu selaimeen.

## Tekniikka

Yksi `index.html`, joka käyttää [three.js](https://threejs.org/):ää CDN:stä. Cardboard-tila piirtää stereokuvan `StereoEffect`illä ja lukee pään asennon puhelimen asentoanturista. Peliohjain luetaan Gamepad API:lla. GitHub Actions julkaisee sivun GitHub Pagesiin jokaisesta `main`-haaran pushista.

Asentoanturi ja WebXR toimivat vain HTTPS-yhteydellä, joten pelaa julkaistua versiota.
