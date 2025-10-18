# 🧾 SOC Case Report — Template

---

## 🕒 Case Information
- Date: YYYY-MM-DD  
- Analyst: Soso Nemsadze  
- Environment: (Ubuntu / Windows / Cloud / TryHackMe Lab / Other)  
- Source File / Log: (syslog, auth.log, Wireshark capture, etc.)  

---

## 🧩 Incident Summary
Description:  
_(Brief summary of what happened or what triggered your attention — e.g., failed logins, network anomaly, suspicious IP, etc.)_

Initial Detection Point:  
- Log file, network alert, or tool used.  
- Example: Detected via Wireshark (DNS query to unknown domain).

---

## 🔍 Investigation Steps
| Step | Action Taken | Command / Tool | Observation |
|------|---------------|----------------|--------------|
| 1 | Viewed log entries for “failed” attempts | grep -i failed /var/log/auth.log | Found 5 attempts from IP 203.0.113.55 |
| 2 | Checked connection behavior | ss -tuln | SSH port 22 open |
| 3 | Verified DNS requests in Wireshark | Filter: dns | Unusual query from 198.51.100.23 |

---

## 🧠 Analysis & Findings
- Type of attack (Brute Force, Reconnaissance, Malware, etc.):  
- IPs involved:  
- Ports and protocols used:  
- Timeline or pattern observed:  
- Indicators of compromise (IOCs):  

---

## 📊 Impact Assessment
| Category | Description |
|-----------|--------------|
| Impact | What this event could cause (e.g., unauthorized access, data exposure, system disruption). |
| Severity Level | Low / Medium / High / Critical |
| Affected System / User | Which host, service, or user was targeted. |

---

## ✅ Recommended Action
- [ ] Block IP / Isolate host  
- [ ] Escalate to SOC Lead  
- [ ] Harden SSH / Change credentials  
- [ ] Enable fail2ban or rate-limiting  
- [ ] Monitor for recurrence  

---

## 🧾 Final Notes
_Use this section for conclusions, lessons learned, or patterns to track in the future._

---

> Template version: v1.0 — created under the guidance of Captain Lexi ⚓  
> “Each case builds your reflex. Each reflex sharpens your defense.”
