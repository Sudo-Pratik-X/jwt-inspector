# 🎫 JWT Inspector

**JWT Inspector** is a local-first, zero-tracking JSON Web Token (JWT) diagnostic utility and signature-forging workbench. Built entirely with vanilla HTML, CSS, and modern asynchronous JavaScript, it enables developers and security engineers to inspect, audit, and test tokens instantly without exposing sensitive key payloads to external networks.

## ⚙️ Core Technical Capabilities

* **Proportional Byte Mapping:** Features a multi-colored structural analyzer that segments and dynamically maps out the exact byte footprint ratio separating the token's Header, Payload, and Signature components.
* **Cryptographic Signing (Client-Side):** Utilizes the high-performance native browser **Web Crypto API** (`crypto.subtle`) to locally verify and generate HMAC structures (`HS256`, `HS384`, `HS512`) securely in the browser runtime.
* **Vulnerability & Compliance Auditing:** Runs a real-time structural diagnostic sweep on token configurations to flag dangerous implementations and structural oversights.
* **Token Sandbox Workbench:** Includes an editable jwt.io-style interface built for altering JSON claims on the fly, setting expiration targets, and generating forged strings for security boundary testing.

## 🔍 Security Flags Monitored

The static analyzer automatically categorizes findings by threat levels (`Critical`, `Warning`, `Valid`) tracking anomalies including:
* **`alg: none` Vulnerabilities:** Critical alerts if a token relies on unsigned verification bypass paths.
* **Deprecated Ciphers:** Identifies weak or broken encryption/hashing standards (like `HS1`).
* **Time Drift & Validation Claims:** Evaluates expiration deadlines (`exp`), not-before limits (`nbf`), and creation age stamps (`iat`).
* **Replay Contexts:** Checks for missing recipients (`aud`) and unauthorized token authority roots (`iss`).

## 🚀 Deployment & Usage

Because the application is built entirely on native client-side web APIs, it requires zero external node packages, compile pipelines, or configurations:

1. Clone or download this directory.
2. Open `index.html` in any modern desktop or mobile browser.
3. Paste an active token string or load the built-in sandbox mock token to run local diagnostic checks instantly.

---
*Designed & Engineered by **Pratik S.** — 2026.*
