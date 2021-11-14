# LaTeX Guide for new iDRAMA students/collaborators

## Formatting (Tables/Figures)

- In Tables, right-align columns with numbers:
```
\begin{tabular}{lr}
Male & 135\\
Female & 132\\
... & ...\\
\end{tabular}
```

- Figures and tables should be at the top of the page &ndash; use [t]:
```
\begin{table}[t]
...
\end{table}
\begin{figure}[t]
...
\end{figure}
```

- Figure captions always go below the figure; table caption could go top or bottom:
```
\begin{figure}           \begin{table}
\includegraphics{...}    \caption{...}
\caption{...}                ...
\end{figure}             \end{table} 
```

- Tables should have minimal lines, and, if possible, use the booktabs package:
```
\begin{table}
\begin{tabular}{lr}
\toprule
Sex & Number\\
\midrule
Male & 135\\
... & ...\\
\bottomrule
\end{tabular}
\caption{...}
\end{table}
```

## Formatting (Numbers)

- Use thousand comma separator in text, figures, tables, etc.
```
10,123 (not 10123)
```

- Consider using k or M:
```
10k, 1M (instead of 10,000 and 1,000,000)
```

- Use decimal precision sparingly:
```
We find 147.37 things --> We find 147 things (unless the .37 is important)
We find 147.3715 things --> We find 147.37 (unlikely you need more than 2 digit precision)
```

## Formatting (Text)

- For quotations, use:
``` 
``text'' and `text' (not "text" or 'text')
```

- Dashes: double dash (&ndash;) and long dash (&mdash;) are written, respectively:
```
-- and ---
```

- And, use them as follows:
```
Blah blah -- blah blah
Blah blah---blah blah
```

- The footnote mark goes after the period if at the end of a sentence
```
blah blah blah.\footnote{fff}
```

- Commas and periods go inside the quotes:
```
``blah.'' ``blah,''
```

- Never use contracted forms for verbs:
```
It’s -> it is, can’t -> cannot
```

- Correct spellings:
```
i.e.,
e.g.,
Internet
Web
```

- Subordinate clauses starting with "which" should have a comma before
```
blah blah, which
```

## Formatting (Citations)

-  Add a tilde before citation, unless the sentence starts with a citation:
```
Blah et al.~\cite{X}
```

- But avoid starting a sentence with a citation, unless using a bibliography format that renders as:
```
\cite{X} --> (Blah et al., 2019)
```

## Writing 

- Avoid verbose expressions like:
``` 
As it can be seen, Notice that, It is worth noting, etc. -> 99% of the times you can just remove them altogether
```

- Use Oxford comma: 
```
x, y and z --> x, y, and z
```
- Always use an editor that has integrated spellcheck.
```
Do not push text you haven't proofread unless extremely urgent.
```

- Do not mix present and past tense.
```
We started with this, then we select that
```

- Try to avoid passive forms as much as possible:
```
The epsilon parameter is set to 0.1 -> We set epsilon to 0.1

