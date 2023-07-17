---
tags: ai, machine_learning, neural_networks, dev
---

Rectified linear activation function (ReLU) är en enkel men effektiv icke-linjär activation function som ofta används i neurala nätverk. Den kan beskrivas som y=x, avklippt vid 0 på den negativa sidan. Alltså; om x är lika med eller mindre än 0 så är y = 0, annars så är y = x. ReLU är väldigt nära att vara en linjär activation function, men den lilla icke-linjäritet den introducerar är mycket effektiv.

Exempelimplementation av ReLU i python
```python
inputs = [0, 2, -1, 3.3, -2.7, 1.1, -100]

output = []
for i in inputs:
    if i > 0:
        output.append(i)
    else:
        output.append(0)

print(output)

>>>
[0, 2, 0, 3.3, 0, 1.1, 0]
```
