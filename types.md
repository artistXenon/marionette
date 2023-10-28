# predefined types
types are represented by 1 byte. 

## boolean
### bit specification
- bits[0,1]: type category
> specific value "00" to represent this type is an boolean
- bits[2,7]: dump
> this part is ignored

## int
### bit specification
- bits[0,1]: type category
> specific value "01" to represent this type is an int
- bits[2,4]: type size
> value representing size of datatype. if value is n, the size becomes (2^n)bytes. <br>
> for example, 000: 1byte, 001: 2byte, 010: 4byte
- bits[5]: type signed
> 0: signed, 1: unsigned
- bits[6,7]: dump
> this part is ignored

## float
### bit specification
- bits[0,1]: type category
> specific value "10" to represent this type is an float
- bits[2,4]: type size
> value representing size of datatype. if value is n, the size becomes (2^n)bytes. <br>
> for example, 000: 1byte, 001: 2byte, 010: 4byte
- bits[5,7]: dump
> this part is ignored

## bytearray
### bit specification
- bits[0,1]: type category
> specific value "11" to represent this type is an bytearray
- bits[2,3]: max size
> value representing maximum size of bytearray. if value is n, the size becomes (2^n)bytes. <br>
> 00: 1byte, 01: 2byte, 10: 3byte, 11: 4byte
- bits[4,7]: dump
> this part is ignored
