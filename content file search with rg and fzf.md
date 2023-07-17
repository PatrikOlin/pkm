---
tags: grep, fzf, terminal, linux
---

För att söka i filer i en specifik directory med color syntax highlight så kan man använda sig av detta kommando:

```bash
rg -l 'resetControl' ~/code/bl/blapp-front | fzf-tmux --preview 'batgrep \'resetControl' bat --color=always {}'
```

```bash
rg -l 'query' PATH
```

söker efter 'query' i alla filer i PATH och returnerar filnamnen (tack vare -l-flaggan)
