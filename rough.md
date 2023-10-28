file extension: .MRN

## file structure

### header 
"mrn:"[human-readable or binary: h|b][version:uint16]

[update_rate:int16 | (n > 0){fps}(n < 0){spf}]

[id:string(,32)][id_splitter:space][type:type][item_splitter:new_line]

[header_splitter:new_line]

### body
[boolean_value: byte[](8 boolean per byte, ceil)],

[number_value:byte[](predefined_size)],

[bytearray_size:uint(predefined_size)][bytearray_value:byte[](predefined_size)],



