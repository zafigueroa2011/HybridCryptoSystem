Hybrid Cryptosystem

Cryptosystem Architecture

Introduction
In this application a design a hybrid cryptosystem that uses ElGamal and DES algorithms to encrypt messages and decrypt cipher text. I use ElGamal for key exchange and DES for data encapsulation. I selected ElGamal since it is a public-key algorithm, the key is not too long, and doesn’t require to have a shared secret to communicate. I choose DES since it is a symmetric key algorithm, and is faster than ElGamal since it doesn’t have to do many mathematical computations.

How it works
The encryption and decryption must be done on the same session since each time the application is started or run it will calculate a new private key and public key. In other words, an encryption from a previous session will not work in the current session decryption.

Encryption Process:
Bob wants to send an encrypted message to Alice:
1.	Alice selects a short key.
2.	Cryptosystem generates a public and private key using ElGamal.
3.	Cryptosystem encrypts Alice’s short key using ElGamal and generated public key.
4.	Bob sends message.
5.	Message is then encrypted using DES and the generated public key.
6.	Cryptosystem displays the encrypted text.

Decryption Process:
Alice wants to decrypt encrypted message sent by Bob:
1.	Alice enters the cipher text generated from the encryption.
2.	Cryptosystem uses private key, prime number, and key cipher text to get Alice’s selected short key.
3.	Cryptosystem uses decrypted short key to decrypt cipher text.
4.	Cryptosystem displays the message sent.

Application

Specifications
This application is a java application that implements a cryptosystem using ElGamal and DES. I got the DES tables and functions from https://en.wikipedia.org/wiki/DES_supplementary_material.
For Encryption the input is the message and the output is the cipher text in hexadecimal format.
For Decryption the input is a hexadecimal string like "0123adcf" and the output is the decrypted message as a string.
The short secret key can be updated at any time. If the value on the text area is different to the one saved it will automatically update to the new value even if the button update is not clicked. But decryption must use the same key as the one used in encryption.
The application can encrypt and decrypt multiple times until is closed. But encryption and decryption must be done on the same session, before it is closed.
Javadoc is located in \dist\javadoc folder. Open the dist\javadoc\index.html to go to the principal page of the java documentation.

Instructions 
1.	Unzip File.
2.	Go to the \dist folder.
3.	Open the jar file “CIS5371_Project1.jar”.
