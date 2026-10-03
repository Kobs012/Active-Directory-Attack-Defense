# MITRE ATT&CK Mapping

The mappings below describe the controlled behaviors demonstrated or attempted in the lab.

| Activity | ATT&CK Technique | Status |
|---|---|---|
| Nmap service discovery | `T1046` Network Service Discovery | Successful |
| Domain-user enumeration | `T1087.002` Account Discovery: Domain Account | Successful |
| Domain-group enumeration | `T1069.002` Permission Groups Discovery: Domain Groups | Successful |
| SMB share discovery | `T1135` Network Share Discovery | Successful |
| Password spraying / reuse testing | `T1110.003` Brute Force: Password Spraying | Successful |
| Authentication with discovered/known domain credentials | `T1078.002` Valid Accounts: Domain Accounts | Successful |
| Kerberoasting | `T1558.003` Steal or Forge Kerberos Tickets: Kerberoasting | Attempted; unsuccessful |
| AS-REP roasting | `T1558.004` Steal or Forge Kerberos Tickets: AS-REP Roasting | Attempted; no eligible account |

## Notes

The lab does not claim a technique as successful merely because a command was run.

For Kerberoasting and AS-REP roasting, the repository explicitly records the failed/partial result.
