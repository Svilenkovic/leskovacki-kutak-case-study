<a href="https://leskovackikutak.rs/"><img src="media/cover.jpg" alt="Leskovački Kutak, naslovna strana na laptopu i telefonu" width="100%"></a>

# Leskovački Kutak

Platforma za porudžbine leskovačkog roštilja sa dva lokala u Beogradu: najbliža kuhinja po adresi, krediti za lojalnost i Android aplikacija.

**[leskovackikutak.rs](https://leskovackikutak.rs/)** · [Studija slučaja](https://svilenkovic.rs/radovi/leskovacki-kutak) · [Stranica aplikacije](https://svilenkovic.rs/aplikacija-leskovacki-kutak) · [English](README.md)

> [!NOTE]
> Klijentski projekat. Izvorni kod pripada klijentu i čuva se u privatnom repozitorijumu. Ova stranica opisuje šta sam uradio i kako.

<table>
  <tr><td><b>Klijent</b></td><td>Leskovački Kutak</td></tr>
  <tr><td><b>Delatnost</b></td><td>Leskovački roštilj, restoran i dostava hrane</td></tr>
  <tr><td><b>Lokacija</b></td><td>Beograd</td></tr>
  <tr><td><b>Vrsta</b></td><td>Platforma za porudžbine: sajt, aplikacije i paneli</td></tr>
  <tr><td><b>Moj deo posla</b></td><td>Dizajn, izrada, SEO, hosting i održavanje</td></tr>
  <tr><td><b>Tehnologije</b></td><td>PHP 8.3, MariaDB, REST API, Server-Sent Events, PWA, Android TWA</td></tr>
</table>

## O projektu

Leskovački Kutak je roštilj sa dva lokala u Beogradu, Veliki Mokri Lug i Leštane, i svaki ima svoje radno vreme, telefon i deo grada. Vlasnik je hteo sopstveni kanal za poručivanje, bez provizije po porudžbini, u kom svaka porudžbina sama stiže u pravu kuhinju, a jelovnik menja on.

Polje za adresu nudi predloge iz registra od 12.263 ulice i 297.101 kućnog broja, a bliža kuhinja se bira po razdaljini. Ako pregledač da koordinate, koriste se one, a ako ne da, uzimaju se od najsličnije ulice iz registra. Kad ni to ne uspe, porudžbinu prima podrazumevani lokal, pa odbijen pristup lokaciji nikoga ne zaustavlja. Sajt, aplikacija za kupce, panel lokala, aplikacija za dostavljače i administracija rade nad jednom MariaDB bazom preko zajedničkog REST API-ja.

## Šta sam uradio

- Nova porudžbina stiže na ekran u kuhinji preko Server-Sent Events, sa zvučnim signalom i štampom naloga, a dostavljaču na telefon čim mu je dodele
- Odvojene aplikacije sa svojom prijavom za kupce, lokale, dostavljače i administraciju; lokal vidi samo svoje porudžbine, a dostavljač samo one koje su mu dodeljene
- Krediti za lojalnost sa četiri nivoa po mesečnoj potrošnji i kodom za preporuku na svakom nalogu, a svaki kredit se knjiži kao transakcija
- Pretraga koja ćevapi i cevapi tretira isto, preko izračunatih i indeksiranih kolona u MariaDB bazi i iste funkcije u PHP-u i JavaScript-u
- PWA koja se instalira direktno sa sajta i potpisan Android paket (TWA) potvrđen preko Digital Asset Links
- Provera pri registraciji, pre upisa u bazu i pre slanja mejla, na oba mesta gde se pravi nalog, pošto se ispostavilo da je 2.230 od 2.256 naloga lažno

## Merenja

| | Performanse | Pristupačnost | Dobre prakse | SEO |
| :-- | :-: | :-: | :-: | :-: |
| Telefon | 98 | 100 | 100 | 100 |
| Desktop | 100 | 100 | 100 | 100 |

PageSpeed Insights, laboratorijsko merenje živog sajta, septembar 2026. Sigurnosna zaglavlja: 6 od 6. HTML validator: bez grešaka. axe provera pristupačnosti: bez prekršaja. Strukturisani podaci: `Restaurant`.

## Snimci ekrana

<table>
  <tr>
    <td width="68%" valign="top"><img src="media/desktop.webp" alt="Leskovački Kutak, naslovna strana na ekranu širine 1440 px"></td>
    <td width="32%" valign="top"><img src="media/mobile.webp" alt="Leskovački Kutak, naslovna strana na telefonu"></td>
  </tr>
</table>

<img src="media/inner-1.webp" alt="Izaberite lokaciju: Veliki Mokri Lug i Leštane, svaka sa svojim radnim vremenom">
<sub>Izaberite lokaciju: Veliki Mokri Lug i Leštane, svaka sa svojim radnim vremenom</sub>

<img src="media/inner-2.webp" alt="Sekcija &quot;Šta želite danas&quot;: kategorije jelovnika sa brojem stavki">
<sub>Sekcija "Šta želite danas": kategorije jelovnika sa brojem stavki</sub>

---

<sub>Izrada: [D. Svilenković](https://svilenkovic.rs).</sub>
