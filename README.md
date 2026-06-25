# Public site — Access Review &amp; Audit Trail for Jira

Statička stranica (čist HTML/CSS) za **Marketplace obavezne URL-ove**:

| Fajl | Svrha | Marketplace polje |
|---|---|---|
| `index.html` | Landing | (opciono) marketing URL |
| `privacy.html` | Privacy Policy | **B3 — Privacy Policy URL** (obavezno za paid) |
| `documentation.html` | Documentation | **B5 — Documentation URL** (obavezno za paid) |
| `logo.svg`, `style.css` | Brending | — |

Nema build koraka, nema dependencija. Otvori `index.html` lokalno u browseru da provjeriš.

---

## Hosting na GitHub Pages (besplatno)

> **Privatnost source-a:** Forge kod je u ovom (privatnom) repou. GitHub Pages na privatnom repou traži plaćeni plan. Da bi stranica bila **javna i besplatna**, preporuka je **zaseban PUBLIC repo** samo za `site/` (legalne stranice ionako treba da budu javne).

### Varijanta A — zaseban public repo (preporuka)

1. Na GitHub-u napravi nov **public** repo, npr. `access-review-site`.
2. Kopiraj sadržaj ove `site/` mape u korijen tog repoa.
3. Push na `main`.
4. Repo → **Settings → Pages** → *Source: Deploy from a branch* → *Branch: `main` / root* → **Save**.
5. Za ~1 min stranica je živa na:
   - `https://<korisnik>.github.io/access-review-site/privacy.html`
   - `https://<korisnik>.github.io/access-review-site/documentation.html`

> Po želji custom domen (`dvlslabs.com` već imaš): Settings → Pages → *Custom domain* → `docs.dvlslabs.com` (dodaj CNAME u Namecheap DNS na `<korisnik>.github.io`). Onda su URL-ovi `https://docs.dvlslabs.com/privacy.html` itd. — ljepše za listing.

### Varijanta B — ovaj repo, ako ga ikad učiniš public

Settings → Pages → Source: *Deploy from a branch* → Branch `main`, folder **`/site`** (GitHub Pages dozvoljava `/docs` ili root; za `/site` najlakše je Varijanta A ili premjesti u `/docs`).

---

## Šta upisati u Marketplace formu

- **Privacy Policy URL** → puni link do `privacy.html`
- **Documentation URL** → puni link do `documentation.html`

`.nojekyll` fajl sprečava Jekyll obradu (čist statički serving).
