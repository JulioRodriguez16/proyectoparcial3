Aqui esta el codigo del latex:      \documentclass[a4paper]{article}

%%%%%%%% CREATE DOCUMENT STRUCTURE %%%%%%%%
%% Language and font encodings
\usepackage[english]{babel}
\usepackage[utf8x]{inputenc}
\usepackage[T1]{fontenc}
%\usepackage{subfig}

%% Sets page size and margins
\usepackage[a4paper,top=3cm,bottom=2cm,left=2cm,right=2cm,marginparwidth=1.75cm]{geometry}

%% Useful packages
\usepackage{amsmath}
\usepackage{graphicx}
\usepackage[colorinlistoftodos]{todonotes}
\usepackage[colorlinks=true, allcolors=blue]{hyperref}
\usepackage{caption}
\usepackage{subcaption}
\usepackage{sectsty}
\usepackage{apacite}
\usepackage{float}
\usepackage{titling} 
\usepackage{blindtext}
\usepackage[square,sort,comma,numbers]{natbib}
\usepackage[colorinlistoftodos]{todonotes}
\usepackage{xcolor}
\definecolor{darkgreen}{rgb}{0.0, 0.4, 0.0}

%%%%%%%% DOCUMENT %%%%%%%%
\begin{document}

%%%% Title Page
\begin{titlepage}

\newcommand{\HRule}{\rule{\linewidth}{0.5mm}} 							% horizontal line and its thickness
\center 
 
% University
\textsc{\LARGE ITESM}\\[1cm]

% Document info
\textsc{\Large Solución deecuaciones diferenciales usando el método de Euler}\\[0.2cm]
\textsc{\large M2025.820}\\[1cm] 										% Course Code
\HRule \\[0.8cm]
{ \huge \bfseries Proyecto Final.}\\[0.7cm]								% Assignment
\HRule \\[2cm]
\large
\emph{Authors: Maxiliano Macotela Nava, Julio Rodríguez Salcedo,Jim Kevin Holguín Rodríguez,Luz Karen Hernández Hernández, Andrés Serrato, César David Rosales Álvar}\\[1.5cm]													% Author info
{\large \today}\\[5cm]
\includegraphics[width=0.6\textwidth]{TecMonterrey_Horizontal_RGB.jpg}\\[1cm] 	% University logo
\vfill 
\end{titlepage}

%%\begin{abstract}
%%Your abstract.
%%\end{abstract}

%%%% SECTIONS
%% Section 1
\section*{INTRODUCCIÓN}
\section*{Las ecuaciones diferenciales ordinarias que modelan una realidad especıfica, aumentan su complejidad en la medida que se aproximen cada vez más al comportamiento del objeto o fenómeno en estudio, razón por la cual en la mayoría de los casos hallar su solución por métodos analıticos es imposible lo que nos lleva a utilizar los métodos numéricos. 
Como sabemos los métodos numéricos son una sucesión de operaciones matemáticas utilizadas para encontrar una solución numérica aproximada a un problema determinado. Es decir, se trata de una serie de cálculos para acercarnos lo más posible a una solución numérica con una precisión razonablemente buena. Los métodos numéricos son utilizados en ingeniería para facilitar la resolución de problemas que conllevan una enorme cantidad de cálculos, lo que permite ahorrar tiempo.
Estos métodos pueden implementarse en programas de cómputo elaborados en Matlab, los que permiten determinar las soluciones de las ecuaciones diferenciales ordinarias de modo que el lector encuentre una herramienta para modelar sus propias aplicaciones.}
\section*{OBJETIVO.}
\section*{Resolver problemas de ecuaciones diferenciales usando el método de Euler como el método clave de la entrega de este proyecto y compararlo con otros 3 métodos que serán: Heun, Simpson y Ralston para verificar el resultado correspondiente.}
\section*{CONTENIDO.}
\section*{Sea el problema de valor inicial 
y ′ = f(x,y) y(x0) = y0 
supongamos que tiene una solución única φ(x) en un algún intervalo con centro en x0. Sea h > 0 y consideremos puntos igualmente espaciados 
xn = x0 + nh n = 0, 1, 2,... 
Los valores de la soluci´on φ(xn) se pueden aproximar con yn, donde los valores de yn se obtienen como sigue [KEN 92]: 
En el punto (x0,y0) la pendiente de la solución de (1.1) es 
dy dx = f(x0,y0)
Por lo tanto, la recta tangente a la curva solución en el punto 
(x0,y0) es y = y0 + (x − x0)f(x0,y0) (1.2) 
Si se usa (1.2) como una aproximación a φ(x), en el punto x1 = x0 + h 
φ(x1) ≈ y1 = y0 + hf(x0,y0) 
En seguida, empezando en el punto (x1,y1) con pendiente f(x1,y1), se tiene la recta y = y1 + (x − x1)f(x1,y1) al pasar de x1 a x2 = x1 + h nos da la aproximación 
φ(x2) ≈ y2 = y1 + hf(x1,y1) 
al repetir el procedimiento se obtiene 
φ(x3) ≈ y3 = y2 + hf(x2,y2)}  
\newpage
\includegraphics[width=0.6\textwidth]{Captura de Pantalla 2021-11-25 a la(s) 19.51.07.png}\\[1cm]
\section*{Este sencillo procedimiento se llama Método de Euler 1 y se resume mediante las siguientes fórmulas recursivas 
xn+1 = xn + h 
 yn+1 = yn + hf(xn,yn), n = 0, 1, 2,...}
 \section*{ ALGORITMO DE EULER.}
