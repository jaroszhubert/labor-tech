# 🔍 Audyt strony labor-tech.pl — treść, architektura i design

## TL;DR

Strona **labor-tech.pl** posiada znakomitą bazę wyjściową, której brakowało w ovydata: **prawdziwe nazwisko, 30 lat autentycznego doświadczenia, zdjęcie właścicielki (Anna Jarosz) oraz realne certyfikaty branżowe**. 

Niestety strona została „ubrana” w ten sam szablonowy garnitur co generyczne landing page AI/SaaS:
1. **Konflikt dwóch światów (B2B vs B2C)** — na jednej stronie głównej mieszają się zaawansowane mosty cyrkonowe dla lekarzy z klejeniem pękniętej protezy dla pacjenta.
2. **Lanie wody i agencyjny żargon** — słowa „przewidywalny” i „spokojny workflow” powtarzają się dziesiątki razy, a do stomatologów mówi się językiem agencji reklamowej („brief i feedback” zamiast karty zlecenia i konsultacji przypadku).
3. **Syndrom „pudełek z cieniem” (Card Soup)** — niemal każdy element, akapit i nagłówek jest wsadzony w identyczny zaokrąglony kafelek z obwódką, cieniem i strzałeczką `→` w rogu. Dodatkowo wstawiono animowany pasek marquee rodem z serwisów Web3/krypto.

---

## 1. ARCHITEKTURA I STRATEGIA: Największy błąd

### Dwie wykluczające się grupy docelowe na jednym ekranie

Strona próbuje jednocześnie sprzedawać usługi dwóm zupełnie różnym odbiorcom:
- **Lekarz dentysta (B2B)** — szuka rzetelnego partnera laboratoryjnego do prac stałych (korony, mosty, e.max, cyrkon, skany STL, dopasowanie okluzji, terminowość).
- **Pacjent indywidualny (B2C)** — najczęściej osoba starsza lub w nagłej potrzebie, której pękła proteza i szuka ratunku „na już w Lublinie”.

> [!WARNING]
> Obecnie na stronie głównej lekarz czytający o „parametrach frezowania CAD/CAM i estetyce IPS e.max” nagle trafia na wielką sekcję: *„Jeśli proteza pękła, uwiera lub poluzowała się…”*. Z kolei pacjent z pękniętą protezą gubi się w żargonie o „skanach STL i warstwowym napalaniu ceramiki”.

**Rekomendacja:**
Strona główna powinna być w **85% dedykowana gabinetom stomatologicznym (B2B)**, z wyraźnym, eleganckim bannerem/przekierowaniem u góry lub w menu: *„Jesteś pacjentem? Potrzebujesz pilnej naprawy protezy w Lublinie? Przejdź tutaj →”*.

---

## 2. TREŚĆ (COPYWRITING) — Co psuje wiarygodność

### 2.1 Słowa-wytrychy i powtórzenia

Podobnie jak na ovydata, strona cierpi na monotematyczny słownik wygenerowany przez prompt AI:

| Zwrot | Wystąpienia | Dlaczego szkodzi |
|---|---|---|
| **„przewidywalny / przewidywalność”** | **22×** | Występuje niemal w każdym nagłówku i akapicie. Zamiast budować spokój, brzmi jak zacięta płyta. |
| **„powtarzalny / powtarzalność”** | **8×** | Używane zamiennie z „przewidywalny”, tworząc masło maślane. |
| **„spokój w gabinecie / spokojny workflow”** | **7×** | Puste hasło bez pokrycia w konkretnych procedurach. |
| **„brief i ustalenia”** | **5×** | **Błąd branżowy!** Żaden stomatolog nie wysyła „briefu”. W stomatologii funkcjonuje *zlecenie protetyczne*, *karta laboratoryjna* lub *rejestracja zwarcia / wycisk*. Słowo „brief” krzyczy, że tekst pisał copywriter z marketingu. |
| **„bez niespodzianek”** | **4×** | Zawsze w cudzysłowie — brzmi asekuracyjnie. |

### 2.2 Anonimowe opinie z dopiskiem z gwiazdką

W sekcji „Opinie lekarzy”:
> *„Prace przychodzą dopasowane i przewidywalne. Komunikacja jest szybka i konkretna.”*  
> — Gabinet stomatologiczny • Lublin  
> *\*Opinie pochodzą od współpracujących gabinetów. Treści skrócone dla czytelności.*

Taka opinia bez nazwiska lekarza, nazwy kliniki i zdjęcia wygląda w 100% jak zmyślona przez chatbota. Jeśli Anna Jarosz prowadzi pracownię od 25 lat i współpracowała z Centrum Stomatologii w Lublinie, to **1 prawdziwa rekomendacja z imieniem, nazwiskiem i nazwą kliniki** (nawet krótka) bije na głowę 5 anonimowych kafelków.

### 2.3 Czego brakuje lekarzowi (konkrety B2B):

1. **Jakie skanery i formaty plików przyjmujecie?** (Medit Link, 3Shape Communicate, iTero, pliki otwarte `.stl`, `.ply`, `.obj`).
2. **Jaki jest standardowy czas realizacji (turnaround)?** (np. korona cyrkonowa: 4–5 dni roboczych, naprawa: 24h, proteza: 7–10 dni).
3. **Logistyka w Lublinie i okolicach:** Czy macie własnego kuriera/odbieracie wyciski osobiście z gabinetu w Lublinie, czy gabinet musi zamawiać kuriera?
4. **Trudne przypadki estetyczne:** Czy lekarz może skierować pacjenta do pracowni na ul. Sielankową na **indywidualny dobór koloru w świetle dziennym** przez technika? (To ogromna wartość dla stomatologa!).

### 2.4 Czego brakuje pacjentowi (konkrety B2C na podstronie napraw):

1. **Czas naprawy:** Czy naprawa pęknięcia jest możliwa w 1–3 godziny / na poczekaniu? (Dla pacjenta bez zębów to sprawa życia i śmierci).
2. **Cena od…:** Choćby orientacyjne widełki: „sklejenie protezy od X zł”, „dostawienie zęba od Y zł”.
3. **Lokalizacja i parking:** Jak wejść, gdzie zaparkować przy Sielankowej 9/1a, czy gabinet jest dostępny bez barier.

---

## 3. DESIGN — Dlaczego wygląda „AIowo” i szablonowo

### 3.1 Pudełkoza (Card Soup)

Wszystko na stronie jest kartą:
- 4 karty usług z tą samą strzałką `→`
- 3 karty zaufania z nazwami Ivoclar / BEGO
- 3 karty procesu z prostymi ikonami
- 3 karty materiałów w sekcji technologicznej
- 4 karty dla pacjenta
- 2 karty z opiniami

Kiedy wszystko jest kartą z tłem `rgba(255,255,255,0.98)`, obwódką `1px solid rgba(0,35,55,0.08)` i `box-shadow: 0 18px 38px`, strona traci hierarchię wizualną. Oko odbiorcy męczy się monotonią.

### 3.2 Animowany pasek Marquee

```html
<div class="design-marquee">
  <span>Korony i mosty</span><span>Protezy</span><span>Szyny</span><span>Ivoclar Certified</span>...
</div>
```
Przesuwający się pasek tekstu (ticker/marquee) pasuje do agencji kreatywnych Web3, krypto albo streetwearu. W pracowni medyczno-protetycznej z 30-letnią tradycją wygląda tanio i sprawia wrażenie wklejonego na siłę z biblioteki komponentów.

### 3.3 Generyczne ikony w procesie

Trzy kroki procesu mają generyczne ikonki SVG (kilka poziomych kresek jak plik tekstowy, ptaszek w okręgu, lista). Zamiast tego proces w pracowni protetycznej powinien być zilustrowany **rzeczywistymi detalami** lub czystą typografią numerowaną (`01`, `02`, `03`).

### 3.4 Pływające etykiety i mikro-elementy

Tag przy zdjęciu na górze: `Realizacja · korona pełnoceramiczna · IPS e.max` z doczepioną liczbą `25` — to kalka z Dribbble/szablonów Figma, która nie niesie żadnej wartości dla lekarza ani pacjenta.

---

## 4. PLAN NAPRAWCZY — Konkretne propozycje zmian

### 4.1 Przeredagowanie Hero (B2B z klasą)

**Obecnie:**
> *Precyzja w laboratorium. Spokój w gabinecie.*  
> *Wspieramy lekarzy stomatologów w realizacjach, które wymagają precyzji, powtarzalnej jakości i sprawnej komunikacji technicznej. Jako pracownia protetyczna w Lublinie wiemy, że precyzja w laboratorium i spokój w gabinecie wynikają z jasnych ustaleń, kontroli jakości i terminowej realizacji.*

