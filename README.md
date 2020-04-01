# 天津大学本科生2020届毕业论文模版
## 来源
原始版本[tjuthesis](https://code.google.com/archive/p/tjuthesis/)
修改自[xnth97/TJUThesisLatexTemplate](https://github.com/xnth97/TJUThesisLatexTemplate)

## 更新日志
+ 调整了封面校徽的大小与位置使其与Word模版接近
+ 增加了独创性声明
+ 对字号进行了调整
+ 对于中文字体没有粗体的问题，宋体加粗和黑体加粗使用了思源字体
+ 增加了翻译的模板，翻译模板更适应IEEE等外文文献

## 预览
[天津大学本科生毕业论文](https://github.com/Checkmate986212/TJU-Thesis-2020/blob/master/TJU-thesis-template-2020/main.pdf)

## 环境
### macOS
[MacTeX](https://www.tug.org/mactex/) + [Texpad](https://www.texpad.com/)

### Windows
[TexLive](https://www.tug.org/texlive/)

## 基本用法
### 章节
```tex
\chapter{章}
\section{节}
\subsection{小节}
\subsubsection{小小节}
```

### 字体
```tex
宋体 \song
黑体 \hei
宋体加粗 \bfsong
黑体加粗 \bfhei

```
### 引用
#### BibTeX
```tex
@article{江泽民1989能源发展趋势及主要节能措施,
  title={能源发展趋势及主要节能措施},
  author={江泽民},
  journal={上海交通大学学报},
  volume={23},
  number={3},
  pages={1--16},
  year={1989},
  language={Chinese}
}
```

#### 上标
```tex
\citeup{江泽民1989能源发展趋势及主要节能措施}
```

#### 行内
```tex
\cite{江泽民2008对中国能源问题的思考}
```

### 图片
```tex
\begin{figure}[htbp!]
	\centering
	\includegraphics[width=0.5\textwidth]{figures/picture.png}
	\caption{图片说明}\label{图片标签}
	\vspace{-1em}
\end{figure}
```

### 表格
```tex
\begin{table}[htbp]
	\caption{表格说明}\label{表格标签}
	\vspace{0.5em}\centering\wuhao
	\begin{tabular}{ccccc}
		\toprule[1.5pt]
		第1列 & 第2列 & 第3列 \\
		\midrule[1pt]
		1.1 & 1.2 & 1.3 \\
		2.1 & 2.2 & 2.3 \\
		3.1 & 3.2 & 3.3 \\
		\bottomrule[1.5pt]
	\end{tabular}
	\vspace{\baselineskip}
\end{table}
```

### 公式
#### 行内公式
```tex
\(G=(V, E)\)
```
#### 行间公式
```tex
$$p_1(v_i, v_j)=\frac{1}{1+\exp(-\overrightarrow{u_i}^T\cdot\overrightarrow{u_j})}$$
```
#### 标号公式
```tex
\begin{align}
	p_2(v_j\mid v_i)=\frac{\exp({\overrightarrow{u_j}'}^T\cdot\overrightarrow{u_i})}{\sum_{k=1}^{|V|}\exp({\overrightarrow{u_k}'^T\cdot\overrightarrow{u_i})}}\label{p2}
\end{align}
```

### 伪代码
```tex
\begin{algorithm}[]
	\SetKwInOut{Input}{输入}
	\SetKwInOut{Output}{输出}
	\caption{\sc DeepWalk\((G, w, d, \gamma, t)\)}\label{DeepWalk}
	\Input{图\(G(V,E)\) \\
		窗大小\(w\) \\
		嵌入维度\(d\) \\
		每个节点游走数\(\gamma\) \\
		游走距离\(t\)
	}
	\Output{节点表征矩阵\(\Phi\in\mathbb{R}^{|V|\times d}\)
	}
	初始化：从\(\mathcal{U}^{|V|\times d}\)采样\(\Phi\) \\
	从\(V\)建立二叉树\(T\) \\
	\For{\(i=0\) to \(\gamma\)}{
		\(\mathcal{O}\) = Shuffle(\(V\)) \\
		\ForEach{\(v_i\in\mathcal{O}\)}{
			\(\mathcal{W}_{v_i}=RandomWalk(G, v_i, t)\) \\
			\(\textsc{SkipGram}(\Phi, \mathcal{W}_{v_i}, w)\)
		}
	}
\end{algorithm}
```

## 致谢

tjuthesis 的原作者们作出了前人栽树的不可磨灭的贡献
+ 张井 天津大学2010级管理与经济学部信息管理与信息系统专业硕士生
+ 余蓝涛 天津大学2008级精密仪器与光电子工程学院测控技术与仪器专业本科生
以及北京大学孟祥溪院士，膜。
