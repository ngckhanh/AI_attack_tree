## Stuxnet (2010)
```
.
└── GOAL: Physically Damage Centrifuges (Root Node)
    └── AND: G1: Achieve Control of PLCs
    └── AND: G2: Modify PLC Code
    └── AND: G3: Execute Payload
    │   └── AND: G3.1: Inject Malicious Code into PLC (Altering centrifuge frequency/speed)
    │   └── AND: A6: Overcome PLC Redundancy (Targeting multiple centrifuges/stages)
    │   └── AND: A7: Conceal Attack (Rootkit component to hide processes/feed false data)
    └── G2: Modify PLC Code (AND)
    │   └── AND: A4.1: Identify Siemens Step7/WinCC Software
    │   └── AND: A4.2: Infect Windows Host (Propagate across network using zero-days)
    └── G1: Achieve Control of PLCs (OR)
        └── OR: G1.1: Gain Access to Internal Network (Air-Gapped Access)
        │   └── Leaf: A1: Use Infected USB Flash Drive
        │   └── Leaf: A2: Social Engineering to Insert Malware
        └── OR: G1.2: Exploit Windows Vulnerabilities
            └── Leaf: A3: Exploit Windows Zero-Day Vulnerabilities (LNK, Print Spooler, etc.)
