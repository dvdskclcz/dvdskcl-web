# David Skácel – Výběr projektů / Selected Projects Portfolio (Context Reference)

Tento dokument slouží jako kontextový podklad pro AI asistenty, generátory webového portfolia a strukturované datové soubory (`projects.json`). Obsahuje všech 10 stěžejních projektů z oficiální projektové brožury včetně technických detailů, byznysových přínosů a kvantifikovaných metrik v češtině i angličtině.

---

## 1. Automatizované zpracování fakturace kreditů SIGNI
* **Anglický název:** Automated Processing of SIGNI Credit Billing
* **Období / Period:** 2026
* **Role:** IT Analyst & Integration Lead
* **Tech Stack / Klíčová slova:** `n8n (Workflow Automation)`, `SIGNI REST API`, `MS SQL Server`, `Helios (ERP)`, `JSON/CSV`, `Delta Load`, `Deduplication`

### Kontext a cíl (Context & Objective)
* **CZ:** Zajištění přesného a škálovatelného vytěžování dat o čerpání kreditů pro elektronické podepisování napříč 22 nezávislými pracovními prostory pro 12 dceřiných společností. Cílem bylo odstranit neefektivní manuální proces, který představoval bezpečnostní a procesní riziko kvůli vázanosti na jediného administrátora s přístupem do systému.
* **EN:** Ensuring accurate and scalable data extraction of e-signature credit usage across 22 independent workspaces for 12 subsidiaries. The objective was to eliminate an inefficient manual process that posed a security and operational risk due to its strict reliance on a single administrator.

### Přehled řešení (Solution Perspective)
* **Byznysový pohled (CZ):** Plná eliminace manuálního stahování a slučování 22 reportů. Proces již nezávisí na dostupnosti jednoho člověka. Výstupem jsou automaticky připravená přesná data pro podklady k fakturaci a automaticky generované Excel přílohy sloužící pro křížovou kontrolu a rychlé řešení případných reklamací.
* **Technický pohled (CZ):** Návrh a realizace integračního toku v n8n. Komunikace je zabezpečena dedikovanými API klíči pro každý workspace. Ústředním prvkem je implementace deduplikační logiky zajišťující inkrementální zápis pouze nových, dosud nezpracovaných záznamů do dedikovaných importních tabulek v MS SQL pro následné zpracování fakturačním oddělením.
* **Architecture Flow:** `SIGNI Workspaces (22x REST API) ➔ n8n Orchestrator (Deduplikace, Rate-limit) ➔ Inkrementální zápis do MS SQL ➔ Podklady pro fakturaci v Helios & Excel reporty`

### Dopad a výsledky (Business Impact & Results)
* **Zkrácení času zpracování:** Redukce celkového času na přípravu dat z více než 1,5 hodiny na automatizovaný běh trvající méně než 5 minut pro všech 12 společností.
* **Odstranění úzkého hrdla (SPOF):** Úspěšná eliminace „single point of failure“ odstraněním provozní závislosti na jediném administrátorovi.
* **Datová integrita:** Zajištění 100% spolehlivosti datového toku mezi externí cloudovou platformou a interním systémem bez rizika lidské chyby.

---

## 2. Pilotní projekt: AI pro začátečníky
* **Anglický název:** Pilot Project: AI for Beginners
* **Období / Period:** 2026
* **Role:** IT Consultant & Trainer
* **Tech Stack / Klíčová slova:** `Generative AI`, `Prompt Engineering`, `LLMs (Gemini, Copilot, ChatGPT, Claude)`, `NotebookLM`, `Digital Adoption`, `Change Management`, `n8n & API Integrations`

### Kontext a cíl (Context & Objective)
* **CZ:** Příprava a exekuce komplexního vzdělávacího rámce pro integraci nástrojů umělé inteligence do každodenní agendy zaměstnanců holdingu. Cílem pilotního programu (4 skupiny po 12 lidech, napříč dceřinými společnostmi a od specialistů po management) bylo zvýšit digitální gramotnost, eliminovat obavy z nových technologií a ukázat reálné využití AI pro úsporu času.
* **EN:** Preparation and execution of a comprehensive educational framework for integrating AI tools into the daily agenda of holding employees. The goal of the pilot program (4 groups of 12 people, across subsidiaries, from specialists to management) was to increase digital literacy, eliminate fears of new technologies, and demonstrate the real-world application of AI for time savings.

