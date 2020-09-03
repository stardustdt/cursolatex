# Soluções dos Exercícios

## Exercício 1

```tex
\documentclass[11pt]{article}
\usepackage[utf8]{inputenc}
\usepackage[portuguese]{babel}
\usepackage[T1]{fontenc}
\usepackage{amsmath}
\usepackage{amsfonts}
\usepackage{amssymb}
\usepackage{graphicx}
\author{Eduardo Adame}
\title{Seu título}
\date{\today}
\begin{document}
\section{Tipos e Tamanhos de Letras}
\subsection{Tipos}
\begin{itemize}
\item \textbf{Bold:} \textbackslash \texttt{textbf\{Bold\}}
\item \emph{Enfase:} \textbackslash \texttt{emph\{Enfase\}}
\item \textit{Italic:} \textbackslash \texttt{textit\{Italic\}}
\item \texttt{Monotype:} \textbackslash \texttt{texttt\{Monotype\}}
\item \textsf{Sans Serif:} \textbackslash \texttt{textsf\{Sans Serif\}}
\item \textsl{Slanted:} \textbackslash \texttt{textsl\{Slanted\}}
\item \textsc{SmallCaps:} \textbackslash \texttt{textsc\{SmallCaps\}}
\item \underline{Underline:} \textbackslash \texttt{underline\{Underline\}}
\end{itemize}
\subsection{Tamanhos}
\begin{itemize}
\item \tiny \texttt{\textbackslash tiny ...}
\item \scriptsize \texttt{\textbackslash scriptsize ...}
\item \footnotesize \texttt{\textbackslash footnotesize ...}
\item \small \texttt{\textbackslash small ...}
\item \normalsize \texttt{\textbackslash normalsize ...}
\item \large \texttt{\textbackslash large ...}
\item \Large \texttt{\textbackslash Large ...}
\item \LARGE \texttt{\textbackslash LARGE ...}
\item \huge \texttt{\textbackslash huge ...}
\item \Huge \texttt{\textbackslash Huge ...}
\end{itemize}
\end{document}
```

## Exercício 2

```tex
\begin{enumerate}
\item Qual o valor de x na equação abaixo?
$$15x + 132 = 25x +72$$
\begin{enumerate}
\item $x=6$
\item $x=7$
\item $x=8$
\item $x=9$
\item $x=10$
\end{enumerate}
\end{enumerate}
```

## Exercício 3

```tex
Para toda equação do segundo grau na forma $ax^2 + bx + c = 0$, suas raízes são definidas por:
$$\dfrac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$
```

## Exercício 4

```tex
\section{Definições Matemáticas}
\subsection{Definição de Derivada}
$$\dfrac{dy}{dx} = \lim_{h \to 0} \dfrac{f(x + h) - f(x)}{h} $$
\subsection{Definição de Integral}
$$\int_a^b f(x) dx = F(b) - F(a)$$
```

## Exercício 5

```tex
Este é um animal muito bacana
\includegraphics[]{animal.jpg}
```

## Exercício 6

```tex
\begin{figure}
\centering
\includegraphics[width = .5\textwidth]{1.jpg}
\includegraphics[width = .5\textwidth]{2.jpg}
\caption{Imagens lado a lado}
\end{figure}
```

## Exercício 7

```tex
\begin{align*}
ax^2 + bx + c &= 0\\
ax^2 + bx &= -c\\
x^2 + \dfrac{bx}{a} &= \dfrac{-c}{a}\\ \\
x^2 + \dfrac{bx}{a} + \dfrac{b^2}{4a^2} &= \dfrac{b^2}{4a^2} - \dfrac{c}{a}\\ \\
\left(x+\dfrac{b}{2a}\right)^2 &= \dfrac{b^2 - 4ac}{4a^2}\\
x + \dfrac{b}{2a} &= \dfrac{\pm \sqrt{b^2 - 4ac}}{2a}\\
x &= \dfrac{-b \pm \sqrt{b^2 - 4ac}}{2a}
\end{align*}
```

## Exercício 8

```tex
% \usepackage{graphicx}
\begin{table}[]
\centering
\resizebox{.6\textwidth}{!}{%
\begin{tabular}{|c|c|c|}
\hline
Nome & Idade & Parentesco \\ \hline
Eduardo & 17 & Eu mesmo \\ \hline
Jeferson & 46 & Pai \\ \hline
Kênnia & 36 & Madrasta \\ \hline
\end{tabular}%
}
\end{table}
```
