file extension: .MRN

## predefined types
types are represented by 1 byte. 

### common
first 2 bits decide type category
00: boolean, 01: int, 10: float, 11: bytearray

### int
000: size8, 001: size16, 010: size32, 011: size64, ...

0: absolute, 1: relative

> updates described in body.<br>
> example) when updated with 6, the value becomes 6 or adds 6 to the previous value according to this flag

0: signed, 1: unsigned

0: dump

### float
000: size8, 001: size16, 010: size32, 011: size64, ...

0: absolute, 1: relative

00: dump

### bytearray
00: size | uint8, uint16, uint32, uint64

> the maximum size of a message. 

0000: dump


## file structure

### header 
"mrn:"[version:uint16]

[update_rate:int16 | (n > 0){fps}(n < 0){spf}]

[id:string(,32)][id_splitter:space][type:type][item_splitter:new_line]

[header_splitter:new_line]

### body
[boolean_value: byte[](8 boolean per byte, ceil)],

[number_value:byte[](predefined_size)],

[bytearray_size:uint(predefined_size)][bytearray_value:byte[](predefined_size)],



