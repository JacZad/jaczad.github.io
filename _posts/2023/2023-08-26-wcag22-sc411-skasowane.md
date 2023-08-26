---
title: 'WCAG 2.2: Usunięcie kryterium 4.1.1'
date: 2023-08-26
tags: ['WCAG', 'HTML', 'walidacja', 'Deque']
---

W oczekiwaniu na oficjalne zatwierdzenie nowej wersji WCAG przyglądam się kryterium sukcesu 4.1.1: Poprawność kodu. Przyglądam się pewnie ostatni raz, bo wkrótce wyleci z hukiem. A ja się zastanawiam, czy to dobrze, czy może nie bardzo.

WCAG, czyli Wytyczne dotyczące Dostępności Treści Internetowych, to międzynarodowe standardy opracowane przez World Wide Web Consortium (W3C) mające na celu zapewnienie dostępności cyfrowej dla wszystkich użytkowników, w tym osób z niepełnosprawnościami. W najnowszej wersji, czyli WCAG 2.2, zaplanowane są pewne istotne zmiany. Jedną z najważniejszych jest usunięcie kryterium sukcesu 4.1.1 Poprawność kodu. Dlaczego autorzy zdecydowali się na usunięcie tego kryterium? Czy jest to dobre czy złe z punktu widzenia dostępności cyfrowej?

## Wprowadzenie do WCAG 2.2

Wytyczne WCAG 2.2 są kontynuacją wcześniejszych wersji, takich jak WCAG 2.0 i WCAG 2.1. Powstały po to, żeby mieć jasne wytyczne, jak zapewnić dostępność treści internetowych dla osób z różnymi rodzajami niepełnosprawności, takimi jak trudności z widzeniem, słuchem, ruchem czy kognitywne. Obejmują one wiele kryteriów sukcesu, które określają wymagania dotyczące dostępności stron internetowych.

Kryterium sukcesu 4.1.1 , które zostało wprowadzone w WCAG 2.0, dotyczyło zapewnienia, że strony napisane w językach znaczników, takich jak HTML i SVG, są napisane w taki sposób, aby przeglądarki i technologie wspomagające mogły je jednoznacznie zrozumieć. Jednakże, wraz z postępem technologicznym, to kryterium stało się coraz mniej istotne.

Kiedy WCAG 2.0 zostały opublikowane, nie było jeszcze ustalonych standardów dotyczących obsługi błędów składniowych. Dlatego kryterium 4.1.1 miało na celu zapewnienie, że błędnie napisany kod nie będzie powodował problemów dla osób korzystających z technologii wspomagających. Jednak obecnie przeglądarki radzą sobie z niepoprawnym kodem znacznie lepiej, a technologie wspomagające korzystają z modelu obiektowego przeglądarki, zamiast tworzyć własne modele na podstawie kodu źródłowego.

Obecnie większość przeglądarek automatycznie poprawia niepoprawny kod, takie jak brakujące znaczniki początkowe i końcowe, a także niektóre inne problemy, takie jak nieprawidłowe zagnieżdżanie elementów. Dzięki temu, kryterium sukcesu 4.1.1 staje się niepotrzebne i niepraktyczne w kontekście współczesnych przeglądarek i technologii wspomagających.

## Problemy z interpretowaniem

Interpretacja kryterium sukcesu 4.1.1 była często różna w zależności od interpretacji osób testujących dostępność. Niektórzy uważali, że kryterium dotyczy poprawności składniowej HTML, podczas gdy inni sądzili, że odnosi się ono jedynie do składni znaczników. Przykładowo, syntaktycznie HTML pozwala na zagnieżdżanie elementów takich jak linki wewnątrz przycisków, ale model zawartości tego nie przewiduje. W związku z tym, w zależności od interpretacji kryterium, można dojść do różnych wniosków dotyczących wystąpienia błędu.

Usunięcie kryterium sukcesu 4.1.1 Parsing jest dobrą wiadomością dla wielu osób zajmujących się dostępnością cyfrową. Wiele problemów zgłaszanych w ramach tego kryterium, takich jak zduplikowane identyfikatory, nie ma rzeczywistego wpływu na funkcjonalność treści dla użytkowników z niepełnosprawnościami. Usuwanie takich problemów wprowadzało jedynie dodatkową pracę dla twórców stron internetowych, która nie miała istotnego wpływu na dostępność.

Jeśli jednak zduplikowany identyfikator powoduje problem, na przykład poprzez generowanie nieprawidłowej etykiety dostępnościowej lub nieprawidłowego powiązania, to takie problemy będą nadal zgłaszane jako naruszenie innych kryteriów sukcesu, takich jak 1.3.1 Informacje i Relacje czy 4.1.2 Nazwa, Rola, Wartość.

## Zmiany w axe-core

Axe-core to popularne narzędzie do testowania dostępności stron internetowych. Wersja 4.8 axe-core, planowana na sierpień 2023 roku, wprowadzi zmiany zgodnie z aktualizacją W3C. Obecnie axe-core ma trzy reguły, które testują kryterium sukcesu 4.1.1 Parsing, dotyczące zduplikowanych identyfikatorów.

Reguła duplicate-id-aria w axe-core będzie teraz zgłaszana w ramach kryterium sukcesu 4.1.2 Nazwa, Rola, Wartość. Sprawdza ona, czy identyfikatory używane w ARIA i etykietach dostępnościowych nie są zduplikowane. Wyniki tej reguły będą zgłaszane jako "wymaga przeglądu" zamiast jako naruszenie, ponieważ nie zawsze oznaczają one problem dostępności.

Reguły duplicate-id i duplicate-id-active, które sprawdzają obecność zduplikowanych identyfikatorów na elementach, które nie mają wpływu na dostępność strony, zostaną zdeprecjonowane. Oznacza to, że te reguły zostaną domyślnie wyłączone, a wersja axe-core 5.0 usunie je całkowicie. Reguły te otrzymały tag "wcag2a-obsolete", dla osób, które z różnych powodów tymczasowo muszą nadal wykonywać te reguły ze względów zgodności wstecznej.

## Podsumowanie
Rozwój technologii i rodzajów treści cyfrowych wymusza dodawanie kolejnych kryteriów sukcesu, a nawet wytycznych. Jednak ten sam rozwój sprawia, że dawne problemy zmieniają się w problemiki. Nie oznacza to jednak, że teraz już można tworzyć śmieciowy kod, bo to generuje problemy nie tylko z dostępnością, ale także z wydajnością i stabilnością. Jednak operowanie technologii asystujących na drzewie DOM bardzo wiele upraszcza. Do rozważenia zostawiam, czy zamiast poprawności kodu nie powinno się sprawdzać właśnie DOM, ale może to za daleko posunięte.

Ta zmiana cieszy mnie z jeszcze innego powodu. Może bowiem wpłynąć na jakość badania i raportowania dostępności. Z raportów znikną tasiemcowe fragmenty kodu z błędami, nie mającymi nic wspólnego z dostępnością. Takie fragmenty łatwo jest wyprodukować, kopiując z walidatora kodu. Teraz audytor będzie się musiał wykazać większymi kompetencjami, bo musi wybrać te naprawdę problematyczne kawałki i do tego przypisać je do konkretnego kryterium sukcesu. No i czekamy na opublikowanie wersji ostatecznej WCAG 2.2.