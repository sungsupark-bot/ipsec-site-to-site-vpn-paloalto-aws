# ipsec-site-to-site-vpn-paloalto-aws
NIST SP 800-77 aligned IPSec Site-to-Site VPN deployment between Palo Alto NGFW and AWS Virtual Private Gateway.
# IPSec Site-to-Site VPN Deployment  
Palo Alto NGFW ↔ AWS Virtual Private Gateway  

## Project Overview  
This project demonstrates the design and deployment of a secure IPSec Site-to-Site VPN between an on-prem Palo Alto firewall and AWS.  

The configuration follows NIST SP 800-77 guidelines for secure VPN implementation.

## Architecture Overview  
- On-prem Palo Alto NGFW  
- AWS VPC  
- AWS Virtual Private Gateway  
- Tunnel Interface configuration  
- Static routing  

## Security Configuration  

### IKE Phase 1  
- Encryption: AES-256  
- Authentication: SHA-256  
- DH Group: 14  
- Lifetime: 28800 seconds  

### IPSec Phase 2  
- Encryption: AES-256-GCM  
- PFS enabled  
- Lifetime: 3600 seconds  

## NIST Alignment  
This project aligns with:  
- NIST SP 800-77 (IPSec VPN)  
- NIST SP 800-61 (Incident Response considerations)  

## Validation Steps  
- Verified tunnel status on PAN-OS  
- Tested ICMP connectivity between EC2 and internal Linux host  
- Confirmed encrypted traffic via tunnel monitoring  

## Troubleshooting Performed  
- Routing misconfiguration corrected  
- Security policy rule adjustments  
- Phase 1 mismatch resolved  

## Key Learning Outcomes  
- VPN architecture design  
- Crypto profile configuration  
- Secure cloud integration  
- Troubleshooting IPSec negotiation failures
