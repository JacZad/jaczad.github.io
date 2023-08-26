---
title: 'Krótka historia mojej porażki'
date: '2018-11-28T20:54:59+01:00'
layout: post
categories:
    - artykuły
tags:
    - EPUB
    - ETR
    - 'język migowy'
    - PDF
---

Amerykanie uważają, że porażki uczą więcej, niż sukcesy. Postanowiłem zatem opisać moją porażkę jako specjalisty od cyfrowej dostępności. Nauczyła mnie kilku rzeczy, a zatem się przydała. W opisie pominę szczegóły pozwalające na skojarzenie z konkretnymi osobami i produktem, chociaż świadomi czytelnicy i tak się domyślą.

### Początek historii

Pewien doktor napisał książkę naukową, żywiąc nadzieję że pozwoli mu ona na awans i dopisanie literek hab. przed nazwiskiem na wizytówkach. Książka dobra, bo ją czytałem już podczas tworzenia. Doktor wymyślił, że będzie to pierwsza w Polsce rozprawa habilitacyjna w pełni dostępna. Dodatkami do niej były zatem tłumaczenia na polski język migowy i tekst łatwy do czytania (ETRT). Książkę przygotowało poważne wydawnictwo uczelniane, w którym nie było miejsca na ekstrawagancje w rodzaju dostępnych plików PDF i EPUB. Jednak doktor się uparł i wydawnictwo uległo. I wtedy się zaczęło.

Doktor zadzwonił do mnie z żądaniem wskazania specjalisty od dostępnych ebooków. Ja wskazałem jednego, który obecnie mieszka w Szczecinie, ale ten się wypiął. Popytałem jeszcze kilku i ci też się wycofali rakiem. W końcu doktor się znudził i wskazał mnie palcem, że ja mam się tym zająć. Przez szacunek dla dostojnego akademika się zgodziłem i to był mój błąd.

To było gdzieś w grudniu 2017 roku, ale sprawa jeszcze chwilę potrwała. Wydawnictwo jeszcze dopieszczało wygląd książki, więc w tym samym czasie ja szukałem podwykonawcy, czyli kogoś, kto ogarnie narzędzia i zrobi dostosowanie. W styczniu trafił do mnie plik PDF z książką i wszystko zaczęło się sypać.

### PDF to największy wróg

Plik otrzymany z wydawnictwa był nawet czytelny, ale tak po łebkach. Semantyki nie było tam za grosz, a w publikacji to przecież bardzo ważne. W książce było trochę tabel, rozdziały, podrozdziały, przypisy, definicje, bibliografia i wreszcie tekst łatwy do czytania z obrazkami. Niby wszystko do ogarnięcia, a jakoś nie szło. Na początek zdecydowaliśmy, że trzeba zrobić reverse engineering i skonwertować plik do Worda, tam zrobić całą semantyką i z powrotem zapisać do PDF. Naiwność!

Na początek zawiodły narzędzia. Calibre konwertuje pliki PDF do Word w taki sposób, że zaciąga tylko tekst i tyle. Jeżeli to możliwe, to semantyki było tam jeszcze mniej, niż w pliku PDF. Potem sprawdziliśmy Google Docs, gdzie jest konwerter z PDF do EPUB i DOCX. Wyglądało to obiecująco, bo semantyka się pojawiła. Jednak po bliższym przyjrzeniu się okazała się wygenerowana sztucznie. Po jeszcze bliższych oględzinach okazało się, że to przetwarzanie oparte jest o optyczne rozpoznawanie tekstu (OCR). Oznaczało to zatem konieczność ręcznego sprawdzania niemalże znaku po znaku, bo przecież OCR się może mylić. Na tym etapie wycofał się podwykonawca, a ja musiałem znaleźć kolejnego.

Drugi zdecydował, że trzeba przekonwertować za pomocą narzędzi od Adobe. To było coś, bo przecież to oni powołali do życia ten szatański format. No i faktycznie – oprogramowanie przerobiło plik PDF na plik Word. Jednak radość była przedwczesna. Brak semantyki w materiale źródłowym oznaczał, że wszystko trzeba było oznaczać ręcznie. Największy problem był z przypisami i tabelami. Praca okazała się być tytaniczną i mało efektywną. Przypisy trzeba było ręcznie wstawiać w dokumencie, czyli kopiować z dołu strony i wstawiać po bożemu. Robota szła coraz wolniej, by w maju ustać całkowicie. Człowiek się poddał, a ja zostałem z rozgrzebanym plikiem Word.

Czytający do tego miejsca może już się puka w czoło i zastanawia, dlaczego nie wziąłem pliku źródłowego z wydawnictwa? Przecież tak byłoby najprościej. Sam też na to wpadłem i poprosiłem, ale wydawnictwo odmówiło. Po pierwsze – nie ma takiej praktyki, by wydawać materiały źródłowe. Po drugie – ich wersja różniła się od ostatecznej wersji. Uwierzyłem i odpuściłem jak jakiś głupi.

