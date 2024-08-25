# JavaFileSystem

JavaFileSystem is designed to create a text file server with encryption, ensuring that all message and file exchanges are secure and maintain their integrity.

In general, JavaFileSystem should consist of a server to which one or more clients can connect. The server follows the request-reply paradigm, where each client, after authenticating with the server, can request text files, which the server will return.

The confidentiality and integrity of the data will be the server's highest priority. For this reason, all communication with the server must be encrypted, and all files returned by the server must be encrypted and maintain their integrity.

The server has a directory 'server/files', which should store all files served by the server. When the server is started, a pair of keys (one public and one private) should be generated. The server should keep its private key in memory, while the public key should be stored with the name 'serverPUk.key' in the 'pki/public_keys' directory.

## Installation

To install this simple application, just clone this repository to your local machine.

```bash
git clone https://github.com/MarcoAbreu2002/JavaFileSystem
```

## Usage

To use this project, simply open the repository with your preferred IDE and first run the MainServer to start the server. After the server is started, in the MainClient configuration, enable the initialization of multiple instances, then you can start the clients by selecting and running MainClient.

On the client, you need to provide the name and then select the encryption algorithms and hash algorithm.

Then the client can request files that are on the server using the command "GET : <file-name>.<file-extension>".
  
## Notes
  
For unit testing purposes, there are predefined values in the numOfRequestsMap.txt file.
