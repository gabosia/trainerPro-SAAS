# Dokumentacja Projektowa SAAS: TrainerPro

## 1. Koncepcja i Cel Biznesowy
**TrainerPro** to platforma SAAS (Software as a Service) zaprojektowana dla trenerów personalnych. Rozwiązuje problem rozproszonej komunikacji (Messenger, SMS) i nieefektywnego planowania (Excel). Platforma centralizuje plany treningowe, postępy podopiecznych i płatności w jednym miejscu.

## 2. Stos Technologiczny (Tech Stack)
Aplikacja została zaprojektowana w oparciu o następujące technologie:
* **Frontend:** React JS (Single Page Application)
* **Styling:** Tailwind CSS (utility-first CSS)
* **Interfejs Użytkownika:** Shadcn UI (gotowe, dostępne i nowoczesne komponenty)
* **Backend i Baza Danych:** Supabase / Firebase (obsługa autoryzacji, bazy danych w czasie rzeczywistym oraz przechowywania plików wideo/zdjęć)

## 3. Analiza Ryzyka - "Kill the Idea"
Aby zweryfikować sens biznesowy projektu, przeprowadzono analizę "Kill the Idea", wymieniając najważniejsze powody, dla których projekt mógłby upaść:

* **Zagrożenie 1: Trenerzy wolą darmowe rozwiązania (Excel/Dysk Google).**
  * *Dlaczego to może zabić projekt?* Ludzie nie lubią płacić za coś, co mogą robić za darmo, nawet jeśli jest to niewygodne.
  * *Jak temu zapobiec?* TrainerPro musi od pierwszego dnia oszczędzać czas. Dodamy automatyczne przypomnienia SMS o treningach i generowanie szablonów ćwiczeń jednym kliknięciem, czego Excel nie potrafi.
* **Zagrożenie 2: Wysoki "Churn" (rezygnacja klientów).**
  * *Dlaczego to może zabić projekt?* Klienci trenerów często tracą motywację po 2-3 miesiącach, przez co trener traci dochód i może zrezygnować z naszego SAASa.
  * *Jak temu zapobiec?* Wdrożenie w aplikacji modułu grywalizacji i wizualizacji postępów (wykresy, odznaki), który utrzyma zaangażowanie podopiecznych na dłużej.

## 4. Model Biznesowy (Monetyzacja)
Model opiera się na miesięcznej subskrypcji opłacanej przez trenera:
* **Plan Basic:** Do 5 podopiecznych (darmowy - zachęta do testów).
* **Plan Pro:** Do 30 podopiecznych (np. 99 PLN / miesiąc).
* **Plan Elite:** Nielimitowana liczba podopiecznych + własny branding.

## 5. Kluczowe Funkcjonalności (MVP)
1. **Zarządzanie podopiecznymi (CRM):** Baza klientów z historią wagi, wymiarów i celów sylwetkowych.
2. **Kreator Treningów:** Kalendarz drag&drop do układania planów na cały tydzień.
3. **Panel Podopiecznego:** Widok na smartfonie, gdzie klient odznacza wykonane serie i wpisuje podniesiony ciężar.