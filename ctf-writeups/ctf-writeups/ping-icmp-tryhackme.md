# Network Fundamentals - Ping (ICMP)

## Concept
Ping is a fundamental network diagnostic tool that uses ICMP (Internet Control Message Protocol) to test connectivity and measure latency between devices.

## How It Works
- Sends ICMP echo request packets to a target
- Target responds with echo reply
- Measures round-trip time (RTT) in milliseconds
- Shows packet loss percentage

## Practical Exercise

### Objective
Test network connectivity to public and private addresses

### Tools Used
- Ping command line utility
- ICMP protocol

### Steps Executed

**Public Server Test:**
- Pinged 8.8.8.8 (Google's public DNS server)
- Received ICMP echo replies
- Measured latency and confirmed connectivity
- Flag obtained: THM{I_PINGED_THE_SERVER}

**Private Network Test:**
- Pinged 10.10.10.10 (private IP address)
- Demonstrated how to test internal network devices

## Key Takeaways
- Ping confirms if a device is reachable on network
- Latency measurements help identify network performance issues
- Works on both public and private networks
- Syntax: `ping [IP/domain]`

## Use Cases
- Network troubleshooting
- Connectivity verification
- Latency measurement
- Host discovery
