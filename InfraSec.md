# 📋 **Note:**

This document provides a detailed overview of the `Infra-Sec-Check` PowerShell script, designed to perform a basic security audit on Windows endpoints. It highlights its functionalities, requirements, and usage to help users identify and mitigate common security weaknesses.

-----

# **🛡️ Infra-Sec-Check**

This PowerShell script performs a **basic security audit** on a Windows endpoint, identifying **weak configurations** and generating an **HTML report** with actionable recommendations. It's a valuable tool for quickly assessing the security posture of individual machines.

-----

## **📋 Script Functions**

The `Infra-Sec-Check` script checks for several critical security configurations:

  * **Verifies UAC (User Account Control), Firewall, and Defender**: Ensures these fundamental security features are properly configured.
  * **Revisa BitLocker**: Checks the status of BitLocker disk encryption.
  * **Identifies users with non-expiring passwords**: Flags accounts that might pose a persistent risk.
  * **Enumera los administradores locales**: Lists local administrators, helping to review privileged access.
  * **Verifies if SMBv1 is enabled**: Detects the presence of this outdated and vulnerable protocol.
  * **Revisa si hay parches críticos pendientes**: Checks for critical Windows updates that need to be installed.

-----

## **⚙️ Requirements**

To run the `Infra-Sec-Check` script successfully, ensure the following are met:

  * **PowerShell 5+**: The script requires PowerShell version 5 or newer.

  * **Execute as administrator**: The script must be run with elevated administrative privileges to perform all checks.

  * **`PSWindowsUpdate` module installed**: For reviewing pending patches, the `PSWindowsUpdate` module is required. Install it using the following command:

    ```powershell
    Install-Module -Name PSWindowsUpdate -Force
    ```

-----

## **🚀 Usage**

To run the audit, simply execute the script in a PowerShell window with administrative rights:

```powersershell
.\audit.ps1
```

Upon completion, an **`report.html`** file will be generated in the same directory, containing the audit results and recommendations.
