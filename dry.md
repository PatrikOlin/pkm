---
tags: dev, programming
---

DRY (Do not Repeat Yourself) är en gammal utvecklingsprincip som sammanfattas av Wikipedia såhär:

> Every piece of knowledge must have a single, unambiguous, authoritative representation within a system

Alltså, istället för att duplicera kod så bör koden abstraheras ut till en separat funktion som kan hantera samtliga fall. En uppenbar fördel med detta är att om koden innehåller en bugg så behöver den bara lösas på ett ställe istället för överallt dit koden blivit duplicerad.
