# Álbum de figurinhas bíblico (versão de teste)

Esta pasta é a versão de teste. O `index.html` principal do jogo não foi alterado.

## Estreia: sexta-feira, 20/11/2026, à 0h

- **Antes da estreia o álbum fica trancado.** O ícone do Álbum no menu aparece apagado, com uma contagem regressiva pequena em cima (por exemplo `1d 1h`, depois `5h 12m`, depois `09:58`).
- **Balão de novidade:** na primeira vez que a pessoa abre esta versão, um balão aponta para o Álbum no menu, avisa da estreia e mostra a contagem. Aparece uma vez por pessoa.
- **Tela do Álbum trancada:** contagem regressiva grande no alto (dias, horas, minutos, segundos), um resumo de como vai funcionar e as duas capas com cadeado. Tocar numa capa abre a mensagem "Os álbuns serão liberados na sexta-feira, 20/11, à 0h".
- **Enquanto está trancado não dá para ganhar, comprar nem trocar figurinha.** O cartão do Início e o pacote da loja também mostram a contagem.
- **Na hora da estreia, com o jogo aberto, tudo destranca sozinho**, com o aviso "O álbum de figurinhas foi liberado!".
- **Só os quizzes feitos a partir de sexta 0h dão pacote.** Os quizzes feitos antes não dão nada. Vale a hora do celular de cada jogador.
- **Todo mundo começa do zero.** As figurinhas, trocas e prêmios dos testes ficaram guardados em campos antigos da conta, que o jogo não lê mais. Os pacotes comprados nos testes deixaram de contar como gasto, então as moedas voltam.
- A data fica numa linha só do código: `ALBUM_INICIO`, em `new Date(2026, 10, 20, 0, 0, 0)` (o mês começa em 0, por isso 10 é novembro).

## O que tem no álbum

- **108 figurinhas:** os 53 personagens e 55 objetos bíblicos. Todas usam a imagem 3D.
- **2 álbuns, 6 temas e 12 páginas.** Toda página é uma grade 3x3 com 9 figurinhas, personagens e objetos misturados, na ordem do tema. Cada tema tem 18 figurinhas (2 páginas).

| Álbum | Tema | Figurinhas |
|---|---|---|
| Antigo Testamento (72) | Do Éden ao Egito | 18 |
| | Êxodo e Conquista | 18 |
| | Reis e Profetas | 18 |
| | Exílio e Retorno | 18 |
| Novo Testamento (36) | Jesus e os Evangelhos | 18 |
| | Igreja e Missão | 18 |

- **As 11 que fecharam as páginas:** Túnica de José, Arca da Aliança, Fornalha Ardente, Túmulo Vazio, Barco de Paulo, Escudo da Fé, Espada do Espírito, Sandálias do Evangelho, Âncora da Esperança, Cálice da Ceia e Coroa da Vida.
- Se um dia um tema ficar com a última página incompleta, os espaços que faltam aparecem sozinhos como **Em breve**.

- **Raridades:** 67 comuns (moldura na cor da página), 38 raras (moldura dourada) e 3 lendárias (moldura furta-cor): Jesus, Arca de Noé e Tábuas da Lei.

## Cartas novas

- **Na grade do álbum, nos pacotes e nas trocas** aparece a carta leve: moldura da raridade, cenário da página, personagem, número e nome.
- **Ao tocar numa figurinha** abre a carta completa, com o título do personagem, o objeto, a referência bíblica e o selo da página. Ela inclina com o dedo, sem nenhum reflexo por cima da imagem.
- **Figurinha que falta** fica apagada, só com a sombra do desenho.

### Pasta `figs` (obrigatória)

As imagens 3D ficam na pasta `figs`, ao lado do `index.html`:

- `figs/p/` tem as imagens pequenas (grade, pacotes, trocas).
- `figs/g/` tem as imagens grandes (carta completa).

Suba a pasta `figs` inteira junto com o `index.html`. Se um arquivo não estiver lá, a carta daquele personagem volta sozinha para o desenho do jogo, sem erro.

### Quando chegarem imagens novas

Coloque as imagens novas na pasta `Imagens para figurinhas` e peça para incluir. Cada imagem é recortada, tratada e gravada em `figs/p` e `figs/g`, e o personagem entra na lista dos que têm imagem 3D.

