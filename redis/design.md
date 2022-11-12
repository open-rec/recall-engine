## i2i
### key
i2i:{itemId}:scene
### value
sorted set(itemId,score)

## hot
### key
hot:{scene}
### value
sorted set(itemId,score)

## new 
### key
new:{scene}
### value
sorted set(itemId,score)

## user
### key
user:{userId}
### value
User

## item
### key
item:{itemId}
### value
Item

## event
### key
event:{userId}:scene:type
### value
sorted set(itemId,timestamp)

## black
### key
black
### value
set(itemId)
