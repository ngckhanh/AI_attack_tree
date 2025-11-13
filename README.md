## Stuxnet (2010)
```
GOAL: Physically Damage Centrifuges (Root Node)
├── AND: G1: Achieve Control of PLCs.
├── AND: G2: Modify PLC Code.
├── AND: G3: Execute Payload.
│   ├── AND: G3.1: Inject Malicious Code into PLC (Altering centrifuge frequency/speed).
│   ├── AND: A6: Overcome PLC Redundancy (Targeting multiple centrifuges/stages).
│   └── AND: A7: Conceal Attack (Rootkit component to hide processes / feed false data).
├── G2: Modify PLC Code (AND).
│   ├── AND: A4.1: Identify Siemens Step7/WinCC Software.
│   └── AND: A4.2: Infect Windows Host (Propagate across network using zero-days).
└── G1: Achieve Control of PLCs (OR).
    ├── OR: G1.1: Gain Access to Internal Network (Air-Gapped Access).
    │   ├── Leaf: A1: Use Infected USB Flash Drive.
    │   └── Leaf: A2: Social Engineering to Insert Malware.
    └── OR: G1.2: Exploit Windows Vulnerabilities.
        └── Leaf: A3: Exploit Windows Zero-Day Vulnerabilities (LNK, Print Spooler, etc.).
```

## BlackEnergy – Ukraine Power Grid Attacks (2015)
```
GOAL: Cause Power Outage & Delay Recovery (Root Node)
└── AND: Compromise IT Network AND Pivot to OT Network AND Execute Cyber-Physical Payload
    ├── AND: Compromise IT Network (Initial Access)
    │   ├── OR: Phishing Attack OR Exploit External Services
    │   │   ├── Leaf: Phishing Email (BlackEnergy Macro)
    │   │   └── Leaf: Exploit Public-Facing Server (VPN/Email Server)
    │   └── AND: Lateral Movement AND Credential Harvesting
    │       ├── Leaf: Use BlackEnergy to Collect Credentials (Stored on IT Systems)
    │       └── Leaf: Use Valid Accounts for Access
    ├── AND: Pivot to OT Network
    │   ├── OR: Access via Dual-Homed Server OR Access via VPN/Jump Host
    │   └── Leaf: Exploit Trust Relationship between IT and OT segments
    └── AND: Execute Cyber-Physical Payload (Simultaneous Actions)
        ├── AND: Issue Remote Trip Command AND Disable Local Control AND Delay Manual Recovery
        │   ├── Leaf: Issue Trip Command (Open Breakers via SCADA/HMI)
        │   └── Leaf: Disable Local Control (Flash Malicious Firmware on Serial-to-Ethernet Converters)
        └── AND: Wipe Critical Files/OS AND Disrupt Operator Communications
            ├── Leaf: Wipe Servers/Workstations with KillDisk
            └── Leaf: Telephony DoS Attack on Call Center (Preventing Customer Reports)
```

## TRITON – Attack on Safety Systems (SIS) (2017)
```
GOAL: Cause Physical Damage / Unsafe State (Explosion/Fire)
└── AND: Compromise Corporate IT AND Pivot to OT Network AND Deploy TRITON Framework
    ├── AND: Compromise Corporate IT (Initial Access & Persistence)
    │   ├── OR: Phishing Attack OR Exploit External Services
    │   │   ├── Leaf: Phishing Email (Targeted Malicious Attachments)
    │   │   └── Leaf: Exploit External VPN/RDP Access
    │   └── AND: Lateral Movement AND Credential Harvesting
    │       ├── Leaf: Harvest Credentials (Mimikatz/SecHack from Memory)
    │       └── Leaf: Establish Persistence (Cryptcat/Web Shells/Renamed Binaries)
    ├── AND: Pivot to OT Network (Lateral Movement)
    │   ├── OR: Traverse DMZ via Misconfiguration OR Admin Tools
    │   │   ├── Leaf: Exploit Firewall Misconfigurations between IT/OT
    │   │   └── Leaf: Use RDP/PsExec to Jump Box (Living off the Land)
    │   └── Leaf: Compromise Engineering Workstation (SIS Engineering Station)
    └── AND: Deploy TRITON Framework (Cyber-Physical Payload)
        ├── AND: Reconnaissance AND Injection AND Logic Modification
        │   ├── Leaf: Reverse Engineer TriStation Protocol (UDP 1502)
        │   ├── Leaf: Identify Target Controller (Schneider Electric Triconex MP3008)
        │   └── Leaf: Inject Malware via Zero-Day Firmware Exploit (Get Execute Primitive)
        └── AND: Execution (Attempted Unsafe State)
            ├── Leaf: Modify Logic to Disable Failsafes (Prevent Safety Trip)
            └── Leaf: Controller Crash (Attack Failure due to Validator Check/Safe Mode Trip)
```

## The Attack on Oldsmar Water Treatment Plant, Florida (2021)
```
```
