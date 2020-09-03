---
author:
- Eduardo Adame
date: 3 de Setembro de 2020
title: Curso de LaTeX
---

Introdução ao TexMaker
======================

Noções Básicas

What you write is what you see O LaTeX não segue o mesmo conceito de
outros editores de texto como o MS Word. Pois, a relação entre o que
você escreve e o arquivo final é assíncrona.

Principais Vantagens:

-   A formatação será a mesma independente de computador, editor,
    sistema operacional, programa, leitor, etc.

-   Você terá 2 arquivos principais: o editável, .tex; e o não editável,
    .pdf (alta qualidade e compatibilidade).

-   Fácil reutilização de estruturas e blocos de texto formatado.

-   Criação e utilização de templates e modelos complexos.

Infelizmente, como nem tudo são flores, também existem desvantagens. No
entanto, ao meu ver, é possível viver com elas ou simplesmente
substituir pelos alternativos.

Então são elas:

-   Sintaxe incomum e vasta. (+ variedade = + dúvida)

-   Menos \"ajudas e ferramentas\"

-   Necessidade de ter o compilador e o editor instalados.

-   Sem interatividades (arrastar o mouse, clicar aqui, ali)

Configurações Na barra superior, existe a aba , e, dentro dela, a janela
(que pode ser acessada pelo atalho ). Essa janela que abrirá dá acesso a
muitas opções relacionadas ao editor.

A opção que eu recomendo que ativem é a , logo na primeira tela, na
janela chamada . Essa opção faz com que você veja o pdf ao lado do seu
código.

Não mexa nas opções de compilação por nada, mas fique livre para
vasculhar as aparência em .

Atalhos e Orientações Úteis Existem várias boas práticas e atalhos que
podem te ajudar: Orientações:

-   Para cada documento que for escrever, crie uma pasta separada.
    Vários arquivos são gerados ao compilar.

-   Não compile com o documento aberto em um leitor externo (como um
    Adobe Acrobat Reader)

-   Compile no mínimo duas vezes antes de compartilhar o documento

Atalhos:

-   \- Compila e Atualiza PDF

-   \- Fecha o Messages/Log

-   \- Comenta a Linha

Conceitos Iniciais
==================

Preâmbulo

Exemplos de parâmetros:

-   Tipo do Documento (Obrigatório)

-   Pacotes (Alguns são obrigatórios)

-   Autor, Título, Data, etc. (Metadata)

-   Temas e parâmetros extras.

Estrutura básica de um documento

``` {.latex}
\documentclass[11pt]{article}
\usepackage[utf8]{inputenc}
\usepackage[portuguese]{babel}
\usepackage[T1]{fontenc}
\usepackage{amsmath}
\usepackage{amsfonts}
\usepackage{amssymb}
\usepackage{graphicx}
\author{Eduardo Adame}
\title{Curso de \LaTeX}
\date{\today}
\begin{document}

\end{document}
```

Ambientes

Tudo que começa, termina Os ambientes é a separação do documento em
blocos de características diferentes. Por exemplo, existem ambientes
para listas enumeradas, para expressões matemáticas, para texto
centralizado, para figuras, etc.

Essa é a forma geral de todo ambiente.

``` {.latex}
\begin{nomedoambiente}
\comando
\end{nomedoambiente}
```

É possível ter ambientes dentro de ambientes.

Escrevendo Documentos
=====================

Criando e estruturando um documento Como vimos anteriormente, precisamos
de um preâmbulo para nosso documento.\
O Texmaker tem um assistente que auxilia na criação dele. Então, após
criar um novo e salvar arquivo () e (), acesse na barra superior e .\
Nele você escolherá as classe do documento, autor, e etc. De priori,
além dos dados pessoais, acho ideal marcar os pacotes e , além do . Esse
pacotes permitem os comandos e funcionalidades \"modernas\" do LaTeX.

Classes de documentos

Para cada classe, existem comandos e comportamentos específicos

-   article

-   book

-   letter

-   report

-   beamer

-   abnTeX2

-   ...

Tipos de letra

-   **Bold:** \\`textbf{Bold}`

-   *Enfase:* \\`emph{Enfase}`

-   *Italic:* \\`textit{Italic}`

-   `Monotype:` \\`texttt{Monotype}`

