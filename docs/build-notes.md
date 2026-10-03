# Build Notes

## Domain Controller

`DC01` was built on Windows Server and configured with Active Directory Domain Services and DNS.

The lab domain is:

```text
adlab.test
```

The domain controller uses:

```text
10.10.10.10
```

Server Manager and the AD/DNS consoles were used throughout setup.

## Windows Client

`CLIENT01` is a Windows 11 endpoint at:

```text
10.10.10.20
```

It was joined to `adlab.test` and used to validate normal domain authentication and endpoint telemetry.

## Kali Attacker

`ATTACK01` is a Kali Linux VM at:

```text
10.10.10.30
```

It was used only for controlled testing against the isolated lab.

Tools used during the project included:

- Nmap
- NetExec
- smbclient
- ldapsearch
- Impacket
- BloodHound / SharpHound tooling

## Directory Objects

The lab included:

- normal employee accounts
- department groups
- a separate administrator account
- a service account with an SPN
- workstations and server OUs

The design intentionally included a small number of weak configurations so that attack, detection, remediation, and retesting could all be demonstrated.

## DNS

`DC01` provided DNS for the domain. Forward lookup records were created for the domain controller and client.

The Kali VM successfully resolved:

- `dc01.adlab.test` -> `10.10.10.10`
- `client01.adlab.test` -> `10.10.10.20`

DNS resolution was verified before attack simulation.