## Pacotes

- Cada quiz do dia feito dá **1 pacote com 3 figurinhas**, sem repetir dentro do mesmo pacote. O pacote comprado também vem com 3.
- No fim do quiz o pacote aparece flutuando na tela, esperando o toque. Quem preferir toca em **Abrir depois** e o pacote fica guardado no Álbum.
- Só contam os quizzes feitos a partir da estreia. Um quiz atrasado feito depois da estreia também dá pacote.
- Com mais de um pacote guardado, o botão "Abrir os pacotes de uma vez" abre até 10.
- O sorteio é fixo para cada jogador e cada dia. Fechar e abrir o jogo não muda as figurinhas.
- As raras saem com metade da chance de uma comum, e as lendárias com um quarto. Na média, uma lendária específica leva cerca de 100 pacotes para sair; as trocas encurtam esse caminho.

### Comprar pacote

- Cada pacote custa **10 moedas**, vem com 3 figurinhas, e só dá para comprar **1 por dia**.
- O botão **Comprar** fica no alto do álbum e na primeira tela da loja.
- Depois da compra o pacote aparece flutuando, com **Abrir agora** e **Abrir depois**. O pacote guardado conta no número do menu e abre pelo botão **Abrir**.
- A compra entra na conta de moedas gastas, junto com os itens da loja.

### Janela de compra (pacote e loja)

- Toda compra abre a mesma janela: o item com a imagem dele, o tipo e as vantagens; embaixo, o recibo com **Seu saldo**, o preço **em vermelho com sinal de menos** e **Depois da compra**, com o saldo descendo até o valor final.
- O botão dourado "Comprar por N" confirma; "Agora não" fecha sem gastar.
- **Sem moedas suficientes** a janela mostra quanto falta e troca o botão por "Ganhar moedas".

### Abertura do pacote

- O saquinho aparece, balança e abre.
- As cartas chegam com as **costas** para cima (azul e dourado, com o logotipo) e viram uma a uma. Tocar numa carta vira na hora.
- Rara e lendária soltam um clarão ao virar.

## Os álbuns e as capas

- **No alto do álbum ficam três botões grandes:** **Abrir** (com o número de pacotes guardados), **Comprar** (preço e limite do dia) e **Trocar** (ícone novo de duas cartas com setas; mostra as propostas para responder).
- Ao tocar em **Álbum** no menu aparecem as capas: **Antigo Testamento** (azul) e **Novo Testamento** (vinho). Cada capa mostra o tema, três personagens, quantas figurinhas já foram coladas e o prêmio.
- Tocar numa capa abre o livro daquele álbum. O botão **Álbuns** volta para as capas.
- Depois de abrir um pacote, o botão "Ver o álbum" abre direto na página da figurinha nova.

### Para criar um álbum novo

No código, a lista `ALBUNS` tem uma linha por álbum (nome, tema, páginas, cores da capa, três personagens da capa e prêmio). Um álbum novo é uma linha nessa lista mais as páginas dele em `ALBUM_PAGINAS`. A capa, o livro, o progresso e o prêmio saem sozinhos. É só pedir.

## O livro

- O álbum é um livro: marcadores coloridos no alto (um por página), capa na cor da página, folha de papel com argolas.
- Cada página é uma grade **3x3**, no celular e no computador. A figurinha que falta aparece como um espaço tracejado com o número, a sombra e o nome.
- Para virar a página: toque num marcador, nas setas do rodapé, na dobra do canto ou arraste o dedo para o lado. A folha gira em volta da lombada e passa por cima da capa, sem ser cortada.
- O **Álbum** está no menu, entre Missões e Loja. O número no ícone soma pacotes para abrir e propostas de troca.

## Trocas

