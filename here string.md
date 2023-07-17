---
tags: linux, terminal, sed
---

Here-string är en förenklad version av heredoc (here-document) som kan användas
för att enkelt redirecta en sträng in i ett kommando. För att skapa en here-string används operatorn ~<<<~ mellan kommandot och strängen. Det vill säga:

```bash
COMMAND <<< $VAR
```

I det här fallet så expanderas variablen ~$VAR~ och den resulterande
strängen matas in till ~COMMAND~.

Kan till exempel användas tillsammans med sed som förväntar sig en fil:

```bash
t=$(git describe --tags)
tag=$(sed 's/v//' <<< "$t")
```

Hämta senaste tag från git, mata in ~$t~ i sed för att plocka bort det
inledande v:et i versions-taggen.
