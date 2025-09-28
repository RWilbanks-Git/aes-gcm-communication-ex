# Description
A simple example of AES-GCM encryption over TCP sockets using client-server communication.



### Key Exchange and Encryption ###

Key Exchange: 
A 32-byte (or 256-bit) AES key is coded on both the server and client.

Encryption Used:
-The method of encryption used is AES-GCM (256-bit).

-The client encrypts a predetermined plaintext, generates a 12-byte IV,
     and sends both the IV and encrypted plaintext (ciphertext) to the
     server.

-The server receives the encrypted text (ciphertext) and IV, then 
     decrypts it using a key and IV identical to the ones the client
     used ("aesgcm.decrypt(IV, ciphertext, None)" for server). 




# Instructions
1.) Install cryptography package using:  pip install cryptography

2.) Head over to the directory containing the server.py and client.py files

3.) Open 2 terminal tabs

4.) Start server by using "python server.py" in one tab

5.) Start client by using "python client.py" in the other tab
