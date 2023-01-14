---
{"dg-publish":true,"dg-home":false,"permalink":"/2-general/general-notes/la-te-x/la-te-x-how-to-format-a-pharagraph/","dgPassFrontmatter":true}
---


```
## 指定文档类型
\documentclass[12pt]{article}

# 前言（Preamble)

## 宏包
\usepackage{amsmath}
\usepackage[margin=2.5cm]{geometry}
\usepackage{graphix}

# 题目区
\title{Insert title here}
\author{Insert author here}
\date{Insert date here}

# 正文
\begin{document}
\maketitle # 显示标题

\textbf{*arg} # 加粗字体
\textit{*arg} # 斜体
\underline{*arg} # 下划线

\section{章节名} # 添加章节
在章节下添加内容


\subsection{子章节名}
子章节内容

\subsubsection{子章节的子章节}
.........

\begin{figure}
\center    # 居中
\includegraphics[width=0.5\textwidth]{图片名不带后缀} # 添加图片
\caption{添加注释}
\end{figure}


## 无序列表
\being{itemize}
\item 列表项1
\item 列表项2
\item 列表项3
\end{itemize}

## 有序列表
\being{enumerate}
\item 列表项1
\item 列表项2
\item 列表项3
\end{enumerate}

## 行内公式
$添加公式$

## 多行公式
\begin{equation}

\begin{equation}

or

\[

\]


## 表格
\begin{table}
\begin{tabular}{|l|c|r|} # 左对齐 居中 右对齐 |:加边框
\center
单元格1 & 单元格2 & 单元格3 \\
\hline # 横向边框
单元格4 & 单元格5 & 单元格6 \\
\hline
单元格7 & 单元格8 & 单元格9 
\hline
\end{tabular}
\caption{输入表格标题}
\end{table}



\begin{align*}
\end{align*}

\end{document}




