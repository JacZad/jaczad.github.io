---
title: 'Poradnik do Mastodona dla osób niewidomych'
date: '2021-10-17T11:11:03+02:00'
author: 'Jacek Zadrożny'
excerpt: 'Krótki poradnik dla osób niewidomych, jak używać Mastodona. Mam nadzieję, że spotkamy się w fediversum'
layout: post
categories:
    - tutoriale
tags:
    - Mastodon
    - niewidomi
    - NVDA
    - poradnik
---

Wczoraj usunąłem konto na Facebooku. Nosiłem się z tym od dawna, tylko nie mogłem się zdecydować. Odczułem ulgę. Teraz moim głównym medium społecznościowym jest Mastodon. Korzystam z niego od 10 miesięcy i uważam go za najbardziej dostępną społecznościówkę dla osób niewidomych. Najlepiej działa pod Windows, a używać go można z każdym czytnikiem ekranu, w tym przede wszystkim NVDA.

## Czym jest Mastodon?

Mastodon to serwis społecznościowy, nieco podobny do Twittera. Są jednak też pewne różnice. Jest zdecentralizowany i każdy może stać się właścicielem swojego Mastodona, czyli instancji. Na samym końcu znajdziesz informacjebardziej szczegółowe na temat komunikowania się między instancjami.

## Pierwsze oględziny

Zarejestruj się na dowolnej instancji Mastodona. Procedura jest tak prosta, że nie będę jej opisywał. Zaloguj się i zacznij oględziny.

Na początek znajdź przycisk menu i przejrzyj, co tam jest. W profilu możesz wpisać dowolne informacje. Tylko adres email musi być poprawny. W preferencjach wyglądu zaznacz interfejs zaawansowany. Teraz znajdź link powrotu do Mastodona, żeby wrócić do głównej części. Porozglądaj się po ustawieniach, stronie. Po włączeniu interfejsu zaawansowanego wyświetlone będą równocześnie różne kolumny. Mogą to być:

- Główna, czyli Twoje tooty oraz osób, które śledzisz. Ta oś jest niemalże kopią Twittera, tylko takiego chronologicznego i bez reklam.
- Powiadomienia, czyli zgodnie z nazwą – oś na której będą się wyświetlać informacje, że ktoś polubił Twój post, skomentował go, podbił, zaczął Cię śledzić.
- Lokalna to z kolei wiadomości z całej instancji, czyli od wszystkich użytkowników. Można ją – z zachowaniem ostrożności – porównać do grup na Facebooku. Przy czym jest to jedna grupa na całą instancję.
- Wiadomości bezpośrednie, czyli skierowane do Ciebie i ewentualnie innych użytkowników. Nie trafiają na publiczne osie.
- Globalna to z kolei oś zawierająca posty z federacji, czyli nie tylko z Twojej instancji, ale także z wielu innych. Moim zdaniem jest mało przydatna, bo jest tam za dużo, często chaotycznych informacji.
- Własne, na przykład zawierające posty oparte o hashtagi lub wątki.

## Podstawowa obsługa klawiaturą

Jeżeli masz włączony zaawansowany interfejs, to na ekranie są przynajmniej 2 kolumny (strumienie). Domyślnie jest to kolumna domowa i powiadomienia. Ich nazwy osadzone są w nagłówkach poziomu 1. Jednak wygodniej będzie korzystać przy włączonym trybie formularzy (NVDA spacja). Zazwyczaj fokus klawiatury ląduje w polu edycji wpisu i trzeba nacisnąć Esc, a potem 1 aby przejść do pierwszej kolumny lub 2 do drugiej. Strzałkami w górę i w dół możesz się przemieszczać między tootami.

Jak już sobie chodzisz po wpisach, to warto poznać kilka poręcznych skrótów. Wystarczy nacisnąć odpowiedni klawisz, żeby wywołać akcję.

- r: otwarcie okna komentarza. 
- f: polubienie
- b: podbicie, czyli coś w rodzaju udostępnienia
- p: otwarcie profilu autora posta
- ? (pytajnik) wyświetla skróty klawiszowe dostępne w Mastodonie

funkcje dotyczące konkretnego toota możesz również znaleźć naciskając klawisz Tab. Jest tam także przycisk z dodatkowymi funkcjami, np. dodanie do zakładek, wyciszenie lub zablokowanie autora, zgłoszenie do moderacji.

## Pierwszy post

