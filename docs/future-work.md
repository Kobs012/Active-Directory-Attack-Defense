# Future Work

The current lab is complete for its main objective: build an AD environment, simulate a credential weakness, investigate the resulting telemetry, harden the environment, and prove the original attack no longer succeeds.

The following items are intentionally left as future extensions.

## 1. Repair BloodHound

- increase RAM available to the BloodHound host
- verify swap and service limits
- perform a clean SharpHound collection
- import a small dataset first
- confirm graph population
- document at least one path-analysis example

## 2. Rebuild Kerberoasting scenario

Create a disposable service account whose SPN and supported Kerberos encryption types are intentionally compatible with the test.

Then:

- request the service ticket
- capture the ticket material
- document the relevant DC Kerberos events
- harden the service account afterward

## 3. Add an AS-REP-roastable test account

Create one disposable account with Kerberos preauthentication disabled solely for the lab.

Then:

- validate the technique
- capture the DC telemetry
- re-enable preauthentication
- retest and show the attack no longer works

## 4. Repair Default Domain Policy permissions

Resolve the AD/SYSVOL permission mismatch and return lockout settings to normal GPO-based administration.

After repair:

- run `gpupdate`
- verify replication/policy application
- recheck effective domain settings

## 5. Expand detection logic

Potential defensive extensions:

- PowerShell hunting queries for bursts of `4625`
- correlation of one source IP across many usernames
- detection of successful `4624` events immediately following repeated failures
- correlation with `4776`
- alert logic for service-ticket anomalies once Kerberoasting is rebuilt

## 6. Centralize telemetry

A future version could forward the AD lab's Windows events into a SIEM such as Wazuh or Microsoft Sentinel and convert the manual investigation into repeatable detection rules.
