
# FakeBank TryHackMe Writeup

## Overview
TryHackMe room focused on web application exploitation and privilege escalation.

## Vulnerability Identified
- Unauthenticated admin portal access
- Unvalidated deposit function allowing arbitrary fund transfers

## Exploitation Steps

### Step 1: Reconnaissance
Used Dirb to enumerate web server endpoints and discover hidden directories/files.

### Step 2: Discovery
Found `/admin` portal through directory brute-forcing.

### Step 3: Exploitation
- Accessed admin panel without authentication
- Located deposit function that accepted arbitrary routing numbers
- Submitted deposit request with test routing number for $2000

### Step 4: Confirmation
Successfully transferred funds to test account, confirming vulnerability.

## Impact
An unauthenticated attacker could manipulate account balances and transfer arbitrary amounts of money.

## Tools Used
- Dirb (directory enumeration)
- Firefox Developer Tools
- cURL/Browser

## Remediation
- Implement authentication checks on admin portal
- Validate routing numbers against legitimate banking institutions
- Add authorization checks before processing transfers
