# Network Fundamentals - IP & MAC Address Spoofing

## Vulnerability Identified
Device access control based solely on IP/MAC address without additional authentication

## Attack Scenario
Initial access denied due to source IP address not being whitelisted on network.

## Exploitation Steps

### Step 1: Reconnaissance
Identified that network access was restricted based on IP address whitelist.

### Step 2: MAC Address Analysis
Discovered that MAC addresses were associated with authorized network devices (workers).

### Step 3: IP Spoofing
Transferred/spoofed my IP address to match an already-accepted worker IP address on the network.

### Step 4: Access Granted
Once IP matched an authorized device IP, network access was granted.

## Impact
Lack of proper authentication mechanisms allowed unauthorized access by simply matching network identifiers without verifying actual device identity.

## Vulnerability Root Cause
- Single-layer authentication (IP-based only)
- No additional verification (certificates, credentials, multi-factor)
- No MAC address binding to prevent spoofing
- No network segmentation

## Remediation
- Implement multi-factor authentication
- Use certificate-based authentication
- Bind MAC addresses to IP addresses
- Implement 802.1X network access control
- Deploy network segmentation and VLANs

## Tools Used
- Network interface configuration
- IP address manipulation
- Network reconnaissance
