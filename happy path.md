---
tags: dev, programming
---

"Happy path" är ett begrepp som används inom mjukvarutveckling för att beskriva
det förväntade och optimala flödet. Det är det naiva flödet som borde följas
förutsatt att ingenting går fel. Till exempel, happy path för att validera ett
kreditkort är det case där alla siffror stämmer och passerar valideringen utan
problem, datum stämmer, cvv stämmer osv. En helt problemlös process, med andra
ord.

Happy path kallas också ibland "happy day", "sunny day" eller "golden path". Det
verkar inte finnas något överenskommet namn på motsatsen; "sad path", "bad
path", "exception path" och "unhappy path" är bara några exempel.


### Happy path i Go
Idiomatisk Go skrivs på ett sätt som oftast har sin happy path på första
nivån av indentation och alla sad paths på den andra nivån av indentation.

Exempel:
```go
func main() {
    // happy path
    x, err := doThingGetX()
    if err != nil {
        // sad path
        panic(err)
    }
}
```
