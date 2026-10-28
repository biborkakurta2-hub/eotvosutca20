# Eötvös utca 20. – weboldal

Az eotvosutca20.hu egyoldalas weboldala. Öt exkluzív lakás, 1067 Budapest, Eötvös utca 20.

## Felépítés

- `index.html` – az egész oldal (szövegek, lakáslista, űrlap, térkép)
- `images/` – a látványtervek és az alaprajz

## Szerkesztés a GitHubon

1. Nyisd meg az `index.html` fájlt, és kattints a jobb felső ceruza ikonra.
2. A Cmd+F (Mac) vagy Ctrl+F keresővel keresd meg a módosítandó szöveget.
3. Írd át, majd kattints a zöld **Commit changes** gombra.
4. A Vercel 1-2 percen belül magától frissíti az élő oldalt.

## Gyakori módosítások

- **Ár:** keresd az `Ár érdeklődésre` szöveget a lakás sorában, és írd át (pl. `129,9 M Ft`).
- **Lakás foglalt:** a sorban a `<span class="status ok">Elérhető</span>` helyett: `<span class="status res">Foglalt</span>`
- **Lakás elkelt:** `<span class="status sold">Elkelt</span>`
- **Űrlap bekötése:** keresd a `FORM_ID` szöveget, és cseréld a Formspree-től kapott kódra.

## Képcsere

Az `images` mappában töltsd fel az új képet **ugyanazzal a fájlnévvel** (Add file → Upload files). Így az oldalon semmit nem kell átírni.

## Görgetéses fejléc (a ház felépül)

- A fejlécben a ház görgetésre „felépül”: előbb lebomlik a régi tető, majd ráépül az új emelet.
- A képkockák az `images/epites` mappában vannak: `a_` (felemelkedés az utcáról), `b_` (tetőbontás), `c_` (ráépítés), `a_` 48, `b_` és `c_` 61 kocka (a két utóbbi Higgsfield-videóból).
- A görgetés hosszát az `index.html`-ben a `.hero{...height:300vh}` érték adja: kisebb szám = gyorsabban felépül.

## Lakások adatlapjai

A „Lakások” szekcióban minden lakásnak saját füle van (`#lakas-1` … `#lakas-5` hivatkozással közvetlenül is nyitható):
fejléc az alapterülettel és az „Ajánlatot kérek erre a lakásra” gombbal (az űrlapon előre kiválasztja a lakást),
alatta az alaprajz, és ha van, a berendezett felülnézet, végül a belső látványképek.

Képek helye: `images/lakasok/`
- `lN-alaprajz.webp` – alaprajz helyiségenkénti m²-rel (N = lakás száma)
- `lN-felulnezet.webp` – berendezett felülnézet (ha van, a lakásnál megjelenik a „Berendezett felülnézet” váltó)
- további enteriőrök tetszőleges néven, pl. `l2-nappali.webp`

Új lakás képeinek felvételekor az 1. lakás blokkját (`<article id="lakas-1">`) érdemes mintának venni.

## Visszaigazoló e-mail

`emails/visszaigazolas.html` – az ajánlatkérés után a látogatónak küldendő automatikus válaszlevél a weboldal stílusában.
A `{{nev}}`, `{{email}}`, `{{telefon}}`, `{{lakas}}`, `{{uzenet}}` mezőket a küldő rendszer (pl. Make.com) cseréli ki az űrlap adataira.
A logó (`images/email/lotusz.png`) a weboldal címéről töltődik, ezért a levélben csak az élesítés után látszik.
