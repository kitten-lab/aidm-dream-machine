# Ven isContainer System

There is one structural property that ensures the world can be made:
`isContainer`

Which means the world graph is simply:
`VEN → contains → VEN`

**That’s it.**

## The Container Logic Is the Secret Sauce

All things contain other things:

> room contains bed  
> quest contains event  
> mira contains lipstick

Notice something elegant here.
We are using the **same structural relationship** for:

|Domain|Relationship|
|---|---|
|space|room → bed|
|narrative|quest → event|
|inventory|mira → lipstick|
|world structure|district → tavern|

So containment becomes a **universal relationship**.

Producing complex entity types become trivial:
### A room
	ven.Room_221  
	  prop: isContainer=true  
	  contains:  
	      ven.Bed_03  
	      ven.Table_02  
	      ven.Mira_01

### Mira
	ven.Mira_01  
	  prop: isCharacter=true  
	  contains:  
	      ven.Lipstick_04  
	      ven.MemoryGraph

### A quest
	ven.Quest_VampireNight  
	  prop: isContainer=true  
	  contains:  
	      ven.Event_Intro  
	      ven.Event_Hunt  
	      ven.Event_Reveal

### A world
	ven.World_Skyline  
	  prop: isContainer=true  
	  contains:  
	      ven.District_A  
	      ven.District_B  
	      ven.District_C


---

