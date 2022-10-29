## scene
### key
scene
### value
set(scene)

## filter
### key 
filter:scene:type:{userId} 
### value
sorted set(itemId,timestamp) 

## i2i
### key
i2i:scene:{itemId}
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
