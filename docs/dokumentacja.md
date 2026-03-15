# Dokumentacja Projektowa SAAS: TrainerPro

## 1. Opis i cel biznesowy
**TrainerPro** to platforma SAAS (Software as a Service) dedykowana trenerom personalnym oraz instruktorom fitness. Aplikacja rozwiązuje problem rozproszonej komunikacji i braku jednego miejsca do zarządzania podopiecznymi. Pozwala trenerom na układanie planów treningowych, monitorowanie postępów klientów oraz automatyzację rozliczeń, a klientom oferuje przejrzysty panel z ich celami i treningami.

## 2. Stos technologiczny (Tech Stack)
Zgodnie z założeniami projektowymi, aplikacja wykorzystuje nowoczesny stack frontendowy oraz chmurowy backend (BaaS):
* **Frontend:** React JS - framework do budowy dynamicznego interfejsu (Single Page Application).
* **Styling:** Tailwind CSS - do szybkiego budowania nowoczesnych widoków w oparciu o klasy użytkowe (utility-first).
* **Komponenty UI:** Shadcn UI - dla zachowania spójnego, profesjonalnego wyglądu i wysokiej dostępności (gotowe, stylowane komponenty takie jak przyciski, modale, formularze).
* **Backend, Baza Danych i Autoryzacja:** Supabase (alternatywnie Firebase) - do bezpiecznego logowania (Auth), przechowywania danych o treningach i profilach w czasie rzeczywistym oraz hostingu materiałów wideo (Storage).

## 3. Główne funkcjonalności (MVP - Minimum Viable Product)
* **Zarządzanie podopiecznymi:** Lista klientów trenera z historią ich wagi, wymiarów i celów.
* **Kreator planów treningowych:** Narzędzie typu "drag & drop" pozwalające na szybkie przypisywanie ćwiczeń do konkretnych dni tygodnia.
* **Panel Klienta:** Osobny widok dla podopiecznego, w którym widzi swój plan na dany dzień i może odznaczać wykonane zadania.
* **Płatności w modelu subskrypcyjnym (SAAS):** Trener opłaca miesięczny abonament za korzystanie z platformy (np. zależny od liczby podopiecznych).

## 4. Architektura i struktura projektu
Wersjonowanie kodu odbywa się za pomocą systemu Git. Dokumentacja projektowa przechowywana jest w katalogu `/docs` w formacie Markdown, co ułatwia jej przeglądanie bezpośrednio z poziomu repozytorium GitHub.