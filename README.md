# One time pad (OTP) example
The index.html file contains two one time pad examples. One uses modulo 26 and the other uses the typical XOR process. Additional debug info is output to the browser console.

## Basic requirements of OTP
- Two copies of a "pad" which contains the same keys
- Pads must be transported and stored securely
- Key length >= message length
- Key must be completely random
- A key may only be used once. It may be possible to decrypt a message if two ciphers are available which were encrypted with the same key.

## Basic process

### Encryption
Combine each character of the message with the corresponding character of the key using some modular arithmetic

### Decryption
Combine each character of the cipher with the corresponding character of the key using the same modular arithmetic

#### Special note for modulo 26
The alphabet, A-Z, is assigned numberic values: A=0 ... Z=25. During encryption, the numberic value of each message character is added with the numberic value of each key character. If the sum exceeds 25, then 26 should be subtracted to form the cipher value for that character. Likewise to decrypt, the numeric value of the key is subtacted from the number value of the cipher. If the difference is negative, add 26 to get the message character value.

XOR works nice for this because the exact same process is done to encrypt and decrypt.
