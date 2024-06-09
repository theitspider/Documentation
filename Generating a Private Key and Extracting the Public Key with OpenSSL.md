# Generating a Private Key and Extracting the Public Key with OpenSSL

## Description

This guide provides comprehensive instructions for generating a private key using OpenSSL and subsequently separating the public key from it. OpenSSL is a widely used open-source toolkit for SSL/TLS protocols, offering robust cryptographic functionalities.

## Prerequisites

Before proceeding, ensure that OpenSSL is installed on the system. OpenSSL is commonly available on most Unix-like operating systems and can be installed on Windows as well.

## Generating a Private Key

To generate a private key using OpenSSL, the following command can be used:

```bash
openssl genrsa -out private_key.pem 2048
```

This command generates an RSA private key with a key size of 2048 bits and saves it in a file named `private_key.pem`.

## Extracting the Public Key

After generating the private key, the next step is to extract the public key from it. This can be done using the following command:

```bash
openssl rsa -pubout -in private_key.pem -out public_key.pem
```

This command extracts the public key from the private key file `private_key.pem` and saves it in a file named `public_key.pem`.

## Wrap-Up

By following these steps, a private key can be generated using OpenSSL, and the corresponding public key can be extracted. These keys can be used for various cryptographic operations, ensuring secure communication and data integrity. It's essential to keep the private key secure and share the public key only with trusted parties as needed.