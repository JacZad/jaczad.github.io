---
title: 'Pani Wiesia robi tabelki w mBanku'
date: '2012-08-10T11:03:00+02:00'
layout: post
categories:
    - artykuły
tags:
    - dokumenty
    - prezentacja
    - semantyka
    - specyfikacja
    - tabele
---

Czy pamiętacie panią Wiesię, która na maszynie do pisania pracowicie robiła tabelki za pomocą spacji? Trafiła teraz do firm projektujących strony internetowe!

Kiedy pani Wiesia dostała – zamiast maszyny do pisania – komputer z edytorem tekstów, nadal robiła tabelki za pomocą spacji lub tabulatorów. Robiła też inne rzeczy – stawiała znak Enter na końcu każdej linii, a tytuły dokumentów "rozstrzeliwała" spacjami, żeby ładnie wyglądały. Potem zanosiła gotowy plik do informatyka i wydawała polecenie umieszczenia go na stronie internetowej. Pani Wiesia była osobą ważną (pracowała w tej instytucji od przedwojny) i informatyk nie mógł na nią nakrzyczeć, choć bardzo chciał, więc brał plik i – zgrzytając zębami – usuwał spacje i tabulatory. Potem się wycwanił i napisał specjalny skrypt "pani\_wiesia.php", który robił to za niego, ale sposobu na tabelki nie znalazł. Trzeba było robić je ręcznie.

Pani Wiesia nie wiedziała, że robi informatykowi krzywdę i skraca jego życie o miesiąc za każdym razem, gdy przynosi mu plik do umieszczenia na stronie. Pani Wiesia po prostu nie rozróżnia struktury logicznej dokumentu od jego wyglądu. Wygląda dobrze, więc jest dobrze. Pani Wiesi można wybaczyć, ale dlaczego tak samo robią młodzi, wyedukowani projektanci stron internetowych?

Języki HTML i XHTML, którymi najczęściej posługują się projektanci stron internetowych, są językami opisu dokumentu. W treści dokumentu umieszcza się specjalne znaczniki, które dzielą treść na mniejsze porcje i precyzyjnie definiują ich rolę w dokumencie. Dla przykładu pomiędzy znacznikami &lt;P&gt; i &lt;/P&gt; umieszcza się akapit tekstu, a pomiędzy &lt;H1&gt; i &lt;/H1&gt; – nagłówek stopnia pierwszego. W3C zaleca w specyfikacjach, by oddzielać strukturę i treść dokumentu od ich wyglądu, który definiuje się za pomocą kaskadowych arkuszy stylów (CSS). To są zasady napisane w każdym przyzwoitym podręczniku i z pewnością znane wszystkim zajmującym się profesjonalnie tworzeniem stron. Tymczasem praktyka jest inna i nagminnie spotykam się z sytuacją, gdy treść umieszczona jest w nieprawidłowych znacznikach, a formatowanie zastępuje strukturę logiczną.

Przyczepię się do mBanku, który najwidoczniej zatrudnił panią Wiesię właśnie do robienia tabelek w kontach klientów. Kto ma tam konto niechaj się zaloguje i obejrzy dane – dajmy na to – zdefiniowanych odbiorców. Tabela? Wcale nie! To coś tylko wygląda jak tabela, ale znaczników TABLE, TR i TD nie znajdziemy ani na lekarstwo. Wszystko jest pozycjonowane stylami, które są odpowiednikami spacji w tabelkach pani Wiesi. Takiej tabelki nie wczytamy do Excela, a poruszanie się po niej za pomocą oprogramowania do odczytu ekranu jest niemożliwe. Podglądając tą ciekawostkę za pomocą FireBuga odkryłem coś jeszcze ciekawszego: za elementy tabeli służą czasem elementy listy, a czasem akapity. Po prostu zgroza.

Na koniec jeszcze jeden przykład działalności pani Wiesi. Szukając prezentu imieninowego dla ojca trafiłem do sklepu internetowego [www.it-strefa.pl](http://www.it-strefa.pl) i tam chciałem zrobić zakupy. Poddałem się w którymś momencie i poprosiłem żonę o dokończenie transakcji. Znalazłem tam jednak – oprócz prezentu dla ojca – także ciekawostkę z obszaru dostępności: checkbox, który nie jest checkboxem. W specyfikacji HTMLa znajduje się odpowiedni znacznik realizujący funkcję kontrolki checkbox i robi to dobrze. Tymczasem w tym sklepie z niego zrezygnowano zastępując obrazkiem (plikiem graficznym) aktywnym po kliknięciu myszką. Podkreślam – tylko myszką, bo klawiaturą stanu tego przełącznika zmienić się nie da. Długo zastanawiałem się skąd ta działalność pani Wiesi bierze się na stronach internetowych.

Opowiedziałem o tym Henrykowi, który mnie objaśnił, że programiści robią takie rzeczy, ponieważ można takie rzeczy robić. Coś jak wdrapywanie się na Mount Everest, bo jest najwyższy. Ktoś siada i wkłada ogromną ilość czasu i wiedzy, stosuje tricki i sztuczki, ryzykuje brak dostępności i użyteczności serwisu po to, by zrobić checkboxa. To wszystko można zrobić jedną linią kodu HTML bez wysiłku i ryzyka. Dlaczego zatem tak robią?

I znowu Henryk mi przypomniał prezentację, którą robiliśmy w firmie Zentropy Partners i spór pomiędzy programistami a designerami. Designerzy projektują wygląd serwisu i żądają, by projekt strony był całkowicie zgodny z tym wymyślonym projektem. Programiści to robią, choć często wiedzą, że robią źle i niezgodnie z zasadami. A dla designera wygląd jest najważniejszy, podobnie jak dla pani Wiesi.