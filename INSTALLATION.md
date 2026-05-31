# MIMOC Installation Guide

This document provides a high-level installation checklist for MIMOC Community / Early Access builds.

## Before you install

Before installing MIMOC, verify that you are authorized to deploy and use it in the target environment.

MIMOC is an IT administration tool and may perform operations that affect endpoints, servers and network devices.

## Recommended environment

Use a dedicated Windows machine or Windows Server VM for evaluation.

Recommended minimum for evaluation:

- Windows x64 system;
- local administrator rights for installation;
- SSD storage;
- stable network connectivity to target subnets;
- modern browser such as Microsoft Edge or Google Chrome.

For production-like testing, use a dedicated VM and avoid installing on a personal workstation shared with other services.

## Network and permission planning

Depending on the modules you plan to test, MIMOC may require access to:

- ICMP for reachability checks;
- WMI / RPC for Windows inventory;
- WinRM for remote operations;
- SMB for file copy and deployment scenarios;
- SSH for Linux-related checks, where applicable;
- SNMP or device APIs for network equipment, where configured;
- Wake-on-LAN broadcast or relay paths.

Enable only the protocols required for your test scope.

## Installation package

Early Access builds may be distributed as an installer package together with:

- release notes;
- SHA256 checksum;
- documentation;
- disclaimer;
- security policy.

If the installer is not code-signed, Windows may show a warning. Verify the SHA256 checksum before installation.

## Verify SHA256 on Windows

Open PowerShell and run:

```powershell
Get-FileHash "MIMOC-Setup.exe" -Algorithm SHA256
```

Compare the output with the checksum published in the release notes.

Do not install the file if the checksum does not match.

## Installation steps

1. Download the installer from the authorized Early Access channel.
2. Verify the SHA256 checksum.
3. Run the installer as an administrator.
4. Follow the installation wizard.
5. Open the MIMOC web console using the local URL or configured server address.
6. Create or access the administrative account.
7. Review legal and operational notices inside the application.
8. Configure only the modules required for your test.
9. Start with a small, controlled target group.

## First-run recommendations

After installation:

- review the dashboard;
- verify the application status;
- configure users and roles;
- configure credentials only if required;
- run discovery on a very small subnet or test range;
- verify inventory results;
- test high-impact actions only on non-critical targets;
- configure backup before broader testing.

## Safe testing approach

Start with read-only or low-impact activities:

1. inventory review;
2. limited network discovery;
3. WMI discovery on one or two test machines;
4. software scan on a small group;
5. scheduler test with harmless tasks;
6. Power Manager only on test endpoints;
7. deployment only with safe pilot packages.

Avoid broad deployment, shutdown, reboot or cleanup actions until you understand the environment and have backups.

## Maintenance and backup

Before testing restore or maintenance operations:

- ensure no critical job is running;
- create a backup;
- verify where backups are stored;
- document how to roll back;
- notify affected users if testing in a shared environment.

## Uninstall

Use the Windows application uninstall flow or the uninstall method provided by the installer.

Before uninstalling, export or back up any data you need to retain.

## Support and feedback

For Early Access feedback, use the GitHub repository instructions.

Do not post credentials, private logs, license files, databases or sensitive infrastructure details in public issues.