### Přehled řešení (Solution Perspective)
* **Byznysový pohled (CZ):** Koncept rozdělený do dvou 4hodinových bloků se 14denní pauzou pro praktické vyzkoušení. Obsah se zaměřil na okamžitou využitelnost od tvorby textů a rešerší až po automatizaci schůzek (Fireflies) či vizuálů (Adobe, HeyGen). Absolventi začali vnímat AI jako užitečného parťáka pro každodenní práci a odbourali počáteční obavy.
* **Technický pohled (CZ):** Multioborová demonstrace schopností napříč různými LLM (Gemini, Copilot, ChatGPT, Claude) a specializovanými nástroji (NotebookLM). Součástí byla i pokročilá demonstrace „pod pokličkou“ – ukázka napojení OpenAI přes API a automatizaci v n8n, aby management získal hlubší přehled o architektonických možnostech podnikových integrací.

### Dopad a výsledky (Business Impact & Results)
* **Vynikající přijetí:** 94 % absolventů hodnotilo celkovou úroveň programu jako vynikající nebo velmi dobrou (100% pozitivní hodnocení lektorského týmu).
* **Časová úspora pro byznys:** 54 % účastníků (19 z 35 dotazovaných) odhaduje, že jim nově nabyté dovednosti s AI ušetří 1 až 3 hodiny týdně.
* **Motivace pro další transformaci:** 100 % účastníků (35 z 35) projevilo zájem se v oblasti AI a IT nadále rozvíjet.

---

## 3. Digitalizace HR procesů a samoobslužný portál
* **Anglický název:** HR Process Digitalization & Self-Service Portal
* **Období / Period:** 2025–2026
* **Role:** Product Owner & Lead Business Analyst
* **Tech Stack / Klíčová slova:** `Business Analysis`, `Wiki (Documentation)`, `DevExpress React`, `Web API`, `MS SQL Server`, `SAP / Helios (ERP Integration)`

### Kontext a cíl (Context & Objective)
* **CZ:** Nahrazení papírových žádostí a manuálního zpracování agendy nepřítomností (dovolené, lékař, home office, služební cesty) centralizovaným digitálním HR portálem. Cílem bylo sjednotit zadávání napříč společnostmi a zajistit automatický datový tok do docházkových a mzdových systémů.
* **EN:** Replacing paper-based requests and manual processing of absence agendas (vacations, doctor visits, home office, business trips) with a centralized digital HR portal. The goal was to unify data entry across companies and ensure an automated data flow into attendance and payroll systems.

### Přehled řešení (Solution Perspective)
* **Byznysový pohled (CZ):** Vedení projektu z pozice Product Ownera od vytěžení požadavků HR oddělení přes specifikaci zadání až po testování, přípravu školení a tvorbu dokumentace (Wiki). Uživatelé získali intuitivní portál pro správu žádostí, který jim v reálném čase zobrazuje schvalovací workflow a zůstatky nároků.
* **Technický pohled (CZ):** Spolutvorba relačního datového modelu v MS SQL s využitím interního DevExpress nástroje. Architektura stojí na komunikaci přes Web API směrem k frontend aplikaci v DevExpress React. Kritickým bodem bylo zajištění obousměrné integrace: přesun dat do docházky, export do mezd (SAP/Helios) a import zpětných mzdových nároků.

### Dopad a výsledky (Business Impact & Results)
* **End-to-end automatizace:** Odstranění manuálních přepisů a chybovosti díky obousměrné datové synchronizaci mezi HR portálem, docházkou a mzdovými ERP systémy (SAP/Helios).
* **Úplná bezpapírovost:** Zavedení 100% digitální evidence a elektronického schvalování pro veškerou agendu nepřítomností napříč firmami.
* **Úspěšná adopce a podpora:** Zajištění hladkého přechodu uživatelů díky kompletnímu cyklu školení, roll-out prezentacím a důkladně zpracované firemní Wiki základně.

