world engine is basically a **living graph** like this:

```
World
 ├ District
 │   ├ Tavern
 │   │   ├ Mira
 │   │   │   ├ Lipstick
 │   │   │   └ Memory
 │   │   └ Bed
 │   └ Market
 └ Quest
     ├ Event1
     └ Event2
```

Everything in the universe is just **nodes connected by relationships**.

The structure screams **graph database**.


Your model also solves **scope** automatically.

Example:

Room  
  contains Mira

means Mira is **in that room**.

Mira  
  contains lipstick

means lipstick is **in her inventory**.

The engine doesn’t need a separate "inventory system" or "location system".

Containment **is both**.
---