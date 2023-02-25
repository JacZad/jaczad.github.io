---
title: 'Rozwijanie skrótów w tekstach'
date: '2013-01-04T09:10:00+01:00'
layout: post
categories:
    - artykuły
tags:
    - semantyka
    - skróty
    - tekst
    - 'prosty język'
---

Redagując tekst publikowany na stronie internetowej trzeba dbać, by był zrozumiały dla jak największego kręgu odbiorców. Jedną z podstawowych zasad jest rozwijanie stosowanych w tekście skrótów, które nie muszą być znane wszystkim.

### Kiedy rozwijać skróty

Skróty warto rozwijać zawsze, to znaczy wtedy gdy pojawiają się w tekście. Jest to jednak zajęcie pracochłonne, więc należy zrobić to przynajmniej raz, przy pierwszym wystąpieniu na stronie. Zdecydowanie nie wystarczy rozwinięcie skrótu raz w całym serwisie, bo użytkownik nie zawsze będzie zaczynał od strony głównej.

Rozwijanie skrótów może być realizowane wprost w tekście lub w sposób semantyczny, przewidziany w specyfikacji HTML. To drugie rozwiązanie jest korzystniejsze ze względu na różnego rodzaju automaty, które otrzymują jasną informację, że dany ciąg znaków jest skrótem.

### Rozwinięcie standardowe

Skrót można rozwinąć w tekście w sposób naturalny, na przykład tak:

> RPO (Rzecznik Praw Obywatelskich) stoi na straży praw obywatelskich Polaków.

> Dostęp do informacji można mieć poprzez kanały RSS (ang. Really Simple Syndication) lub Atom.

Zaletą takiego rozwijania skrótów jest to, że nigdy nie znikną podczas konwersji, na przykład drukowania strony lub zapisywania do zwykłego pliku tekstowego.

### Rozwinięcie semantyczne

W języku HTML zaproponowano dwa znaczniki służące oznaczaniu skrótów i dających możliwość ich rozwinięcia. Są to ABBR i ACRONYM. Różnica pomiędzy nimi jest na tyle mglista, że w HTML 5 zrezygnowano z tego drugiego i pozostawiono tylko pierwszy. Stosowanie znacznika jest banalnie proste i wygląda następująco:

```
<p><abbr title="Rzecznik Praw Obywatelskich">RPO</abbr> stoi na straży praw obywatelskich Polaków.</p>

<p>Dostęp do informacji można mieć poprzez kanały <abbr title="Really Simple Syndication">RSS</abbr> lub Atom.</p>
```

### Który sposób stosować?

Odpowiedź jest prosta – należy stosować oba sposoby, o ile tylko się da.

```
<p><abbr title="Rzecznik Praw Obywatelskich">RPO</abbr> (Rzecznik Praw Obywatelskich) stoi na straży praw obywatelskich Polaków.</p>
```

Jeżeli oznaczanie semantyczne nie jest możliwe, na przykład ze względu na ograniczenia edytora, to pozostaje rozwijanie w sposób naturalny. Ze względu na ograniczenia technologii asystujących nie należy stosować wyłącznie rozwijania semantycznego, gdyż taka informacja może pozostać nie zauważona.
