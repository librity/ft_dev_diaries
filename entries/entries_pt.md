Todos os dias eu escrevo uma update do meu progresso na 42, respondendo:

- O que eu fiz ontem
- O que eu vou fazer hoje
- Qual foi o meu maior impedimento

Assim que a gente faz as dailies onde eu trabalho.

# 2021-02-05

- Ontem eu configurei meu makefile do libft e fiz 6 das funcoes mandatorias
- Hoje planejo continuar as funcoes de memoria do libft
- Meu maior impedimento foi a documentacao do make: tem varias regras cripticas e tem 50 jeitos diferentes de fazer a mesma coisa.

# 2021-02-06

- Sexta feira eu avancei ate a segunda parte do libft, ate a funcao ft_split.
- Hoje planejo terminar a segunda parte do libft e comecar os bonus
- Meu maior impedimento foi saber quais corner cases o moulinette vai testar. Espero que os testes automaticos cobram tudo.

# 2021-02-07

- Ontem terminei todas as funcoes mandatorias do libft e comecei o bonus.
- Hoje planejo terminar o bonus e testar tudo no guacamole.
- Meu maior impedimento foi ft_split: essa funcao foi bem chata de implementar. A ft_itoa tambem ficou bem tosca.

# 2021-02-08

- Ontem terminei o bunus do libft, corrigi os testes que estavam falhando e fiz a primeira correcao.
- Se abrir slot planejo fazer a segunda correcao hoje.
- Nessa semana e na proxima vou fazer aulas para tirar a habilitacao, e vou ficar indisponivel depois das 19h. Meu maior impedimento eh achar slot de correcao antes das 19h.

# 2021-02-09

- Ontem nao fiz nada relacionado ao cursus da 42.
- Hoje vou fazer minha segunda correcao da libft.
- Meu maior impedimento sao as aulas para tirar a habilitacao: vao das 19h ate as 23h. Estou chegando tarde em casa.

# 2021-02-10

- Ontem eu fiz a segunda correcao do libft.
- Se der tempo, hoje vou instalar a vm par poder fazer avaliacoes de outros cadetes e ganhar pontos.
- Meu maior impedimento nesses ultimos dias tem sido tempo.

# 2021-02-11

- Ontem eu nao consegui instalar a vm.
- Hoje vou fazer a terceira correcao do libft.

# 2021-02-12

- Ontem eu terminei o libft!!!
- Se der tempo, hoje vou comecar o get next line.

# 2021-02-14

- Ontem eu implementei testes unitarios com Unity no Libft (so 14 funcoes, WIP):
  - https://github.com/librity/ft_libft/tree/main/tests
- Hoje estou comecando o get_next_line.
- Nao tive impedimentos.

# 2021-02-15

- Ontem eu comecei o get_next_line. Ja tenho uma boa ideia do que eh para fazer. Estou achando um jeito de avancar a posicao do file descriptor no `read`.
  Tambem estou tentando entender como vou allocar suficiente memoria para uma linha inteira sendo que so posso ler `BUFFER_SIZE` bytes por vez, e a linha pode ser mais longa que esse `BUFFER_SIZE`.
- Hoje nao vou conseguir codar muito pelo trabalho e o CFC.
- Meu maior impedimento foi a falta de contexto: o get_next_line eh tipo um `getc` so que pega a linha inteira.

# 2021-02-16

- Ontem eu conversei com o @rdutenke, que me tirou varias duvidas sobre o `get_next_line`:
  _Agora eu sei que o read avanca a poicao no file descriptor automaticamente._
  O "pulo do gato" para este projeto eh utilizar um ponteiro statico como buffer, allocado com `BUFFER_SIZE + 1`: assim podemos passa-lo para `read` e tratar os differentes casos:

1. Se o buffer lido nao tem `'\n'` ou `EOF`, concatenamos com o buffer anterior e chamamos `read` novamente.
2. Se o buffer lido tem `'\n'` concatenamos com o buffer anterior ate o `'\n'`.
3. Se o buffer lido tem `EOF` concatenamos com o buffer anterior ate o `EOF`.
4. Finalmente temos que apontar o ponteiro `line` passado para uma string allocada que contenha a linha inteira sem o `'\n'`. Depois liberamos a memoria allocada nas strings intermediarias e retornamos `1` ou `0` para `'\n'` ou `EOF` respectivamente.
5. Se os parametros tem algum problema (`BUFFER_SIZE <= 0`), ou em alguma dessas operacaoes nao conseguimos allocar memoria, liberamos toda a memoria allocada e retornamos `-1`.

