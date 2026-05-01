# Tier 1 IT Support Portfolio

This repository showcases real IT support issues I have worked on and how I resolved them.



## 👤 User Offboarding (Microsoft 365 / Active Directory)

### Overview
Performed user offboarding for employees by securing accounts, removing access, and preserving data according to organizational procedures.

### Active Directory Actions
- Disabled user accounts
- Reset account passwords
- Removed users from security groups (except required domain local groups)
- Updated Attribute Editor:
  - Set `msExchHideFromAddressLists` to TRUE
  - Verified `proxyAddresses` left as not set

### Microsoft 365 Admin Center
- Blocked user sign-in
- Removed all assigned licenses

### Exchange Admin Center
- Converted user mailboxes to shared mailboxes to retain access
- Ensured mailbox visibility was hidden from address list

### Entra ID (Azure AD)
- Revoked all active sessions
- Enforced re-registration of Multi-Factor Authentication (MFA)

### Result
User access fully removed while maintaining required data and mailbox availability for business use.

### Key Takeway
Followed a structured offboarding process to ensure security, compliance, and proper access management.






## 📷 Camera Issue (Teams / Zoom)

### Issue
User reported camera not functioning across Microsoft Teams, Zoom, and browser. Camera preview appeared black in all applications.

### Investigation
- Verified issue across multiple platforms (Teams, Zoom, browser)
- Disabled and re-enabled camera device in Device Manager
- Checked for application conflicts (Zoom running in background) — no impact
- Confirmed issue persisted regardless of application used

### Resolution
- Navigated to Windows Camera Advanced Settings
- Enabled “Turn on basic camera” (forces device to use standard functionality)

### Validation
- Tested 1:1 calls in Teams and Zoom (desktop and browser)
- Confirmed video and audio functioning correctly
- Verified camera feed visible from external participant

### Result
Camera functioning normally across all applications after enabling basic camera mode.

### Key Takeaway
Enabling basic camera mode can resolve compatibility issues by bypassing advanced camera features, though it may limit functionality such as virtual backgrounds.







## 📁 File Access Issue (Path Length Limitation)

### Issue
User was unable to open or attach files due to a “path too long” error. Issue occurred in File Explorer and when attaching files to email.

### Investigation
- Verified files were accessible via SharePoint/OneDrive web
- Confirmed issue only occurred locally in File Explorer and attachment dialogs
- Identified deeply nested folder structure causing excessive path length

### Findings
Windows file path length limitation (~260 characters in many environments) prevented file access.

### Resolution
- Moved affected files from deeply nested OneDrive directory to a shorter local path (Desktop/Downloads)
- Reduced overall file path length

### Result
- User successfully opened files
- User successfully attached files to email
- Issue fully resolved after shortening path

### Root Cause
Excessive folder depth and long file naming structure exceeded Windows path length limitation.

### Key Takeaway
Deep folder structures can break file access in Windows. Keeping paths shorter or using web access can prevent and resolve these issues.