---

## 4. Zavedení systému elektronického podepisování
* **Anglický název:** Implementation of Electronic Signature System
* **Období / Period:** 2024–Současnost
* **Role:** Project Manager & System Administrator
* **Tech Stack / Klíčová slova:** `Vendor Management`, `SIGNI`, `DocuSign`, `DigiSign`, `eIDAS Compliance`, `PKI (Tokens & Certificates)`, `Workflow Configuration`

### Kontext a cíl (Context & Objective)
* **CZ:** Výběr a celofiremní implementace platformy pro elektronické podepisování dokumentů s cílem zefektivnit schvalovací procesy napříč dceřinými společnostmi. Projekt zahrnoval tržní analýzu, nasazení systému a následnou administraci bezpečnostních tokenů a certifikátů.
* **EN:** Selection and company-wide implementation of an electronic signature platform to streamline approval processes across subsidiaries. The project included market analysis, system deployment, and ongoing administration of security tokens and certificates.

### Přehled řešení (Solution Perspective)
* **Byznysový pohled (CZ):** Kompletní řízení výběrového řízení od sběru požadavků managementu přes srovnání platforem (DocuSign, Signi, DigiSign) až po finální vyjednání smluv s vítězem (Signi). Úspěšné nasazení odlišných procesů pro různé firmy (standardní smlouvy, dokumenty představenstva, vydané objednávky). Role garanta a hlavní podpory uživatelů.
* **Technický pohled (CZ):** Administrace a technická správa platformy včetně zajištění souladu s legislativními požadavky (eIDAS). Kompletní správa životního cyklu bezpečnostních tokenů a kvalifikovaných certifikátů pro podepisování. Nastavení specifických schvalovacích workflow pro různé úrovně citlivosti dokumentů.

### Dopad a výsledky (Business Impact & Results)
* **Strategický výběr dodavatele:** Analýza trhu a testování demo verzí vedly k nákladově i funkčně nejefektivnější volbě schválené vrcholovým managementem.
* **Flexibilní adopce v holdingu:** Úspěšné nasazení napříč firmami se zohledněním jejich specifických potřeb (od běžných objednávek po vysoce důvěrné dokumenty představenstva).
* **Centralizovaná správa:** Zajištění jednotné administrace, podpory a správy certifikátů z jedné centrální pozice.

---

## 5. Implementace systému kybernetické bezpečnosti (ZOKB)
* **Anglický název:** Cybersecurity Compliance System (ZOKB)
* **Období / Period:** 2023–Současnost
* **Role:** Lead Business Analyst & ISMS Specialist
* **Tech Stack / Klíčová slova:** `DevExpress .NET`, `MS SQL Server`, `ZOKB Compliance`, `ISO/IEC 27001`, `GAP Analysis`, `Asset Inventory`, `Data Integration`

### Kontext a cíl (Context & Objective)
* **CZ:** Návrh a vývoj centralizovaného systému pro řízení souladu se zákonem o kybernetické bezpečnosti (ZOKB) a standardy ISO 27001 napříč dceřinými společnostmi. Cílem bylo sjednotit evidenci aktiv, automatizovat skórování firem a poskytnout nástroj pro kontinuální GAP analýzu bezpečnostních standardů.
* **EN:** Design and development of a centralized system for managing compliance with the Cyber Security Act (ZOKB) and ISO 27001 standards across subsidiaries. The goal was to unify asset inventory, automate company scoring, and provide a tool for continuous GAP analysis of security standards.

### Přehled řešení (Solution Perspective)
* **Byznysový pohled (CZ):** Vytvoření nástroje pro hodnocení a opakované skórování firem z hlediska dopadu ZOKB. Systém umožnil kompletní evidenci primárních i podpůrných aktiv, evidenci dodavatelů a OT (Operational Technology) zařízení včetně přidělených přístupů. Součástí byla i metodika pro GAP analýzu.
* **Technický pohled (CZ):** Vývoj v prostředí .NET DevExpress nad centrální MS SQL databází. Propojení s HR a ERP systémy pro automatizovaný import kmenových zaměstnanců a dodavatelských smluv. Návrh robustního datového modelu pro správu aktiv, opakované skórování a historizaci dat, podpořený certifikovaným know-how (ISMS dle ISO/IEC 27001).

