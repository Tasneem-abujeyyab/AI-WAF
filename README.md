# AI-WAF
AI-powered Web Application Firewall for real-time threat detection
# Overview:
A smart, real-time WAF combining traditional rule-based defenses with machine learning to detect and block web attacks like SQLi, XSS, File inclusion, and command injection.
# Key Features
🔍 Real-Time Traffic Inspection Intercepts and analyzes HTTP requests using mitmproxy with Python addon support.

🧠 Machine Learning Classification Detects attacks like SQL Injection, XSS, Command Injection, and File Inclusion using a trained Random Forest model.

📁 Custom Dataset Creation Built and labeled a proprietary dataset of real and synthetic HTTP requests, covering both benign and malicious traffic.

⚡ Inline Blocking Mechanism Automatically returns HTTP 403 responses for malicious requests—blocking threats in real time.

🔄 Asynchronous Execution Classification and logging run in parallel to ensure high throughput and minimal latency under load.

📊 Live Dashboard Built with Dash and Flask-SocketIO for:
          Real-time log updates via WebSocket 
          Visual alerts for malicious activity
          Summary charts and metrics
          
🛢️ SQL Database Logging Stores detailed records of all HTTP requests and detection results in a relational database for analysis and auditing.
🧾 Reporting Module Generates security reports daily, weekly, monthly, and yearly insights. 
# System Architecture 
![Screenshot 2025-06-21 162329](https://github.com/user-attachments/assets/931910b4-35c0-4d0d-9564-0f7452b4f959)
# 📊 Results
1. Achieved 96% detection accuracy using a Random Forest classifier trained on diverse web traffic datasets
2. Successfully detected and blocked major attack types:
       SQL Injection, XSS, Command Injection, File Inclusion
3. Detected common evasion techniques, such as payload encoding (e.g. URL encoding, hex, base64), by analyzing underlying request features rather than surface patterns
4. Real-time dashboard achieved 100% alert delivery accuracy using Flask-SocketIO and Dash
5. Significantly reduced false negatives compared to traditional WAFs
6. Logged detailed traffic for reporting and trend visualization, aiding in post-incident analysis