- Hoje nao vou conseguir codar muito pelo trabalho e o CFC.

# 2021-02-17

- Ontem nao consegui me dedicar ao projeto.
- Hoje nao vou conseguir codar muito pelo trabalho e o CFC. Pelo menos eh o meu penultimo dia de CFC, e ja vou me livrar disso.

# 2021-02-18

- Ontem eu aprendi com o @viniseneda#6780
  sobre como operacoes bitwise otimizam o codigo: ~~fazer comparacoes com `|` envez de `||`.~~ Compiladores modernos fazem varias otimizacoes diferentes, e estas variam de compilador a compilador. O ideal eh analizar o assembly gerado para saber quais otimizacoes sao melhores para o compilador utilizado:
  - https://stackoverflow.com/questions/52137520/when-use-bitwise-operations-instead-of-arithmetic-alternatives
  - https://github.com/agavrel/42-Bitwise_Operators
- Hoje eh meu ultimo dia de CFC :partying_face:!

# 2021-02-19

- Ontem eu aprendi com o @viniseneda#6780
  sobre a diferenca entre `arrays` e `pointers`, entre `memory stack` e `heap`, e sobre ponteiros `static` e `extern`.
  - https://stackoverflow.com/questions/29717970/do-i-need-to-free-char-array-of-fixed-length
  - https://vivadifferences.com/difference-between-stack-and-heap-in-c/
  - https://stackoverflow.com/questions/1286515/extern-and-static-pointers-in-c
- Hoje vai dar pra codar!

# 2021-02-20

- Ontem eu deixei meu get_next_line funcionando!
- Hoje vou refatorar, deixar ele em par com a moulinette e rodar os testes do github.
- Minha maior dificuldade esta sendo quebrar o get_next_line em funcoes menores ja que tem que passar um monte de referencias para as sub-funcoes.

# 2021-02-21

- Ontem refatorei e corrigi (quase) todos os erros do get_next_line. Tambem criei um script para facilitar nos testes do projeto:
  - https://github.com/librity/ft_get_next_line/blob/main/github_testers.sh
- Hoje vou fazer get_next_line passar nos testes que faltam e avaliar se vale a pena fazer o bonus.
- Meu maior impedimento foi abrir os testes automaticos para ver o que estava falhando.

# 2021-02-22

- Ontem eu terminei o get_next_line!
- Hoje vou comecar o netwhat, estudando sobre ips privados, masks, DHCP e IPV6.

# 2021-02-23

- Ontem eu estudei varios conceitos conceitos de redes. Tambem fiz uma call com meu squad onde expliquei gnl, e escrevi uma versao condensada disso:
  - https://github.com/librity/ft_get_next_line/blob/main/README.md
- Pretendo botar o netwhat para correcao hoje e termina-lo o antes possivel.

# 2021-02-24

- Ontem me lasquei no teste do netwhat, e vou ter que esperar 3 dias para tentar novamente :laughing: :tired_face: :rofl:
  Ja que nao posso me inscrever em outro projeto ate terminar esse, comecei o printf sozinho: estudei sobre argumntos variadicos com `stdarg.h` e adicionei algumas funcoes no meu libft.
  O Workshop de git foi animal: o cara mangia muito.
- Pretendo continuar o printf, comecando por definir uma estrutura escalavel para ele.
- Meu maior impedimento eh o tempo de retry do netwhat.

# 2021-02-25

- Ontem continuei estudando sobre o printf. Ele faz varias `conversions` que a gente vai ter que implementar, e para cada `conversions` ainda temos que considerar as flags (exemplo: `%06.2f`, `%15.10s` e `%*d`). Inicialmente vou estruturar meu codigo em duas partes:
  1. Vou verificar que o numero de argumentos passados corresponde ao numero de `conversions` na string de formato, e retornar erro (`-1`) caso contrario.
  2. Perocrrer a string de formato, escrevendo cada caracter ate chegar numa `conversion`. Para cada `conversion` vou gerar um metodo que cria uma string alocada e devidamente formatada: dai eh so escrever a string, adicionar o length na contagem de characteres e liberar a memoria.

