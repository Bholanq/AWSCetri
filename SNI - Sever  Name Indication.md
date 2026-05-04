**SNI (Server Name Indication)** is a TLS extension that lets a client tell the server **which hostname it wants to connect to during the SSL/TLS handshake**.

Suppose a server hosts:
- `site1.com`
- `site2.com`
Both share same IP: `192.0.2.1`
Without SNI:
- Server doesn’t know which cert to send → SSL error
With SNI:
- Browser says: “I want `site2.com`”
- Server sends `site2.com` certificate

![[Pasted image 20260503181927.png]]

# Supported LBs

![[Pasted image 20260503182108.png]]
