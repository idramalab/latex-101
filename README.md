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

-  Add a tilde before citations, unless the sentence starts with a citation:
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
As it can be seen, Notice that, It is worth noting, etc. --> 
  99% of the time you can just remove them altogether
```

- Use Oxford comma: 
```
x, y and z --> x, y, and z
```
- Do not mix present and past tense:
```
We started with this, then we select that (wrong!)
```

- Try to avoid passive forms as much as possible:
```
The epsilon parameter is set to 0.1 -> We set epsilon to 0.1
```

- Don't have single sub/subsections:
```
No Section 4.1 or 4.1.1 if you don't have 4.2/4.1.2
```

- If you are unsure about a statement, try to ask yourself "as opposed to what?": 
```
It is interesting to observe that blah blah --> 
  As opposed to not being interesting? 
  If it wasn't interesting then you'd just not write it perhaps?
```

- Set your locale to US English; never use British English spelling
```
Sorry British/Australian friends :-)
```
- Always use an editor that has an integrated spellchecker

- Do not push text you haven't proof-read, unless extremely urgent


## Bibliography
- Remove useless fields from the bib file:
```
E.g., publisher, city, abstract, etc.
```

- Shorten conference names:
```
Proceedings of the 17th ACM Internet Measurement Conference -> ACM IMC
(or even just IMC; just be consistent)
```

- If a paper on arXiv was also/later published in some conference/journal:
```
Cite the conference/journal version, not the arXiv version
```

- Correct way of citing arXiv preprints:
```
Arxiv preprint arXiv:12309482 -> arXiv:12309482 or arXiv preprint 12309482
```

- No duplicate bib entries with the same key

- It's great to use tools like Zotero, Mendeley, etc., or Google Scholar, DBLP, etc. to generate/export bib entries. However, you will still probably need to edit the overwhelming majority of the bib entries. Sorry :-)


## Plots
- Never generate plots in excel
- No pie charts
- Use sufficiently large fonts in your plots
- Make sure to export plots at high resolution (in a vector format); usually, pdf works best
- Use the `tight` option when exporting plots from matplotlib etc. to make sure there is no white space around the plot


## Git
- Commit latex changes incrementally (don’t wait to be “done”)
- Don’t use TeXStudio/TeXMaker. If you do, make sure to set the option that monitors external changes on disk; see [this](https://tex.stackexchange.com/questions/226355/texmaker-overwrites-file-that-was-externally-modified). (It will avoid overwriting others’ changes by mistake)
- Agree on line ending style (one sentence per line, one paragraph per line) up front. Don’t reformat the updated TeX to break after 80 chars (will cause *all* possible conflicts)
- Make sure everyone can compile what you commit (e.g., if you're using Overleaf, it might still compile so make sure there are *no LaTeX errors*)
- Do not add your code/large data files in the same repo as the latex repo. Latex repo should have only latex, plots, and notes
- Make sure to not push intermediate latex files in the repo (like .log .aux etc). You can do this by adding an appropriate .gitignore file
