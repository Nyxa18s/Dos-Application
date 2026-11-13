# Dos-Application
Dos Application for Android 
⚡ NETSTRESS v5.0 — Advanced DDoS & Stress Testing Suite

https://img.shields.io/badge/version-5.0.0-blue.svg
https://img.shields.io/badge/platform-Android-green.svg
https://img.shields.io/badge/language-Java-orange.svg
https://img.shields.io/badge/license-Educational-red.svg

NETSTRESS is a high-performance, multi-vector network stress testing and DDoS simulation framework designed for Android. Built with a sleek "Cyber-Blue" UI and powered by an advanced multi-threaded engine, it is designed for security researchers, penetration testers, and network administrators to evaluate the resilience of their infrastructure under heavy load.

---

⚠️ DISCLAIMER

This tool is strictly for authorized penetration testing and educational purposes. Using this tool against targets without prior mutual consent is illegal. The developer assumes no liability and is not responsible for any misuse or damage caused by this program. Use it only on systems you own or have explicit permission to test.

---

🚀 Key Features

· 10 Advanced Attack Vectors: From standard HTTP floods to application-layer logic exploits.
· Modular Interface: A clean, card-based home menu where each attack has its own dedicated configuration screen.
· Real-Time Metrics: Live tracking of sent, successful, and failed requests, along with request-per-second (req/s) rate.
· Advanced Evasion: Randomizes User-Agents, injects spoofed X-Forwarded-For headers, and randomizes request paths to bypass basic WAFs and caching.
· Automated Reporting: Generates a professional .txt report containing full statistics and raw logs, which can be shared directly to other apps (Telegram, WhatsApp, Email).
· Sleek UI/UX: Dark mode with Glassmorphism cards, neon gradients, and smooth animations.

---

🛠️ Attack Vectors Explained

1. HTTP FLOOD

Sends a massive volume of HTTP GET requests to overwhelm the target server. It uses header spoofing (random IPs and User-Agents) and randomizes request paths to bypass caching and basic rate-limiting.

2. POST FLOOD

Similar to HTTP Flood, but injects custom, randomly generated payloads into the POST body. This targets form processing endpoints, database queries, and API endpoints that accept JSON or form data.

3. SLOWLORIS

A classic Layer 7 attack. Instead of sending complete requests, it opens thousands of connections to the server and sends HTTP headers extremely slowly. This exhausts the server's connection pool, making it unable to serve legitimate users.

4. R.U.D.Y. (R-U-Dead-Yet)

A targeted attack that sends a POST request with a very large Content-Length but transmits the body byte-by-byte. The server is forced to keep the connection open indefinitely, waiting for the rest of the data.

5. HTTP/2 RAPID RESET

Simulates CVE-2023-44487. It rapidly opens and resets HTTP/2 streams, forcing the server to allocate and deallocate resources at a massive rate, leading to severe CPU exhaustion.

6. CACHE BYPASS FLOOD

Appends a unique random query parameter (?cb=xxxx) to every request. This forces the CDN or caching layer to bypass its cache and forward the request directly to the origin server, effectively DoSing the backend.

7. API ABUSE

Sends malformed PUT and DELETE requests with random JSON payloads to API endpoints. This targets poorly authenticated or misconfigured REST APIs.

8. XML BOMB (Billion Laughs)

Sends an XML payload containing deeply nested entities. When the server parses this, it rapidly expands in memory, leading to RAM exhaustion and application crashes.

9. TCP CONNECT FLOOD

Opens thousands of raw TCP connections to the target server. This exhausts the server's socket and file descriptor limits, preventing new legitimate connections.

10. MIXED MULTI-VECTOR

A true DDoS simulator. It randomly switches between GET, POST, Slowloris, and TCP attacks during the test, making it nearly impossible for standard WAFs to fingerprint and block the traffic pattern.

---

📊 Reporting System

Once an attack is stopped, the Export Report button becomes active. NETSTRESS generates a well-formatted .txt file containing:

· Target URL & Attack Mode
· Total Time & Requests Sent
· Success Rate Percentage
· Breakdown of Status Codes
· Full Raw Logs (ID, Code, Response Time, Errors)

The app uses Android's FileProvider to share the report securely via the native Share Dialog.

---

⚙️ Installation & Usage

1. Download the latest .apk from the Releases page.
2. Install it on your Android device (Android 8.0+ recommended).
3. Grant the INTERNET permission.
4. Select an attack vector from the main menu.
5. Enter the target URL, configure Threads, Request Count, and Rate Gap.
6. Hit START ATTACK.
7. After finishing, tap EXPORT REPORT to save your .txt log.

---

👨‍💻 Author

Built by NYXA (Nixa)

· 🔗 Telegram: @khubkir
