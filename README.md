# Közös Cica – Supabase + GitHub Pages

## 1. Supabase
1. Hozz létre egy ingyenes projektet a supabase.com-on.
2. **SQL Editor** → illeszd be a `setup.sql` tartalmát → Run.
3. **Authentication → Sign In / Providers → Email**: kapcsold ki a **Confirm email** opciót (különben a név+jelszó regisztráció nem fog működni).
4. **Project Settings → API**: másold ki a **Project URL**-t és az **anon public** kulcsot.

## 2. index.html
Az elején írd át a két értéket:
```js
const SUPABASE_URL='...', SUPABASE_ANON_KEY='...';
```
Az anon kulcs publikus, ez normális: az adatokat a `setup.sql` sorszintű jogosultságai (RLS) védik.

## 3. GitHub Pages
1. Új GitHub repo, töltsd fel az `index.html`-t.
2. **Settings → Pages → Deploy from a branch → main / root**.
3. A játék a `https://FELHASZNALO.github.io/REPO/` címen lesz elérhető.

## Használat
- Regisztráció: név + jelszó (min. 6 karakter). Egy fiókhoz több cica is tartozhat.
- Meghívó: a cica oldalán a „Link másolása" gomb adja a `?join=KOD` linket; az első belépő lesz a társ.
