---
tags: dev, programming
---

Man pratar ofta om [[dry]] som är en gammal utvecklingsprincip som säger att kod inte ska dupliceras. AHA (Avoid Hasty Abstractions) är en princip som som i kontrast till DRY menar att duplicerad kod inte alltid är av ondo. Ett enkelt sätt att beskriva AHA är helt enkelt:

> prefer duplication over the wrong abstraction

Det vill säga, det finns en fara med att abstrahera kod för tidigt. Det är
bättre med lite duplicerad kod än en avancerad och svår abstraktion. Faran med
att abstrahera kod för tidigt är att du lyfter ut den duplicerade koden till en
egen funktion och sedan märker du att den funktionen passar nästan perfekt för
ett liknande fall. Så du lägger till en parameter och lägger till lite logik för
att hantera dom olika case som uppstår. Sedan kommer nästa utvecklare, ser
metoden och lägger till ännu ett case. Helt plötsligt så har abstraktionen
blivit rätt avancerad och beter sig på olika sätt i olika case, vilket gör den
svårare att hantera och resonera om.

[the wrong abstraction](https://sandimetz.com/blog/2016/1/20/the-wrong-abstraction)
[AHA-programming](https://kentcdodds.com/blog/aha-programming)
