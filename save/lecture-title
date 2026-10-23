\documentclass{article}

%Кодировки и языки
\usepackage[T2A]{fontenc}
\usepackage[utf8]{inputenc}
\usepackage[english, russian]{babel}

%Математика
\usepackage{amsmath, amsthm, amssymb, mathtools}
\usepackage{icomma}

%Геометрия страницы
\usepackage[top=15mm, bottom=20mm, left=20mm, right=20mm]{geometry}

%Колонтитулы
\usepackage{fancyhdr}
\pagestyle{fancy}
\fancyhf{}
\fancyhead[L]{ Лекция №$3 } %номер лекции
\fancyhead[R]{ $4 } %название
\fancyfoot[C]{\small Страница \thepage}
\renewcommand{\headrulewidth}{0.3pt}
\renewcommand{\footrulewidth}{0pt}
%Цвета и графика
\usepackage[svgnames]{xcolor}
\usepackage{tikz}
\usepackage[many, skins, breakable]{tcolorbox}
\usepackage{graphicx}
\usepackage{varwidth}
\usepackage{indentfirst}
\usepackage{soulutf8}
\usepackage{hyperref}
\usepackage{cleveref}
\usepackage{multicol}
\usepackage{listings}
\usepackage{tikz-cd}
\usepackage{fancyvrb}
\usepackage{tempora}
\usepackage{newtxmath}
%Гиперссылки
\hypersetup{
    colorlinks = true,
    linkcolor  = DarkSlateBlue,
    citecolor  = DarkSlateGray,
    urlcolor   = DarkSlateBlue,
}
%Пользовательские команды
\newcommand{\deriv}[2]{\frac{\partial #1}{\partial #2}}
%Палитра
\definecolor{softbordeaux}{RGB}{140,50,50}
\definecolor{slateblue}{RGB}{112,128,144}
\definecolor{graphite}{RGB}{85,85,85}
\definecolor{warmgray}{RGB}{120,110,100}
%Общие настройки блоков
\tcbset{
    boxrule=0.6pt,
    arc=3pt,
    colback=white,
    before skip=14pt,
    after skip=14pt,
    fonttitle=\bfseries\large,
    colbacktitle=white,
    titlerule=0pt,
    left=10pt, right=10pt, top=8pt, bottom=8pt,
}
%Стили окружений
\newtcolorbox{theorembox}{
    colframe=softbordeaux!70!white,
    coltitle=softbordeaux,
    fonttitle=\bfseries\large,
    boxrule=1.1pt,
}
\newtcolorbox{definitionbox}{
    colframe=slateblue,
    colback=slateblue!5!white,
    coltitle=slateblue,
    fonttitle=\bfseries,
    borderline west={2pt}{0pt}{slateblue},
    boxrule=0pt,
    sharp corners,
    left=12pt,
}
\newtcolorbox{lemmabox}{
    colframe=warmgray,
    colback=warmgray!5!white,
    coltitle=warmgray,
    fonttitle=\bfseries,
    borderline west={2pt}{0pt}{warmgray},
    boxrule=0pt,
    sharp corners,
    left=12pt,
}
\newtcolorbox{consequencebox}{
    colframe=graphite!50!white,
    coltitle=graphite,
    fonttitle=\bfseries,
    boxrule=0.5pt,
}
\newtcolorbox{formulabox}[1][Формула]{
    colframe=graphite!30!white,
    colback=graphite!2!white,
    coltitle=graphite!70!black,
    fonttitle=\bfseries,
    title=#1,
    boxrule=0.5pt,
}
%Внутренние окружения amsthm
\theoremstyle{plain}
\newtheorem*{theorem}{\textbf{\large\color{softbordeaux}Теорема}}
\newtheorem*{lemma}{\textbf{\color{warmgray}Лемма}}
\newtheorem*{consequence}{\textbf{\color{graphite}Следствие}}
\theoremstyle{definition}
\newtheorem*{definition}{\textbf{\color{slateblue}Определение}}
%Нумерация уравнений
\renewcommand{\theequation}{\arabic{equation}}
%Отступы
\setlength{\parindent}{1.25cm}
\linespread{1.4}
%Подзаголовок с линией
\newcommand{\sectionline}[1]{%
  \vspace{40pt}
  \noindent
  \begin{tikzpicture}[baseline]
    \draw[line width=1.2pt, graphite!70] (0,0) -- (\textwidth,0) 
      node[midway, fill=white, inner sep=10pt, draw=graphite!70, line width=0.8pt, rounded corners=9pt] {\large\bfseries\color{black} #1};
    \fill[graphite!70] (0,0) circle (2.2pt);
    \fill[graphite!70] (\textwidth,0) circle (2.2pt);
  \end{tikzpicture}
  \vspace{18pt}
}
\newcommand{\customtitle}[3]{%
  \thispagestyle{empty}
  \null\vfill
  \begin{center}
    \begin{tikzpicture}
      % Нижний левый уголок
      \draw[line width=1.2pt, graphite!70] 
        (0,0) -- ++(0.7cm,0) 
        (0,0) -- ++(0,0.7cm);
      % Нижний правый уголок
      \draw[line width=1.2pt, graphite!70] 
        ({0.72\textwidth},0) -- ++(-0.7cm,0) 
        ({0.72\textwidth},0) -- ++(0,0.7cm);
      % Верхний левый уголок
      \draw[line width=1.2pt, graphite!70] 
        (0,4.8cm) -- ++(0.7cm,0) 
        (0,4.8cm) -- ++(0,-0.7cm);
      % Верхний правый уголок
      \draw[line width=1.2pt, graphite!70] 
        ({0.72\textwidth},4.8cm) -- ++(-0.7cm,0) 
        ({0.72\textwidth},4.8cm) -- ++(0,-0.7cm);
      % Текст по центру
      \node[text width=0.62\textwidth, align=center] 
        at ({0.36\textwidth},2.4cm) {
          {\large\color{graphite} #1}
          \\\[14pt]
          {\huge\bfseries\color{black} #2}
          \\\[10pt]
          {\color{softbordeaux}\rule{40pt}{1.4pt}}
          \\\[10pt]
          {\large\color{graphite!80} #3}
        };
    \end{tikzpicture}
  \end{center}
  \vfill\newpage
}
\begin{document}
\customtitle{ Лекция №$2 }{ $5 }{ $1 } %номер лекции, название, дата
\pagestyle{fancy}
$0
\end{document}
