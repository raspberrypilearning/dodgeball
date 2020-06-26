## Gravidade e salto

Agora você fará seu personagem se mover de maneira mais realista: você adicionará gravidade ao seu jogo e dará ao personagem a capacidade de pular.

\--- task \---

No jogo, mova seu personagem para que ele saia de uma plataforma. Você vê que ele pode caminhar para no espaço vazio?

![captura de tela](images/dodge-no-gravity.png)

\--- /task \---

\--- task \---

Para corrigir isso, adicione gravidade ao seu jogo. Para fazer isso, crie uma nova variável chamada `gravidade`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

Você pode esconder esta variável do seu Palco se quiser.

![captura de tela](images/dodge-gravity-annotated.png)

\--- /task \---

\--- task \---

Adicione esses novos blocos de código que definem `gravidade` para um número negativo e use o valor de `gravidade` para mudar repetidamente a coordenada y do seu personagem:

![ator pico walking](images/pico_walking_sprite.png)

```blocks3
    quando ⚑ for clicado
    mude [gravidade v] para [-4]
    sempre
        adicione (gravidade) a y
    end
```

\--- /task \---

\--- task \---

Clique na bandeira, e então arraste seu personagem para o topo do Palco. O que acontece? A gravidade funciona como você esperava?

![captura de tela](images/dodge-gravity-drag.png)

\--- /task \---

\--- task \---

A gravidade não deve mover seu ator personagem através de uma plataforma ou de uma escada! Adicione um bloco `se`{:class="blockcontrol"} ao seu código para que a gravidade só funcione quando seu personagem estiver no ar. O código de gravidade agora deve ficar assim:

![ator pico walking](images/pico_walking_sprite.png)

```blocks3
    quando ⚑ for clicado
    mude [gravidade v] para [-4]
    sempre
        se < não < <touching color [#0000FF]?> ou <touching color [#FF69B4]?> > > então
            adicione (gravidade) a y
        end
    end
```

\--- /task \---

\--- task \---

Teste o jogo novamente para ver se a gravidade funciona corretamente agora. O seu ator personagem para de cair quando toca uma plataforma ou uma escada? Você pode fazer o personagem sair da borda das plataformas e cair no nível abaixo?

![captura de tela](images/dodge-gravity-drag.png)

\--- /task \---

\--- task \---

Agora adicione um código para fazer seu personagem pular sempre que o jogador pressionar a tecla <kbd>espaço</kbd>. Uma maneira muito fácil de fazer isso é mover seu personagem algumas vezes:

![ator pico walking](images/pico_walking_sprite.png)

```blocks3
    quando a tecla [espaço v] for pressionada
    repita (10) vezes
        adicione (4) a y
    end
```

Como a gravidade está constantemente empurrando seu personagem para baixo por 4 pixels, você precisa escolher um número maior que `4` em seu bloco `adicione (4) a y`{:class="blockmotion"}. Altere este número até ficar satisfeito com a altura que o seu personagem salta.

\--- /task \---

\--- task \---

Teste seu código. Observe que o movimento de salto não é muito suave. Para fazer o salto parecer mais suave, você precisa mover seu ator personagem em quantidades cada vez menores, até que ele não suba mais.

\--- /task \---

\--- task \---

Para fazer isso, crie uma nova variável chamada `altura do salto`{:class="block3variables"}. Mais uma vez, você pode ocultar essa variável, se preferir.

\--- /task \---

\--- task \---

Exclua o código de salto que você adicionou ao seu ator personagem e adicione este código no lugar:

![ator pico walking](images/pico_walking_sprite.png)

```blocks3
    quando a tecla [espaço v] for pressionada
    mude [altura do salto v] para [8]
    repita até que < (altura do salto) = [0] >
        adicione (altura do salto) a y
        adicione (-0.5) a [altura do salto v]
    end
```

Esse código move seu personagem para cima em 8 pixels, depois 7,5 pixels, depois 7 pixels e assim por diante, até que não suba mais. Isso faz com que o salto pareça muito mais suave.

\--- /task \---

\--- task \---

Altere o valor da variável `altura do salto`{:class="block3variables"} que é definida antes do `repita`{:class="block3control"} começar. Então teste seu jogo.

Altere este número até ficar satisfeito com a altura que o seu personagem salta.

\--- /task \---