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
| **Gemma 3n v telefonu** | Multimodální model běžící lokálně přes MediaPipe — **funguje i na střední třídě**, model si stáhneš sám (viz níže) |

### Gemma 3n offline (bez AICore i bez internetu)

Aplikace umí spustit **Gemma 3n** přímo v telefonu — nepotřebuje AICore ani API klíč.

1. Stáhni si soubor modelu `.task` (doporučeno **Gemma 3n E2B**, ~2–3 GB) z LiteRT community na
   Hugging Face — vyžaduje přihlášení a odsouhlasení licence Gemma.
2. V aplikaci: *Nastavení → AI provider →* **Vybrat model** a soubor `.task` najdi v úložišti.
   Model se zkopíruje do aplikace (chvíli to trvá, hlásí průběh v MB).
3. Nastav **Gemma 3n v telefonu** jako primárního (nebo záložního) providera.

> Inference na střední třídě trvá jednotky až desítky sekund a model zabere místo v telefonu.
> Kdykoli ho lze zase smazat tlačítkem *Smazat model*.

Lze zvolit **primárního** a **záložního** providera (při vyčerpání kvóty se přepne automaticky).

## Soukromí

- Poznámky, fotky i nastavení zůstávají **v telefonu** (lokální databáze, žádný cloud).
- Přihlašovací údaje k bazarům a AI klíče jsou uložené **šifrovaně** (Android Keystore).
- Do AI odchází jen obsah, ze kterého se tvoří inzerát; hesla se maskují.

## Instalace

**[Stahovací stránka s QR kódem](https://walterx12.github.io/notepad-rapid/)** — nebo přímý odkaz na
nejnovější verzi: [`notepad-rapid-latest.apk`](../../releases/latest/download/notepad-rapid-latest.apk).

1. **Samsung: vypni Auto Blocker** — *Nastavení → Zabezpečení a soukromí → Auto Blocker*. Se zapnutým
   Auto Blockerem se APK nenainstaluje.
2. Stáhni APK a otevři ho v **Chrome** („Stažené soubory") nebo v aplikaci **Files**.
   Správce souborů z Play Store (Total Commander) instalovat APK nesmí.
3. Povol instalaci z tohoto zdroje a potvrď instalaci.
4. V *Nastavení* zadej svůj AI klíč a kontaktní údaje pro inzeráty.

> **Povolení platí jen asi 30 minut** — telefon si ho sám vypne. Před každou další instalací (i při
> aktualizaci na novou verzi) je proto nutné Auto Blocker vypnout a instalaci ze zdroje povolit znovu.

> APK je podepsané vývojářským klíčem — Android proto při instalaci upozorní, že aplikace není z obchodu.

## Stav

Osobní projekt ve vývoji. Zdrojový kód je v privátním repozitáři; zde se distribuují sestavené verze.
