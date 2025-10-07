# Hidden Image Encryption Project

## Overview

This project demonstrates a **simple image-based steganography** concept using Python and OpenCV. It allows a user to **hide a secret message inside an image** and retrieve it later using a password. The message is encrypted into the pixel values of the image, creating an "encrypted image" that visually appears the same but contains hidden information.

---

## Features

* Hide a secret message inside any image.
* Encrypt the message using a simple password-based verification.
* Decrypt the hidden message using the correct password.
* Saves the encrypted image for storage or sharing.

---

## How It Works

1. The script reads an image using OpenCV.
2. Each character of the secret message is converted to its ASCII value.
3. The ASCII values are encoded sequentially into the image pixels.
4. A password is required to decrypt the message, ensuring basic security.
5. Decryption is performed by reading the modified pixels and converting them back to characters.

> **Note:** This is a basic demonstration and not meant for secure cryptography purposes.

---

## Prerequisites

* Python 3.x
* OpenCV library

Install OpenCV via pip if not already installed:

```bash
pip install opencv-python
```

---

## How to Use

### 1. Encryption

1. Save your image as `boss.jpg` (or another supported format like `.jpeg`).
2. Run the script:

```bash
python hiddenimage.py
```

3. Enter your **secret message**.
4. Enter a **password** for encryption.
5. The script will generate `encryptedImage.jpg` and open it automatically.

### 2. Decryption

1. Run the same script again.
2. Enter the **password** you used for encryption.
3. If the password is correct, the hidden message will be displayed in the console.

---

## Example

* Original image: `boss.jpg`
* Encrypted image: `encryptedImage.jpg`
* Secret message: `"Hello World"`
* Password: `"1234"`
* Output: `"Decryption message: Hello World"`

---

## Important Notes

* The image must be large enough to contain the secret message. Each character modifies one pixel component.
* Supports simple ASCII characters (0-255).
* This project is for educational purposes and demonstrates **basic steganography**.
* Avoid using this for highly sensitive data as the encryption is minimal.

---

## File Structure

```
Hidden-Image-Encryption/
│
├── hiddenimage.py          # Python script for encryption/decryption
├── boss.jpg                # Sample input image
├── encryptedImage.jpg      # Output encrypted image
└── README.md               # Project documentation
```

---

## Technologies Used

* Python 3
* OpenCV (Open Source Computer Vision Library)
* Basic ASCII encoding

---

## License

This project is open-source and available under the MIT License.

---

