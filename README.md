# Windows Privilege Escalation

A practical Windows privilege escalation knowledge base for penetration testing, red-team labs, CTFs, and security research.

## Contents

- [Methodology](./methodology/privilege-escalation-methodology.md)
- [Enumeration](./enumeration/)
- [Privilege Escalation Techniques](./techniques/)
- [Automated Tools](./tools/)
- [Exploit Research](./exploits/)
- [Reverse Shells](./shells/)
- [Labs](./labs/)
- [References](./references/)

## Scope

This repository focuses on **local Windows privilege escalation** after initial access or authenticated local access.

It covers:

- Host and security-context enumeration
- Users, groups, privileges, services, scheduled tasks, registry and filesystem permissions
- Credential exposure
- Service and application misconfigurations
- DLL/path hijacking concepts
- UAC-related security research
- Kernel exploit research
- Automated enumeration and exploit-suggestion tools
- Reverse-shell and payload references
- Validation, false positives, and defensive considerations

## Safety

Use these techniques only on systems you are authorized to assess, such as your own systems, approved client environments, CTFs, or dedicated labs.

This repository is intentionally structured as a learning and assessment reference rather than a collection of ready-to-run attacks.

## Technique Format

Each technique should document:

1. Overview
2. Preconditions
3. Enumeration
4. Manual validation
5. Automated enumeration
6. Exploitation concept
7. Evidence / expected result
8. Common false positives
9. Defensive notes
10. References

## Tool Status

Tool status should be treated as a maintenance/coverage indicator, not a quality ranking. Legacy or deprecated tools can still be useful for understanding historical techniques or validating older systems.

## External References

See [references/guides.md](./references/guides.md), [references/exploit-databases.md](./references/exploit-databases.md), and [references/external-tools.md](./references/external-tools.md).