Escolhi fazer assim por que eh simples, vou allocar o minimo de memoria possivel (evitar memory leaks), e consigo reaproveitar varias funcoes do libft. Me basieie na secao 7.3 do `The Ansi C Programming Language`, onde eles dao um exemplo do printf com essa estrutura.

Minha ideia original era fazer com split e join na string de formato, que requeriria fazer umas verificacoes loucas entre strings, alem da questao da memoria.

Tambem aprendi sobre como fazer verificacao de tipagem em C. Estou em duvida se precisamos verificar se os tipos dos parametros correspondem ao da string de formato: Preciso retornar erro em `ft_printf("%s", 42);`?

Por fim, adicionei github actions no meu projeto, que automaticamente rodam os testers em ambiente macos sempre que eu dou push na master. Me basiei neste repositorio: - https://github.com/wblech/42_github_actions

- Hoje vou continuar o printf, comecando pelo makefile.

- Meu maior impedimento ainda eh o tempo de retry do netwhat.

# 2021-02-26

- Ontem consegui dar um bom progresso no printf: ja estou com um codigo estruturado que printa strings, chars e ints.
- Hoje vou continuar o printf.
- Meu maior impedimento ainda eh o tempo de retry do netwhat.

# 2021-02-27

- Ontem fiz a trilha de Elixir da NLW da Rocket Seat. Fiz uma api bem basica de pagamentos. Foi a primeira vez que mexi em Elixir, e amei a liguagem. Aprendi varios conceitos e boas praticas de programacao funcional que me ajudaram com os projetos da 42.
  - https://github.com/librity/nlw_elixir
- Hoje vou fazer as outras duas trilhas do NLW: Node e React. Tambem vou fazer o netwhat, e se der tempo continuar trabalahndo no printf.

# 2021-02-28

- Ontem eu terminei o netwhat e avancei na trilha de React do NLW.
- Hoje vou continuar as trilhas do NLW e trabalhar no printf.

# 2021-03-01

- Ontem eu terminei as trilhas do NLW.
- Hoje vou trabalhar no printf.

# 2021-03-02

- Ontem eu estudei outras tecnologias e nao consegui trabalhar no printf.
- Hoje vou trabalhar no printf.

# 2021-03-03

- Meu printf ja esta printando numero hexadecimais e pontieros.
- Hoje vou trabalhar no printf.

# 2021-03-04

- Ontem fiz um CLI de ruby onde utilizei printf para criar uma view de tabela. Tambem ajudei outro cadete a debuggar o gnl.
- Hoje vou trabalhar no printf.

# 2021-03-05

- Ontem avancei no printf: debuggei e refatorei muita coisa. Ta ficando com uma estrutura bem legal, com structs isoladas para cada "modulo" do programa.
- Hoje vou trabalhar no printf.

# 2021-03-06

- Ontem avancei no printf: o meu printf ja esta fazendo todas as flags exceto a de wildcard `'*'`, que eh a mais dificil.
  Tambem aprendi que existem algums defines que ficam em headers diferentes dependendo do sistema.
  Um exemplo eh o `ARG_MAX`, que ficam com `limits.h` em macos, e em `linux/limits.h` em linux.
  Por questoes de portabilidade eh legal verificar e incluir o header apropiado nos projetos, especialmente para quem esta fazando em linux.
- https://stackoverflow.com/questions/5919996/how-to-detect-reliably-mac-os-x-ios-linux-windows-in-c-preprocessor
- Espero acabar o printf ate amanha.

```c
# include <limits.h>

# ifdef __linux__
# include <linux/limits.h>
# endif
```

# 2021-03-07

- Ontem eu resolvi botar todos meus updates diarios num site estatico com Hugo. Achei uma boa oportunidade de aprender a tecnologia, e estou gostando muito. Tambem estudei outras coisas e nao consegui trabalhar muito no printf.
- https://github.com/librity/ft_dev_diaries
- Hoje vou continuar trabalhando no printf.
