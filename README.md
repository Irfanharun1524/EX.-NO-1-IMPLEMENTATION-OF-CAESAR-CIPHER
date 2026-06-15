## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
```
plain = input("\n Enter the plain text: ")
key = int(input("\n Enter the key value: "))

print("\n \n \t PLAIN TEXT: " + plain)
print("\n \n \t ENCRYPTED TEXT: ", end="")

cipher = ""
for i in range(len(plain)):
    cipher_char = chr(ord(plain[i]) + key)
    if plain[i].isupper() and ord(cipher_char) > ord('Z'):
        cipher_char = chr(ord(cipher_char) - 26)
    if plain[i].islower() and ord(cipher_char) > ord('z'):
        cipher_char = chr(ord(cipher_char) - 26)
    cipher += cipher_char
    print(cipher_char, end="")

print("\n \n \t AFTER DECRYPTION : ", end="")
decrypted = ""
for i in range(len(cipher)):
    decrypted_char = chr(ord(cipher[i]) - key)
    if cipher[i].isupper() and ord(decrypted_char) < ord('A'):
        decrypted_char = chr(ord(decrypted_char) + 26)
    if cipher[i].islower() and ord(decrypted_char) < ord('a'):
        decrypted_char = chr(ord(decrypted_char) + 26)
    decrypted += decrypted_char
    print(decrypted_char, end="")

print() 
```

## OUTPUT:

<img width="344" height="114" alt="Screenshot 2026-05-31 at 21-04-36 Irfanharun1524_EX -NO-1-IMPLEMENTATION-OF-CAESAR-CIPHER" src="https://github.com/user-attachments/assets/40f5b0b2-954b-42f8-879a-124db479819b" />

## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
