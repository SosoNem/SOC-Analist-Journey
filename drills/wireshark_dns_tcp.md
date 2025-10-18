## Wireshark Drills

Drill 1: DNS Lookup
- Filter: dns
- Command: nslookup openai.com 8.8.8.8
- Goal: Confirm query & response (UDP port 53)

Drill 2: HTTP (Unencrypted)
- Filter: tcp.port==80
- Command: curl http://example.com
- Goal: Find HTTP GET in Info column

Drill 3: HTTPS (Encrypted)
- Filter: tcp.port==443
- Command: curl -v https://openai.com
- Goal: See Client Hello and SNI (openai.com)
