# Dokumentacja Projektu: TrainerPro - Kompleksowa Platforma SaaS dla Trenerów Personalnych
 
## 1. Wstęp i Przegląd Projektu
* **Nazwa Projektu:** TrainerPro
* **Model Biznesowy:** B2B / B2C (Software as a Service)
* **Koncepcja:** TrainerPro to zintegrowana platforma zaprojektowana z myślą o niezależnych trenerach personalnych oraz małych studiach fitness. Aplikacja ma na celu całkowite wyeliminowanie przestarzałych narzędzi (takich jak arkusze Excel, notatniki i komunikatory typu Messenger), przenosząc cały proces obsługi klienta do jednego, profesjonalnego ekosystemu.
 
## 2. Analiza Biznesowa (Problem i Rozwiązanie)
 
### 2.1. Diagnoza Problemu:
Obecny rynek usług trenerskich opiera się na mocno pofragmentowanych narzędziach. Trenerzy tracą wiele godzin tygodniowo na pracę administracyjną:
* **Chaos informacyjny:** Plany treningowe są wysyłane w plikach PDF lub Excel, co utrudnia ich aktualizację.
* **Rozproszona komunikacja:** Wiadomości od klientów gubią się w prywatnych komunikatorach, co obniża jakość usług.
* **Problemy z płatnościami:** Brak zautomatyzowanego systemu przypomnień o kończących się pakietach treningowych prowadzi do utraty płynności finansowej.
 
### 2.2. Rozwiązanie - Funkcje TrainerPro:
* **Kreator Planów Treningowych:** Intuicyjny interfejs "przeciągnij i upuść" (drag & drop) pozwalający na szybkie budowanie i modyfikowanie jednostek treningowych.
* **Śledzenie Postępów (Data Tracking):** Zintegrowane wykresy monitorujące wagę, obwody ciała oraz progresję ciężaru w konkretnych ćwiczeniach.
* **Wewnętrzny Komunikator:** Dedykowany czat na linii trener-podopieczny, pozwalający na szybki feedback i wysyłanie filmów z techniką ćwiczeń.
* **Moduł Finansowy:** Zautomatyzowane subskrypcje i płatności podpięte pod bezpieczną bramkę.
 
## 3. Analiza Ryzyka - "Kill the Idea"
Aby projekt miał szansę na sukces, konieczne jest chłodne spojrzenie na potencjalne zagrożenia rynkowe.
 
* **Zagrożenie 1: Wysokie nasycenie rynku (Red Ocean).** Istnieją już duże aplikacje zagraniczne (np. Trainerize).
*Rozwiązanie (Mitygacja):* Skupienie się początkowo wyłącznie na rynku polskim, oferując w 100% zlokalizowany interfejs, polskie wsparcie techniczne oraz integrację z lokalnymi systemami płatności (np. BLIK).
 
* **Zagrożenie 2: Opór technologiczny klientów.** Klienci trenerów mogą nie chcieć instalować kolejnej aplikacji.
*Rozwiązanie (Mitygacja):* TrainerPro będzie działać jako PWA (Progressive Web App), co oznacza, że klient otworzy ją z poziomu linku w przeglądarce, bez konieczności pobierania czegokolwiek ze sklepu.
 
* **Zagrożenie 3: Bezpieczeństwo danych wrażliwych.** Aplikacja przechowuje dane o zdrowiu i sylwetce.
*Rozwiązanie (Mitygacja):* Zastosowanie bazy danych Supabase z rygorystycznymi regułami RLS (Row Level Security), zapewniającymi pełną zgodność z RODO.
 
## 4. Proponowany Stos Technologiczny (Tech Stack)
Wybór technologii został podyktowany potrzebą szybkiego wdrożenia na rynek (Time-to-Market) oraz łatwością skalowania.
* **Frontend:** React JS połączony z Tailwind CSS oraz gotowymi komponentami Shadcn/ui, co gwarantuje nowoczesny i responsywny interfejs użytkownika.
* **Backend (BaaS):** Supabase. Wykorzystano moduł autoryzacji, bazę danych PostgreSQL o dużej wydajności oraz system Storage do przechowywania materiałów wideo i zdjęć sylwetki.
* **Płatności:** Integracja API Stripe do obsługi płatności cyklicznych.
 
## 5. Architektura Systemu
 
Poniższy diagram przedstawia wysokopoziomową architekturę przepływu danych w aplikacji:
 
```mermaid
graph TD
    A[Trener i Podopieczny] --> B[Aplikacja TrainerPro]
    B --> C[Frontend React JS]
    B --> D[Backend Supabase]
    D --> E[Baza Danych PostgreSQL]
    D --> F[Autoryzacja i Bezpieczenstwo]
    B --> G[Bramka Platnosci Stripe]
