# 🎫 JWT Inspector

**JWT Inspector** is a local-first, offline-capable JSON Web Token (JWT) diagnostic utility and signature-forging testing environment built using vanilla HTML, CSS, and modern asynchronous JavaScript.

## ⚙️ Core Technical Capabilities

* **Proportional Byte Mapping:** A custom layout engine segments and dynamically maps out the byte footprint ratio separating the token's Header, Payload, and Signature components.
* **Alg Weakness Auditing:** Automatically runs real-time security flag scans assessing structural flaws like `alg: none` parsing logic, weak hashing parameters (`HS1`), expired `exp` claims, or missing token parameters (`aud`, `iss`).
* **Cryptographic Signing (Client-Side):** Utilizes the browser's high-performance native **Web Crypto API** (`crypto.subtle`) to locally verify and generate HMAC structures (`HS256`, `HS384`, `HS512`) without network transit.
* **Token Forging Sandbox:** Includes a complete jwt.io-style editor matrix built for changing internal JSON parameters on the fly and creating testing tokens.
