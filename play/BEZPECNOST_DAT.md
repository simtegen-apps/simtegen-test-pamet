# Google Play — co vyplnit v Play Console

GENEROVANÝ SOUBOR z data-manifest.json (`python vykresli_aplikaci.py`) — needituj ručně.
Kde je `<adresa>`, doplň adresu produktu (vlastní doména, nebo `<repo>.pages.dev`).

## 1. Hlavní záznam v obchodě (Main store listing)

Workflow Vydání ho nahrává sám, jakmile má servisní účet. Ručně jen poprvé, nebo bez něj:

- **Název aplikace:** SimteGen test
- **Krátký popis:** Testovací aplikace SimteGenu pro ověření sestavení.
- **Kategorie:** Nástroje (`TOOLS`) — v Play Console: Nastavení obchodu
- **Kontaktní e-mail:** podpora@example.cz
- **Web:** `<adresa>`
- **Úplný popis:**

```
Testovací aplikace SimteGenu. Slouží jen k ověření, že se z webu produktu dá sestavit aplikace pro Android a připravit její záznam v Google Play. Zákazníkům se nenabízí.
```

## 2. Zásady ochrany soukromí (Privacy policy)

`<adresa>/zasady.html`

## 3. Bezpečnost údajů (Data safety)

1. *Shromažďuje nebo sdílí aplikace některý z požadovaných typů uživatelských údajů?* **Ano**
2. *Jsou všechny shromážděné údaje šifrovány při přenosu?* **Ano** (jen HTTPS)
3. *Poskytujete uživatelům způsob, jak požádat o smazání údajů?* **Ano** — v aplikaci Účet → Smazat účet a všechna data; popis na webu.
4. *Umožňuje aplikace vytvořit účet?* **Ano** (e-mailem). Odkaz na smazání účtu: `<adresa>/zasady.html`

**Sdílení: u žádného typu Ne.** Cloudflare (hosting, databáze), Resend (e-maily) a GitHub (evidence hlášení, šifrovaně) zpracovávají údaje pro nás — Google je za sdílení nepočítá.
**Zpracování dočasné (ephemeral): Ne** — údaje se ukládají.

| Kategorie | Typ údajů | Shromažďováno | Povinné? | Účely | Odkud (manifest) |
|---|---|---|---|---|---|
| Osobní údaje (Personal info) | E-mailová adresa (Email address) | Ano | povinné | Správa účtu (Account management), Prevence podvodů, zabezpečení a dodržování předpisů (Fraud prevention, security, and compliance) | uzivatele, prihlasovaci_odkazy |
| Osobní údaje (Personal info) | Jméno (Name) | Ano | volitelné | Funkce aplikace (App functionality), Správa účtu (Account management) | objednavky |
| Osobní údaje (Personal info) | Adresa (Address) | Ano | volitelné | Funkce aplikace (App functionality), Správa účtu (Account management) | objednavky |
| Osobní údaje (Personal info) | ID uživatelů (User IDs) | Ano | povinné | Správa účtu (Account management), Prevence podvodů, zabezpečení a dodržování předpisů (Fraud prevention, security, and compliance) | relace |
| Finanční údaje (Financial info) | Historie nákupů (Purchase history) | Ano | povinné | Funkce aplikace (App functionality), Správa účtu (Account management) | predplatne, platby, objednavky |
| Zprávy (Messages) | Jiné zprávy v aplikaci (Other in-app messages) | Ano | volitelné | Funkce aplikace (App functionality), Komunikace vývojáře (Developer communications) | hlaseni, hlášení chyb (tlačítko Nahlásit chybu) |
| Informace o aplikaci a výkonu (App info and performance) | Diagnostika (Diagnostics) | Ano | volitelné | Funkce aplikace (App functionality), Komunikace vývojáře (Developer communications) | hlášení chyb (tlačítko Nahlásit chybu) |

## 4. Obsah aplikace — ostatní prohlášení (App content)

- **Reklamy:** Ne, aplikace neobsahuje reklamy.
- **Cílová skupina:** 18 let a více.
- **Hodnocení obsahu (dotazník IARC):** kategorie Nástroje / Produktivita; na otázky o násilí, sexu, vulgaritách, drogách, hazardu a sdílení polohy odpověz Ne. Uživatelé spolu v aplikaci nekomunikují.
- **Zpravodajská aplikace / vládní aplikace / finanční funkce / zdraví:** Ne.
- **Přístup k aplikaci:** část funkcí vyžaduje přihlášení. Interní testování to nepotřebuje; před vydáním do produkce Google chce přístup pro kontrolu — přihlášení odkazem e-mailem kontrolor sám nedokončí, takže to vyřešíme demo účtem.
