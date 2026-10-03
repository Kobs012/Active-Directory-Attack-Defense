# Screenshot Index

| File | What it shows | Recommended use |
|---|---|---|
| `01.png` | VMware `VMnet2`, host-only `10.10.10.0/24` | README / Architecture |
| `02.png` | `DC01` Server Manager / server state | Build Notes |
| `03.png` | Early Active Directory view | Build Notes |
| `04.png` | DNS Manager and `adlab.test` records | Build Notes |
| `05.png` | Final OU structure | README / Architecture |
| `06.png` | Example IT OU users/group | Architecture |
| `07.png` | `acarter` domain identity and Kerberos tickets | README / Build |
| `08.png` | PowerShell Operational / 4104 logging | Telemetry |
| `09.png` | Sysmon Event 1 process telemetry | Telemetry |
| `10.png` | Additional Sysmon event evidence | Telemetry |
| `11.png` | Sysmon DNS-query events | Telemetry |
| `12.png` | DNS resolution and early Nmap scans | Enumeration |
| `13.png` | LDAP base query and anonymous SMB limitation | Enumeration / Troubleshooting |
| `14.png` | LDAP-signing error followed by authenticated SMB success | Troubleshooting |
| `15.png` | NetExec shares + domain users | Enumeration |
| `16.png` | Domain-group enumeration | Enumeration |
| `17.png` | Focused Nmap scan of AD services | README / Enumeration |
| `18.png` | Initial multi-user shared-password success | README / Attack |
| `19.png` | Filtered successful 4624 network logons | Investigation |
| `20.png` | Repeated shared-password success | Attack |
| `21.png` | Authenticated SMB share enumeration | Enumeration |
| `22.png` | SYSVOL GPO/audit file retrieval | Enumeration |
| `23.png` | Authenticated LDAP check / MachineAccountQuota | Enumeration |
| `24.png` | `svc_sql` SPN and encryption configuration | Kerberoast troubleshooting |
| `25.png` | AS-REP attempt returning no eligible entries | Troubleshooting |
| `26.png` | Filtered 4625 failures from `10.10.10.30` | Investigation |
| `27.png` | Broad successful 4624 activity from `10.10.10.30` | Investigation |
| `28.png` | Event 4776 successful credential validation | Investigation |
| `29.png` | Domain Account Lockout Policy GPO linked to `adlab.test` | Hardening |
| `30.png` | Account lockout settings in GPO editor | Hardening |
| `31.png` | Effective domain lockout policy `5 / 15 / 15` | README / Hardening |
| `32.png` | Old password fails; new password succeeds | README / Retest |
| `33.png` | Old shared password fails for all five users | README / Retest |
| `34.png` | Final 4625 failures for all remediated users | README / Retest |
| `bloodhoundlogin.png` | BloodHound Community Edition login page | Troubleshooting |
| `failure.png` | BloodHound JSON ingestion failures | Troubleshooting |
| `KDC_ERR_ETYPE_NOSUPP.png` | Kerberos encryption-type mismatch during ticket request | Troubleshooting |

## Strongest portfolio screenshots

If the README needs to stay visually short, prioritize:

1. `01.png` - isolated architecture
2. `05.png` - AD structure
3. `17.png` - AD service discovery
4. `18.png` - successful weakness validation
5. `19.png` or `27.png` - successful defender-side correlation
6. `31.png` - effective hardening
7. `33.png` - failed post-hardening attack
8. `34.png` - defender-side confirmation after remediation

The remaining images work better inside the supporting documentation.
