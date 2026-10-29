# Rules of Engagement (RoE)

## 1. Purpose
Define the legal scope and safety rules for an educational ethical hacking lab.

## 2. Authorization
The tester may test only the local OWASP Juice Shop instance installed and controlled by the tester. This authorization does not cover any external system.

## 3. In-Scope Target
- Application: OWASP Juice Shop
- Runtime: Local Docker container
- URL: http://127.0.0.1:3000
- Port: TCP 3000, loopback-bound
- Data: Synthetic test data only

## 4. Permitted Activities
- Manual application browsing
- Inspection of HTTP requests and responses
- Harmless input validation tests
- Controlled beginner-level security exercises against the local target
- Documentation of findings and recommended fixes

## 5. Prohibited Activities
- Testing systems not owned or explicitly authorized by the tester
- Testing public websites, college systems, or third-party networks
- Denial-of-service and destructive testing
- Phishing, credential theft, and collection of real personal information
- Attempts to escape the container or compromise the host
- Testing any target outside the approved scope

## 6. Isolation Requirements
- Bind the application port to 127.0.0.1 only.
- Do not configure router port forwarding or public exposure.
- Verify the target address before testing.
- Use a dedicated isolated VM/network for stronger isolation when required.
- Treat localhost binding as one safety control, not proof of complete isolation.

## 7. Stop Conditions
Stop immediately if:
- The target address is unexpected.
- Testing reaches an external system.
- Unexpected sensitive data is encountered.
- The host becomes unstable.
- Isolation or authorization becomes uncertain.

## 8. Evidence Handling
Capture genuine screenshots of the running lab and port binding. Do not include credentials, tokens, or personal data. Record actual verification results accurately.

## 9. Cleanup
Stop the Docker container after the exercise. Remove it when no longer required, and recreate a clean baseline before another test session.

## 10. Scope Statement
This is a self-authorized educational lab. No permission to test third-party systems is granted.

**Status:** Rules documented. Technical isolation and evidence checks must be verified separately.
