# Security Decisions

## Isolated network

Attack traffic stayed on the VMware host-only `10.10.10.0/24` segment.

## Disposable lab identities

The users and passwords in this project were created only for the lab.

No production accounts were used.

## Controlled scope

Enumeration, credential testing, and attack simulations targeted only:

- `DC01`
- `CLIENT01`
- the intentionally created `adlab.test` identities

## Limited password-spray scope

The main password test used a very small list of lab accounts. After the lockout threshold was configured, retesting was limited to one controlled attempt per account so the validation did not unnecessarily lock users.

## Failed techniques were not forced

BloodHound, Kerberoasting, and AS-REP roasting were not represented as successful when their required conditions were not met.

Instead, the failures were documented along with what was learned and how the scenarios could be rebuilt later.

## Effective-state validation

The account-lockout control was verified with Active Directory's effective domain policy rather than relying only on the GPO editor.

That verification caught a configuration problem before the lab was marked complete.
