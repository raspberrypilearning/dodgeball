\--- challenge \---

## Desafio: Gravidade melhorada

Há outro pequeno erro no seu jogo: a gravidade não puxa seu personagem para baixo se*alguma*parte dele estiver tocando uma plataforma azul - até mesmo a cabeça! Você pode testar isso subindo a maior parte do caminho até uma escada e, em seguida, movendo-se para a esquerda! Você pode testar subindo a maior parte do caminho até uma escada e, em seguida, movendo-se para a esquerda.

![captura de tela](images/dodge-gravity-bug.png)

Você pode corrigir esse erro? Para fazê-lo você precisa dar ao seu personagem diferentes calças. (em *todas*roupas)...

![captura de tela](images/dodge-trousers.png)

...Então mude o código:

```blocks
    < touching color [#0000FF]? >
```

with:

```blocks
    < color [#00FF00] is touching [#0000FF]? >
```

Lembre-se de testar as melhorias para ter certeza que você corrigir o erro!

\--- /challenge \---