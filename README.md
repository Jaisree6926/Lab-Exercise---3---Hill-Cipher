# Lab-Exercise---3---Hill-Cipher
# Aim:
To write a Python program to implement the Hill Cipher encryption algorithm for encrypting and decrypting plaintext messages using a $2 \times 2$ matrix key.
# Procedure:
1. Input Collection: Prompt the user to enter a plaintext message. Convert the input to uppercase and remove any spaces.
2. Padding: Check if the length of the plaintext is odd. If it is, append the character "X" to make its length even, ensuring it can be divided into pairs of bigrams.
3. Key Matrix Definition: Define the $2 \times 2$ encryption key matrix
4. Encryption Loop: Iterate through the plaintext in steps of 2 characters:Convert each character to its corresponding numeric value ($A=0, B=1,....., Z=25$).Apply the matrix multiplication formulas modulo 26,Convert the resulting numeric cipher values back into letters
5. Output Display: Print the processed plaintext and the final generated ciphertext.
# Output:
```
# Jaisree B
# 212224230100

key = [[3, 3],
]

plaintext = input("Enter plaintext: ").upper().replace(" ", "")

if len(plaintext) % 2 != 0:
    plaintext += "X"

ciphertext = ""

for i in range(0, len(plaintext), 2):
    a = ord(plaintext[i]) - ord('A')
    b = ord(plaintext[i + 1]) - ord('A')
    
    c1 = (3 * a + 3 * b) % 26
    c2 = (2 * a + 5 * b) % 26
    
    ciphertext += chr(c1 + ord('A'))
    ciphertext += chr(c2 + ord('A'))

print(f"Plaintext: {plaintext}")
print(f"Ciphertext: {ciphertext}")
```
<img width="330" height="82" alt="image" src="https://github.com/user-attachments/assets/7becc206-3917-4618-a296-0446204f0807" />

# Result:

