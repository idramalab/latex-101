# LaTeX, Git, Etc.
## Guide for new iDRAMA students and collaborators

### Formatting

1. In Tables, always right-align columns with numbers
```
\begin{tabular}{lr}
Male & 135\\
Female & 132\\
\end{tabular}
```

2. Unless you have a valid reason, figures and tables should be at the top of the page [t]
```
\begin{table}[t]
...
\end{table}
\begin{figure}[t]
...
\end{figure}
```

3. Always Use thousand comma separator in text, figures, tables, etc.
```
10,123 (not 10123)
```

4. Consider using k or M as much as possible
```
10k, 1M (instead of 10,000 and 1,000,000)
```

5. For quoted text use
``` 
``text'' and `text' (not "text" or 'text')
```

6. Dashes: double dash &ndash; and long dash &mdash; are, respectively:
```
-- and ---
```

7. Use dashes as follows:
```
Blah blah -- blah blah
Blah blah---blah blah
```

8. Always add a tilde before citation, unless the sentence starts with a citation:
```
Blah et al.~\cite{X}
```

9. Avoid starting a sentence with a citation, unless using a bibliography format that renders as
```
\cite{X} --> (Blah et al., 2019)
```

10. The footnote mark goes after the period if at the end of a sentence
```
blah blah blah.\footnote{fff}
```

11. Commas and periods go inside quotes
```
``blah.'' ``blah,''
```

12. Never use verb contracted forms
```
It’s -> it is, can’t -> cannot
```

13. Correct spellings:
```
i.e.,
e.g.,
Internet
Web
```

14. Subordinate clauses starting with "which" should have a comma before
```
blah blah, which
```

