# Lab Title: LAB2: Man-in-the-middle attacks (ARP spoofing)

## Challenge Answers

- **Challenge 1:** [Insert answer here, i.e., a Chuck Norris fact]
- **Challenge 2:** [Insert answer here, i.e., a `password` to unlock the next lab]

## Other Relevant Information

[Insert here, if applicable]

## Lab Prep Questions and Answers

1. What is the Address Resolution Protocol (ARP), and what is its role in a network?

   - Address Resolution Protocol (ARP) is a procedure for mapping a dynamic IP address to a permanent physical machine address (or MAC) in a local area network (LAN). The job of ARP is essentially to translate 32-bit addresses to 48-bit addresses and vice versa. This is necessary because IP addresses in IP version 4 (IPv4) are 32 bits, but MAC addresses are 48 bits. It enables network communications to reach a specific device on the network.

2. What is a Man-in-the-Middle (MitM) attack, and how does ARP spoofing enable it?

   - MitM attack is a type of attack where the attacker inserts itself into the communcation between two parties, while making it appear as if a normal exchange of information is underway. ARP spoofing: the attacker sends forged ARP Messages. This links the attacker machine’s MAC Address to the legitimate IP Address. Once the MAC Address has been linked the attacker will now receive the messages intended for the legitimate IP Address.

3. How does an attacker use ARP spoofing to intercept network traffic?

   - Fake messages that are sent by the attacker contain a spoofed MAC address, which maps to the attacker's device instead of the legitmate device.

4. How is the cookie used to derive the encryption/decryption key?

   - The cookie is passed to the derive_key function which derives the encryption/decryption key from the given key_seed. It uses function scrpyt, a modern key derivation.

5. What REST API request do you need to send to the crypto oracle the secret cookie?

   - GET /arp/cookie

6. How do you obtain the authentication token?

   - You request it from crypto oracle server using the right credentials.

7. How do you use the authentication token to obtain the cookie?

   - By sending a REST API request using the authentication token.

8. What encryption mode is used to encrypt the challenge in this lab?

   - AES-CBC

9. What tool can you use to capture network traffic on a local network interface?
   - tcpdump
