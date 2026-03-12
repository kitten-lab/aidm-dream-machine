```
PROPERTY NAMING CONVENTION

prop_*              - root level property
prop_is(Property)*  - whether or not an entity has a property set
prop(Property)_*    - subgroup of properties for a propery

Can chain, for example:

propTemporal_canTimeTravel = True
	add a set of properties "TimeTravel"
	
	propTimeTravel_*
	
	i.e.
	
	propTimeTravel_mode
	propTimeTravel_duration
	propTimeTravel_triggerType
	propTimeTravek_range
	etc
```



