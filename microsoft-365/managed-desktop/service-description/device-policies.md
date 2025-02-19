---
title: Device configuration 
description: Learn about the default policies applied to Microsoft Managed Desktop devices.
keywords: Microsoft Managed Desktop, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
---

# Device configuration


<!--This topic is the target for a "Learn more" link in the Enterprise Agreement (aka.ms/dev-config); do not delete.-->

<!-- Device configuration and Security Addendum-->

When a new Microsoft Managed Desktop device is being set up, we ensure that it has the right configuration optimized for Microsoft Managed Desktop. This includes a set of default policies that are set as part of the onboarding process. These policies are delivered using Mobile Device Management (MDM) whenever possible. For more information, see [Mobile Device Management](https://docs.microsoft.com/windows/client-management/mdm/). 

>[!NOTE]
>To avoid conflicts, do not alter these policies.

Devices will arrive with a signature image, and then join the Azure Active Directory domain when the first user signs in. The device will automatically install required policies and applications without any intervention from your IT personnel.

## Default policies

This table highlights the default policies that are applied to all Microsoft Managed Desktop devices during device provisioning. All detected changes not approved by Microsoft Managed Desktop Operations Team to objects managed by Microsoft Managed Desktop will be reverted.

Policy | Description
--- | ---
Security baseline | [Microsoft security baseline](https://docs.microsoft.com/windows/device-security/windows-security-baselines) for MDM is configured for all Microsoft Managed Desktop devices. This baseline is the industry-standard configuration. It is publicly released, well tested, and has been reviewed by Microsoft security experts to keep Microsoft Managed Desktop devices and apps secure in the modern workplace. <br><br>To mitigate threats in the constantly evolving security threat landscape, the Microsoft security baseline will be updated and deployed to Microsoft Managed Desktop devices with each Windows 10 feature update.<br><br>For more information, see [Security baseline for Windows 10](https://blogs.technet.microsoft.com/secguide/2017/10/18/security-baseline-for-windows-10-fall-creators-update-v1709-final/).
Microsoft Managed Desktop recommended security template | A set of recommended changes to the security baseline that optimize user experience.  These changes are documented in [the Security Addendum](#security-addendum). Updates to the policy addendum occur on an as needed basis.  
Update deployment | Use Windows Update for Business to perform gradual deployment of software updates. IT admins can’t modify settings for the deployment group policies. For more information on group-based deployment, see [How updates are handled](../working-with-managed-desktop/updates.md).
Diagnostic data | Devices will be set to provide enhanced diagnostic data to Microsoft under a known commercial identifier. As part of Microsoft Managed Desktop, IT admins can not change these settings. For customers in General Data Protection Regulation (GDPR) regions, end users can reduce the level of diagnostic data that is provided, but there will be a reduction in service. For example, Microsoft Managed Desktop will be unable to collect the data necessary to iterate on settings and policies to best serve performance and security needs. For more information, see [Configure Windows diagnostic data in your organization.](https://docs.microsoft.com/windows/privacy/configure-windows-diagnostic-data-in-your-organization#enhanced-level)
Metered connections | By default, updates over metered connections (such as LTE networks) are turned off, though each user can independently turn on this feature in **Settings > Updates > Advanced options**. If you want to allow all users to enable updates over metered connections, [submit a change request](https://docs.microsoft.com/microsoft-365/managed-desktop/working-with-managed-desktop/admin-support), which will turn on this setting for all devices.

 ## Security addendum

 This section outlines the policies that will be deployed in addition to the standard Microsoft Managed Desktop policies listed in [Default policies](#default-policies). This configuration is designed with financial services and highly regulated industries in mind, optimizing for the highest security while maintaining user productivity.

 ### Additional security policies

 These policies are added to increase security for highly regulated industries. 
 - **Security monitoring**: Microsoft will monitor devices using [Microsoft Defender Advanced Threat Protection](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection). If a threat is detected, Microsoft will notify the customer, isolate the device, and rectify the issue remotely. 
 - **Disable PowerShell V2**: Microsoft removed PowerShell V2 in August 2017. This feature has been disabled on all Microsoft Managed Desktop devices. For more information on this change, see [Windows PowerShell 2.0 Deprecation](https://devblogs.microsoft.com/powershell/windows-powershell-2-0-deprecation/).
