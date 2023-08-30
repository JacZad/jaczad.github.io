---
title: 'Testowanie dostępności strony internetowej'
date: '2012-07-23T10:30:40+02:00'
layout: post
categories:
    - artykuły
tags:
    - audyt
    - procedura
    - walidacja
---

W życiu każdego autora strony internetowej nadchodzi taki moment, że chciałby wiedzieć, czy jest ona dostępna (accessible). A jeżeli nie nadchodzi, to powinna nadejść. Testowanie jest zadaniem trudnym, jeżeli nie wie się, jak to robić. Po poznaniu technik robi się nieco łatwiej, ale nadal nie jest to proste. Poniżej opiszę etapy testowania, zaproponuję pewne rozwiązania i wskażę najczęściej popełniane błędy.

## Na początek – wzorzec

testując stronę internetową należy odnieść się do jakiegoś wzorca, z którym należy zachować zgodność. W różnych krajach [podejście do dostępności może być różne](https://zadzior.wordpress.com/2010/05/10/dostepnosc-stron-internetowych-w-systemach-prawnych-innych-krajw/), ale ogromna większość z nich korzysta wprost lub pośrednio z [Web Content Accessibility Guidelines](http://www.w3.org/TR/WCAG20/), którą to specyfikację [pokrótce opisałem](https://zadzior.wordpress.com/2009/12/12/wcag-2-0-ma-juz-rok/) przy okazji rocznicy jej powstania. A zatem – o ile nie napiszę inaczej – będę się odnosił właśnie do tego dokumentu.

## Trzy kroki do wiedzy

Pełne testowanie dostępności składa się z trzech etapów, z których każdy daje pewien efekt informacyjny, ale dopiero wykonanie wszystkich daje pełną wiedzę. Można jednak czasem zatrzymać się na pierwszym lub drugim i na nich poprzestać, chociażby dla obniżenia kosztów, ale wówczas należy mieć świadomość, że nie wolno popadać w błogostan, a już na pewno nie twierdzić, że strona jest dostępna. Te trzy kroki to:

1. Testowanie automatyczne z wykorzystaniem specjalnego oprogramowania.
2. Analiza ekspercka w oparciu o informacje pochodzące z automatów testujących.
3. Testy z użytkownikami.

## Etap pierwszy – automat

To jest najłatwiejszy do wykonania we własnym zakresie element testowania. Osoba testująca wykorzystuje narzędzia dostępne w sieci i za ich pomocą dokonuje walidacji strony.

Wypróbujmy zatem jedno z moich ulubionych, a mianowicie [Eval Access](http://sipt07.si.ehu.es/evalaccess2/). Na stronie dostępne są trzy narzędzia: (1) sprawdzanie pojedynczej strony; (2) sprawdzanie pojedynczej strony z pliku i (3) sprawdzanie serwisu, przy czym Dwie pierwsze różnią się tylko źródłem (adres url lub plik). Wpiszmy zatem jakiś przykładowy adres, zaznaczmy oba checkboxy i wybierzmy wszystkie trzy priorytety dostępności. Teraz przycisk "Evaluate" i po chwili otrzymujemy wynik.

Teraz kilka wyjaśnień dotyczących interpretacji wyników. Błędy to takie miejsca, gdzie automat z pewnością wykrył brak dostępności. Ostrzeżenia to z kolei miejsca, gdzie potencjalnie błąd może się pojawić, ale automat nie jest w stanie zdecydować, czy faktycznie wystąpił. Natomiast priorytety to tak naprawdę poziomy dostępności, których są trzy, przy czym spełnienie pierwszego dopiero daje prawo do stwierdzenia, że strona jest dostępna, drugiego – że jest użyteczna, a trzeciego, że jest wygodna. W raporcie pokazywane są informacje, czego dotyczy dany błąd lub ostrzeżenie, a opisy i numery odnoszą się do specyfikacji WCAG 1.0, która nie jest już aktualna. Zaraz… To po co testujemy tym narzędziem skoro nie jest aktualna? Ano dlatego, że narzędzi zgodnych z WCAG 2.0 jeszcze nie ma, a jeżeli są to po prostu wykorzystują te same algorytmy, więc nie ma tu wielkiej różnicy.

Kolej na drugi test dający lepszy obraz całego serwisu, a więc testowanie serwisu. W praktyce wpisujemy adres internetowy i wybieramy liczbę stron poddanych testom, przy czym proponuję dać maksymalną liczbę 15 podstron. Należy też zaznaczyć głębokość 2 lub 3, bo inaczej przetestujemy tylko stronę główną. Teraz przycisk "Evaluate" i mamy raport, ale troszkę inny. Otóż dostajemy kilkanaście tabelek poprzedzonych linkiem do strony, gdzie automat wypisuje nam liczbę błędów i ostrzeżeń. Tylko liczbę, bez rodzaju i objaśnień. To dlatego, że w pierwszej kolejności autor powinien usunąć błędy w skryptach generujących serwis, a dopiero potem wziąć się za wyszukiwanie pomniejszych uchybień.. A wówczas ten raport jest pomocny, bo adres wyśledzonej strony można wkleić do narzędzia testującego pojedynczą stronę i zobaczyć raport szczegółowy.

## Etap drugi – ekspert

Mamy zatem część pracy wykonanej, a teraz do pracy musi usiąść człowiek. Ten człowiek musi mieć wiedzę o dostępności, rozumieć ją, a przynajmniej musi przeczytać raz specyfikację WCAG. Bez tego ani rusz. Ten ekspert (tak go będę nazywał) bierze raporty i sprawdza ostrzeżenia, które wygenerował automat. Musi je sprawdzić uważnie, z wykorzystaniem technologii asystujących, w sposób nietypowy i na różnych urządzeniach.

Ekspert musi zatem punkt po punkcie przejrzeć ostrzeżenia zgłoszone przez automat testujący i podjąć decyzję, czy zakwalifikować dany element jako błędny, czy też prawidłowy. Musi się w tym posiłkować swoją wiedzą i kolejnymi aplikacjami wspomagającymi, a także – jak wspomniałem wcześniej – technologiami asystującymi.

W tym miejscu koniecznie trzeba nadmienić, że korzystanie z technologii asystujących (na przykład screen readera) może być mylące, jeżeli robi się to nieprawidłowo. Technologie asystujące używane są w pewien konkretny sposób, którego nie znają osoby nie używające go na codzień. Przykładem może być program do odczytu ekranu, który mówi mową syntetyczną. Wspomaga on osoby niewidome, które używają go niemal wyłącznie za pomocą klawiatury. Nieświadomy tego tester spróbuje użyć myszki i kliknąć wątpliwy element strony i oczywiście uzyska pożądaną reakcję. W ten sposób zakwalifikuje ten element jako prawidłowy. Tak naprawdę nadal nic nie wie o jego dostępności, bo niewidomi użytkownicy będą używać klawiatury, a wówczas efekt może być zupełnie inny. Jak zatem widać – testowanie eksperckie nie jest wcale takie proste.

## Etap trzeci – użytkownicy

Ostatnim etapem jest testowanie serwisów internetowych za pośrednictwem użytkowników. Grupę takich przeciętnych użytkowników sadza się przed komputerami, przekazuje zestaw zadań do wykonania i rejestruje ich działania. Jest to zatem proces podobny do testowania usability serwisu i to podobieństwo wcale nie jest przypadkowe. Różnice natomiast są dwie. Po pierwsze użytkownicy są specjalnie dobrani z powodu ich ograniczeń – wzrokowych, słuchowych, percepcyjnych, kognitywnych i innych. Przykładowa grupa może wyglądać następująco: osoba niewidoma, osoba słabowidząca, osoba głucha od urodzenia (ewentualnie druga z implantem lub aparatem słuchowym), osoba lekko niepełnosprawna intelektualnie, osoba chora na epilepsję, osoba z niedowładem rąk. Taką grupę należy dobierać z rozmysłem, aby możliwie szeroko reprezentowała ogół użytkowników z ograniczeniami. Muszą też korzystać ze swoich technologii asystujących. Podkreślam "swoich", bo tylko wówczas można w miarę obiektywnie oceniać ich działania.

Druga różnica polega na tym, że zwraca się uwagę na nieco inne elementy, niż w wypadku usability, a dokładniej – na nieco więcej rzeczy. Oprócz standardowej oceny użyteczności trzeba zwracać uwagę, czy pojawiają się jakieś problemy z dostępnością. To w zasadzie wszystko.

## Efekt testowania

Produktem końcowym testowania dostępności serwisu powinien być raport. Z jego treści autor serwisu powinien móc wywnioskować, jakie błędy dostępności znajdują się na stronach oraz jak je usunąć. Najlepiej, gdy całość przyjmie formę tutoriala, który przeprowadzi krok po kroku przez proces dostosowania serwisu aż do końcowego sukcesu. Czego wszystkim życzę.
