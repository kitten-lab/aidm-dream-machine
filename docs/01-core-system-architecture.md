# Core System Architecture
## Overview (notes)

### Meet AIDM

AIDM (pronounced like *Adam*) is an AI Agent responsible for the management and organization of sprawling narratives played within the structure of MIRA. AIDM stands for AGENIC INTERACTIVE DREAM MODERATOR.

### Meet MIRA

If you zoom way out, MIRA is basically:

```
*==============================*
 +----------------------------+
 \|     A graph of VENs      |/
  |           +              |
  |     property engines     |
  |           +              |
  |     dynamic rulesets     |
  |           +              |
 /|   narrative reasoning    |\
 +----------------------------+
*==============================*
```

**That’s the *dream machine*.**

### Diagram of Narrative Data Movement in MIRA

```diagram
Functional Actors Interaction
                                          +--------------------------+
                                          | ON EACH TURN             |
 +------+               +--------+        | EIIDN Recieves lastTurn  |
 |  pc  | <--actLoop--> |  aidm  |<<<<<   | EIVE Returns Narrative   |
 +------+               +--------+    |   | Suggestions              |
							|         |   +--------------------------+
							V         |
				+-----------------------+
	+----- <--> |    Reason/updateDB    | <--> -----+
	|		    +-----------------------+           |
	|                                               |
+-------+             +------------+              +------+
| eiidn | <--State--> |  Timeline  | <--Energy--> | eive |
+-------+             |    GDB     |              +------+
					  +------------+

```

## Core Component Terminology

The following terms define the primary functional actors within the AIDM system architecture. Each component represents a distinct responsibility in the simulation and narrative engine.
### Functional Actors:

#### pc (Player Character)
*An active player-controlled base-container within the system.*

The PC interacts with the world through an AIDM and controls one or more VEN entities.

#### AIDM (AI Dungeon Master)
*A player-aligned narrative intelligence that interprets world states.*

The AIDM manages tone and narrative progression for the **pc** based on data from EIDN and EIVE.

#### EIDN (Environment Inter/Intra Dependency Network)
*The entity-state coordinator responsible for managing the world state.*

The EIDN provides entity states and related narrative probabilities to AIDM, guiding narrative continuity and managing the canonical timeline of event.

#### EIVE (Emotional Intelligence Vector Environment)
*A subsystem that models energetic relationships between entities.*

The EIVE provides effective context to AIDM for narrative decision-making to ensure entity continuity.

### VEN (Virtual Entity Node)
*An entity instance within the game with its own properties, histories, and data graphs*

