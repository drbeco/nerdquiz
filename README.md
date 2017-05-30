## Nerd Quiz

### Introdução 

Jogo de cartas com perguntas e respostas do mundo Nerd.

O jogo inicia com um menu de opções. Uma das opções é para jogar, e o jogo propriamente se inicia.

A cada 5 respostas certas, o jogador avança de nível. São três níveis, e se o jogador passar do terceiro vence.

Se o jogador vencer ou desistir, o jogo termina e o menu inicial reaparece.

### Menu

O jogo apresentará um menu inicial com as opções:

    1. ler arquivo
    2. inserir novo nodo
    3. buscar um nodo
    4. alterar um nodo
    5. apagar um nodo
    6. jogar
    7. sair

Para cada item do menu tem-se as operações como descritas a seguir.

#### 1. ler arquivo

* Pedir o nome do arquivo a ser lido. Deve-se imprimir um nome "default" para o caso do usuário digitar `enter` sem escolher um arquivo. Se o nome não for dado, um arquivo padrão deverá ser usado.
* O arquivo lido recria na memória a lista de nodos com perguntas e respostas.
* Uma mensagem de sucesso ou falha deve aparecer e voltar ao menu inicial.

#### 2. inserir novo nodo

* Ler uma string (máximo 256 caracteres - deve ser conferido se não ultrapassa), contendo a pergunta.
* Ler uma string (idem), contendo a resposta.
* Ler de um menu qual a categoria da pergunta. As categorias são:

    1. Brinquedos (brinquedos)
    2. Desenhos animados (cartoons)
    3. Ciência e tecnologia (ciencia)
    4. Clássicos da literatura nerd (literatura)
    5. Datas comemorativas e eventos nerds (eventos)
    6. Dispositivos (gadgets)
    7. Filmes (filmes)
    8. Frases nerds (frases)
    9. Histórias em quadrinhos (gibis)
   10. Línguas (linguas)
   11. Nerds famosos da ficção (personagens)
   12. Nerds famosos da vida real (famosos)
   13. Referências que só um nerd entende (referencias)
   14. Seriados de TV (seriados)

Entre parênteses estão as palavras-chaves que devem ser usadas como enumeração (`enum`).

* Ler um inteiro com o nível (1, 2 ou 3).
* Após a leitura do conteúdo do nodo (informação), o nodo deve ser inserido numa lista encadeada por ponteiros para categorias e para níveis.

#### 3. buscar um nodo

* Deve imprimir um sub-menu com os itens:
    1. Buscar por nível
    2. Buscar por categoria
    3. Voltar ao menu principal

Se escolhido 1, deve-se perguntar o nível e então passar um a um cada item do nível escolhido, até que o usuário confirme que encontrou o que ele queria. O item selecionado fica guardado no ponteiro pbusca. Se não encontrar, pbusca deve ser nulo. Ao fim, retornar ao menu principal.

Se escolhido 2, analogamente ao item 1, pergunta-se a categoria (mostrando o menu de categorias), apresentam-se todas as cartas da categoria escolhida, uma por vez, perguntando a cada passo se é a carta escolhida. O ponteiro pbusca deve apontar para a carta escolhida ou para nulo ao final do processo, e retorna ao menu principal.

#### 4. alterar um nodo

Se o ponteiro pbusca for nulo, deve-se primeiro pedir para o usuário buscar um elemento no menu de buscas, e retornar ao menu principal.

Caso contrário, imprime-se o cartão, confirma se é realmente o que se quer alterar, e então pergunta-se novamente as informações do cartão. Se o nível ou a categoria for alterado, a lista deve ser re-organizada a contento.

#### 5. apagar um nodo

Se o ponteiro pbusca for nulo, deve-se retornar ao menu principal, indicando ao usuário que primeiro ele deve escolher o nodo a ser apagado.

Apresenta-se o nodo, pede-se confirmação, e se confirmado, apaga-se o nodo, re-organizando a lista com os nodos restantes, caso pbusca tenha um nodo válido já escolhido.

#### 6. jogar

Como já colocado na introdução, o jogo é simples: apresenta-se perguntas e aguarda-se que o usuário pense na resposta.

A resposta correta é então apresentada e deve-se perguntar ao usuário se ele confirma que acertou ou não. É o usuário que diz se acertou. Se ele aceitou, soma-se um ponto em sua pontuação.

A cada cinco pontos o usuário avança de nível, iniciando no 1 até o 3.

Se atingir 15 pontos, o jogo termina e o usuário vence. O menu principal deve ser mostrado ao final.

Se o usuário desistir, o jogo termina sem vitória e volta ao menu principal. O usuário poderá desistir a cada vez que lhe for perguntado se acertou ou não, em um menu:

Digite:

    - 'a' para acertei
    - 'e' para errei
    - 'd' para desistir

#### 7. sair

Ao entrar neste menu, um novo submenu será mostrado com as opções:

    1. Salvar e sair
    2. Sair sem salvar
    3. Voltar ao menu principal

Caso a opção 1 for escolhida, deve-se perguntar o nome do arquivo (e imprimir um nome default caso o usuário prefira não digitar nada e apenas teclar `ENTER`). Então o programa salva toda a informação da lista no arquivo indicado, e um laço passando por todos elementos também libera a memória da lista com a função `free()`.

Caso a opção 2 seja escolhida, basta liberar todos os nodos da memória e terminar o programa.

E finalmente, a opção 3 aborta o menu de sair, voltando ao menu principal.

### Orientação

* Autor: Prof. Dr. Ruben Carlo Benante
* Email: rcb@upe.br
* Data: 2016-09-07
* Licensa: GNU/GPL v2.0

### Copyright

Este é um programa sobre listas encadeadas e alocação de memória. As perguntas inseridas não fazem parte do programa, cujo fim é apenas educacional. 

As questões de conhecimento público sobre temas famosos "nerds" (filmes, conhecimento científico e ficção, etc.) são encontradas em diversos foruns e podem ser utilizadas como "dados" para fomentar o programa.

As perguntas usadas aqui como exemplo, bem como a classificação em categorias e níveis, são retiradas do baralho **NERD QUIZ**, e tem autorização dos autores para seu uso na forma deste programa educacional. Para outros usos, contate diretamente a editora em editorial@pandabooks.com.br

* Referência:
    - FERNANDES, Luís Flavio & RIOS, Rosana
    - Nerd Quiz, São Paulo, Panda Books, 2013
    - www.pandabooks.com.br
    - ISBN 978-85-7888-265-5

Este repositório e o trabalho aqui desenvolvido não é responsável e nem dá autorização para trabalhos derivados.

