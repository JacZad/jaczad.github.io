---
title: 'Zrozumieć WCAG 2.0'
date: '2012-07-20T11:31:28+02:00'
layout: post
categories:
    - artykuły
tags:
    - dokumenty
    - specyfikacja
    - W3C
    - WAI
    - WCAG
---

Spełnienie wymagań zawartych w [Web Content Accessibility Guidelines (WCAG) 2.0](http://www.w3.org/tr/wcag20) wymaga zrozumienia tego dokumentu. Na pierwszy rzut oka może się wydawać zawiły, ale jest logiczny i konsekwentny. Aby jakoś przybliżyć moment zaprzyjaźnienia się z nim prezentuję poniżej kilka informacji na temat jego konstrukcji.

Zarówno w tym artykule, jak i we wszystkich innych, stosowane będą pewne skróty, na przykład G x.x oznacza wytyczną (guideline) o numerze składającym się z dwóch cyfr rozdzielonych kropką. Analogicznie SC x.x.x oznaczać będzie kryterium sukcesu (success criterium) o numerze składającym się z trzech cyfr rozdzielonych dwoma kropkami.

## Cztery główne zasady

Wszystkie wskazówki – dla porządku – zgrupowano w czterech grupach tematycznych nazwanych zasadami (principle). W strukturze WCAG 2.0 są one na samej górze i obejmują:

1. Postrzegalność (Perceivable), co oznacza że każda informacja powinna dać się dostrzec.
2. Funkcjonalność (operable), co oznacza możliwość korzystania ze wszystkich funkcji.
3. Zrozumiałość (understandable), oznacza że każda informacja powinna być zrozumiała.
4. Rzetelność (robust), oznacza że każda informacja powinna być przygotowana zgodnie z obowiązującymi standardami.

Zasady mają charakter porządkujący, a jednocześnie pozwalają na sensowne grupowanie wskazówek, które stanowią esencję całego dokumentu. Od nich także zaczynają się numery początkowe wytycznych, na przykład wskazówka 1.1 jest częścią zasady pierwszej, a 4.1 – czwartej.

## Wytyczne

WCAG 2.0 zawiera 12 wytycznych, które określają sposób osiągania celów zawartych w czterech zasadach. Poniżej ich lista w wersji bardzo skróconej.

- G 1.1 – alternatywa tekstowa dla każdej treści nie tekstowej.
- G 1.2 – dostarczenie alternatywy dla mediów dynamicznych.
- G 1.3 – możliwość adaptacji (zmiany) treści.
- G 1.4 – oddzielenie informacji od tła.
- G 2.1 – wszystkie funkcje muszą być dostępne z klawiatury.
- G 2.2 – wystarczający czas dla użytkownika.
- G 2.3 – brak treści mogącej wywoływać ataki padaczki.
- G 2.4 – możliwość łatwej nawigacji w serwisie.
- G 3.1 – treść powinna być czytelna i zrozumiała.
- G 3.2 – serwisy internetowe powinny działać w przewidywalny sposób.
- G 3.3 – wspomaganie użytkownika przy wprowadzaniu informacji i zapobieganie popełnianiu błędów.
- G 4.1 – kompatybilność z obecnymi i przyszłymi technologiami.

## Poziomy dostępności

Na potrzeby WCAG przyjęto trzy poziomy dostępności:

- Poziom A (podstawowy) – musi być spełniony, aby większość użytkowników mogła korzystać z serwisu internetowego.
- Poziom AA (rozszerzony) – powinien być spełniony, aby większość użytkowników mogła swobodnie korzystać z serwisu internetowego.
- Poziom AAA (pełny) – może być spełniony, jeżeli chcemy, by wszyscy użytkownicy mogli z serwisu korzystać w sposób komfortowy.

W praktyce w każdej wytycznej można spełnić jeden z trzech poziomów dostępności, jeżeli zapewni się spełnienie kryteriów sukcesu (success criteria). Czasem jest wręcz tak, że kryterium na dwóch poziomach dostępności różni się nieznacznie. Dla przykładu spełnienie kryterium sukcesu SC 1.4.2 oznacza, że kontrast pomiędzy czcionkami i tłem wynosi 4,5:1. Jeżeli jednak chcemy spełnić analogiczny warunek na poziomie AAA, to należy spełnić SC 1.4.6, który określa ten kontrast na 7:1. Jak z tego wynika – oczekiwania na poziomie AAA są wyższe, niż na poziomie AA, które są z kolei wyższe od tych na poziomie A.

Można zatem powiedzieć, że WCAG jest swego rodzaju matrycą, w której na jednej osi umieszczono wytyczne, a na drugiej poziomy dostępności. Zapewnienie zgodności z WCAG 2.0 (dostępności) na najniższym poziomie A oznacza spełnienie **wszystkich** kryteriów sukcesu dla tego poziomu. Dopiero potem można badać zgodność na poziomie rozszerzonym (AA), a po spełnieniu w nim wszystkich oczekiwań – poziomu ajwyższego. Dla ułatwienia pracy przygotowano różnego rodzaju narzędzia automatyczne i dokumenty wspomagające (listy sprawdzające).
