# Implement-the-AES-Encryption-and-decryption.
# Ex-8-Implement-the-AES-Encryption-and-decryption.
## Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

## ALGORITHM:
1.AES is based on a design principle known as a substitution–permutation.

2.AES does not use a Feistel network like DES, it uses variant of Rijndael.

3.It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.

4.AES operates on a 4 × 4 column-major order array of bytes, termed the state

## PROGRAM:
```
#include <stdio.h>
#include <string.h>

void xor_encrypt_decrypt(char *str, const char *key) {
    size_t str_len = strlen(str);
    size_t key_len = strlen(key);

    for (size_t i = 0; i < str_len; ++i) {
        str[i] = str[i] ^ key[i % key_len]; 
    }
}

int main() {
    char url[] = "DHINESH M";
    char key[] = "secretkey";

    printf("Original URL: %s\n", url);

    xor_encrypt_decrypt(url, key);
    printf("Encrypted URL: %s\n", url);

    xor_encrypt_decrypt(url, key); 
    printf("Decrypted URL: %s\n", url);

    return 0;
}
```


OUTPUT:

![Screenshot 2024-10-19 100929](https://github.com/user-attachments/assets/3157dc3d-d068-4405-bddc-6bdff6eb9071)


RESULT:

Hence,to use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption is done successfully.