### Zrobimy to sami

W desperacji wpadłem na genialny w swej prostocie pomysł. Zrobimy to sami, to znaczy ja z Ewą. Narzędziem miał być Adobe Acrobat Pro, bo w nim daje się tagować dokumenty PDF. Sięgnąłem po wiedzę do Polskiej Akademii Dostępności, która okazała się nieco zdezaktualizowana i nie pasowała do najnowszej wersji Acrobata. Na szczęście znalazłem fajny poradnik po angielsku i wzięliśmy się do pracy. Zainstalowałem Acrobat Pro w wersji próbnej na komputerze Ewy i zaczęliśmy działać. Mieliśmy tydzień, bo potem trzeba było zapłacić subskrypcję. Miesięcznie nawet nie tak drogo, ale wykupić i tak trzeba było na rok. Dobrze, że tego nie zrobiliśmy…

Sprawdziliśmy plik w inspektorze dostępności i bez zdziwienia dowiedzieliśmy się, że jest kiszka. Nie ma żadnego tagowania i nawet język nie jest ustawiony. Chociaż poradnik to odradzał, uruchomiliśmy automatyczne tagowanie. Efekt wyglądał na niezły, więc się ucieszyliśmy. Na krótko.

Z nagłówkami, przypisami i bibliografią poszło dosyć zgrabnie. Jednak automatyczne tagowanie w wielu miejscach źle rozpoznało intencje projektantów i zrobiło tabele tam, gdzie ich nie powinno być, a część tabel beztrosko pominęło. Co gorsza – aplikacja działała coraz wolniej, z każdym dodanym tagiem. Komputer Ewy to nie demon szybkości, ale też i zadania nie były tej skali, by aż tak mulić. Od pewnego momentu każde przejście po drzewku DOM zamrażało komputer na kilkadziesiąt sekund. Praca ponownie stanęła, a był już czerwiec.

### Ostatnia deska ratunku

W takich sytuacjach pomóc może tylko telefon do przyjaciela. Zadzwoniłem i pomimo niechęci współpracowników, postanowił mi pomóc. Okazał się przy tym o wiele mniej naiwny ode mnie i przycisnął wydawnictwo, które z bólem wydało mu materiały źródłowe w formacie Indesign. To wcale jednak tak szybko nie poszło i wakacje spędziłem jeszcze w nerwach. Potem przyszedł październik i pierwsze wersje dostępnych plików PDF. Jako nasz wsad do produktu przesłałem teksty alternatywne do grafik. Na początku listopada pliki były gotowe. Jeszcze tylko sprawdzenie poprawności i poleciały do doktora. Kamień wreszcie spadł mi z serca. Nie zamierzam opisywać sposobu rozliczenia za tą usługę. W grę wchodziły praca, wzajemne przysługi, a chyba też jakieś owce i działki na Marsie. Ja się w tym absolutnie zgubiłem i wciąż czekam na koński łeb w łóżku. Grunt że po 10 miesiącach pliki w formacie PDF i EPUB trafiły do autora i to wciąż przed habilitacją.

Ktoś może spytać, dlaczego uważam całą historię za porażkę, skoro skończyła się dobrze? Po pierwsze – trwało to strasznie długo i najczęściej nie miałem kontroli nad całym procesem. Po drugie – stanąłem po drugiej stronie barierki i musiałem zrobić dostępne z niedostępnego. Okazało się to trudniejsze, niż oczekiwałem i teraz łagodniej patrzę na niedociągnięcia innych.

### Nauka z całej historii

Postanowiłem zebrać wnioski, jakie wyciągnąłem z tego wydarzenia.

1. Najważniejszym jest potwierdzenie, że dostępność najlepiej planować od początku. Poprawianie spapranego jest często bardzo trudne i pracochłonne. Pogrzebanie w pliku źródłowym też zajmuje czas, ale i tak jest drastycznie prostsze i szybsze, niż poprawianie gotowego pliku. Gdyby wydawnictwo zrobiło to wszystko od razu…
2. Format PDF nie przyjaźni się z dostępnością. Można tą świnię szminkować, ale to nadal będzie tylko świnia. PDF jest formatem do wydruku i można go tylko uzdatniać w ograniczonym zakresie. Do tego można to robić tylko narzędziami od Adobe, które są drogie i mało wydajne.
3. Nie powinienem się brać za rzeczy, których nie jestem w stanie zrobić sam lub z Ewą. Poznajemy kolejne narzędzia i być może kiedyś znowu podejmiemy podobne wyzwanie, ale na pewno nie będzie to prędko. Nauczyliśmy się czegoś nowego, zerknęliśmy głęboko w bebechy formatu PDF.i nie spodobało mi się to, co tam znalazłem.
4. Większość specjalistów od dostępności robi rzeczy łatwe i przyjemne, to znaczy krytykuje. Ja też to robię i taki kubeł zimnej wody dobrze mi zrobił na arogancję. Każdemu zatem życzę takiej porażki.