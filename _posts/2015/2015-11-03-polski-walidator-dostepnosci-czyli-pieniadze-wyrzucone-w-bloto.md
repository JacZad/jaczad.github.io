---
title: 'Polski Walidator Dostępności, czyli pieniądze wyrzucone w błoto'
date: '2015-11-03T10:35:13+01:00'
layout: post
categories:
    - artykuły
tags:
    - audyt
    - błędy
    - MAiC
    - narzędzia
    - pieniądze
---

Coś takiego jak walidator dostępności stron internetowych nie istnieje i nieprędko powstanie. Większości z kryteriów sukcesu zawartych w WCAG 2.0 nie da się zbadać automatycznie, a pozostałe tylko w ograniczonym zakresie. Jednak wciąż ktoś próbuje zrobić coś niewykonalnego w tej dziedzinie, bo przecież wszystko należy zautomatyzować. Z tego samego powodu MAiC zapłacił za zrobienie Polskiego Walidatora Dostępności, który jest wyjątkowo ograniczonym narzędziem. Nawet nie czytajcie tabeli z rankingiem, bo nie ma ona żadnego sensu. Na podstawie informacji zawartych na stronie jestem to w stanie wykazać, chociaż uprzedzam, że tekst będzie długi.

## Co jest w środku

Autorzy PWD udostępnili tabelę zawierającą 29 metryk, czyli swego rodzaju walidatorów sprawdzających poszczególne elementy dostępności. Pokazali też krótki opis i odniesienie do WCAG 2.0. Na pierwszy rzut oka wygląda to obficie, ale wystarczy rzucić drugi raz i tabelka skraca się o połowę. Z tej połowy tylko kilka elementów ma sens.

### 1.1.1 – tekst alternatywny

> Metryka weryfikuje czy grafiki osadzone na stronie (tagi img) mają ustawiony atrybut alt. Atrybut ten powinien zawierać treść alternatywną, która jest pokazywana jeśli przeglądarka użytkownika ma wyłączoną obsługę grafiki, przykładowo: ![Smiley face](smiley.gif)

ALT nie jest jedynym sposobem opisywania grafik, chociaż jest atrybutem obowiązkowym. Jednak większy problem jest w tym, że grafiki nie są jedynymi nietekstowymi elementami na stronach internetowych. Badanie robione jest zatem po łebkach.

### 1.3.1 – Gęstość tagów formatujących

> Metryka weryfikuje gęstość tagów formatujących.

Co też ma pokazywać takie podejście do semantyki dokumentu? Brak bliższych wyjaśnień, choćby czy lepiej mieć dużo tych tagów, czy może mało. Moim zdaniem najlepiej mieć ich odpowiednio. Długi tekst, na przykład artykuł, będzie miał ich mało i nie wiem, czy to dobrze, czy źle. A może algorytm promuje dużo tagów, więc lepiej wypadną poszatkowane sztucznie serwisy polujące na wyszukiwarki…

### 1.4.2 – Dźwięk na przy wyświetlaniu strony

> Metryka weryfikuje czy zaraz po wczytaniu strony nie jest odtwarzany dźwięk. Sprawdza czy zostały użyte mechanizmy wywołujące taki efekt …

To może nawet działać, ale nie bierze pod uwagę faktu, że dźwięk może być emitowany z filmów, w tym osadzonych reklam we Flashu.

### 1.4.3 – Kontrast

Zamiast opisu – niekompletny cytat z WCAG. Jeżeli działa, to nawet cenne narzędzie. Jednak podobne już istnieją.

### 1.4.4 – Zmiana rozmiaru tekstu

> Metryka weryfikuje czy na stronie są mechanizmy polegające na stopniowym powiększaniu czcionki.

Nie wiem, co metryka weryfikuje, bo kluczowe jest powiększanie za pomocą narzędzi wbudowanych w system operacyjny i przeglądarkę. Sprawdzenie występowania paska dostępności nie wystarcza, bo może działać wadliwie lub wcale.

### 2.4.2 – Tytuł strony

