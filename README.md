### Project Title

**Designing Next-Generation Cryptography for Secure and Private Communication**

### Project Overview

My major project was a **Python-based security application** designed to protect confidential information while transmitting it over an unsecured network.

The main idea was to combine **cryptography and steganography**. Cryptography was used to convert the original message into unreadable encrypted data, and steganography was used to hide that encrypted data inside an image.

I developed the application using **Python and Flask** and implemented the encryption, decryption, and image-based data hiding processes.

### How the Project Works

The project works in four main steps:

**1. Input confidential data**

First, the user provides the confidential message that needs to be protected.

**2. Encryption**

The message is encrypted before transmission. The encryption process converts the original readable message into **ciphertext**, so even if someone obtains the data, they cannot directly understand it.

In our implementation, encryption involved operations such as **bit-level processing, circular shifts, XOR operations, and secret keys**.

**3. Steganography**

After encryption, the ciphertext is hidden inside a **cover image** using a modified **LSB (Least Significant Bit)** technique.

Instead of simply using one LSB position, the approach uses different bit positions such as **LSB-1, LSB-2 and LSB-3** in an alternating manner.

The resulting image is called the **stego image**.

The important advantage is that the encrypted information is not transmitted as an obvious text or file. It is concealed inside an image.

**4. Extraction and Decryption**

At the receiver's side, the process is reversed.

First, the hidden encrypted data is extracted from the stego image. Then the extracted ciphertext is decrypted using the appropriate key to recover the original message.

### Technologies Used

* **Python** – Main programming language
* **Flask** – Web application/microservice framework
* **Cryptography** – Encryption and decryption
* **Steganography** – Hiding encrypted information inside an image
* **LSB technique** – Image-based data hiding
* **HTML/CSS** – Web interface

### My Contribution

My contribution to the project was mainly focused on understanding and implementing the **security workflow**, including:

* Implementing encryption and decryption logic
* Working with image-based steganography
* Implementing the modified LSB approach
* Integrating the security functionality with the Flask application
* Testing the encryption, embedding, extraction, and decryption flow
* Debugging errors and improving the application workflow

### Why We Combined Cryptography and Steganography

Cryptography alone makes the information unreadable, but the encrypted data can still attract attention.

Steganography hides the existence of the information.

By combining both techniques, our approach provides **two layers of protection**:

**Original Message → Encryption → Ciphertext → Hide inside Image → Stego Image**

At the receiver:

**Stego Image → Extract Ciphertext → Decrypt → Original Message**

