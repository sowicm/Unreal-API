
# Lua API for Unreal Mods

## unreal

### unreal.log(string)

```
Output string to Forge development console
```

### unreal.dialog(prev, name, {0/1, Text, suggestion_order})

```
prev and name is the chain of dialogs.

name must be Global unique. Use your unmod name as prefix.

0/1, 0 means player to entity, 1 means otherwise.

Text actually is Language Node name. Just see the demos.

suggestion_order is used to sort dialogs has same 'prev'.
```

### unreal.tickhandler(interval, name)
```
interval is how many Minecraft ticks run one time.

name must be Global unique, Use your unmod name as prefix.
```

### unreal.on_update(entity, name)
```
Call when any Unreal entity update.
entity is the update entity.
```

### unreal.register_slot(slot)
```
If you declare new slot in your unmod, register it to prevent conflict.
```

### unreal.register_task(task)
```
If you declare new task in your unmod, register it to prevent conflict.
```

### unreal.set_text(text)
```
Use this function to override text. Currently only used by override dialog text.
```

### unreal.close_screen()
```
Just do it's name
```

### unreal.achievement_page()
```
Add Achievement for your unmod. See the demoes.
```

### unreal.items_and_blocks()
```
Add items and blocks to your unmod. See the demos.
```

### entity_get_slot(entityID, slot)
```
Get the specified slot of the entity.
Can also use this way: entity.get_slot(slot)
```

### entity_set_slot(entityID, slot, value)
```
Set the specified slot of the entity to the specified value.
Can also use this way: entity.set_slot(slot, value)
```

### get_entity_by_id(entityID)
```
Just do it's name.
See 'entity' section for more informations.
```

### get_block_id(x, y, z)

### set_block({x, y, z}, block)
```
Attention with this. the position of block must in a table.
because of the limit of arguments count.
```

### ~~unreal.nearestBlockNearEntity(entity, block(s))~~
```
if you find one block type.
unreal.nearestBlockNearEntity(entity, blockID)
else if you find more than one block type.
unreal.nearestBlockNearEntity(entity, {blokID1, blockID2, …})
this function will returen the nearest block belongs any type of you want.
the returned table has these keys: 'id', 'x', 'y', 'z'
```

## player

### player.username()

### player.experienceLevel()

### player.experienceTotal()

### player.experience()

### player.itemInUseID()

### player.itemInUseDamage()

### player.itemInUseCount()

### player.isUsingItem()

### player.itemInUseDuration()

### player.stopUsingItem()

### player.clearItemInUse()

### player.isBlocking()

### player.currentEquippedItem()

### player.destroyCurrentEquippedItem()

### player.addChatMessage(string)

### player.entities_within_distance(n)
```
Retrieves a table contains all unreal entities with in n blocks.
You can implement this function in lua by yourself.
```

### player.trigger_achievement(achievement)
```
Trigger the name of your unmod achievement.
```

## entity

### entity.entityId()

### entity.name()

### entity.inventoty()
```
Retrieves the inventory of the entity, see 'inventoty' section for more information.
```

### entity.move_to(x, y, z)

### entity.x()

### entity.y()

### entity.z()

### entity.get_slot(slot)

### entity.set_slot(slot, value)

### entity.open_inventory()

### entity.entities_within_distance(n)
```
Retrieves a table contains all unreal entities with in n blocks.
You can implement this function in lua by yourself.
```

### entity.find_wood_and_cut()

### entity.say(string)

### entity.face(x, y, z)

### entity.die()

## inventory

### inventoty.count_item(itemID)

## server

### server.is_day_time()