\section*{Este algoritmo calcula la solución del problema de valor inicial en puntos equidistantes
x1 = x0 + h ,x2 = x0 + 2h, x3 = x0 + 3h, · · · ,xN = x0 + Nh, aquí f es tal que tiene una solución única en [x0,xN ].}
\section*{Entrada: Valores iniciales x0,y0, tamaño de paso y número de pasos N}
\section*{Para n=0,...,N-1, hacer xn+1 = xn + h yn+1 = yn + hf(xn,yn) Salida xn+1, yn+1 }
\section*{Parar.}
\section*{En matemática y computación, el método de Euler, llamado así en honor de Leonhard Euler, es un procedimiento de integración numérica para resolver ecuaciones diferenciales ordinarias a partir de un valor inicial dado.
El método de Euler es el más simple de los métodos numéricos resolver un problema del siguiente tipo:}
\includegraphics[width=0.6\textwidth]{imagen2.png}\\[1cm]
\section*{Consiste en multiplicar los intervalos que va de  a  en  subintervalos de ancho ; ósea:}
\includegraphics[width=0.6\textwidth]{imagen3.png}\\[1cm]
\section*{de manera que se obtiene un conjunto discreto de  puntos: Xo,X1,X2,.....,Xn  del intervalo de interés[Xo,Xf] . Para cualquiera de estos puntos se cumlple que:}
\includegraphics[width=0.6\textwidth]{imagen4.png}\\[1cm]
\section*{La condición inicial Y(Xo)=Yo , representa el punto Po=(Xo,Yo)  por donde pasa la curva solución de la ecuación de el planteamiento inicial, la cual se denotará como F(x)=y.
Ya teniendo el punto Po se puede evaluar la primera derivada de F(x) en ese punto; por lo tanto:}
\includegraphics[width=0.6\textwidth]{imagen5.png}\\[1cm]
\includegraphics[width=0.6\textwidth]{imagen6.png}\\[1cm]
\section*{correspondiente a . Entonces, podemos deducir segun la Gráfica A:}
\includegraphics[width=0.6\textwidth]{imagen7.png}\\[1cm]
\section*{Se resuelve para Y1}
\includegraphics[width=0.6\textwidth]{imagen8.png}\\[1cm]
\section*{Es evidente que la ordenada Y 1 calculada de esta manera no es igual a F(X1), pues existe un pequeño error. Sin embargo, el valor  sirve para que se aproxime F´(x) en el punto P= P=(X1,Y1)y repetir el procedimiento anterior a fin de generar la sucesión de aproximaciones siguiente:}
\includegraphics[width=0.6\textwidth]{imagen9.png}\\[1cm] 
\section*{DESCRIPCIÓN DEL PROBLEMA A RESOLVER}
\section*{1)Dada la ecuación diferencial y'=x2+y2, use el método de Euler para aproximar y(2.3) tomando como número de paso n = 3 para el proceso iterativo, si la condición inicial es y(2) = 0.5}
\section*{RESULTADOS}
\includegraphics[width=0.6\textwidth]{imagen10.png}\\[1cm] 
\section*{CONCLUSIÓN}
\section*{Al final retomando todos los métodos vistos en clase como: Regresión lineal, Newthon Raphson, euler, integración numérica, Euler, Heun, Ralston  y Runge Kutta logramos resolver un sencillo pero común problema de matemáticas como una ecuación diferencial para aproximar y.}