**Propozycja (konkret, rzemiosło, medycyna):**
> # Prace protetyczne, które siadają na modelu za pierwszym razem.
> **Laboratorium protetyczne Anny Jarosz w Lublinie.** Łączymy 30 lat doświadczenia klinicznego z cyfrowym frezowaniem CAD/CAM. Korony cyrkonowe, IPS e.max i protezy wykonywane w bezpośrednim kontakcie: lekarz – technik.
>
> `[ Zobacz ofertę dla gabinetów ]` `[ Zadzwoń: +48 608 373 443 ]`
> 
> *Dla pacjentów: [Ekspresowa naprawa protez w Lublinie →]*

---

### 4.2 Zmiana sekcji „O pracowni / Anna Jarosz” (Budowanie autorytetu)

Zamiast generycznych kafelków z hasłami, zróbmy z tego **prawdziwą historię rzemieślnika**:
- Podkreślić: Ponad 30 lat przy stole protetycznym, w tym wieloletnie doświadczenie w Centrum Stomatologii w Lublinie.
- Usunąć hasło „krótka komunikacja techniczna” → zastąpić: *„Dzwoniąc do Labor-Tech, rozmawiasz bezpośrednio z technikiem wykonującym Twoją pracę, a nie z rejestratorką czy handlowcem.”*
- Wyeksponować certyfikaty: Anna szkoliła się bezpośrednio w Ivoclar (Liechtenstein/Niemcy) w 1996 roku, kiedy ceramika w Polsce dopiero raczkowała — to jest **ogromna przewaga konkurencyjna**, którą należy się chwalić!

---

### 4.3 Likwidacja „pudełkozy” w sekcjach

1. **Usunąć animowane marquee** — zamiast tego dać elegancki pasek logotypów technologii: *Ivoclar IPS e.max | BEGO | Scheu Dental | Vita*.
2. **Sekcja Usługi:** Zamiast 4 identycznych białych kart z min-height 220px:
   - Zrobić układ asymetryczny: 2 główne filary prac stałych (Korony cyrkonowe & e.max) jako większe elementy wizualne ze zdjęciem, a szyny i naprawy jako uzupełniające.
   - Usunąć strzałki `→` w prawym górnym rogu.
3. **Sekcja Procesu:** Zastąpić obecne karty poziomą, czystą osią czasu (Timeline) ze wskazaniem realnych terminów:
   - `01. Skan STL lub wycisk` (wsparcie Medit, 3Shape, Carestream)
   - `02. Weryfikacja marginesu i okluzji` (kontakt w razie wątpliwości przed frezowaniem)
   - `03. Gotowa praca w terminie` (odbiór w Lublinie / wysyłka)

---

### 4.4 Przebudowa strony dla pacjenta (`/naprawa-protez-lublin/`)

Dla pacjenta liczą się 3 rzeczy: **czas, cena i dojazd**.
- Dodać wyraźny komunikat: *„Naprawy w trybie pilnym — większość pęknięć realizujemy w ciągu [X] godzin.”*
- Dodać prostą tabelę lub listę orientacyjną:
  - Pęknięcie płyty protezy
  - Złamanie protezy na pół
  - Dostawienie zęba / klamry
  - Podścielenie (poprawa przylegania)
- Dodać mapkę z informacją o parkingu na ul. Sielankowej (Czechów / okolice).

---

## 5. PODSUMOWANIE PORÓWNAWCZE: ovydata vs labor-tech

| Element | ovydata-website | labor-tech |
|---|---|---|
| **Produkt / Usługa** | Custom dashboardy (Vue / .NET) | Pracownia protetyczna (B2B) + naprawy (B2C) |
| **Główny problem contentu** | Zmyślone korpo-hasła, brak case study | Zderzenie dwóch grup docelowych + żargon agencyjny („brief”, „workflow”) |
| **Główny problem designu** | 4 białe karty w kółko, brak grafik | Pudełkoza (card soup), animowany ticker marquee, strzałki `→` w kafelkach |
| **Największy niewykorzystany atut** | Doświadczenie IT i case study pralni | 30 lat doświadczenia Anny Jarosz, certyfikaty Ivoclar/BEGO, prawdziwe zdjęcia |

---

## Rekomendowany plan działania:

1. **Krok 1 (Treść):** Oczyścić teksty z korpo-żargonu („brief”, „przewidywalność x22”) i wprowadzić terminologię stomatologiczną.
2. **Krok 2 (Architektura):** Rozdzielić komunikację: strona główna w 90% profesjonalna dla lekarzy, a podstrona pacjenta dedykowana naprawom z czasem i dojazdem.
3. **Krok 3 (Design):** Usunąć ticker marquee, zróżnicować karty, usunąć powtarzający się schemat kafelków i strzałek.
