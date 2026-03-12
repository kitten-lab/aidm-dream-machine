# Temporal Timestamps & Version Tracking


## Every Entity has a Temporal Location State
##### PLANS FOR MULTIPLAYER TIMELINE CONVERGENCE AND DIVERGENCE MANAGEMENT
---
```
#K-ID = rootEntity key ID
#venID = instance of RootEntity (K)
```

K-ID may be assigned to any `Entity` by marking #prop_isRootEntity = `True`

Every `RootEntity` produces at least `1 VEN` of itself.
```
KID = RootEntity "Sword" K1123
            |
            V
ven = InstanceEntity "Sword 21" ven1123V21

if KID = "Tree" K920
            |
            V
ven = "Tree 31" ven920V31

if ven920V31 becomes a new RootEntity "Oak Tree"
            |
            V
KID = K:920_V31 "Oak Tree" which can now produce
            |
            V
ven = "Oak Tree 9" ven:920/31_V9    


pc:kitten-lab/ven:0/808113 - Calls to a player loading a ven instance of their character which has a rootEntity of K0 "Player" and the Character Entity ven808113 "Remir Roadian".


#propTemporal_venID = venID
```

An `Entity` marked #prop_isPC removes or dampens property constraints around the data for that `Entity`.

```
P[player_number]C[character_number]
For example, Greg is P369 playing character C5

Start string temporal
P369/C5/
```


This has the most narrative gravity. The STATE of the 

CONTAINER STATE 1 = 
CONTAINER STATE 2



t-numeric contains:
	propTemporal_state:
	
	
Example:
K-ID of "Sword" is K1123

- how are we handling player characters? only creation, or can become an NPC if #prop_canPlay is `True`?

```

## A Branch
Generate for and `Entity` when #K-ID #propWorld_isRoot is `True`

Ontological level - Star Wars vs Earth

```
A-BRANCH sets conditions of ontology and K-ID start-propogation.
```
## B Branch
Narrative Beginning - War vs Race-to-Space
Start B brand as number. Iterate versions of global change via . system.
```
B Branch start # is 20 (Global War/Unity Start)
            	|
            	|
  ----------------------------
  |             |            |
20.1           20.2         20.3

The war takes place in time and 3 outcomes occur:
B20.1 - The War Lost, World Ends.
B20.2 - The War was Won, Good Guys prosper
B20.3 - The War continues
```


# C Branch
Wide-area player-driven divergence - Steve Runs for President
`Shares regional events`
# D Branch



```
A/B/C/D/E/...etc - Per CONTAINER in decent

World > Country > State > City > Neighboorhood > Building > Room > Grid Location

Each is a temporal code representing the STATE of the Entities held within it.
So if World contains Country One, Two, Three and Four

```

### What is a temporal state?

A temporal state is the shared narrative state of any given Entity
- #prop_isDestroyed 