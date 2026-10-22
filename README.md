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
- A képkockák az `images/epites` mappában vannak: `a_001–a_064.webp` (tetőbontás), `b_001–b_064.webp` (ráépítés).
- A görgetés hosszát az `index.html`-ben a `.hero{...height:250vh}` érték adja: kisebb szám = gyorsabban felépül.
