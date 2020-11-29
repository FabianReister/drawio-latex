# drawio-latex
LaTeX package to include draw.io (diagrams.net) diagrams without having to manually export them.

## Dependencies

This package requires **draw.io desktop** to be installed. For installation instructions please read https://github.com/jgraph/drawio-desktop/releases .

Required LaTeX dependencies (also listed in drawio.sty):
 - [filemod] will check if source file *.drawio is newer than the produced *.pdf artifact and will trigger conversion.
 - [write18] conversion is done through the drawio command line interface. Therefore, ensure that the 'shell-escape' option is set. 

## Configuration

 - [**cache**|nocache] if disabled, conversions are always executed

bold = default

## Installation
Currently, this package is not available through CTAN. Therefore, just download *drawio.sty* and place it next to your root tex file.

## Usage

Add the following to your LaTeX header

    \usepackage[]{drawio}


Then, whereever you want to include your diagram, use **\includedrawio** instead of **\includegraphics**. **\includedrawio** is just a wrapper for **\includegraphics**. It will convert a drawio diagram to a pdf file (vector graphics)  

\begin{figure}[H]
 \centering
 \includedrawio[width=0.7\textwidth]{Figures/own/concept/architecture-option-critic-style-simplified-presentation}
 \caption{The hierarchy of the options and the policy over options (adopted from~\cite{bacon2017option}).}
 \label{fig:methods:options-simplified}
\end{figure}