- Só com pessoas da **mesma sala**.
- No álbum, toque em **Trocar**, escolha a pessoa, escolha uma repetida dela e uma repetida sua. O ponto verde marca as que faltam no álbum de quem vai receber.
- **A lista só mostra quem tem figurinha repetida**, com a quantidade ao lado do nome, de quem tem mais para quem tem menos. Se você não tem repetida para oferecer, a janela avisa.
- A outra pessoa vê a proposta no álbum (e um aviso no cartão do Início) e toca em **Aceitar** ou **Recusar**.
- **Aviso de proposta:** quando chega uma proposta, aparece uma caixinha no alto da tela com quem propôs e as figurinhas, o sino mostra o número e o ícone do Álbum no menu também. O jogo confere ao abrir, ao trocar de tela e a cada 3 minutos. O aviso só aparece com o jogo aberto; não é notificação do celular com o jogo fechado.
- Quem propôs pode cancelar enquanto não houver resposta. Cada pessoa pode ter até 5 propostas abertas.
- Só dá para oferecer figurinha repetida. Quem recebe a proposta pode aceitar entregar uma que não é repetida; nesse caso o jogo pede confirmação.

## Prêmios

- **Página completa: +20 moedas** (uma vez por página; são 12 páginas).
- **Álbum completo: +50 moedas** em cada álbum. A conquista **Colecionador** sai quando todos os álbuns estão completos.
- As moedas aparecem com a caixinha e a animação até o total. A janela "Ganhar moedas" ganhou a linha do álbum.

## Outros ajustes desta versão

- **Espaço entre as caixas:** todas as telas e janelas foram conferidas no celular, no tablet e no computador. Corrigido: as salas encostadas na caixa "Outras salas do jogo" e a aba não escolhida (Lição ou Quiz) encostada na caixa de baixo. Uma regra geral agora dá espaço a qualquer caixa que venha depois de outra.
- **Tela de carregamento:** saiu a mensagem "Tentar de novo". Quando o jogo abre numa versão nova, aparece "Baixando a atualização do jogo…".
- **Notificações:** a janela não tem mais barra de rolagem para o lado; nome ou título comprido é cortado com reticências ou quebra de linha.
- **Contagem regressiva:** um som para o 3, o 2 e o 1 (cada um mais agudo) e um acorde no "VAI!".

## Ícones próprios (modelo Joia)

- O jogo não usa mais emoji na tela: são **80 ícones desenhados para o jogo**, iguais em todo celular. Estão no menu, nos botões, nas conquistas, nas reações do mural, nas ajudas do quiz, na conta e na área do administrador. A moeda também passou para o mesmo modelo.
- **Movimento:** cada ícone se mexe uma vez quando a pessoa toca no botão dele (a casa pula, o sino balança, a moeda gira). O sino também balança quando chega aviso novo.
- **Como funciona por dentro:** o jogo continua escrevendo o emoji no texto, e um trecho novo troca o emoji pelo desenho antes de aparecer. Por isso vale também para o que já está gravado, como as publicações do mural.
- **Onde o emoji continua:** nas mensagens que saem do jogo como texto (WhatsApp), porque lá não dá para mandar desenho.
- **Cartão de imagem das conquistas:** usa os ícones novos, e agora cabe a quarta linha (são 14 conquistas).
- A folha com todos os ícones está em `icones-joia-todos.png`.

## Fim do quiz

- Depois que os pontos sobem e as moedas voam para o total, **o pacote aparece flutuando**, com brilho e raios, esperando o toque. Tocar no pacote ou em "Abrir agora" abre; "Abrir depois" guarda. Se outra janela estiver aberta (missão cumprida, conquista), ele espera fechar. O botão "Abrir o pacote" continua na tela do resultado para quem deixou para depois.

## Para as trocas funcionarem no Firebase

As trocas usam uma coleção nova, `trocas`. Publique o arquivo `firestore.rules` desta pasta em Firebase Console → Firestore Database → Regras → Publicar. Ele é igual ao atual, com um bloco a mais para as trocas, e não muda nada para o site principal.

Sem publicar, o álbum e os pacotes funcionam, mas ao tentar trocar aparece o aviso de que as trocas ainda não foram liberadas.

## Para subir para a versão oficial

1. Suba o `index.html` desta pasta no lugar do oficial.
2. Suba a pasta `figs` inteira (as duas pastas, `p` e `g`).
3. Confira se as regras do Firestore com o bloco das trocas estão publicadas (seção acima).

A data de início e o álbum zerado já estão nesta versão; não falta nenhum ajuste.

## O que ainda dá para decidir

- A chance das raras e lendárias.
