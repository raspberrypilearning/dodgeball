## Esquivando das bolas

Seu personagem já pode se mover e pular, então é hora de adicionar algumas bolas que o personagem tem que evitar.

--- task ---

Crie um novo ator bola. Você pode escolher qualquer tipo de bola que quiser.

![captura de tela](images/dodge-balls.png)

--- /task ---

--- task ---

Redimensione o ator bola para que o personagem possa pular sobre ele. Tente fazer o personagem pular sobre a bola para testar se a bola é do tamanho certo.

![captura de tela](images/dodge-ball-resize.png)

--- /task ---

--- task ---

Adicione este código ao ator bola:

![ator bola](images/ball_sprite.png)

```blocks3
when green flag clicked
hide
forever 
  wait (3) seconds
  create clone of (myself v)
end
```

```blocks3
when I start as a clone
go to x: (160) y: (160)
show
repeat (22) 
  change y by (-4)
end
repeat (170) 
  change x by (-2)
  turn ccw (6) degrees
end
repeat (30) 
  change y by (-4)
end
delete this clone
```

Este código cria um novo clone do ator bola a cada três segundos. Cada novo clone se move ao longo da plataforma superior e então cai.

--- /task ---

--- task ---

Clique na bandeira para testar o jogo.

![captura de tela](images/dodge-ball-test.png)

--- /task ---

--- task ---

Adicione mais código ao seu ator bola para que os clones dele se movam entre todas as três plataformas.

![captura de tela](images/dodge-ball-more-motion.png)

--- hints ---


--- hint ---

Repita o bloco de código que você usou para mover o novo ator bola através da primeira plataforma. Você precisa alterar os valores de `x`{:class="block3motion"}, `y`{:class="block3motion"}, e `repita`{:class="block3control"} para que os clones sigam as plataformas corretamente.

--- /hint ---

--- hint ---

Estes são os blocos que você precisa. Certifique-se de adicioná-los na ordem correta.

![ator bola](images/ball_sprite.png)

```blocks3
repeat (170) 
  change x by (-2)
  turn ccw (6) degrees
end

repeat (180) 
  change x by (2)
  turn cw (6) degrees
end

repeat (30) 
  change y by (-4)
end
```

--- /hint ---

--- hint ---

O código para seus clones do ator bola deve ficar assim:

![ator bola](images/ball_sprite.png)

```blocks3
when I start as a clone
go to x: (160) y: (160)
show
repeat (22) 
  change y by (-4)
end
repeat (170) 
  change x by (-2)
  turn ccw (6) degrees
end
repeat (30) 
  change y by (-4)
end
repeat (180) 
  change x by (2)
  turn cw (6) degrees
end
repeat (30) 
  change y by (-4)
end
repeat (170) 
  change x by (-2)
  turn ccw (6) degrees
end
delete this clone
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Agora adicione alguns blocos de código para transmitir (enviar) uma mensagem se seu personagem for atingido por uma bola!

Adicione este código ao seu ator bola:

![ator bola](images/ball_sprite.png)

```blocks3
    when I start as a clone
	  forever
		  if < touching (Pico walking v)? > then
			  broadcast (atingido v)
		  end
	end
```

--- /task ---

--- task ---

Finalmente, adicione blocos de código ao seu ator personagem para movê-lo de volta à sua posição inicial quando receber a mensagem `atingido`:

![ator pico walking](images/pico_walking_sprite.png)

```blocks3
    when I receive [atingido v]
	  point in direction (90)
	  go to x: (-210) y: (-120)
```

--- /task ---

--- task ---

Teste seu código. Verifique se o personagem volta ao início depois de tocar uma bola.

--- /task ---