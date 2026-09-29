# System Enumeration

## Objectives

Identify the Windows version, architecture, hostname, installation details, patch context, environment variables, and security controls.

## Useful Data

- OS version/build
- Architecture
- Hostname
- Domain/workgroup
- Environment variables
- Installed updates
- Security products
- Running processes
- System directories

## Validation

Correlate version and patch information with authoritative vendor documentation before treating a kernel or application issue as applicable.

## False Positives

- Old version strings without missing patches
- Third-party scanners reporting generic CVEs
- Architecture mismatch
- Vulnerability requires a feature that is not installed
