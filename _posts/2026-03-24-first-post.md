---
layout: post
title: "Malware Analysis: Suspicious Sample Investigation"
date: 2026-03-24
tags: [malware, dfir, analysis]
excerpt: "Phân tích một file nghi ngờ bằng phương pháp static và dynamic analysis trong môi trường lab."
---

## 🧠 Overview

Trong bài viết này, mình thực hiện phân tích một file nghi ngờ (suspicious sample) bằng cách kết hợp:

- Static Analysis
- Dynamic Analysis
- Network Monitoring

Mục tiêu là xác định:
- Hành vi của malware
- IOC (Indicators of Compromise)
- Khả năng persistence

---

## 🧪 Lab Setup

Môi trường phân tích:

- Windows 10 VM (isolated)
- Network NAT (monitor bằng Wireshark)
- Tools:
  - Process Monitor
  - TCPView
  - PEStudio

---

## 🔍 Static Analysis

### File Information

| Field | Value |
|------|------|
| File Name | sample.exe |
| File Type | PE32 |
| Size | 245 KB |

### Strings Analysis

```bash
cmd.exe /c powershell -enc ...
http://malicious-domain.com
👉 Nhận định:

Có dấu hiệu gọi PowerShell
Hardcoded domain
🚨 Dynamic Analysis
Process Behavior
sample.exe → powershell.exe → cmd.exe

👉 Malware spawn process chain để:

evade detection
thực thi payload
Registry Changes
HKCU\Software\Microsoft\Windows\CurrentVersion\Run

👉 Persistence mechanism:

Tự động chạy khi user login
Network Activity
TCP 192.168.1.5 → 45.77.x.x:443

👉 Kết nối ra external server

🧾 Indicators of Compromise (IOC)
Type	Value
IP Address	45.77.x.x
Domain	malicious-domain.com
File Hash	abcd1234efgh5678
Registry Key	HKCU...\Run
🛡️ Detection & Mitigation
Detection
Monitor process chain bất thường:
powershell.exe spawn từ file lạ
Detect outbound traffic tới domain không tin cậy
Mitigation
Block domain/IP tại firewall
Xóa registry persistence
Isolate host
🎯 Conclusion

Sample có đặc điểm:

Sử dụng PowerShell để execute payload
Thiết lập persistence qua registry
Kết nối tới C2 server

👉 Đây là một mẫu malware đơn giản nhưng đủ để bypass detection cơ bản.

📌 Notes
Luôn phân tích trong môi trường VM
Snapshot trước khi chạy sample
Không chạy trên máy thật
