---
title: o que é o terminal?
excerpt: lorem ipsum
date: 2022-06-08
slug: terminal
tags:
  - linux
  - intro
---

Você já deve ter visto aquelas telas pretas, com linhas pequenas pipocando sem parar.

Possivelmente você viu isso em contextos de filme, onde há um super hacker escrevendo dezenas de letras por segundo com o objetivo de quebrar todas as senhas e acessar o sistema secreto do pentágono.

Bom, não que você não viu um terminal... mas ele é bem mais que isso.

A ideia desse texto é desmistificar e explicar **tudo que você precisa saber para conhecer o `terminal`**, além de mostrar o quanto ele pode ser divertido e útil.

## O que é o terminal, afinal?

Terminal é um equipamento que **lhe permite interagir com um computador por meio de texto**. Bem por isso, é quase sempre constituindo por uma **tela** e **teclado** para essa interface.

Mais especificamente, neste texto falaremos sobre o `vídeo terminal`, que **possui uma tela além do teclado**, em contraste com terminais mais antigos, que **interfaciavam com o computador por impressão do texto** (semelhante ao fax). Um exemplo de video terminal é o [VT100](https://pt.wikipedia.org/wiki/VT100).

E se logo de cara você está com medo, ou acha que deve ser muito difícil mexer em um terminal, quero que você me diga quão dificil é mexer nesse cara:

![2021-05-03-21_29_17.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1620088181906/hviJ5cKG4.jpeg)

É isso mesmo, um chat. Você sabe usar ele? Então você já tem metade do que precisa, acredite. De forma bem simples, o terminal é um chat... com o seu computador! Nele você escreverá algo para o computador, e ele vai lhe responder. **As mensagens que mandamos para o computador serão sempre `comandos` para ele executar.**

E antigamente isso fazia mais sentido ainda. Visto que os computadores eram caros (e enormes), a melhor solução era ter vários equipamentos menores que só pedem coisas para o único computador do local. Esses equipamentos eram literalmente os terminais, também chamados de terminais burros. Burro porque fazer algo sozinho ele não fazia. Não possuía memória, nem processador dedicado. Ele só pedia para o servidor, e o servidor devolvia na tela o que lhe foi pedido.

E hoje ainda é assim. Claro, já não precisamos de dois equipamentos, temos um só. Mas ainda falamos com o computador por um terminal, com uma pequena mudança: agora o terminal é um programa, também conhecido como `emulador de terminal`, não sendo mais aquele monitor de tubo com comunicação serial.

![terminal history](https://cdn.hashnode.com/res/hashnode/image/upload/v1620269974602/1UrRBhHnE.png)

**O terminal agora vive dentro do próprio computador, se tornando apenas uma abstração digital mantida unicamente pela conveniência de comunicação dos humanos para com as máquinas.**

E por meio de uma das interfaces mais antigas de computador, que ainda hoje vemos uma infinidade de usos e aplicações para o ambiente de desenvolvimento.

## O que o terminal tem:

Diga oi para o meu terminal.

![2021-08-22-12_14_26.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1629648793583/kAopJQuOY.png)

Ele é bem vazio de cara, porque ele é só um monitor. Ele só mostra um programa alí no topo. O `shell`!

### Shell

**O shell é o interpetador de comandos do terminal**, eu vou digitar nosso primeiro comando. O `ls`.

![shell.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1629856068335/GS4CzRHud.png)

Em toda tela de terminal você vai se deparar com duas coisas:

- O `prompt`: Indica onde você começa o seu comando, sua "mensagem". Nele costuma conter algumas informações úteis como **o diretório (pasta) que você está** ou **usuário que vocês está logado**, além de várias outras coisas que você mesmo pode adicionar.

- A `linha de comando`: Espaço onde se escreve o comando em si.

O `$` é um indicador que tudo que vem depois dele deve ser interpretado como um comando. Quando você está logado como root, o símbolo muda para um `#`. Em sistemas baseados no DOS, como o windows, esse símbolo pode ser um `>`

Por sinal, tem várias opções de shell. O shell que eu mostrei é o mais comum, o `bash`, mas no dia a dia eu uso o `zsh`, bem famoso pelas suas customizações.

![zsh.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1629860866026/IGjri2orv.png)

Mais estiloso, né. E sim, eu curto roxo.

Quando um comando é enviado, o sistema retornará a resposta logo embaixo, sendo possível 3 opções:

- ℹ️ **As informações solicitadas:** Quando o seu comando solicita alguma informação, isso aparecerá logo abaixo a linha de comando;
- ❌ **Uma mensagem de erro:** Quando o comando chamado não executou como o esperado.
- ☑️ **Nada:** Pra comandos que deram certo e não respondem nada, esse é o padrão. Quando o comando deu certo, espere por nenhuma resposta.

Parece contra intuitivo, mas isso se deve por otimização. O terminal só responde o que ele precisa te dar, ou seja, a informação que você pediu, ou algum erro. Para comandos que não se esperam um retorno, confirmar que o comando deu certo é visto como uma redundância, visto que "dar certo" já é o esperado, e no começo do terminal (lá do terminal burro), o custo de tranferência de dados era alto para trocar essas mensagens entre terminal x servidor.

## Usando o terminal

Voltando ao comando exemplo, o `ls`. Ele serve para `listar os arquivos` e subpastas presentes no diretório que você se encontra.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1632019370523/hXpw0XQ1j.png)

Notou o `~` logo no final do prompt? Ele simboliza a sua pasta `home`, a pasta inicial do seu usuário, onde as suas coisas ficam no sistema. O comando `ls` me listou todas as pastas e arquivos da minha home.

Para irmos numa pasta especifica, o comando `cd` (_change directory_) servirá para `mudar a pasta` que você se encontra.

Note que ao mudarmos o diretório onde estamos, o prompt atualizará o caminho atual.

![2021-09-12-18_17_10.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1631481464222/nLXgrurrh.png)

Para voltarmos para o diretório anterior, podemos escrever `cd ..`, onde `..` sempre se refere ao diretório pai do que você se encontra.

Os comandos por texto podem receber `parâmetros`, mensagens a mais que informam formas específicas que o comando deve ser executado. No comando `ls` por exemplo, podemos informar o parâmetro `--color` para termos uma lista formatada por cor, diferenciando pastas, arquivos e atalhos.

![2021-09-12-18_19_51.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1631481720341/3STm-3Yi3.png)

Essa interação por texto pode parecer lenta, mas é exatamente o contrário. Em grande parte das vezes, o ambiente de linha de comando será muito mais rápido que com mouse (e já descorrerei mais sobre isso).

Esse estilo por "chat" de interação é chamado de `CLI` (do inglês, `interface de linha de comando`).

![cat.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1632020178477/_OX9UgEht.png)

![man.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1632020226916/OeqNZCNBE.png)

E por interagir por texto, não quer dizer que tudo se resume à essa troca de mensagem. Aplicações para o terminal também podem ter interfaces visuais próprias bem ricas.

Como por exemplo o `vim` e `nvim` (editores de texto), `htop` e `bpytop` (gerenciadores de tarefas), players de música como `moc`, entre outros vários para email, calendário e até navegar pela web. Se usa muito o termo **TUI** (_Text User Interface_) para descrever esse tipo de programa.

![2021-08-22-20_29_04.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1629674966105/4kky1z0-7.png)

[O projeto awesome-cli-apps](https://github.com/agarrharr/awesome-cli-apps) tem uma lista enorme de programas interssantes para o terminal.

E não, eles não podem competir em tudo com aplicações GUI (Graphical User Interface). Quando você entende as utilidades do terminal, você tira o melhor proveito dele.

## Por que usar o terminal

Recaptulando, há duas formas principais de se interagir com o computador:

- ** Por aplicações gráficas (GUI)**, que desenham e processam livremente os pixels na tela, esperando que você navegue pela tela com o mouse;
- **Por aplicações de terminal (CLI, TUI)**, apresentando informações basedas em texto;

Muitos dos programas que se usa por interface gráfica também tem para o terminal.

![2021-08-22-01_47_19.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1629669618913/qeANutksd.png)
_Gerenciador de arquivos - pcmanfm e nnn_

![2021-08-22-20_18_54.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1629674379234/rna1AtHZP.png)
_Editores de texto - vscodium e nvim_

Não se pode concluir uma forma como _a_ melhor, mas há muitas situações onde de fato o terminal se destaca.

### ⚡Velocidade

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1631632996607/lkeDj4EbT.png)

Como já dito, ao se usar o terminal, você se verá navegando muito pelos diretórios do seu sistema. E, sem muito tempo de uso, você já pode estar navegando super rápido. Me acompanha: se você for uma pessoa que já se dá super bem digitando no computador, imagina usar essa velocidade pra navegar por ele.

Essa velocidade não precisa ficar só na navegação de arquivos e não se resume à digitação de palavras. Ter macros e comandos no teclado para controlar o programa é comum. **Para uma aplicação com bom suporte ao teclado, toda interação pode ser feita na velocidade que sua digitação alcançar**, e isso lhe permite ir melhorando com a pratica.

Os benefícios são claros também pra quem não digita rápido. Entre **navegar mais de uma tela**/menu ou digitar/**copiar uma única frase** no seu terminal, você pode ganhar tempo com a segunda opção. **Você não está refém ao que a tela lhe mostra para clicar.**

[Exemplo para instalar n programas GUI x CLI]

### 🎯 Precisão

Uma coisa que a linha de comando permite de forma natural é a chance de lidarmos com o computador de forma MUITO específica. Sabe quando você pede uma pizza num aplicativo, **clicando** em cada sabor, sem problema algum? Se você quiser que escrevam uma mensagem de aniversário na caixa, como faria? Nessas horas, ter um lugar pra por uma observação seria o ideal, né?

Você nunca terá **todas** as opções possíveis de pedido numa tela, por isso há disponível o que é mais comum. Qualquer outra coisa específica, há uma forma livre: escrever. Assim você será mais específico. Desta forma, interface gráfica e linha de comando se completam.

Elas se diferenciam pela **densidade de informações** que uma situação demanda:

- Em **GUI** recebemos informações mais bem apresentadas, mas o _input_ do usuário é mais simples e menos denso, como um prato _a la carte_ no cardápio.
- Em **CLI** você possui uma gama de opções disponíveis que podem ser declaradas mais do seu jeito, mencionando apenas o que voc"e precisa Como seu prato do _buffet_, que tem muito mais batata frita que deveria.

[Exemplo com AWK]

### 🔗 Integração

- Ele permite integrar e extender os programas
- Como ele trabalha com lihas de entrada e saidas que o programa cospe, a regra sempre se baseia por texto. Uma saida entra na entrada da outra.

#### STDIN e STDOUT

A chamada de um comando sempre terá dois componentes, a informação de entrada (STandarD INput, ou Entrada Padrão) e a saída da informação (de _STandarD OUTput_, ou Saída Padrão)

### 🤖 Automação

- muitas dessas coisas vem por meio de scripts, imagine como uma carta, uma receita que vc já fala tudo que tem que pedir

## terminal: MONSTRO ou MELHOR AMIGO?

- Não é dificil, é diferente
  - uma questao de densidade de informações
  - Em GUI, recebemos informações mais bem apresentadas, mas o input do usuário é mais simples e menos denso
- TUI não precisa ser feio
- Não tem oq temer pois ele faz apenas o que vc manda, e não é tão facil fazer algo que faça mal
- novos comandos, como girias, que lhe permitem fazer coisas diferentes
  - como um chat, que vc escreve e conversa com a maquina, vc pede coisas e ela responde, lhe mostra coisas que vc quer
- Ele é consistente, unificado
  - Não importa em qual computador você vá, a maioria das coisa que você faz podem ser feitas em todos os lugares. Basta haver um terminal, e suas palavras pra serem escritas

## GUI x CLI/TUI e por que ficamos mais idiotas

- terminal burro: http://www.linfo.org/dumb_terminal.html
