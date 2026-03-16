# Entity Data Table

**Common Fields**

| `field name`          | `value`      | `description`                                                                                                            | `Type`        |
| --------------------- | ------------ | ------------------------------------------------------------------------------------------------------------------------ | ------------- |
| `ID`                  | `K_ID`       | `The core ID for the primary entity`                                                                                     | `Gen Code`    |
| `Is_Root_Entity`      | `K_root`     | `Entity is the top class of its chain, I.E. Human is K_root=True`                                                        | `Boolean`     |
| `Multi_Instance`      | `K_canVen`   | `Copies of the entity can be made, I.E. soliders or clones of entities`                                                  | `Boolean`     |
| `Can_Generate`        | `K_venGen`   | `The entity can birth new entities which are not itself. I.E. Hybrid instancing (new patterns) or birthing children`     | `Boolean`     |
| `Name`                | `e_Name`     | `The name of the entity`                                                                                                 | `Text`        |
| `Type`                | `e_Type`     | `The entity type, i.e. Place or Concept`                                                                                 | `Multiselect` |
| `Properties`          | `e_Proper`   | `Custom properties and attributes`<br> - can-generate<br> - can-multi-instance<br> - can-generate<br> - can-change<br> - | `Multiselect` |
| `Instances`           | `ven_Allot`  | `The number of the entity present in the system and usable`                                                              | `Numeric`     |
| `Available_Instances` | `ven_Avail`  | `Total number of instances available for use in narratives (unassigned)`                                                 | `Numeric`     |
| `Pulled_Instances`    | `ven_Pulled` | `Total number of instances actively involved in a narrative`                                                             | `Numeric`     |
**Instance (list Per Instance)**

| `field name`           | `value`        | `description`                                                                                                        | `Type`          |
| ---------------------- | -------------- | -------------------------------------------------------------------------------------------------------------------- | --------------- |
| `Instance_ID`          | `ven_ID`       | `The core ID for the primary entity`                                                                                 | `Gen Code`      |
| `Sub_Instance`         | `ven_canVen`   | `Copies of the instance itself can be made, I.E. a class of solider or clones of one specific clone`                 | `Boolean`       |
| `Can_Generate`         | `ven_canGen`   | `The entity can birth new entities which are not itself. I.E. Hybrid instancing (new patterns) or birthing children` | `Boolean`       |
| `Instance_Name`        | `ven_Name`     | `The name of the entity`                                                                                             | `Text`          |
| `Relationships`        | `ven_Rel`      | `Links to other entities`                                                                                            | `Related Iems`  |
| `Contain_Path`         | `ven_inChain`  | Breadcrumb path                                                                                                      |                 |
| `Contains`             |                | `can be list (ie: fish, wallet, a stray hair) or breadcrumb (ie. self/wallet/pocket universe/house/self)`            |                 |
| `Temporal_Position`    | `ven_Loc`      | `The position of this entity in time, see Temporal Table`                                                            | `Gen Code`      |
| `Timeline_Instance(s)` | `ven_(s)`      | `The timeline instances the entity is presently rendered in`                                                         | `Related Items` |
| `Relationships`        | `ven_relateTo` | `Links to other entities`                                                                                            | `Related items` |
| `Generated_From`       | `ven_Parent`   | `If produced from another Entity, which entity was the generator`                                                    |                 |
| `Generated_To`         | `ven_Child`    | `If produced another Entity, what did it produce`                                                                    |                 |

```
entities may contain entities 
enities may have more than one type (sub-table)
entities may have more than 1 available instances in the system
	each instance is managed as its own unique entity branch
```

## Table: EN-TYPE

| `ENTITY TYPE` | `DESCRIPTION`                     | `EXAMPLE`                      | `LABEL or SUB-TABLE` |
| ------------- | --------------------------------- | ------------------------------ | -------------------- |
| Place         | A spacial environment or location | Tavern, temple, forest, city   |                      |
| Event         | A time-bound occurance            | Festival, ritual, an arguement |                      |
| Thing         | A physical object                 | Sword, bottle, book, bag       |                      |
| Character     | An autonomous agent               | Mira, wolf                     |                      |
| Concept       | An abstract narrative force       | God, Destiny, rebellion        |                      |
| Symbol        | A non-material representation     | Sigil, patterns, meanings      |                      |
