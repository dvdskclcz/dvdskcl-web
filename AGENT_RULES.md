# Antigravity Agent Rules: IT Portfolio Website

## 🎯 Cíl projektu
Vytvořit profesionální, moderní a vysoce reprezentativní osobní one-page portfolio pro:
**David Skácel – IT Analyst & Project Manager | Process Digitalization, Automation & AI Adoption**.

Web slouží jako technická výkladní skříň (Proof of Work) pro technické ředitele (CTO), provozní manažery a technologické recruitery.

---

## 🏗️ Architektura a technologie
- **Framework:** Astro (Static Site Generation – SSG)
- **Styling:** Tailwind CSS (výchozí elegantní tmavý režim – Dark slate/zinc background)
- **Komponenty:** Modulární `.astro` komponenty
- **Data Source:** Striktně oddělená data v `src/data/profile.json` a `src/data/projects.json`

---

## ✅ Striktní pravidla: CO DĚLAT (DO)
1. **Data-Driven:** Veškeré texty o mně, projekty, technologie a odkazy se MUSÍ načítat ze souborů `src/data/*.json`. V komponentách nesmí být žádný pevně zakódovaný text (hardcoded content).
2. **Designový tón:** Čistý inženýrský minimalismus (styl Linear / Vercel / GitHub). Tmavé pozadí (`bg-slate-950` nebo `bg-zinc-950`), akcentní barvy jemná modrá / smaragdová / fialová pro štítky.
3. **Struktura projektu (STAR):** U každé případové studie musí být jasně odděleno:
   - Problém a výchozí stav (Context)
   - Architektura a tok dat (Architecture / Flow)
   - Konkrétní výsledky a metriky (Business Impact)
4. **Vizuální toky dat:** Tok dat u projektů (např. *Wiki -> Git -> AnythingLLM -> Ollama*) naformátuj jako stylové interaktivní flow-boxy nebo čisté diagramy v Tailwindu.
5. **Dvojjazyčnost:** Připravit čisté přepínání jazyků (CZ jako výchozí, EN na `/en`).
6. **Jasná CTA tlačítka:**
   - Hlavní CTA: Rezervace hovoru (odkaz na Cal.com: `https://cal.com/dvdskcl`).
   - Sekundární CTA: Prohlídka GitHubu (`https://github.com/dvdskclcz`) a spojení na LinkedIn.
7. **Responzivita a rychlost:** 100% funkční na mobilu, tabletu i 4K monitoru. Žádné zbytečné externí knihovny, které brzdí načítání.

---

## 🚫 Striktní pravidla: CO NEDĚLAT (NOT TO DO)
1. **ŽÁDNÝ generický buzzword balast:** Nepoužívat klišé věty typu „jsem dynamický vizionář hledající výzvy“. Vše musí stát na faktech, datech a konkrétních nástrojích.
2. **ŽÁDNÉ těžké frontend frameworky:** Nepřidávat do projektu zbytečný React runtime pro jednoduché statické zobrazení, pokud to není nezbytné pro interaktivní stav.
3. **ŽÁDNÁ citlivá data:** Do kódu ani JSONů nepatří žádná reálná hesla, interní IP adresy, neveřejné firemní názvy databází ani interní smlouvy.
4. **ŽÁDNÉ stockové generické obrázky:** Žádné fotky podávajících si rukou nebo robotů s modrým světlem. Vizuální síla webu stojí na kódu, architektuře, odznacích a typografii.