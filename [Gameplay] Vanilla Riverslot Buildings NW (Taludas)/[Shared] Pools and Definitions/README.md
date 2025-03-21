# Shared Pools and Definitions

Shared effect target pools, New World hotel needs and other definitions to use as sub-mod.

The modloader will always load the latest version.
You do not need to update your sub-mod if you don't need the new features yourself.

## Do not modify contents of this mod

Making changes may break mods and cause compatibility issues.

Go to [github.com/anno-mods/shared-resources](https://github.com/anno-mods/shared-resources) and create an issue to make change suggestions.

## How to Use

Copy the `[Shared] Pools and Definitions` into your mod and add `shared-pools-and-definitions` to your `LoadAfterIds`.

### Pools

Generic approach:

```xml
<!-- add to pools having sand mine -->
<ModOp Type="add"
  Path="//ItemEffectTargetPool/EffectTargetGUIDs[Item/GUID='1010560']">
  <Item>
    <GUID>1500010708</GUID> <!-- NW Sand Pit -->
  </Item>
</ModOp>
```

Fast approach:
```xml
<!-- add to sand pool -->
<ModOp Type="add" GUID="1500010714"
  Path="/Values/ItemEffectTargetPool/EffectTargetGUIDs">
  <Item>
    <GUID>1500010708</GUID> <!-- NW Sand Pit -->
  </Item>
</ModOp>
```

### Hotel Needs

```xml
<!-- copy needs from vanilla/NW Tourism hotel -->
<ModOp Type="add" GUID="601379" Path="/Values/PopulationLevel7/PopulationInputs/Item/RequiredBuildings[Item/Region='Moderate']">
  <Item>
    <RequiredBuilding>1500010500</RequiredBuilding>
    <Region>Moderate</Region>
  </Item>
</ModOp>
<ModOp Type="add" GUID="601379" Path="/Values/PopulationLevel7/PopulationInputs/Item/RequiredBuildings[Item/Region='Colony01']">
  <Item>
    <RequiredBuilding>1500010529</RequiredBuilding>
    <Region>Colony01</Region>
  </Item>
</ModOp>
```

## Changes

- 7: Added pools for motor assembly plant and subway station
- 7: Renamed most pool names from plural / 'all' to singular
