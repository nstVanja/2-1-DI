# Figma vežba – Rezervacija bioskopskih karata

## Opis zadatka

Dizajniraj **mobilnu aplikaciju za rezervaciju karata u bioskopu** sa tri ekrana i poveži ih u interaktivni prototip u Figmi.

Korisnik u aplikaciji bira film, zatim bira projekciju (datum i vreme) i sedišta, i na kraju dobija potvrdu rezervacije. Prototip radiš **u boji, prema zadatoj paleti – umesto fotografija koristiš obojene placeholder bloko**ve.

Na raspolaganju imaš 2 školska časa. Postupak izrade biraj sam – u nastavku su samo zahtevi koje gotov rad mora da ispuni.

## Zadatak 1 – Skica na papiru

1. Na tri lista papira nacrtaj tri ekrana telefona (samo konture, bez detalja):
   - Ekran 1: lista filmova
   - Ekran 2: izbor projekcije i sedišta
   - Ekran 3: potvrda rezervacije
2. Strelicama označi kojim elementom korisnik prelazi sa jednog ekrana na drugi, kao i povratak nazad.
3. Razmeni skicu sa učenikom pored sebe. Daj mu 2 pozitivna komentara i 1 predlog za poboljšanje, pa svoju skicu doradi prema dobijenom predlogu.

## Zadatak 2 – Dizajn ekrana u Figmi

Digitalizuj svoju skicu u Figmi. Fajl nazovi **Bioskop\_Ime\_Prezime**.

### Opšti zahtevi

- Tri frejma veličine **iPhone 17**, bele pozadine, poređana horizontalno sa razmakom od 80 px.
- Frejmovi se zovu: Ekran 1 – Lista filmova, Ekran 2 – Projekcija i sedišta, Ekran 3 – Potvrda.
- Iznad svakog frejma stoji natpis sa nazivom ekrana (font 14, boja #888888).
- Koriste se **samo boje iz palete**:

| Namena | Boja |
| --- | --- |
| Pozadina frejma | #FFFFFF (bela) |
| Zaglavlje, primarno dugme | #B71C1C (tamnocrvena), tekst #FFFFFF |
| Izabrani element (datum, termin, sedište) | #FFB300 (zlatna), tekst #212121 |
| Kartice, polja, slobodna sedišta | #F5F5F5 (svetlosiva) |
| Zauzeta sedišta, rasprodat termin | #BDBDBD (siva) |
| Placeholder za poster i QR kod | #FFCDD2 (svetlocrvena) |
| Ikonica uspešne rezervacije | #2E7D32 (zelena) |
| Ivice i linije razdvajanja | #E0E0E0 |
| Tekst | #212121 (glavni), #757575 (pomoćni) |
| Sekundarno dugme | belo, ivica i tekst #B71C1C |

- Svaki ekran ima **zaglavlje** preko cele širine frejma, visine 56 px, sa naslovom ekrana centriranim po obe ose.
- Na sva tri ekrana su ivice sadržaja udaljene **16 px** od leve i desne ivice frejma.
- Elementi koji čine jednu celinu (kartica filma, dugme, red informacija) moraju biti grupisani i smisleno imenovani (npr. Film 1, btnDalje).

### Ekran 1 – Lista filmova

- Polje za pretragu ispod zaglavlja (pravougaonik sa zaobljenim uglovima i tekstom „Pretraži film…“).
- Lista od **4 kartice filmova**, jednake veličine i jednakog razmaka (8 px). Svaka kartica sadrži:
  - placeholder za poster (uspravni pravougaonik, odnos stranica oko 2:3),
  - naziv filma (podebljano) i žanr (pomoćna boja teksta),
  - trajanje filma kao tekst (npr. 118 min).
- Kartica prvog filma vodi na Ekran 2.

### Ekran 2 – Projekcija i sedišta

- Ispod zaglavlja naziv izabranog filma.
- **Izbor datuma**: red od 5 dana (npr. Pon 12 – Pet 16), jedan dan je označen kao izabran.
- **Izbor vremena projekcije**: najmanje 4 termina (npr. 16:00, 18:30, 20:15, 22:00), jedan označen kao izabran, jedan kao rasprodat.
- Tekst „EKRAN“ i linija ili traka koja označava platno.
- **Mreža sedišta**: 6 redova × 8 sedišta, sa jednakim razmacima, uređena pomoću Auto Layout-a. Mreža mora da prikaže tri stanja sedišta: slobodno, zauzeto i izabrano (najmanje 2 izabrana sedišta).
- **Legenda** ispod mreže koja objašnjava sva tri stanja.
- Pri dnu tekst sa brojem karata i ukupnom cenom (npr. 2 karte · 1000 din).
- Primarno dugme „Nastavi“ (vodi na Ekran 3) i sekundarno dugme „Nazad“ (vodi na Ekran 1), širine kao sadržaj ekrana, sa razmakom 8 px.

### Ekran 3 – Potvrda

- Kružna ikonica uspešne rezervacije sa kvačicom.
- Poruka „Rezervacija je uspešna!“.
- Redovi sa podacima, svaki sa labelom levo (pomoćna boja) i vrednošću desno: **Film, Datum, Vreme, Sala, Sedišta, Ukupno**. Između redova su linije razdvajanja.
- Placeholder za QR kod (kvadrat najmanje 120 × 120 px), centriran.
- Primarno dugme „Sačuvaj kartu“ i sekundarno dugme „Početna“ (vodi na Ekran 1).

### Moguće rešenje

Ovako bi gotov rad mogao da izgleda. Plave strelice označavaju veze iz Zadatka 3.

&#91;image: Skica rešenja – tri ekrana aplikacije za rezervaciju bioskopskih karata\]

## Zadatak 3 – Interaktivni prototip

Poveži ekrane tako da korisnik može da prođe ceo tok rezervacije u režimu prezentacije (Present).

| Sa ekrana | Element | Vodi na |
| --- | --- | --- |
| Ekran 1 | Kartica prvog filma | Ekran 2 |
| Ekran 2 | Dugme „Nastavi“ | Ekran 3 |
| Ekran 2 | Dugme „Nazad“ | Ekran 1 |
| Ekran 3 | Dugme „Početna“ | Ekran 1 |

- Sve veze se aktiviraju klikom.
- Prelaz unapred i prelaz unazad moraju imati različite animacije (npr. klizanje ulevo i udesno).
- Prototip mora da počinje od Ekrana 1.

## Proveri pre predaje

- [ ] Fajl se zove Bioskop\_Ime\_Prezime.
- [ ] Postoje tri frejma iPhone 17 sa tačnim nazivima i natpisima iznad.
- [ ] Korišćene su samo boje iz palete, svaka za zadatu namenu.
- [ ] Svaki ekran ima zaglavlje sa centriranim naslovom.
- [ ] Ekran 1 ima pretragu i 4 jednako razmaknute kartice filmova.
- [ ] Ekran 2 ima izbor datuma, termine, mrežu 6 × 8 sedišta sa tri stanja i legendu.
- [ ] Ekran 3 ima ikonicu, poruku, 6 redova podataka, QR placeholder i dva dugmeta.
- [ ] Elementi su grupisani i smisleno imenovani.
- [ ] Sve 4 veze rade u režimu Present.
