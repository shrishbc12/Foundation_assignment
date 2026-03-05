# Task 1 – Secure Data Exchange

## Overview
Demonstrates how **encoding formats** ensure safe data transmission across modern web protocols while highlighting security risks.

**Encoding formats:** Base64, ASCII, URL Encoding, Hex  
**Protocols:** HTTPS, TLS, SMTP, REST API, OAuth  

## Features
- Encoding demonstrations via Python  
- File/email transmission between Docker containers  
- Diagrams of encoding & protocol flow  
- Security analysis and mitigation strategies  

### Task Structure
```
Task1/
├── README.md                 # Main documentation 
├── images/                 
│   ├── base64-docker.png     # Figure 1
│   ├── url-docker.png        # Figure 2
│   ├── http-post.png         # Figure 3
│   ├── https-tls-flow.png    # Figure 4
│   ├── docker-server.png     # Figure 5
│   ├── docker-client.png     # Figure 6
│   ├── http-headers.png      # Figure 7
│   ├── base64-decode.png     # Figure 8
│   ├── email-base64.png      # Figure 9
│   ├── smtp-tls.png          # Figure 10
│   ├── rest-api.png          # Figure 11
│   ├── oauth-request.png     # Figure 12
│   └── oauth-response.png    # Figure 13
│
└── Scripts/ 
  ├── Base64_encode.sh # Bash script for Base64 encoding
  ├── Url_Encoding.py # Python script for URL encoding
  └── Docker_file_transfer.cmd # file transfer in docker
```

## Encoding Formats Covered

### 1. ASCII Encoding
- Standard character encoding system for text data
- Assigns numerical codes to characters, digits, and symbols
- **Use Case**: Basic text representation across platforms

### 2. Base64 Encoding
- Converts binary data into text format
- Enables transmission over text-based protocols
- **Use Case**: Email attachments, API authentication

### 3. URL Encoding
- Converts characters into safe URL format
- Replaces unsafe characters with % followed by hex digits
- **Use Case**: Web forms, HTTP requests

## Protocol Integration

| Protocol | Role | Encoding Integration |
|----------|------|---------------------|
| **HTTPS** | Secure HTTP communication | Base64-encoded credentials in headers |
| **TLS** | Transport layer security | Encrypts encoded payloads |
| **SMTP** | Email transmission | Base64 for attachments |
| **REST API** | Web service communication | JSON with Base64 encoding |
| **OAuth** | Authorization framework | Token encoding |

## Docker Demo: File Transmission Between Containers (CMD)

This demonstration shows secure file transfer between Docker containers using direct CMD commands:

### Step 1: Create and Serve File from Container 1

Open **Command Prompt (CMD)** and run:

```cmd
:: Run a Python container and create a file
docker run -d --name server -p 8081:8081 python:3-slim sh -c "echo 'Hello from Docker Container' > myfile.txt && python -m http.server 8081"

:: Check if container is running
docker ps

:: Verify file is created
docker exec server cat myfile.txt

## Four Scripts Overview

| # | Script Name | Language | Purpose |
|---|-------------|----------|---------|
| **2** | `Base64_encode.sh` | Bash | Shows Base64 conversion for binary data |
| **3** | `Url_Encoding.py` | Python | URL encoding/decoding demonstration |
| **4** | `Docker_file_transfer.cmd` | Commandline | File transfer between Docker containers |

---

## Script 1: ASCII_Encoding.ps1

### Purpose
Demonstrates ASCII encoding standard for text data representation.

### Code
```
```
Format-Hex "C:\Users\L E G I 0 N\OneDrive\Desktop\hello.txt.txt" | more
```