Teraz napisz pierwszy post, czyli „toot”, bo przecież słoń trąbi. Kursor najczęściej ląduje od razu w polu tekstowym toota i pyta, co Ci chodzi po głowie. Możesz pisać, wklejać linki, hashtagi, na przykład#Mastodon zmieni się w link, który pozwoli Ci znaleźć inne wpisy zawierające taki hashtag. Można też wymienić kogoś w treści, na przykład @jaczad to mój nick. Dostanę wtedy powiadomienie, że ktoś o mnie wspomniał. Gdy przygotujesz wpis, klawiszem Tab przemieszczaj się, , aż trafisz na przycisk Wyślij. Klik i już! A można jeszcze prościej – skrót to Ctrl+Enter.

Na chwilę wróćmy do przygotowania toota. Jego długość jest domyślnie ograniczona do 500 znaków. Możesz dodać do niego grafiki i nagrania wideo, a do każdego takiego pliku możesz dodawać tekst alternatywny. Nawiasem mówiąc – w żadnym innym medium nie spotkałem tylu grafik z tekstem alternatywnym. Możesz dodać także emoji i ankietę, czyli prosty formularz do głosowania lub wyrażania opinii.

Każdy toot możesz opublikować z określonym zasięgiem. Domyślnie z publicznym, a w przypadku wiadomości prywatnych – bezpośredni. W Mastodonie są 4 takie parametry:

- Publiczny – dociera wszędzie, bez żadnych ograniczeń
- Niewidoczny – niewidoczny poza instancją, gdzie został opublikowany
- Tylko dla śledzących – widoczny tylko dla użytkowników śledzących dany profil
- Bezpośredni – widoczny tylko dla użytkowników wymienionych w treści toota

## Organizacja interfejsu

Mastodon ma nieco odmienną naturę od Twittera lub Facebooka. Jest instancją lokalną, a jednocześnie potrafi komunikować się z innymi instancjami tworząc tzw. fediversum. Trzeba to zrozumieć, żeby się nie pogubić. Dlatego jest w nim oś lokalna z wpisami użytkowników danej instancji oraz globalna z wpisami z serwerów podłączonych. Można śledzić użytkowników z innych instancji, ale nie pojawią się automatycznie na osi globalnej.

Wróćmy na chwilę do kolumn. Możesz dodawać kolejne, na przykład globalną lub z konkretnym hashtagiem. Kolejne kolumny są dokładane na końcu i można do nich przechodzić klawiszami cyfr. Kolumnę można przypiąć i wtedy zostaje na stałe. Można to zrobić po otwarciu ustawień przy nazwie danej kolumny. W tym samym miejscu można sobie przesuwać kolumny i zmieniać ich kolejność. Kolejna kolumna jest dodawana także wtedy, gdy klawiszem Enter otworzysz wątek i wtedy zawiera wpisy z danego wątku.

## Otwarte instancje Mastodona

W Internecie możecie znaleźć wiele instancji Mastodona. Tutaj wskazuję zaledwie 2 z nich. Jednak korzystać możesz z dowolnej. Na oficjalnej stronie Mastodona możesz znaleźć rozbudowaną listę z dodatkowymi informacjami, na przykład o tym, czy jest otwarta na rejestrację, ilu ma użytkowników i z jakiego kraju jest.

- <https://101010.pl> – jedna z największych polskich instancji. Zaletą są wydłużone wpisy do 2048 znaków.
- <https://dragonscave.space/about> – instancja zasiedlona głównie przez osoby z niepełnosprawnością wzroku. Język angielski.

A teraz to, co najlepsze. Z poziomu takiej instancji możesz obserwować i wchodzić w interakcję z użytkownikami każdej innej instancji. A żeby było jeszcze lepiej – nie tylko z instancjami Mastodona. Otwarte są też przed Tobą Pleroma, Friendica, FunkWhale, PeerTube, BookWyrm i wiele innych wyspecjalizowanych usług. Są nawet usługi do blogowania, na przykład WriteFreely. Jeżeli jednak masz już blog oparty o WordPress, to możesz doinstalować wtyczkę Activitypub i w ten sposób dołączyć do federacji. 

## Aplikacje mobilne

A jeżeli chcesz korzystać z Mastodona na smartfonie, to są do tego różne aplikacje. Ja przetestowałem tylko te na iOS, więc jeżeli ktoś zna dostępne aplikacje na Android, to poproszę o informacje. Na iOS polecam:

- [Metatext](https://apps.apple.com/pl/app/metatext/id1523996615?l=pl) – bezpłatna, w pełni dostępna i po polsku. Sam przetłumaczyłem interfejs, więc pochwały i krytykę proszę kierować do mnie.
- [Toot!](https://apps.apple.com/pl/app/toot/id1229021451?l=pl) – aplikacja po angielsku, a za to z wieloma dodatkowymi funkcjami.Bardzo stabilna i niezawodna.

W razie pytań – piszcie do mnie na [Mastodonie](https://101010.pl/@jaczad).