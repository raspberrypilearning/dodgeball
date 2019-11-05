## Wyzwanie: poprawiona grawitacja

Istnieje jeden mały błąd w Twojej grze: grawitacja nie ciągnie Twojego charakteru w dół jeżeli **jakakolwiek** część duszka dotyka niebieskiej platformy. Więc nawet jeśli głowa duszka dotknie platformy, duszek nie spada! Możesz to przetestować sama: spraw, by Twoja postać wspięła się po drabinie o znaczną odległość, a następnie przesuwaj ją na boki pod platformą:

![screenshot](images/dodge-gravity-bug.png)

Aby naprawić ten błąd, musisz najpierw dać duszkowi postaci nowe spodnie, które mają różny kolor (na **wszystkich** kostiumach).

![zrzut ekranu](images/dodge-trousers.png)

Następnie zamień ten blok kodu:

```blocks3
    < czy dotyka koloru [#00FF00]? >
```

z tym blokiem kodu:

```blocks3
    < czy kolor [#00FF00] dotyka [#0000FF]? >
```

Aby upewnić się, że naprawiłeś błąd, przetestuj grę po wprowadzeniu tych zmian!