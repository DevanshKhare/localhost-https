# Next.js HTTPS Development Server

This project demonstrates how to configure a Next.js application to use HTTPS with a self-signed certificate for local development.

## Prerequisites

- Node.js and npm installed
- OpenSSL installed

## Setup

### Step 1: Generate a Self-Signed Certificate

Generate a private key and a self-signed certificate using OpenSSL:

```bash
# Generate a private key
openssl genpkey -algorithm RSA -out localhost.key -pkeyopt rsa_keygen_bits:2048

# Generate a certificate signing request (CSR)
openssl req -new -key localhost.key -out localhost.csr

# Generate a self-signed certificate
openssl x509 -req -days 365 -in localhost.csr -signkey localhost.key -out localhost.crt
```
