# Encryption and Decryption Application

This Python application allows you to encrypt and decrypt files using asymmetric key cryptography. The application consists of three main components:

1. **decrypt.py**: Decrypts an encrypted file using a private key.

2. **encrypt.py**: Encrypts a file using a public key.

3. **gen_keys.py**: Generates a pair of public and private keys.

## Prerequisites

Before running the application, ensure that you have the following prerequisites:

1. Install a virtual environment (venv) in your IDE. Run the following command in the terminal:

    ```
    venv
    ```

2. Install the cryptography library. Run the following command in the terminal:

    ```
    pip3 install cryptography
    ```

## Steps to Run the Application

Follow these steps to run the application:

1. **Generate Keys**: Run the following command to generate public and private keys:

    ```
    python gen_keys.py
    ```

    This will create two files, `priv.pem` and `pub.pem`, containing the private and public keys, respectively.

2. **Encrypt a File**: Run the following command to encrypt a file:

    ```
    ./encrypt.py original_filename
    ```

    Replace `original_filename` with the name of the file you want to encrypt. The encrypted file will be saved as `original_filename.encrypted`.

3. **Decrypt a File**: Run the following command to decrypt the encrypted file:

    ```
    ./decrypt.py original_filename.encrypted
    ```

    The decrypted file will be saved as `original_filename.decrypted`.

## Notes

- Ensure that you have the necessary permissions to read and write files in the specified directories.

- Set the environment variable `PEMK` to the path of the private key (`priv.pem`) and `PUB_PEMK` to the path of the public key (`pub.pem`).

- The application uses the `cryptography` library for cryptographic operations.