### Dopad a výsledky (Business Impact & Results)
* **Komplexní evidence aktiv:** Úspěšné vytvoření jednotného registru primárních a podpůrných aktiv, dodavatelů a OT přístupů.
* **Automatizace compliance procesů:** Automatizované skórování a importy dat výrazně zrychlily identifikaci legislativních dopadů na jednotlivé společnosti.
* **Odborná garance (ISMS):** Využití certifikovaných znalostí (Manažer IT bezpečnosti) k vytvoření systému, který reálně odráží požadavky auditu a bezpečnosti.

---

## 6. Implementace bankovního systému MultiCash
* **Anglický název:** MultiCash Banking System Implementation
* **Období / Period:** 2024
* **Role:** Project Manager & System Administrator
* **Tech Stack / Klíčová slova:** `MultiCash`, `SAP ERP`, `LAN & Firewalls`, `Banking APIs`, `MS SQL`, `Vendor Management`, `PKI / Security Keys`

### Kontext a cíl (Context & Objective)
* **CZ:** Zajištění bezpečné a efektivní komunikace s bankovními institucemi (ČS, UniCredit, ČSOB, KB) pomocí aplikace MultiCash. Cílem bylo sjednotit platební styk pro společnosti Sev.en Services a Teplárna Kladno a plně jej integrovat s podnikovým systémem SAP na oddělených serverových farmách.
* **EN:** Ensuring secure and efficient communication with banking institutions (ČS, UniCredit, ČSOB, KB) using the MultiCash application. The objective was to unify payment processing for Sev.en Services and Teplárna Kladno and fully integrate it with the SAP enterprise system across separate server farms.

### Přehled řešení (Solution Perspective)
* **Byznysový pohled (CZ):** Sběr požadavků od oddělení platebního styku, zajištění smluvní dokumentace a přístupových klíčů. Příprava školení a tvorba uživatelské dokumentace. Systém nyní funguje jako centrální uzel pro odesílání platebních příkazů a stahování bankovních výpisů s přímou rolí systémového administrátora.
* **Technický pohled (CZ):** Návrh a příprava infrastruktury na serverových farmách v Mostě a na Kladně (aplikační servery, databáze, prostupy v LAN). Fyzická instalace a konfigurace ve spolupráci s dodavatelem. Úzká spolupráce se SAP konzultanty na mapování datových formátů pro export platebních příkazů ze SAPu a zpětný import bankovních výpisů.

### Dopad a výsledky (Business Impact & Results)
* **Úspěšný roll-out pro dvě společnosti:** Bezproblémové nasazení na dvou geograficky oddělených lokalitách (Most, Kladno).
* **End-to-end integrace se SAP:** Plná automatizace obousměrného datového toku mezi účetním systémem a bankami.
* **Zvýšení bezpečnosti a kontroly:** Centralizace přístupů a bezpečné uložení certifikátů a klíčů pod hlavičkou interního administrátora.

---

## 7. Implementace systému GNSS na velkostrojích
* **Anglický název:** GNSS System Implementation on Heavy Mining Machinery
* **Období / Period:** 2021
* **Role:** Project Manager & IT Coordinator
* **Tech Stack / Klíčová slova:** `GNSS / GPS`, `OT Integration`, `MS SQL Server`, `Data Visualization`, `Networking & Firewalls`, `3D Mining Models`

### Kontext a cíl (Context & Objective)
* **CZ:** Nasazení navigačního a monitorovacího systému GNSS na těžebních velkostrojích společnosti Vršanská uhelná (VUAS). Cílem bylo digitalizovat přípravu těžby, zefektivnit práci báňského oddělení a přesně propojit technologické a objemové modely s reálným pohybem strojů v terénu.
* **EN:** Deployment of a GNSS navigation and monitoring system on heavy mining machinery for Vršanská uhelná (VUAS). The goal was to digitize mining preparation, streamline the work of the mining department, and accurately connect technological and volume models with the actual movement of machines in the field.

