Consumable
==========
A Buffer wrapper that makes it easy to read binary data. 

Installation
------------
```
$ npm install consumable
```

API
---
### new Consumable(buffer [, endianness = 'BE'])
Creates a new consumable object from `buffer`. `endianness` can either be 'LE' or 'BE'.

### Consumable.fromFile(src [, endianness = 'BE'])
Creates a new consumable object from a file path.

### consumable.read(n)
Returns a buffer containing the next `n` bytes of the underlying buffer.

### consumable.move(n)
Moves the read offset by `n` bytes.

### consumable.\<type\>()
Reads and returns a `type` from the buffer. `type` can be:

* `byte` (1 byte)
* `int8`, `uint8` (1 byte)
* `int16`, `uint16` (2 bytes)
* `int32`, `uint32` (4 bytes)
* `float` (4 bytes)
* `double` (8 bytes)

### consumable.char([n = 1])
Reads `n` bytes from the buffer and returns their ascii representation.
