# Notepad Rapid

Rychlý poznámkový blok pro Android, který z fotek a poznámky **vytvoří inzerát** a **předvyplní ho
na českých bazarech**.

**Stažení: [nejnovější APK](../../releases/latest)** (Android 13+)

---

## Co appka umí

### Poznámky
- Seznamy s odškrtávatelnými položkami **i volným textem**
- **Fotky** z galerie (i více naráz) a z fotoaparátu, náhledy, mazání
- Přesouvání položek tažením (☰), swipe gesta, editace položky
- **Koš s Undo** a automatickým mazáním po nastavené době
- **Připnutí seznamu na plochu** telefonu
- Sdílení fotky/textu z jiných aplikací **do vybraného seznamu**
- Cold start **~284 ms** (měřeno na Galaxy A53)

### Inzeráty z fotek (AI)
- Z fotek + poznámky vygeneruje **český inzerát** (titulek, popis, cena, kategorie, stav)
- **Cena podložená trhem**: srovná konkurenční nabídky na Bazoši, pracuje s **mediánem** a vyřazuje
  extrémní nabídky; volitelně počítá z **procenta z ceny nového** se srážkami za stáří a opotřebení
- **Předvyplnění inzerátu na portálu** (Bazoš, Sbazar) — včetně **fotek**; odeslání potvrzuje uživatel
- **AI kontrola formuláře** před odesláním: nejdřív rozpozná, co je na stránce, pak porovná hodnoty
  s inzerátem a chybějící pole umí doplnit
- **QR platba do banky** (SPAYD) pro ověřovací platbu bazaru

## AI provideři

Aplikace **neobsahuje žádné API klíče** — zadáš si vlastní v *Nastavení → AI klíče*:

| Provider | K čemu |
|---|---|
| **Gemini** | generování inzerátu z fotek (vision) i kontrola |
| **Groq** | rychlá textová kontrola formuláře |
| **OpenRouter** | libovolný model, volitelný zvlášť pro generování a zvlášť pro kontrolu |
| **V telefonu (bez cloudu)** | Gemini Nano přes AICore — jen na podporovaných zařízeních (Pixel 9+, Galaxy S25…) |

Lze zvolit **primárního** a **záložního** providera (při vyčerpání kvóty se přepne automaticky).

## Soukromí

- Poznámky, fotky i nastavení zůstávají **v telefonu** (lokální databáze, žádný cloud).
- Přihlašovací údaje k bazarům a AI klíče jsou uložené **šifrovaně** (Android Keystore).
- Do AI odchází jen obsah, ze kterého se tvoří inzerát; hesla se maskují.

## Instalace

1. Stáhni `app-release.apk` z [Releases](../../releases/latest).
2. V telefonu povol instalaci z neznámých zdrojů a APK nainstaluj.
3. V *Nastavení* zadej svůj AI klíč a kontaktní údaje pro inzeráty.

> APK je podepsané vývojářským klíčem — Android proto při instalaci upozorní, že aplikace není z obchodu.

## Stav

Osobní projekt ve vývoji. Zdrojový kód je v privátním repozitáři; zde se distribuují sestavené verze.
