---
title: 'Semantyka informacji i zależności (WCAG 2.0 SC 1.3.1, poziom A)'
date: '2012-08-09T10:42:00+02:00'
layout: post
categories:
    - artykuły
tags:
    - dokumenty
    - nagłówki
    - prezentacja
    - specyfikacja
    - tabele
---

Czy sprawdzaliście kiedyś, jak wygląda serwis internetowy w którym wyłączono style? Na pewno wygląda inaczej, ale czasem pozostaje użyteczny, a czasem staje się całkowicie bezużyteczny. A wszystko zależy od semantyki, czyli prawidłowego zdefiniowania rodzaju informacji i struktury dokumentu.

Kryterium sukcesu 1.3.1 nakazuje, by informacja w treści internetowej miała programowo określoną strukturę. Jeżeli dana technologia tego nie przewiduje, to można – w drodze wyjątku – opisać tą strukturę w oddzielnym dokumencie tekstowym. Chodzi zaś przede wszystkim o to, by konkretny rodzaj informacji, na przykład tabela, był faktycznie tabelą w sensie semantycznym, a nie ciągiem znaków rozdzielanych spacjami i tabulatorami. Skorzystają z tego:

 użytkownicy niewidomi, - użytkownicy starych przeglądarek internetowych,
- użytkownicy i programy przetwarzające informacje do innych form.

Specyfikacja HTML jest od początku językiem opisu dokumentów, czy ściślej – informacji zawartej w dokumencie. Wywodzi się z SGML, którego jedyną prawdziwą funkcją było semantyczne opisywanie informacji. Dlatego w HTML są znaczniki pozwalające na określenie, które fragmenty dokumentu są definicjami, nagłówkami, akronimami, adresami, tabelami itd. Niestety – webmasterzy bardzo często zapominają o tej cesze HTMLa i stosują jedynie wizualne formatowanie, a w tym wypadku zarówno rodzaj informacji, jak i zależności z innymi informacjami mogą się łatwo zagubić. Czasem wystarczy wyłączyć obsługę stylów.

Za przykład niech posłużą nam nagłówki, których zadaniem jest strukturalizowanie dokumentu – dzielenie go na części i określanie ich wagi. Doświadczenie życiowe uczy nas, że najważniejsze tytuły (na przykład rozdziałów) powinny być pisane największą czcionką. Mniej ważne (na przykład podrozdziały) czcionką nieco mniejszą i td. Tak zatem są one wyróżniane na stronach internetowych, ale to jest wyróżnienie tylko wizualne, za którym powinno pójść określenie semantyczne w kodzie. Dlatego tytuły rozdziałów powinny znajdować się w znacznikach wyższego poziomu, niż tytuły podrozdziałów. Powinna być przy tym zachowana odpowiednia kolejność zagnieżdżania. W takiej sytuacji nawet wyłączenie stylów nie pozbawi dokumentu sensu, a informacja będzie łatwa do przetworzenia.

Analogicznie należy rozpatrywać sposób tworzenia tabeli, które są szczególnie wrażliwe na przetwarzanie, a zachowanie zależności (układu kolumn i wierszy) jest już zupełnie kluczowe. Kto próbował przenosić tabele utworzone za pomocą spacji i tabulatorów do arkusza kalkulacyjnego na pewno zrozumie, o co w tym chodzi.