---
tag: dev, programming, javascript
---

Ett _closure_ är en funktion som har tillgång till sitt [[lexical scope]]  även om den exekveras utanför det.

Exempel:
```js
function outerFunc() {
    let outerVar = 'Calling from outer scope';

    function innerFunc() {
        outerVar; // => 'Calling from outer scope';
    }

    return innerFunc;
}

function exec() {
    const myInnerFunc = outerFunc();
    myInnerFunc();
}

exec();
```

`innerFunc()` exekveras utanför sitt _lexical scope_ men har fortfarande
tillgång till `outerVar` från sitt _lexical scope_. Man kan säga att
`innerFunc()` 'closes over' variablen `outerVar` från sitt _lexical scope_, dvs
`innerFunc()` är ett _closure_.

En tumregel för att identifiera ett _closure_ är om du i en funktion ser en
variabel som inte definieras i den funktionen (eller i global scope), då är det
hög sannolikhet att funktionen är ett _closure_ som har med sig variablen från
sitt _lexical scope_

https://dmitripavlutin.com/simple-explanation-of-javascript-closures/