-   [Sans Serif:]{.sans-serif} \\`textsf{Sans Serif}`

-   *Slanted:* \\`textsl{Slanted}`

-   [SmallCaps:]{.smallcaps} \\`textsc{SmallCaps}`

-   [Underline:]{.ul} \\`underline{Underline}`

Tamanhos de letra

-   `\tiny ...`

-   `\scriptsize ...`

-   `\footnotesize ...`

-   `\small ...`

-   `\normalsize ...`

-   `\large ...`

-   `\Large ...`

-   `\LARGE ...`

-   `\huge ...`

-   `\Huge ...`

Ambientes: Listas Existem listas enumeradas e não enumeradas, veja:

Enumerada

``` {.latex}
\begin{enumerate}
\item Eduardo
\item João
\item Mario
\end{enumerate}
```

Resultado

1.  Eduardo

2.  João

3.  Mario

Ambientes: Listas

Não Enumerada

``` {.latex}
\begin{itemize}
\item Eduardo
\item João
\item Mario
\end{itemize}
```

Resultado

-   Eduardo

-   João

-   Mario

Ambientes: Listas Você ainda pode alterar o simbolo de cada item (Isso
independe de qual das listas):

Exemplo

``` {.latex}
\begin{enumerate}
\item[1th] Eduardo
\item[2nd] João
\item Mario
\end{enumerate}
```

Resultado

1.  Eduardo

2.  João

3.  Mario

Ambientes: Listas DESAFIO: Listas dentro de listas.

Enumerada

``` {.latex}
\begin{enumerate}
\item Eduardo
\begin{enumerate}
\item Jorge
\item Carlos
\begin{enumerate}
\item Maria
\end{enumerate}
\end{enumerate}
\item João
\end{enumerate}
```

Notas de Rodapé É muito fácil criar notas de rodapé no LaTeX

Entrada

``` {.latex}
Stardust: gente que voa.\footnote{GOMES, Paulo.}
```

Saída Stardust: gente que voa.[^1]

Fórmulas Matemáticas no LaTeX

Fórmulas em linha de texto

-   `$ ... $`{.latex}

Fórmulas destacadas do texto

-   `$$ ... $$`{.latex}

Algumas estruturas simples

-   Índice: $Z_{gnd}$

-   Expoente: $e^{-j\omega t}$

-   Fração e radical: $\dfrac{-b\pm\sqrt{b^2-4ac}}{2a}$

-   Letras gregas, operadores\...: $\Omega$, $\Re$, $\nabla^2$,
    $\partial$\...

Como escrever uma fórmula no LaTeX

Índices e expoentes

\<símbolo\>\_\<índice\>  ̂\<expoente\>

Como escrever uma fórmula no LaTeX

Barras

Chaves horizontais

Raiz de grau $n$

Como escrever uma fórmula no LaTeX

Alguns símbolos

    Símbolo     Código    Descrição
  ----------- ---------- ------------
                         
    $\sum$      \\sum     Somatório
                         
    $\prod$     \\prod    Produtório
                         
    $\int$      \\int      Integral
                         
   $\bigcap$   \\bigcap   Interseção
                         
   $\bigcup$   \\bigcup     União
                         

O Alfabeto Grego

  --------- ---------- ------------ -- --------- ----------- ----------- -- --------- ------------ ------------
    Alpha      $A$       $\alpha$        Iota         I        $\iota$         Rho        $P$         $\rho$
                                                                                                   
    Beta       $B$       $\beta$         Kappa       $K$      $\kappa$        Sigma     $\Sigma$     $\sigma$
                                                                                                   
    Gamma    $\Gamma$    $\gamma$       Lambda    $\Lambda$   $\lambda$        Tau        $T$         $\tau$
                                                                                                   
    Delta    $\Delta$    $\delta$         Mu         $M$        $\mu$        Upsilon   $\Upsilon$   $\upsilon$
                                                                                                   
   Epsilon     $E$      $\epsilon$        Nu         $N$        $\nu$          Phi       $\Phi$       $\phi$
                                                                                                   
    Zeta       $Z$       $\zeta$          Xi        $\Xi$       $\xi$          Chi        $X$         $\chi$
                                                                                                   
     Eta       $H$        $\eta$        Omicron      $O$         $o$           Psi       $\Psi$       $\psi$
                                                                                                   
    Theta    $\Theta$    $\theta$         Pi        $\Pi$       $\pi$         Omega     $\Omega$     $\omega$
  --------- ---------- ------------ -- --------- ----------- ----------- -- --------- ------------ ------------

