Packages required: 
1. Paramiko
2. Boto3
3. dontenv

|Protocol|Purpose|
|---|---|
|SSH|Secure remote access to a server|
|SFTP|Secure file transfer over SSH|
[Paramiko](https://www.paramiko.org/?utm_source=chatgpt.com) is a Python library used for:
- SSH connections
- SFTP file transfers
- Remote command execution

It lets Python communicate securely with Linux servers over SSH.

# Socket Issue 
can't bring a very large data over SFTP, need to bring it in chunks, the connection can break when there's no user interference.
can do that by reconnecting the with the sftp server in loop.

# Types of Sockets

## 1. TCP Socket (Most Common)

Reliable connection-oriented communication.

Used by:

- SSH
- SFTP
- HTTPS
- databases

Your SFTP uses TCP sockets.

---

## 2. UDP Socket

Faster but unreliable.

Used by:

- video streaming
- gaming
- DNS

---

# Server Socket vs Client Socket

## Server Socket

Waits for incoming connections.

Example:

```
SFTP server listening on port 22
```

---

## Client Socket

Initiates connection.

Your Python script creates the client socket.