> Metryka weryfikuje czy strona posiada znacznik określający tytuł strony …

Nie chodzi o to, czy tytuł występuje, tylko czy zmienia się na różnych stronach i jest deskryptywny wobec treści. Z opisu sądząc – to narzędzie działa nieprawidłowo.

### 2.4.10 – Nagłówki sekcji

> Metryka weryfikuje, każda z sekcji z treścią jest opisana za pomocą nagłówków (tytułów), tam gdzie będzie to konieczne.

Trochę brakuje szczegółów, ale gdyby działało, to byłoby epokowe osiągnięcie. Znowu – nie chodzi o wstawienie nagłówków dowolnego poziomu gdziekolwiek, tylko logiczny podział strony i opatrzenie tych części deskryptywnymi nagłówkami.

### 3.1.1 – Język strony

> Metryka weryfikuje czy strona ma określony domyślny język strony internetowej, może zostać odczytany przez program komputerowy.

I ponownie jak przy tytułach stron – nie chodzi o występowanie w ogóle, ale prawidłowe określenie języka. Z praktycznego punktu widzenia często lepiej, gdy strona nie ma określonego języka w ogóle, niż gdy jest on zadeklarowany nieprawidłowo. WCAG wymaga zgodności deklaracji ze stanem faktycznym, a nie deklaracji. To narzędzie na pewno działa źle.

### 3.3.2 – Etykiety lub instrukcje

> Metryka weryfikuje, czy wszystkie elementy do wprowadzania danych na stronie mają etykiety.

To użyteczna część, która jednak występuje w absolutnie każdym walidatorze. Postępem byłoby sprawdzenie, czy etykiety są widoczne i logiczne. Uzupełnia ją dodatkowo poniższa metryka:

### Etykietowanie elementów

> Metryka weryfikuje, czy wszystkie poetykietowane elementy nie mają elementów podrzędnych poza etykietą.

### Unikalność identyfikatorów elementów

> Metryka weryfikuje, czy nie ma zduplikowanych identyfikatorów elementów.

Wartościowa funkcja, której autorzy nie przypisali do żadnego z kryteriów sukcesu. Podpowiadam: SC 4.1.2.

### Kontakt

> Metryka weryfikuje czy na stronie głównej znajduje się odnośnik do informacji kontaktowych.

Konia z rzędem temu, kto wskaże stosowne zapisy w WCAG. A przypisana waga to aż 3 punkty… Co ze stronami, które kontaktu nie przewidują? Albo dane kontaktowe są od razu na stronie głównej?

## Do czego służy ARIA

ARIA to technologia służąca łataniu niedostatków HTML i kiepskiej pracy programistów. Tutaj służy maskowaniu słabości narzędzia i metryki związane z tą technologią to aż 12 pozycji:

- Elementy ARIA z rolami muszą być poprawne
- Atrybut ARIA powiązany
- Wymagane atrybuty dla elementów z rolami ARIA
- Stan i poprawność właściwości elementów ARIA
- Atrybut role=main tylko na kluczowych elementach
- Zbędny atrybut aria-owns
- Wielokrotne używanie atrybutu aria-owns
- Właściwe role elementów podrzędnych
- Właściwy zakres elementów ARIA
- Obsługiwane atrybuty ARIA
- Prawidłowe atrybuty ARIA
- Wsparcie dla ról, stanów i właściwości ARIA

Można byłoby to zwinąć do jednej metryki "poprawność ARIA" i dałoby to jakąś informację. Miałoby też związek z dostępnością, chociaż sami autorzy nie potrafili wskazać, z którym kryterium sukcesu. Podpowiem, że z SC 4.1.1. Chociaż oczywiście bardzo brakuje tutaj zwykłej walidacji kodu HTML.

## Ciekawe i wątpliwe eksperymenty

Jest jeszcze kilka metryk o charakterze eksperymentalnym, a zatem wątpliwej pewności. Jeżeli działają, to godne podziwu. Jednak nie bardzo wierzę, co zaraz wykażę.

### Elementy audio posiadają kontrolki

