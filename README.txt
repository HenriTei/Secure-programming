#Secure File Encryption and Management System

A Java command-line application for securely storing and managing
encrypted files.

#Project scope

The application will allow users to:
- Authenticate using a password.
- Encrypt files and store them in a private application directory.
- List, decrypt and delete their own stored files.

Planned security measures include input validation, salted password
hashing, file ownership checks, restricted file permissions and
error handling that does not expose sensitive information.

#Language and libraries

- Java.
- Java cryptography APIs (JCA/JCE) for encryption and password hashing.
- Java file APIs (java.nio.file) for file operations and permissions.
- Java Console for password input without displaying it.

#Planned command-line interface

The following commands describe the intended interface:

- java -cp out Main register USERNAME
- java -cp out Main encrypt USERNAME SOURCE
- java -cp out Main list USERNAME
- java -cp out Main decrypt USERNAME FILE_ID OUTPUT
- java -cp out Main delete USERNAME FILE_ID

#Planned build and run instructions

Requirements:
- JDK 17 or newer.
- A Linux environment for development and testing of file permissions.

The planned entry point is src/Main.java. 
Compile and display command help using:

javac -d out src/Main.java
java -cp out Main --help