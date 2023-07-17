---
tags: dev, programming, javascript
---

I javascript/typescript kan man använda destructuring i console.log() för att
enkelt hålla koll på vilken variabel det är som man loggar.

Exempel:

Vi har en variabel, `debounce`, som vi vill logga. På klassiskt vis skulle man
göra något i den här stilen:

```typescript
const debounce = 300
console.log('debounce', debounce)
```

och då få ut `debounce 300` i konsolen. Med destructuring kan man göra såhär istället:

```typescript
const debounce = 300
console.log({ debounce })
```

och få ut `{ debounce: 300 }` i konsolen, dvs man får med både värdet och variabelnamnet.