### Přehled řešení (Solution Perspective)
* **Byznysový pohled (CZ):** Komplexní koordinace projektu mezi interním odborem báňských činností, uživateli a externími dodavateli (GPS, OT, GNSS). Systém plně využívá mapové podklady (vrty, letecké nálety) a specializované báňské modely. Nasazeny byly také vizualizační nástroje pro online sledování a zpětnou analýzu těžby.
* **Technický pohled (CZ):** Zajištění kompletní IT infrastruktury od přípravy serverů a připojení na centrální MS SQL databázi až po konfiguraci síťových prostupů (firewally). Řízení fyzické instalace hardwaru (OT) a aplikačního softwaru přímo na velkostrojích, klientských PC a serverech. Následná integrace a předávání dat z GNSS do primárního systému řízení výroby.

### Dopad a výsledky (Business Impact & Results)
* **Přesnost a digitalizace těžby:** Propojení reálného pohybu velkostrojů s přesnými 3D modely a mapovými podklady v reálném čase.
* **Úspěšná integrace IT a OT:** Bezproblémové napojení provozních technologií (OT) na strojích do podnikové IT sítě a centrálního SQL.
* **Datová návaznost na výrobu:** Zajištění automatického toku dat z GNSS přímo do podnikového systému řízení výroby.

---

## 8. Obměna docházkového systému elektrárny Počerady
* **Anglický název:** Replacement of Počerady Power Plant Attendance System
* **Období / Period:** 2020
* **Role:** On-Site Implementation Lead & IT Analyst
* **Tech Stack / Klíčová slova:** `Vendor Management`, `Access Control SW`, `Hardware Integration`, `LAN Configuration`, `ID Card Systems (RFID/NFC)`, `Change Management`

### Kontext a cíl (Context & Objective)
* **CZ:** Převzetí správy docházkového a přístupového systému (vč. návštěv a vjezdů) po akvizici elektrárny Počerady. Kvůli nekompatibilitě stávajícího hardwaru s novější verzí softwaru bylo cílem navrhnout a provést kompletní obměnu čteček a řídicích jednotek bez výpadku kritického provozu elektrárny.
* **EN:** Taking over the attendance and access control system (including visitor and vehicle management) following the acquisition of the Počerady power plant. Due to hardware incompatibility with the newer software version, the objective was to design and execute a complete replacement of readers and control units with zero downtime in critical plant operations.

### Přehled řešení (Solution Perspective)
* **Byznysový pohled (CZ):** Příprava analýzy, harmonogramu a zajištění schválení od vedení i zákazníka. Zajištění plynulého chodu koordinace s firmami skupiny ČEZ. Řízení plošné výměny zaměstnaneckých ID karet, nasazení nového systému žádostí o karty a komplexní proškolení obsluhy vrátnic pro agendu návštěv a vjezdů.
* **Technický pohled (CZ):** Působení jako vedoucí implementačního týmu na místě. Řízení přesunů zařízení mezi starou a novou LAN infrastrukturou a koordinace paralelní demontáže a montáže. Osobní konfigurace serverové části, řídicích jednotek a čteček včetně fyzické instalace koncových zařízení v perimetru.

### Dopad a výsledky (Business Impact & Results)
* **Bezvýpadkový přechod (Zero Downtime):** Úspěšná výměna kritické bezpečnostní infrastruktury bez narušení nepřetržitého provozu elektrárny.
* **Komplexní integrace přístupů:** Plynulé převedení docházky, vjezdů a návštěv do nového systému včetně úspěšné plošné výměny všech ID karet.
* **Perfektní koordinace třetích stran:** Bezproblémová spolupráce bezpečnostních, síťových a hardwarových týmů obou korporací (Sev.en a ČEZ).

---

## 9. Vývoj aplikace a obměna mobilních čteček
* **Anglický název:** Mobile App Development & Reader Replacement for Entry Perimeters
* **Období / Period:** 2019
* **Role:** Lead IT Analyst & Project Manager
* **Tech Stack / Klíčová slova:** `Mobile Application Design`, `UI/UX Prototyping`, `Vendor Management (IMA)`, `K4 Attendance System`, `Hardware Selection`, `UAT & Testing`

