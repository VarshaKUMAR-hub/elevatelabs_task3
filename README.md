# elevatelabs_task3
# Vulnerability Scan Report

## Tool Used

Nessus Essentials

## Target
192.168.70.1


## Scan Summary

The scan identified a medium-level vulnerability related to SMB security configuration.

## Critical Findings

### 1. SMB Signing Not Required

#### Severity

Medium

#### Risk

The system does not require SMB signing, which can allow attackers to perform man-in-the-middle (MITM) or SMB relay attacks by intercepting or modifying network communications.

#### Impact

An attacker on the same network may tamper with SMB traffic or capture authentication information.

#### Mitigation

Enable SMB signing on both the SMB client and server settings.

#### Fix Applied

* Enabled:

  * “Microsoft network server: Digitally sign communications (always)”
  * “Microsoft network client: Digitally sign communications (always)”
* Restarted the system after applying changes.

## Conclusion

The vulnerability assessment identified SMB signing configuration as a security weakness. Enabling SMB signing improves the integrity and security of SMB communications and helps protect the system against network-based attacks.