> Metryka weryfikuje, czy elementy związane z audio posiadają kontrolki do sterowania.

No dobrze, ale co to ma wspólnego z dostępnością? Czy te kontrolki są dostępne z poziomu klawiatury? Co właściwie robią i jak są wykrywane? Mają moje zaciekawienie, chociaż bardzo ostrożne.

### Cel odnośnika czytelny na bazie opisu

> Metryka weryfikuje, czy cel wszystkich odnośników wynika z ich treści .

Na jakiej podstawie można dokonać takiej weryfikacji? Tu trzeba zaprząc zaawansowane algorytmy analizujące treści dostępne po kliknięciu i porównywać z treścią linku. Jakoś nie wydaje mi się, by tak to działało. Niektóre walidatory ostrożnie zagłębiają się w ten temat, ale wątpliwości zgłaszają jako ostrzeżenia. Tutaj waga wynosi 2 punkty, a zatem autorzy są pewni swojego narzędzia.

### Znaczące obrazy nie są tłem

> Metryka weryfikuje, czy obrazki, które mają znaczenie dla strony, nie są używane jako tło.

I ponownie – skąd algorytm wie, że obraz jest znaczący? Czy dokonuje analizy informacji w obrazie? Moja ciekawość wzrasta, chociaż odpowiedzi nie znalazłem.

### Niewidoczne elementy z focusem

> Metryka weryfikuje, czy elementy, które mogą uzyskać fokus nie są niewidoczne lub zasłonięte przez inne elementy strony.

Bardzo ciekawa funkcja i jeżeli działa, to jest przydatna. Co prawda widoczność fokusa to jeszcze kilka innych elementów, to jednak automatyzacja tutaj jest możliwa. Znowu podpowiem autorom, że jest to SC 2.4.7.

## Podsumowanie

PWD to kiepskie narzędzie przygotowane przez osoby, które o dostępności wiedzą niewiele lub zgoła nic. Może też być niebezpieczne dla dostępności, ponieważ bardzo silnie zakłamuje rzeczywistość. WCAG 2.0 poziom AA to 38 kryteriów sukcesu, z czego 36 znajduje się w załączniku nr 4 do rozporządzenia w sprawie Krajowych Ram Interoperacyjności. Z tych 38 lub 36 kryteriów PWD sprawdza prawdopodobnie dobrze 4, na pewno źle sprawdza 3, a są i takie, które z dostępnością mają związek luźny. Jest też kilka eksperymentalnych metryk o wątpliwej jakości. Na tak słabych podstawach tworzony jest syntetyczny wskaźnik dostępności, który nie znaczy zupełnie nic. Za to może zbudować we właścicielu strony, na przykład burmistrzu Myszyńca, poczucie że strona jest w porządku. Nie jest w porządku, co zauważy nie tylko specjalista od dostępności, ale choćby niewidomy użytkownik internetu.

Od początku byłem sceptyczny wobec tego projektu, o czym pisałem w notatce na temat wyników konkursu. Aby rozwiać lub potwierdzić wątpliwości skontaktowałem się z przedstawicielem Stowarzyszenia Na Rzecz Rozwoju Regionu "Dolina Gubra”, aby mi coś o sobie i narzędziu opowiedział. Ponieważ od razu zorientowałem się, że na temat dostępności nie wiedzą nic, więc podrzuciłem kilka linków i zniechęciłem do robienia projektu. Jak widać – nieskutecznie. Nie wiem, jakie będą dalsze losy PWD, ale zapewne zostanie porzucony przez autorów. Pieniądze z MAiC nie posłużyły nawet edukacji wnioskodawców, bo strona PWD ma tak krytyczne błędy dostępności, że źle świadczą o kompetencjach twórców. Jest to tym dziwniejsze, że główna strona stowarzyszenia jest pod tym kątem całkiem niezła. Szkoda tych pieniędzy, chociaż wiem, że jest to nagminne. Jeszcze raz przestrzegam – nie bierzcie na poważnie rankingu zrobionego przez PWD. Nie ma to żadnego sensu.