# Defensive Security Intro - FakeBank Writeup

## Attack Detected
Web Discovery Attack - automated directory enumeration on admin endpoints

## Source IP
32.122.195.63

## Attack Summary
- URLs attempted: 31
- Duration: 16 minutes 32 seconds
- Blocked requests: 10
- Attack started: 14/07/2025, 10:21:39

## Defensive Actions Taken
1. Identified malicious IP conducting brute-force directory enumeration
2. Implemented 72-hour IP ban with note "until further notice continuously ban"
3. Set rate limiting: 60-second window, max 50 requests per window
4. Created WAF rule: "Block suspicious enumeration attempts"

## Tools/Methods Used
- SIEM dashboard analysis
- IP reputation analysis
- WAF configuration
- Rate limiting implementation

## Key Findings
Attack pattern matches automated directory scanning. Proper rate limiting and IP blocking prevented further exploitation attempts.
