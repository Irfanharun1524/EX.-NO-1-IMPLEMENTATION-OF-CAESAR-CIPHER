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
def encrypt(text, key):
    result = ""
    for ch in text:
        if ch.isupper():
            result += chr((ord(ch) - 65 + key) % 26 + 65)
        elif ch.islower():
            result += chr((ord(ch) - 97 + key) % 26 + 97)
        else:
            result += ch
    return result

def decrypt(text, key):
    result = ""
    for ch in text:
        if ch.isupper():
            result += chr((ord(ch) - 65 - key) % 26 + 65)
        elif ch.islower():
            result += chr((ord(ch) - 97 - key) % 26 + 97)
        else:
            result += ch
    return result

plain = input("Enter the plain text: ")
key = int(input("Enter the key value: "))

print("\nPLAIN TEXT:", plain)

cipher = encrypt(plain, key)
print("ENCRYPTED TEXT:", cipher)

decrypted = decrypt(cipher, key)
print("AFTER DECRYPTION:", decrypted)
```

## OUTPUT:

<img width="675" height="976" alt="Screenshot 2026-05-11 090734" src="https://github.com/user-attachments/assets/c5daa396-8d0f-42ec-94c9-a64ef323143c" />

## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
