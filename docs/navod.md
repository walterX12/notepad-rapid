# SnapSell — návod k použití

Aplikace na **inzeráty**: vyfotíš věc, AI napíše text i cenu a formulář na bazaru se předvyplní.
Odeslání vždy potvrzuješ ty.

---

## 1. První nastavení (5 minut)

**Jazyk**: při prvním spuštění si vybereš jazyk (nabídne se ten z telefonu). Appka umí češtinu,
slovenštinu, angličtinu, němčinu, polštinu, ukrajinštinu, ruštinu, vietnamštinu, rumunštinu,
bulharštinu, maďarštinu, španělštinu, francouzštinu, italštinu a portugalštinu. Změnit ho můžeš kdykoli v *Nastavení → Jazyk aplikace* — vybereš ze seznamu a appka se hned přepne.


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

**Nejrychlejší cesta — z plochy**: přidej si widget **Vyfotit a inzerovat** (menu ⋮ → *Widget na
plochu*) nebo dlaždici do rychlého nastavení (menu ⋮ → *Dlaždice do nastavení*). Jedno klepnutí
otevře fotoaparát a ze snímku rovnou vznikne inzerát.


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

> **Nastavení publikace**: v *Nastavení* si můžeš zapnout, že appka sama zaškrtne **souhlas
> s podmínkami** portálu a že se u inzerátu **zveřejní telefon**. Obojí je výchozí vypnuté.

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

**Kontrola před odesláním**: po vyplnění appka sama zkontroluje formulář a napíše, jestli sedí
s inzerátem — ikonou ☑ v horní liště ji spustíš znovu. Dialog má tři části:

- **shrnutí** („vše v pořádku" / „AI našla 2 připomínky"),
- **připomínky** — co na stránce neodpovídá inzerátu nebo co portál hlásí červeně (třeba odmítnuté
  telefonní číslo, cena v jiné měně),
- **Portál ještě čeká na:** — kroky, bez kterých inzerát nepustí (ověřený telefon, souhlas).

Tlačítkem **Doplnit dle AI** necháš doplnit prázdná pole; vyplněné hodnoty appka nepřepisuje
a jméno, telefon ani hesla nedoplňuje nikdy.

> **Nastavení → Kontrolovat i snímky stránky** (výchozí vypnuto): kontrola dostane i **obrázky
> stránky tak, jak ji vidíš ty** — červené rámečky, vykřičníky a hlášky, které ve formuláři nejsou
> vidět. Delší stránku projde po obrazovkách (až tři snímky) a vrátí ji tam, kde byla. Kontrola pak
> trvá déle a spotřebuje víc kreditu, ale najde i to, co je „jen" nakreslené.

---

**Co ještě zbývá dokončit**: po vyplnění se nad stránkou objeví karta *Zbývá dokončit* — vypíše, co
je hotové (✓ fotky, ✓ kategorie) a co musíš udělat ty (ověřit telefon, zaškrtnout souhlas
s podmínkami, klepnout na odeslání). Kartu můžeš **Skrýt**, tlačítkem **Znovu** ji přepočítáš a
kdykoli ji vyvoláš ikonou ✓ v horní liště.

---

## 4. Evidence inzerátů

Hlavní obrazovka = přehled všeho, co inzeruješ. U každého inzerátu je vidět:

- fotka, titulek, cena,
- **zadání pro AI**, se kterým vznikl,
- **kam a kdy** byl publikován (*Připraveno* = formulář byl předvyplněn, *Publikováno* = potvrdil jsi
  odeslání, *Nedokončeno* = nedoběhlo).

Klepnutím na inzerát se otevře detail s celým textem, podkladem k ceně a tlačítkem **Publikovat**
(nebo *Publikovat znovu*, když už někde běží).

**Publikace na víc portálů**: v nabídce *Kam publikovat?* si **zaškrtni portály** (jeden, dva nebo
všechny tři) a klepni na *Publikovat (N)*. Appka tě provede zaškrtnutými portály za sebou — po
zavření jednoho hned otevře další. Sérii můžeš kdykoli ukončit tlačítkem *Ukončit sérii*.

**Stav inzerátů**: menu ⋮ → *Zkontrolovat stav na Bazoši*. Appka si otevře výpis tvých inzerátů
a u každého evidovaného doplní, jestli **běží**, nebo **už neběží**. Inzeráty, které máš na portálu
a v evidenci chybí, ti nabídne převzít.

**Úprava inzerátu**: v detailu jsou vedle *Publikovat* tlačítka **Upravit** (titulek, cena, popis)
a **Upravit přes AI** — napiš nebo nadiktuj, co má být jinak („zlevni na 120", „zdůrazni, že je
nepoužitá"), a AI inzerát přepíše.

**Menu ⋮** v horní liště: *Návod*, *Nahlásit chybu* a *O aplikaci* (číslo verze a odkaz na novější).

**Hledání a filtr** (nad výpisem):

- do pole **Hledat v inzerátech** stačí napsat cokoli z inzerátu — hledá i v zadání pro AI a v názvu
  portálu, diakritiku psát nemusíš („capek", „bazos"),
- čipy **Vše / Nepublikované / Připravené / Publikované** ukážou jen inzeráty v daném stavu.

**Hromadné mazání**: podrž prst na inzerátu → zapne se výběr (lišta *Vybráno: N*). Klepáním vybereš
další, ✓ vybere všechny zobrazené, koš je smaže (po potvrzení). Maže se **jen evidence v aplikaci** —
inzeráty, které už na portálu běží, musíš smazat na portálu.

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
