# NetworkWalks Penetration Testing Lab

A structured four-week penetration testing and cybersecurity laboratory
project developed under NetworkWalks.

The project focuses on building an isolated security testing environment,
network experimentation, penetration testing tools, automation, and
security assessment techniques.

## Lab Environment

| Component | Configuration |
|---|---|
| Host OS | Arch Linux |
| Container Platform | Docker |
| Security Machine | Kali Linux |
| Target Machine | Windows 11 |
| Container Network | `pentest-lab` |
| Network Automation | Python / Netmiko / Paramiko |
| Security Tools | Nmap / Metasploit and others |
| Additional Work | HexStrike AI |
| Future Networking | GNS3 |
| Internship Verification | [📄 Internship Offer Letter (PDF)](./docs/OfferLetter_Sangharsa_Adhikari.pdf) |

## Lab Architecture

```text
                    Arch Linux Host
                          |
                         Docker
                          |
                ┌─────────┴─────────┐
                │                   │
                ▼                   ▼
        Kali Linux             Windows 11
        kali container         target container
                │                   │
                └─────────┬─────────┘
                          │
                   pentest-lab
                    Docker Network
