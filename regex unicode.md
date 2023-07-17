---
tags: dev, regex
---

Istället för att använda `=a-zA-Z=` för att matcha alfanumeriska tecken i regex kan man använda flaggan `=\p=` eller `=\P=`. Till exempel, för att matcha vilken bokstav som helst från nästan vilket språk som helst `=\p{L}\p{M}=` eller `=\p{Letter}\p{Mark}=`

`=Letter=`-kategorin inkluderar alla bokstäver från nästan alla språk, men inga tecken såsom '<', '>', '+' eller '$'. `=Mark=`-kategorin innehåller 'combining marks'. I Unicode kan en bokstav som 'ö' t.ex vara en eller flera kombinerade code point(s), så för att vara säker på att få med bokstäverna oavsett hur dom är kodade bör både `=Letter=` och `=Mark=` användas i kombination.

[Unicode character category](http://www.regular-expressions.info/unicode.html#category)

### Browser support
[Browser support](https://caniuse.com/mdn-javascript_builtins_regexp_property_escapes) för detta är bra, det är egentligen bara IE som är problemet.
