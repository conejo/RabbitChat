# RabbitChat

## Simple Explanation
RabbitChat is intended to be a simple encrypted chat application. It will be a client-server architecture with the clients connecting via TLS. In the initial version communication will only be between 2 parties, in later versions it might be expanded to multiparty chat groups or channels. A user will create an account and upload a public key. The client application will generate a public/private key pair if the user for the user if needed. All communications between parties will be encrypted. If a user is not online to receive a message, the server will hold on to it until it can be delivered. All messages flowing through the server or stored on the server will be encrypted and unreadable. Decryption will only be done on the client application.

## Architecture
The application will consist of 2 primary applications: Server and Client.

### Server
  The Server will:
  * Maintain a list of registered users 
    ** Name, Username, Password, Public Key (more than one?)
  * Maintain a list of currently logged in users
  * Deliver messages to correct user
    ** If user is not logged in, message will be stored and delivered when they login

### Client
  The Client will:
  * Generate public / private key
  * Register user if they need an account
  * Login / Logout user
  * Display notification if 'friend' available/unavailable
  * Encrypt / Decrypt messages

## Goals

