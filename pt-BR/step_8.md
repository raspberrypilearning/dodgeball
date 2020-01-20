## Lasers!

Para seu jogo ficar um pouco mais difícil de completar, você vai adicionar lasers!

\--- task \---

Adicione um novo sprite ao seu jogo e chame-o `laser`. Deve ter dois trajes: um chamado "on" e outro denominado "off".

![screenshot](images/dodge-lasers-costume1.png)

![screenshot](images/dodge-lasers-costume2.png)

\--- /task \---

\--- task \---

Coloque seu novo sprite laser entre duas plataformas.

![screenshot](images/dodge-lasers-position.png)

\--- /task \---

\--- task \---

Adicione código ao seu sprite laser para alternar entre seus dois trajes.

![laser sprite](images/laser_sprite.png)

```blocks3
    when flag clicked
    forever
        switch costume to (on v)
        wait (2) seconds
        switch costume to (off v)
        wait (2) seconds
    end
```

Se você preferir, você pode alterar o código mostrado acima para que o sprite `Esperar`{:class="block3control"} a `aleatório`{:class="block3operators"} quantidade de tempo entre as mudanças de traço.

\--- /task \---

\--- task \---

Finalmente, adicione código ao seu sprite laser para que o sprite laser transmita uma mensagem 'hit' quando toca o sprite.

\--- hints \---

\--- hint \---

Este código deve ser muito parecido com o código que você adicionou ao seu sprite.

\--- /hint \---

\--- hint \---

Copie o código que você adicionar ao sprite para fazer este sprite `broadcast 'hit'`{:class="block3control"} quando ele estiver `tocando seu personagem`{:class="block3sensing"}.

\--- /hint \---

\--- hint \---

Este é o código que você deve adicionar:

![laser sprite](images/laser_sprite.png)

```blocks3
when green flag clicked
forever 
  if <touching (Pico walking v) ?> then 
    broadcast (hit v)
  end
end
```

\--- /hint \---

\--- /hints \---

Você não precisa adicionar nenhum código extra aos seus caracteres sprite, porque o personagem sprite já sabe o que fazer quando recebe o `transmitir 'hit'`{:class="block3control"}!

\--- /task \---

\--- task \---

Teste seu jogo para ver se você consegue mover o personagem para além do laser. Se o laser for muito fácil ou muito difícil de evitar, altere o `Espera`{:class="block3control"} vezes no código para o sprite.

\--- /task \---