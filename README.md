# Test slučajevi

| Ulazni izraz | Očekivani rezultat | Dobijeni rezultat | Status | Zapažanje |
|--------------|--------------------|-------------------|--------|-----------|
| 4+5 | 9 | 9 | PASS | Sabiranje funkcioniše ispravno |
| 10+5*4 | 30 | 30 | PASS | Poštovan prioritet operacija |
| 8-3 | 5 | 5 | PASS | Oduzimanje funkcioniše |
| 6/2 | 3 | 3 | PASS | Deljenje funkcioniše |
| 3*7 | 21 | 21 | PASS | Množenje funkcioniše |
| 10/0 | Greška | Infinity | FAIL | Deljenje nulom nije pravilno obrađeno |
| 5++2 | Greška | Neočekivan rezultat | FAIL | Program ne proverava ispravnost izraza |
| *5+3 | Greška | Neočekivan rezultat | FAIL | Izraz ne bi smeo početi operatorom |
| 5+ | Greška | Neočekivan rezultat | FAIL | Nepotpuni izraz nije obrađen |
| 10+5*4+3 | 33 | 33 | PASS | Kompleksniji izraz radi ispravno |

---

# Uočeni nedostaci

Tokom testiranja primećeni su sledeći problemi:

1. Kalkulator ne proverava da li je uneti izraz ispravan.
2. Deljenje nulom ne vraća grešku već vrednost "Infinity".
3. Program dozvoljava izraze koji počinju operatorom.
4. Nepotpuni izrazi nisu pravilno obrađeni.

---

# Zaključak

Na osnovu sprovedenog testiranja može se zaključiti da kalkulator pravilno izvršava osnovne aritmetičke operacije kada je unos ispravan.  
Međutim, program nema implementiranu proveru validnosti unosa, zbog čega dolazi do neočekivanog ponašanja u određenim slučajevima.

Za unapređenje aplikacije preporučuje se dodavanje validacije unosa i obrade grešaka pre samog računanja izraza.
