# More Types
More Types introduces 7 new types to PenguinMod: Object, Array, Set, Map, Symbol, Nothing, and Function. 

These types can be used to do all sorts of things.

All of the new types, except for Nothing, are passed by reference, meaning that each new instance you create is different from every other instance.

NOTE: The square inputs cannot be displayed here, and we have turned them into circular inputs.
## Blocks
Here are the blocks are their usage:

### print to console
```scratch
print [Hello, World!] to console::#B300FF
```
This block outputs a value into the JavaScript console. You can open the console by pressing Ctrl + Shift + I (but don't type anything in if you don't know what you're doing).

### set variable to
```scratch
set [my variable v] to [0]::#B300FF
```
This is the same as the regular set variable block.

### variable
```scratch
variable [my variable v]::#B300FF reporter
```
This is the same as the regular get variable block, except that you know that it may not be text, a number, true or false.

### new
```scratch
new [Object v]::#B300FF reporter
```
Creates an object, array, set, or map.

### typeof
```scratch
typeof [Insert Anything Here]::#B300FF reporter
```
Gets the type of the value provided, it can be:
string,
number,
boolean,
Object,
Array,
Set,
Map,
Symbol,
nothing,
or Function.
### get / set / remove Key
```scratch
get key [foo] of [Insert Object / Array / Map Here]::#B300FF reporter
```
```scratch
set key [foo] of [Insert Object / Array / Map Here] to [bar]::#B300FF
```
```scratch
remove key [foo] of [Insert Object / Array / Map Here]::#B300FF
```

Here is an analogy to help you understand keys and values.
You have a giant, infinite hotel where each room is identified by its key. 
When you are using "set" key, you effectively kick out whatever was inside previously, and then put in the "value", which is the thing you want to put inside the room.
When you are using "get" key, you are peeking inside the room to see what is inside the room, without affecting anything.
When you are using "remove" key, you are kicking out whatever was inside the room, and leaving it empty.

Objects, Arrays, and Maps use these keys and value
Value can be anything, but key can be different things depending on the type.

For objects, key can be a symbol or a string. 
For arrays, key must be a number.
For maps, key can be anything; key can even be the map itself.
(You can delete values from sets)

### add to end
```scratch
add [foo] to the end of [Insert Array / Set Here]
```
Sets are really just a list of unique values, and arrays are really just a list.
This block adds a new value and puts it at the end.

### exactly the same?
```scratch
is [0] and [-0] EXACTLY the same?::#B300FF boolean
```
It's the same as Scratch's =, except it is case-sensitive, and can tell the difference between 0 and -0.
You should use this to compare objects, arrays, sets, maps, and symbols.

### In?
```scratch
[foo] in [Insert Object / Array / Set / Map Here]?::#B300FF boolean
```
It checks if key is a non-empty room. For sets, it checks if the value was previously added.

### sizeof
```scratch
sizeof [Insert Object / Array / Set / Map Here]::#B300FF reporter
```
It checks how many values are actually there.

### for key value in
 ```scratch
for key [my variable v] value [my variable v] in [Insert Object / Array / Map / Set Here] {

}@loopArrow::#B300FF
```
It loops through the object / array / set / map. The variable after "key" is the variable which is set to the key. The variable after "value" is the variable which is set to the value.
For sets, key and value are the same.

### create a symbol and nothing
```scratch
create a symbol::#B300FF reporter
nothing::#B300FF reporter
```
The first one creates a symbol (which is a guaranteed-to-be-unique value that can be used as an object or map key), and the second one is the special value called nothing (which is the value you get when you peek inside an empty room)

### Anonymous Function / return
```scratch
Anonymous Function {
}::#B300FF cap

return []::#B300FF cap
```
Anonymous Function essentially dynamically creates a custom block, which can then be "called". Return allows you to immediately stop the execution of the blocks inside of the function, and "returns" a value.

### Call function

```scratch
call function [Insert Function Here]::#B300FF

call function [Insert Function Here] and get return value::#B300FF reporter
```
The first block allows you to execute the function, as the sprite it was created in, but ignores whatever value the function returned.

The seconds block does what the first block does, but it is an input, and it gets you the value that the function returned.
