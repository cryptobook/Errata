## Errata and Remarks for *A Course in Cryptography*

p. 14, Example 1.24 (3). Add the following line before the SageMath commands:  
`from sage.crypto.boolean_function import BooleanFunction`

p. 145, Beginning of Chapter 7.5. Add:   
SHA-384 and SHA-512 use an internal state of 512 bits (eight 64-bit words).

p. 205, Last bullet of Definition 11.4. Change:   
 <img src="https://render.githubusercontent.com/render/math?math=m\in\mathbb{Z}_{N}^*">
 
p. 211, Exercise 10. Tasks (a) to (e) refer to the ElGamal signature scheme. 

p. 226, End of Example 12.23. Change:  
The order of the point P over GF(p) is 168=2<sup>3</sup> \*3\*7 so that (7!)P=O mod p. The order of P over GF(q) is 347, and hence (7!)P≠O mod q. 

p. 284, Exercise 13 (d). Append `% 2` to the last line of the SageMath code:  
`return ZZ(round(y)) % 2`  
Alternatively, interpret multiples of 2 in the coordinates of `w` and `v-w` as 0.
