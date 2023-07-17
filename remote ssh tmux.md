---
tags: linux, devops, tmux
---

För att kunna ansluta till en remote tmux-session på en server i dina lokala tmux-session kör

```bash
ssh <user@hostname> -t tmux a
```

För att kunna skicka kommandon till den inre tmux-sessionen, lägg till detta i dina lokala tmux-conf:

```sh
bind-key -n C-a send-keys C-b
```

Den bindingen gör att C-a i din yttre session skickar default-prefix (C-b) till din inre session.

Hett tips är att skapa upp ett enkelt alias:

```sh
alias servername="ssh <user@hostname> -t tmux a"
```

Då är det sen väldigt enkelt att bara ansluta med `servername` och sedan bara
köra `C-a + d` när du är klar för att detacha från sessionen och disconnecta
från SSH. Tmux-sessionen kommer fortsätta köras på servern så att du sedan kan
ansluta till samma session igen.
