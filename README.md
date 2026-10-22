# SCADALattice

Modularna SCADA platforma za simulaciju, nadzor i upravljanje fizičkim procesima.

**Predmet:** Informaciona bezbednost infrastrukturnih sistema  
**Studije:** Master akademske studije  
**Ustanova:** Fakultet tehničkih nauka, Univerzitet u Novom Sadu  
**Projekat:** 01

## Status i specifikacija

Početni šablon za studentski projekat. Implementacija još nije započeta.

📄 [Tehnička specifikacija projekta](docs/SCADALattice_Tehnicka_specifikacija.pdf)

PDF specifikacija je merodavna za obuhvat, zahteve i kriterijume prihvatanja. Ovaj README je uvod i šablon koji tim dopunjava tokom razvoja; pregled ispod ne zamenjuje kompletnu specifikaciju.

## O projektu

Platforma za projektovanje i izvršavanje HMI ekrana, obradu procesnih signala, istorijske podatke, alarme i izdavanje komandi simuliranim fizičkim procesima. Različiti simulatori povezuju se kroz stabilan Simulator SDK.

Glavne funkcionalne celine:

- Upravljanje SCADA projektima, konfiguracijom, tagovima i pravima pristupa.
- Web HMI editor, vezivanje grafičkih elemenata za tagove i režim nadzora.
- Registracija simulatora, upravljanje instancama, telemetrija i komande.
- Trendovi, istorijski podaci, alarmi, audit i kontrolisani kvarovi.

## Kako započeti

1. Pročitajte tehničku specifikaciju, posebno arhitekturna pravila i kriterijume prihvatanja.
2. Izaberite **Use this template → Create a new repository** da napravite repozitorijum svog tima.
3. Klonirajte svoju kopiju. U primeru zamenite `VAS_NALOG` i `VAS_REPOZITORIJUM` stvarnim nazivima:

   ```bash
   git clone https://github.com/VAS_NALOG/VAS_REPOZITORIJUM.git
   cd VAS_REPOZITORIJUM
   ```

4. Popunite podatke o timu, izbor tehnologija i uputstvo za lokalno pokretanje.
5. Organizujte implementaciju prema granicama odgovornosti iz specifikacije i pratite zahteve kroz zadatke i testove.

## Tim

| Ime i prezime | Broj indeksa | GitHub nalog |
| --- | --- | --- |
| TODO | TODO | TODO |

**Školska godina:** TODO

## Tehnologije i arhitektura

| Oblast | Izbor i verzija |
| --- | --- |
| Backend | TODO |
| Frontend | TODO |
| Skladište podataka | TODO |
| Simulacija / integracije | TODO |
| Alati za testiranje i pokretanje | TODO |

Izbor programskog jezika i biblioteka dokumentujte u skladu sa specifikacijom. Primenite Clean Architecture i SOLID: domen, aplikacione slučajeve korišćenja, adaptere i infrastrukturu razdvojite prema njihovim odgovornostima. U README dodajte stvarnu strukturu projekta i linkove ka arhitekturnim odlukama kada budu dostupni.

## Lokalno pokretanje

TODO: Nakon dodavanja implementacije navedite:

- preduslove i tačne verzije alata;
- instalaciju zavisnosti i pripremu baze;
- potrebne promenljive okruženja i primer konfiguracije bez tajni;
- komande za pokretanje svih komponenti;
- adrese lokalnog interfejsa i API-ja;
- učitavanje demonstracionih podataka i vraćanje početnog stanja.

Lozinke, pristupne tokene i privatne ključeve ne unosite u repozitorijum.

## Testiranje i demonstracija

TODO: Dodajte komande za pokretanje testova, potrebne testne podatke i vezu između zahteva iz specifikacije i dokaza njihove provere.

Referentna demonstracija: Rezervoar sa pumpom, ventilom, senzorom nivoa i alarmom: povezati simulator sa sopstvenim HMI ekranom, pratiti nivo, proveriti odbijanje neovlašćene komande i uključiti drugi simulator bez izmene SCADA jezgra.

Precizan tok demonstracije i očekivane rezultate proverite u PDF specifikaciji.

## Kontrolna lista za pripremu predaje

Ova lista pomaže organizaciji rada; kompletni kriterijumi prihvatanja nalaze se u specifikaciji.

- [ ] Popunjeni su podaci o timu i dokumentovan je izbor tehnologija.
- [ ] Dokumentovano lokalno pokretanje provereno je iz čiste kopije repozitorijuma.
- [ ] Funkcionalni i bezbednosni zahtevi povezani su sa testovima i dokazima.
- [ ] Poštovane su granice Clean Architecture slojeva i SOLID principi.
- [ ] Dokumentovani su javni ugovori, konfiguracija i obrada grešaka.
- [ ] Demonstrirano je proširenje dodavanjem drugog simulatora preko stabilnog SDK ugovora.
- [ ] Referentni scenario izvršen je kroz korisnički interfejs uz proveru događaja i API-ja.
- [ ] README odražava stvarno stanje implementacije i sadrži uputstvo za testiranje.
