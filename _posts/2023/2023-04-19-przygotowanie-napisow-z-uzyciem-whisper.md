---
title: 'Jak przygotować napisy do filmu?'
subtitle: 'Sztuczna inteligencja może Ci pomóc przygotować napisy do filmu. Nie zrobi za Ciebie całej pracy, ale przeważającą większość.'
description: 'Wykorzystanie automatycznego rozpoznawania mowy do tworzenia napisów do filmów. Wersja na terminal MacOS i aplikację pod Windows'
categories: artykuły
tags: ['napisy', 'Whisper', 'sztuczna inteligencja', 'Subtitle edit']
---

Napisy do filmów są ważnym elementem dostępności cyfrowej. Dzięki nim można oglądać filmy i zapoznać się z ich treścią nie słysząc ścieżki dźwiękowej. Wbrew pozorom, służy to nie tylko osobom głuchym. Napisy przydadzą się każdemu, kto w konkretnym momencie nie może słuchać, bo dookoła jest bardzo głośno lub chce ukryć, że ogląda film.

Przygotowywanie napisów ręcznie jest pracą ogromnie żmudną, nudną i technicznie trudną. Rewolucja związana ze sztuczną inteligencją dostarcza nam jednak narzędzia, które tę pracę bardzo upraszczają, a przede wszystkim przyśpieszają. Naszym dzisiejszym bohaterem jest Whisper.

## Czym jest Whisper?

Whisper to model rozpoznawania mowy, który został niedawno opracowany przez OpenAI i jest systemem automatycznego rozpoznawania mowy wielojęzycznego i wielozadaniowego.  Whisper został wytrenowany na 680 000 godzin różnorodnych i wielojęzycznych danych mowy, z czego jedna trzecia danych była w językach innych niż angielski. Model może transkrybować mowę w różnych językach i przetłumaczyć je na angielski, a także jest odporny na akcenty, hałas tła i żargon techniczny. A do tego jest open-source na licencji MIT, czyli można go po prostu wziąć i używać.

## Jak używać Whisper?

Metod na używanie Whisper jest wiele, ale ja przedstawię tu tylko 2 z nich. Jeżeli ktoś znajdzie dla siebie wygodniejsze narzędzie, to super! Zatem dalej opis metody na terminal w MacOS i w edytorze Subtitle edit pod Windows.

## Praca w terminalu

Na moim Macbooku Air z 2017 roku zainstalowałem Whisper za pomocą systemu pakietów Homebrew. Instalacja polega na wpisaniu w terminalu brew install openai-whisper i odczekaniu, aż instalacja się zakończy. Potem można już przetwarzać mowę na tekst. Chociaż może nie tak od razu.

Możesz teraz w konsoli wpisać:

whisper nazwa-pliku.wav --model small --language pl

* nazwa pliku to oczywiście Twoje nagranie, które chcesz przetworzyć i wcale nie musi to być WAV, bo ja używam najczęściej MP3;
* --model to parametr określający, z jakiego modelu będziesz korzystać, ale o tym za chwilę;
* --language to określenie języka, w tym wypadku języka polskiego.

Parametrów jest o wiele więcej, ale te nam na razie wystarczą.

## Jakie modele oferuje Whisper?

Możesz wskazać jeden z kilku modeli rozpoznawania mowy, przy czym pamiętaj że od wybranego modelu zależy, jak dokładne będzie rozpoznanie mowy. Oto nazwy modeli od najmniejszego do największego:

* tiny
* base
* small
* medium
* large

Przy pierwszej próbie użycia modelu, Whisper musi go pobrać z internetu. Największy model ma prawie 3Gb wielkości, więc trochę trzeba poczekać.

Jeżeli teraz myślisz "biorę ten najlepszy", to może się okazać to błędem. Jeżeli nie masz dobrej karty graficznej, to rozpoznawanie godzinnego nagrania może trwać całą dobę lub więcej. Oczywiście zachęcam Cię do testowania, ale uprzedzam. Model tiny działa szybko, ale jakość rozpoznanego tekstu jest dość średnia. Large działa u mnie okropnie wolno, ale daje doskonały efekt.

Po przetworzeniu, Whisper zapisze tekst w kilku formatach. Ciebie prawdopodobnie najbardziej zainteresuje ten z rozszerzeniem SRT, bo to są właśnie napisy, których możesz użyć w Youtube lub na Facebooku. **Koniecznie je przejrzyj i popraw. Błędy będą na pewno.**

## Jak używać Whisper w Windows?

Dla okienkowców zaproponuję aplikację do przygotowywania napisów o nazwie [Subtitle Edit](https://www.nikse.dk/subtitleedit). Aplikacja jest bezpłatna i open-source, co jest dodatkową zaletą. [Pobierz pakiet instalacyjny](https://github.com/SubtitleEdit/subtitleedit/releases) ze strony programu i zainstaluj. Aplikacja ma polską wersję językową, więc poszukaj takiego ustawienia, o ile aplikacja sama nie przestawiła się na język polski.

A teraz po kolei:

1. Z menu *Plik* wybierz *Nowy* lub użyj skrótu ctrl + N.
2. Z menu *Wideo* wybierz *Otwórz plik wideo*. Wbrew nazwie - możesz wybrać także plik audio, na przykład MP3. Otwórz plik do przetworzenia.
3. Z tego samego menu *Wideo* wybierz opcję *Audio na tekst (Whisper)*.
4. W otwartym oknie dialogowym wybierz język, na przykład *polish*.
5. Teraz wybierz model z proponowanego zestawu. Jeżeli materiał nie jest po angielsku, pomiń te z dopiskiem *en*. Przy modelu od razu zobaczysz, jaki jest duży.
6. Naciśnij *Generuj* i spokojnie poczekaj.
7. Kiedy proces się zakończy, możesz poprawić napisy w aplikacji, a potem je wyeksportować. Oczywiście najlepiej do SRT.

To jest łatwe i za darmo. A skoro jesteś w tym miejscu artykułu, to już nie masz wymówki, że nie wiesz jak robić napisy. Dobrej zabawy.
