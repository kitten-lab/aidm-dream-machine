# AIDM & The Dream Machine
This is the working space for the following concept:
  An MUD-style text-based RPG environment utilizing AI assistance.
  Continuity and emergence of story generation is pivitol.
  Capacity for immersive collabrative world building.

# What is **the Dream Machine?**

Breakdown of the Dream Engine concept, how Entities and Properties create the world.

# What is AIDM

What is an AI assisted DM and why would we even want one?

# Design Philosophy

forest metaphors, narrative story consideration, player agency, stories which feed themselves more stories

why this is different then scripted games

# 01.1: Core:  Entity System (k/ven)

Everything in the world is an [[Entity]].
[[Entity]] objects can represent:
- characters
- objects
- locations
- concepts
- symbols
- events
- narratives

Some core properties of every [[Entity]]
#prop_worldScale
#prop_isContainer 
#prop_isMobile
#prop_narrativeGravity


# Container System (prop_isContainer = True)

Containment defines and [[Entity]] space and structure.

[[Container]]s determine:
- spacial relationships
- simulation scope
- multiplayer shared environment handling
- narrative propagation
- what exists where inside of what

Every [[Entity]] in the world may contain other [[Entity]] instances inside of itself.
For example:

```
Planet 
	Contains -> Locations
Location
	Contains -> Characters
Character
	Contains -> Inventory
```

This is the world topology.

# Properties System (prop_ and prop[Name]_ )

Properties define what an [[Entity]] or [[Dynamic]] can do. These are its **capacities and traits**.

Example groups:
```
propMobility_* 
propTemportal_*
propNarrative_*
propObj_*
```

Each group contains properties related to that attribute, for example #propMobility_isCarryable is part of the #propMobility_* property group, becoming available when the master property #prop_isMobile is set to `TRUE`

# Dynamic Reasoning System

The threads that weave between the Entities.

# Narrative System

Systems that help determine the **story importance and simulation priority**.

#propNarrative_gravity 
#propNarrative_impactContainer
#propNarrative_decayRate

This is the story physics layer.

# Temporal System (Timeline Architecture)

Handles:
- branching timelines
- time travel
- timeline knowledge
- casual events

## Key concepts:
- Timeline branches
- Proximity ranges
- Knowledge capacity for other timelines
- Timeline travel and modification properties
- Time behavior properties per [[Entity]]

#propTemporal_branchID
#propTemporal_proximityRange
#propTemporal_canKnow
#propTemporal_canTravel

### Ven Specific calls:
#venTemporal_position

# Social Spaces System

- [ ] add social spaces can be destroyed in timelines

Containers where **multiplayer timelines interact**.

These spaces can allow:
- cross-timeline interaction
- rumor exchange
- timeline discovery

Example:
#propTemporal_isSocial set to `TRUE`
Taverns, marketplaces, guild halls

# Event System

Tracks what actually happens in the world.

Events record:
- participants
- location
- timeline
- related dynamics
- narrative weight

Events feed into narrative gravity.

# Planners
EIDN(e) - Environmental Intellegence Data(base) Network Entity

- Graph/node based database managed by AI entity "EIDN"
- User can interface with EIDN in casual conversation language to manage the world and develop new locations
- EIDN enters and manages the information in relational database

Need to plan DB structures to suppose multidimensional and non-linear realities.

AIDM - Artificial Intellegence Dungeon Master (Dream Master)

- Narrative management and story progression managed by AI entity "AIDM"
- AIDM manages the storyline, ensures continuity with EIDN and updated worlds-DB to ensure no narrative-drift

Need to plan multi-agent concepts for Party Members
