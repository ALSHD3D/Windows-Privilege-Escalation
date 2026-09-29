# Windows Privilege Escalation Methodology

## 1. Establish Context

Before testing, determine:

- Current username
- Current integrity level
- Local vs domain context
- Group memberships
- Enabled/disabled privileges
- OS version and architecture
- Hostname
- Security products
- Network interfaces
- Current working directory
- Available administrative paths

Do not assume that a finding is exploitable merely because an enumeration tool reports it.

## 2. Enumerate Broadly

Prioritize:

1. System information
2. Users and groups
3. Token privileges
4. Services
5. Scheduled tasks
6. Registry
7. Filesystem permissions
8. Installed software
9. Credentials and secrets
10. Network configuration
11. Security controls
12. Patch/kernel information

## 3. Identify Candidate Paths

For every candidate, ask:

- What permission does the current user have?
- What privileged process or account uses the resource?
- Can the resource actually be modified?
- Is the configuration reachable?
- Is there a dependency that blocks exploitation?
- Is the reported issue a real security boundary crossing?

## 4. Validate Manually

Automated tools are discovery aids.

A candidate should normally be manually validated by checking:

- Effective permissions
- Owner
- Service/task configuration
- Execution context
- File paths
- Registry values
- DLL search behavior
- Version/patch applicability
- Environmental constraints

## 5. Select the Least-Complex Valid Path

Prefer the simplest **authorized** path that can be demonstrated reliably.

Avoid unnecessary changes to the target.

## 6. Document Evidence

Record:

- Initial security context
- Enumeration evidence
- Vulnerable configuration
- Validation steps
- Result
- Privileged security context obtained, if applicable
- Cleanup
- Defensive recommendation

## 7. False-Positive Discipline

A tool finding is not proof of exploitability.

Use these states:

- `Observed` — configuration exists
- `Interesting` — configuration may be security-relevant
- `Validated` — permissions/conditions confirmed
- `Exploitable` — authorized test demonstrated impact
- `Not Exploitable` — required condition is absent
- `Unknown` — insufficient evidence

## Decision Flow

```text
Initial access
     |
     v
Identify current context
     |
     v
System + user + privilege enumeration
     |
     v
Services / tasks / registry / filesystem / credentials
     |
     v
Candidate finding?
   /       \
 No         Yes
 |           |
 v           v
Continue   Manual validation
             |
        +----+----+
        |         |
     Invalid    Valid
        |         |
        v         v
    Record      Assess impact
                   |
                   v
              Authorized test
                   |
                   v
               Document
```
