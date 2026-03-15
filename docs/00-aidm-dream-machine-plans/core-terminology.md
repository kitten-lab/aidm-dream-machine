# Core Component Terminology

The following terms define the primary functional actors within the AIDM system architecture. Each component represents a distinct responsibility in the simulation and narrative engine.
#### Functional Actors:

> [!success] pc (Player Character)
> *An active player-controlled base-container within the system.*
> 
> The **pc** interacts with the world through an **aidm** and controls one or more **ven** entities.

> [!success] aidm (AI Dungeon Master)
> *A player-aligned narrative intelligence that interprets world states.*
> 
> The **aidm** manages tone and narrative progression for the **pc** based on data from **eiidn** and **eive**.

> [!SUCCESS] eiidn (Environment Inter/Intra Dependency Network)
> *The entity-state coordinator responsible for managing the world state.*
> 
> The **eiidn** provides entity states and related narrative probabilities to **aidm**, guiding narrative continuity and managing the canonical timeline of event.

> [!SUCCESS] eive (Emotional Intelligence Vector Environment)
> A subsystem that models energetic relationships between entities.
> 
> The **eive** provides effective context to **aidm** for narrative decision-making to ensure entity continuity.

> [!success] ven (Virtual Entity Node)
> An entity instance within the game with its own properties, histories, and data graphs

#### Diagram

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
