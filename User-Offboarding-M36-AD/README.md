## 👤 User Offboarding (Microsoft 365 / Active Directory)


## Overview
Performed user offboarding by securing accounts, removing access, and preserving data according to organizational procedures.

## Active Directory Actions
- Disabled user accounts
- Reset account passwords
- Removed users from security groups (except required domain local groups)
- Updated Attribute Editor:
  - Set `msExchHideFromAddressLists` to TRUE
  - Verified `proxyAddresses` left as not set

## Microsoft 365 Admin Center
- Blocked user sign-in
- Removed assigned licenses

## Exchange Admin Center
- Converted user mailboxes to shared mailboxes
- Hid mailbox from address lists

## Entra ID (Azure AD)
- Revoked active sessions
- Enforced re-registration of Multi-Factor Authentication (MFA)

## Result
User access was fully removed while maintaining required data and mailbox availability for business use.

## Key Takeaway
Followed a structured offboarding process to ensure security, compliance, and proper access management.