### Kontext a cíl (Context & Objective)
* **CZ:** Na základě požadavků zákazníků docházkového systému byla identifikována potřeba modernizovat odbavení na vjezdových autobránách. Cílem bylo navrhnout novou mobilní aplikaci, vybrat adekvátní hardware nahrazující dosluhující mobilní čtečky a zajistit integraci se stávajícím systémem K4 od společnosti IMA.
* **EN:** Based on requirements from attendance system customers, a need was identified to modernize vehicle gate processing. The objective was to design a new mobile application, select adequate hardware to replace aging mobile readers, and ensure integration with the existing K4 attendance system from IMA.

### Přehled řešení (Solution Perspective)
* **Byznysový pohled (CZ):** Od sběru požadavků k vizuálnímu prototypu – sestavení funkční prezentace uživatelského rozhraní a aplikační logiky pro schválení zákazníkem. Řízení postupného nasazení (roll-out) na všech vstupních perimetrech včetně kompletního zaškolení obsluhy vrátnic a strážných.
* **Technický pohled (CZ):** Vytvoření detailní specifikace (zadání) pro dodavatele (IMA) k vývoji aplikace s přímou komunikací do systému K4. Testování (UAT) před nasazením do ostrého provozu a technické vytipování a validace nových hardwarových mobilních čteček z hlediska kompatibility a výkonu.

### Dopad a výsledky (Business Impact & Results)
* **Modernizace a zrychlení odbavení:** Nasazení nové aplikace a moderního hardwaru výrazně zefektivnilo proces kontroly vozidel a osob na vjezdových branách.
* **Úspěšné end-to-end nasazení:** Zajištění hladkého přechodu od tvorby prototypu až po plošnou integraci bez přerušení bezpečnosti perimetru.

---

## 10. Automatizované zpracování přijatých faktur (AP)
* **Anglický název:** Accounts Payable (AP) Invoice Automation
* **Období / Period:** 2017
* **Role:** Lead IT Analyst & Process Architect
* **Tech Stack / Klíčová slova:** `SAP ERP`, `Accounts Payable (AP)`, `OCR & Scanning SW`, `Barcode Routing`, `Process Optimization`, `DMS`

### Kontext a cíl (Context & Objective)
* **CZ:** Třídění a přepisování velkého objemu přijatých faktur pro různé dceřiné společnosti představovalo pomalý a chybový manuální proces. Cílem projektu bylo navrhnout a realizovat centrální skenovací pracoviště, které by tyto dokumenty automaticky digitalizovalo a bezpečně směřovalo přímo do správných účetních okruhů v systému SAP.
* **EN:** Sorting and transcribing a high volume of incoming invoices for various subsidiaries was a slow, error-prone manual process. The project's goal was to design and implement a central scanning workstation that would automatically digitize these documents and securely route them directly to the correct accounting company codes in the SAP system.

### Přehled řešení (Solution Perspective)
* **Byznysový pohled (CZ):** Vytvoření štítkovacího systému – každá faktura je na podatelně označena odpovídajícím kódem dle firmy. Účetní na jednotlivých dceřiných společnostech se již nestarají o fyzické papíry; faktury mají automaticky naskenované a přiřazené v SAPu, kde rovnou provádějí likvidaci a schvalování.
* **Technický pohled (CZ):** Analýza, výběrové řízení a samotná realizace skenovacího pracoviště. Nastavení skenovacího softwaru pro rozpoznávání kódů a navržení automatizovaného workflow. V úzké spolupráci se SAP konzultanty bylo zajištěno datové napojení, které přesměruje digitální PDF kopii do přesně definovaného účetního okruhu v SAPu.

### Dopad a výsledky (Business Impact & Results)
* **Skokové zrychlení procesu:** Dramatická redukce času mezi fyzickým přijetím faktury na podatelně a jejím doručením k elektronické likvidaci účetnímu oddělení.
* **Eliminace chyb a ztrát:** Centralizovaný digitální přenos zabránil riziku ztráty papírových dokumentů a odstranil manuální třídění na úrovni účtáren.
* **Synergie IT a Financí:** Úspěšná demonstrace propojení fyzického hardwaru (skenery), podatelny a centrálního finančního systému (SAP).