# 📁 File Access Issue (Path Length Limitation)

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
