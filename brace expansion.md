---
tags: linux, terminal
---

Brace expansion är en funktion i Bash/ZSH (och delvis också i Fish) som kan vara ovärderlig för att undvika repetition.

Istället för att skriva:
``` bash
mv some_long_file_name.txt some_long_file_name.bak
```

Kan du helt enkelt göra:
``` bash
mv some_long_file_name.{txt,rs}
```

Fler exempel:
``` bash

# Brace expansion
echo x{Hello,World}x
$ echo xHellox xWorldx

# With an empty string
cp some_file{,.bak}
$ cp some_file some_file.bak

# In a path
mv x/{before,after}/asdf/file
$ mv x/before/asdf/file x/after/asdf/file

# Number range (number range funkar ej i fish)
rm d{01..20}/file
$ rm d01/file d02/file d03/file ...etc

# Multiple braces:
touch {a,b,c}.{rs,cpp}
$ touch a.rs a.cpp b.rs b.cpp c.rs c.cpp

# Nested braces
git add {main,x{1,2}}.rs
$ git add main.rs x1.rs x2.rs

# Letter range
cat {a..f}.txt
$ cat a.txt b.txt c.txt d.txt e.txt f.txt
```
