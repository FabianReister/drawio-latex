# drawio-latex
LaTeX package to include draw.io (diagrams.net) diagrams without having to manually export them.

## Dependencies

This package requires **draw.io desktop** to be installed. For installation instructions please read https://github.com/jgraph/drawio-desktop/releases .

Required LaTeX dependencies (also listed in drawio.sty):
 - [filemod] will check if source file *.drawio is newer than the produced *.pdf artifact and will trigger conversion.
 - [write18] conversion is done through the drawio command line interface. Therefore, ensure that the 'shell-escape' option is set. 

## Configuration

 - [**cache**|nocache] if disabled, conversions are always be executed

bold = default

## Installation
Currently, this package is not available through CTAN. Therefore, just download *drawio.sty* and place it next to your root tex file.

## Usage

Add the following to your LaTeX header

    \usepackage[]{drawio}


Then, whereever you want to include your diagram, use **\includedrawio** instead of **\includegraphics**. **\includedrawio** is just a wrapper for **\includegraphics**. It will convert a drawio diagram to a pdf file (vector graphics)  

    \begin{figure}[ht]
     \centering
     \includedrawio[width=0.7\textwidth]{Figures/path/to/drawio/diagram/without/extension}
     \caption{Some caption}
     \label{fig:mylabel}
    \end{figure}
    
## Acknowledgement
 
The research leading to these results has received funding from the Carl Zeiss Foundation.

The research was performed at the Institute for Anthropomatics and Robotics - Intelligent Process Automation and Robotics Lab (IAR-IPR), Karlsruhe Institute of Technology (KIT).
