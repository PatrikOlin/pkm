---
tags: dev, web
---

Punycode är en representation av Unicode med det mer begränsade ASCII-teckenkodningen som används för host-namn på internet. Med hjälp av punycode så kodas host-namn som innehåller Unicode-karaktärer om till ett subset av ASCII som kallas [[letters digits hyphens (LDH)]]. _München_ blir till exempel kodat som _Mnchen-3ya_.

DNS stödjer tekniskt sätt Unicode i domännamn men DNS-standarden rekommenderar att LDH används för host-namn.