Formatação Avançada {#ForAvan}
===================

Além de ser possível adicionar os seguintes comandos dentro do ambiente:

Além de dentro do no `\includegraphics`{.latex} ser possível adicionar a
opção `width=\textwidth`{.latex}[^2], que faz a imagem ficar do tamanho
do texto.

Align: matemática alinhada É possível escrever várias expressões
matemáticas em sequência (o que é normal em demonstrações), com o
ambiente que usa o caractere de alinhamento (&).

Entrada

``` {.latex}
\begin{align*}
a + b - c + d  + 4 &= 78 - 23 + 31\\
a + b + d &= c + 82
\end{align*}
```

Saída $$\begin{aligned}
a + b - c + d  + 4 &= 78 - 23 + 31\\
a + b + d &= c + 82\end{aligned}$$

Também pode ser lado a lado:

Entrada

``` {.latex}
\begin{align*}
a &= 4 & b &= 8 & c &= 12 \\
d &= 16 & & & e &=20
\end{align*}
```

Saída $$\begin{aligned}
a &= 4 & b &= 8 & c &= 12 \\
d &= 16 & & & e &=20\end{aligned}$$

Criando Tabelas Para criar tabelas, existe o modo \"simples e difícil\"
que é escrevendo a mão pelo ambiente . Utilizando o mesmo sistema do .

Entrada

``` {.latex}
\begin{tabular}{|c|c|c|}
\hline 
a & b & c \\ 
\hline 
u &  & o \\ 
\hline 
\end{tabular} 
```

Saída

   a   b   c
  --- --- ---
   u       o

Criando Tabelas Utilizando o Site A outra forma é visitando o site
abaixo: <https://www.tablesgenerator.com/>

Assim será possível ter uma interface parecida com o Excel e uma grande
diversidade de opções. Após isso, basta clicar em Generate e copiar o
código. (Preste atenção nos comentários, eles podem pedir que você
adicione pacotes ao preâmbulo)

Utilizando o Tables Generator

DESAFIO: 0.6 tamanho do texto, estilo de livro.

Utilizando o Tables Generator

``` {.latex breaklines="" breakafter="\\}"}
\begin{table}[]
\centering
\resizebox{.6\textwidth}{!}{%
\begin{tabular}{@{}cccc@{}}
\toprule
Nome & Curso & Idade & SO \\ \midrule
\multicolumn{1}{|c|}{Eduardo} & \multicolumn{1}{c|}{Tec. Mec.} & \multicolumn{1}{c|}{17} & \multicolumn{1}{c|}{Arch Linux} \\ \midrule
 &  &  &  \\ \bottomrule
\end{tabular}%
}
\caption{Relação de SO e Curso por Aluno.}
\end{table}
```

Pacotes
=======

CTAN Dando uma atenção especial aos pacotes, eles são basicamente
extensões para o LaTeX, ou seja, adicionam funções extras. Para entender
como um pacote específico funciona, ou procurar um que te atenda,
existem dois sites:

-   CTAN: <https://www.ctan.org/>

-   Stack Exchange: <https://tex.stackexchange.com>

O CTAN armazena informações sobre todos os pacotes disponíveis no LaTeX,
junto de seus manuais que ensinam como utilizá-lo. Já o Stack Exchange
serve para tirar dúvidas ou ler a de outros já solucionadas. Muito
possivelmente um pacote irá resolver seu problema.

Existem alguns pacotes bem conhecidos e com boa documentação por aí:

-   indentfirst: Automatiza os parágrafos

-   hyperref: Cria hyperlinks automaticamente

-   tikz: Disponibiliza o ambiente tikzpicture para ilustrações

-   minted: Adiciona highlight para códigos

-   chemfig: Adiciona funções químicas

[^1]: GOMES, Paulo.

[^2]: Você pode adicionar um decimal entre 0 e 1 antes de
    `\textwidth`{.latex} para utilizar em proporção
