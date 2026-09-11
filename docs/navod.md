# SnapSell — návod k použití

Aplikace na **inzeráty**: vyfotíš věc, AI napíše text i cenu a formulář na bazaru se předvyplní.
Odeslání vždy potvrzuješ ty.

---

## 1. První nastavení (5 minut)

Otevři **Nastavení** (ozubené kolo vpravo nahoře).

| Co vyplnit | Kde a proč |
|---|---|
| **AI klíč** | *AI klíče* — stačí jeden (Gemini, Grok/Groq nebo OpenRouter). U providera bez klíče je v seznamu napsáno „(bez klíče)". Klíč se ukládá **šifrovaně v telefonu**. |
| **Kontaktní jméno, telefon, e-mail** | Vyplní se do inzerátu na portálech. |
| **Heslo k inzerátu** | Bazoš ho vyžaduje pro pozdější úpravu a smazání inzerátu. |
| **PSČ** | Lokalita pro Bazoš a Sbazar. |
| **Obec / město** | Facebook samotné PSČ neuzná, chce obec. |
| **Výchozí text inzerátu** | Připojí se ke každému inzerátu (např. „K vyzvednutí ve Všenorech"). |
| **Minimální cena** | Tvrdá pojistka — appka nikdy nenabídne míň. |

Bez AI klíče appka funguje jako evidence inzerátů, jen negeneruje text.

---

## 2. Nový inzerát

**Dvě cesty, obě končí stejně:**

1. **Z aplikace** — tlačítko *Nový inzerát* → vyber fotky.
2. **Z galerie** — označ fotky → *Sdílet* → **SnapSell**. Otevře se rovnou příprava inzerátu,
   žádný mezikrok.

Pak napíšeš (nebo nadiktuješ) **zadání pro AI** — třeba „je to na stůl, ne na zeď". AI podle fotek
a zadání napíše titulek, popis a navrhne cenu.

### Náhled inzerátu

Vidíš titulek, popis, cenu a **podklad k ceně**: jak cena vznikla a s jakými nabídkami se srovnávala.
Konkrétní nabídky jsou **klikatelné** — otevřou se na bazaru, takže si cenu můžeš ověřit. Vedle je
odkaz na **cenu nového kusu**.

Cokoli můžeš přepsat ručně, nebo použít **Upravit přes AI** — napíšeš/nadiktuješ, co má být jinak
(„zdůrazni, že je nepoužitá", „zlevni na 120"), a AI přepíše celý inzerát.

---

## 3. Publikace

Tlačítko **Publikovat** → vybereš portál (nebo *Všechny portály*).

Otevře se stránka portálu s **předvyplněným formulářem**. Co udělá appka a co zbývá na tebe:

| Portál | Appka vyplní | Ty dokončíš |
|---|---|---|
| **Bazoš** | kategorii, titulek, popis, cenu, PSČ, kontakt, heslo k inzerátu, **fotky** | souhlas s podmínkami → *Odeslat* |
| **Sbazar** | titulek, popis, cenu, kategorii, lokalitu (vybere obec z nabídky), telefon, fotky | zkontrolovat fotky, souhlas → *Zveřejnit* |
| **Facebook** | titulek, cenu, popis, **fotky** | Kategorii a Stav (rozbalovátka), lokalitu → *Další* → *Zveřejnit* |

**Aplikace nikdy neodesílá inzerát sama** (pokud si v Nastavení výslovně nezapneš plně automatickou
publikaci). Po zavření okna se tě zeptá, jestli inzerát vyšel — podle odpovědi to zapíše do evidence.

První publikace na Bazoši vyžaduje **ověření telefonu SMS** a **ověřovací platbu 1 Kč**. Appka SMS kód
odchytí sama a u platby nabídne **QR kód do bankovní aplikace**.

---

## 4. Evidence inzerátů

Hlavní obrazovka = přehled všeho, co inzeruješ. U každého inzerátu je vidět:

- fotka, titulek, cena,
- **zadání pro AI**, se kterým vznikl,
- **kam a kdy** byl publikován (*Připraveno* = formulář byl předvyplněn, *Publikováno* = potvrdil jsi
  odeslání, *Nedokončeno* = nedoběhlo).

Klepnutím na inzerát se otevře detail s celým textem, podkladem k ceně a tlačítkem **Publikovat**
(nebo *Publikovat znovu*, když už někde běží).

---

## 5. Automatické zlevňování

V *Nastavení* zapneš **Automatické zlevňování** a nastavíš plán (např. −10 % každých 7 dní,
nejníže na 50 % původní ceny).

Při publikaci se tě appka zeptá, jestli plán pro ten inzerát chceš. Pak jednou denně spočítá, jestli
je čas zlevnit, a **pošle notifikaci**. Klepnutím na ni se otevře úprava ceny přímo na portálu
(u Bazoše přes „Moje inzeráty" → *Upravit*, s předvyplněným heslem a novou cenou).

Běžící plány najdeš v *Nastavení → Zlevňované inzeráty*, kde je můžeš zastavit.

---

## 6. Když se něco pokazí

**Zatřes telefonem.** Appka připraví hlášení: snímek obrazovky, poslední kroky v aplikaci, log, model
telefonu a typ připojení. Pak si vybereš:

- **Issue na GitHubu** — otevře předvyplněný formulář v repozitáři aplikace,
- **Odeslat hlášení** — pošle soubory přes sdílení (e-mail, WhatsApp…).

Nic neodchází samo a **hesla ani API klíče se do hlášení nezapisují**. Zatřesení jde vypnout
v Nastavení, kde je i tlačítko *Nahlásit chybu teď*.

---

## 7. Seznamy a poznámky

Původní poznámkový blok zůstal jako doplněk — ikona vlevo od ozubeného kola. Seznamy s odškrtáváním,
fotkami, štítky a složkami, koš s vrácením zpět. Hodí se na přípravu podkladů; hlavní náplní aplikace
jsou ale inzeráty.

---

## 8. Instalace a aktualizace

Stahovací stránka: **https://walterx12.github.io/notepad-rapid/**

- **Samsung: vypni Auto Blocker** (*Nastavení → Zabezpečení a soukromí → Auto Blocker*), jinak se APK
  nenainstaluje.
- Povolení instalace z neznámého zdroje **platí jen ~30 minut** — před každou další instalací ho povol
  znovu.
- APK otevři v **Chrome** („Stažené soubory") nebo v aplikaci **Files**; správce souborů z Play Store
  (Total Commander) instalovat APK nesmí.
- Aktualizace **nepřijde o data** — balíček zůstává stejný a databáze se migruje.
