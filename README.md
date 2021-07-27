## Errata and Remarks for *A Course in Cryptography*

p. 14, Example 1.24 (3). Add the following line before the SageMath commands:  
`from sage.crypto.boolean_function import BooleanFunction`

p. 15, SageMath code in Example 1.26. Starting from version 9.0, SageMath is running on top of Python 3, where the behavior of `print` has changed. Basically, you need to add parentheses, and for example write `print(n)` instead of `print n`. This applies to several code examples in this book.  
`print(binomial(15,n), end=" ")`  

p. 50, First line: addition is done modulo 2<sup>l</sup>.  

p. 144, SageMath code in Example 7.8. Hex encoding and decoding has changed in Python 3. Use `unhexlify` instead of `decode("hex")` as suggested by *juanjo-two*. The modified lines are: 
```
import binascii
h1 = hashlib.sha1();h1.update(binascii.unhexlify(prefix+m1))
h2 = hashlib.sha1();h2.update(binascii.unhexlify(prefix+m2))

h1 = hashlib.sha1();h1.update(binascii.unhexlify(prefix+m1+m))
h2 = hashlib.sha1();h2.update(binascii.unhexlify(prefix+m2+m))
```

p. 145, Beginning of Chapter 7.5. Add:   
SHA-384 and SHA-512 use an internal state of 512 bits (eight 64-bit words).

p. 205, Last bullet of Definition 11.4. Change:   
 <img src="https://render.githubusercontent.com/render/math?math=m\in\mathbb{Z}_{N}^*">
 
p. 211, Exercise 10. Tasks (a) to (e) refer to the ElGamal signature scheme.  

p. 223, Example 12.19. The shared secret key is k=(0,10).

p. 226, End of Example 12.23. Change:  
The order of the point P over GF(p) is 168=2<sup>3</sup> \*3\*7 , and so (7!)P=O mod p. The order of P over GF(q) is 347, and hence (7!)P≠O mod q. 

p. 284, Exercise 13 (d). Append `% 2` to the last line of the SageMath code:  
`return ZZ(round(y)) % 2`  
Alternatively, interpret multiples of 2 in the coordinates of `w` and `v-w` as 0.

p. 287, Proposition 15.5. Add `c≠O` in the definition of the minimum weight:  
<img src="https://render.githubusercontent.com/render/math?math=\min_{c \in C,\,c \neq 0\, } wt(c)">
