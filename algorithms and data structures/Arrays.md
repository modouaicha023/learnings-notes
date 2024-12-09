# Array
- a continuous memory space
- there are fixed size; continuous memory chunks
- that means you cannot grow it
- there is no insertAt, push or pop. ( doesn't mean we can't write theose though)
  - a array have to be a fixed size, we can not gropw it ( we can reallocate it,   by creating a new array with a biggest size and take the old one to write it to the new one 🙆🏾‍♂️ )

```
> const a = new ArrayBuffer(6)
undefined
> a
ArrayBuffer { [Uint8Contents]: <00 00 00 00 00 00>, byteLength: 6 }
> const a8 = new Uint8Array(a)
undefined
> a8
Uint8Array(6) [ 0, 0, 0, 0, 0, 0 ]
> a8[0]=45
45
> a
ArrayBuffer { [Uint8Contents]: <2d 00 00 00 00 00>, byteLength: 6 }
> const a16 = new Uint16Array(a)
undefined
> a8[2]=45
45
> a
ArrayBuffer { [Uint8Contents]: <2d 00 2d 00 00 00>, byteLength: 6 }
> a6[2]=0x4545
Uncaught ReferenceError: a6 is not defined
> const a16 = new Uint16Array(a)
Uncaught SyntaxError: Identifier 'a16' has already been declared
> a16[2]=0x4545
17733
> a
ArrayBuffer { [Uint8Contents]: <2d 00 2d 00 45 45>, byteLength: 6 }
>
```