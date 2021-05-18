#Finds devices with AppLocker disabled in the registry

DeviceRegistryEvents
//Find recent DeviceRegistryEvents for AppLocker Registry sub-keys https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-application-control/applocker/applocker-settings
| where Timestamp < ago(30m) and RegistryKey startswith @"HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\SrpV2"
//Filter includes only changes to AppLocker enforcement state from 'Enabled' to 'Disabled'
| where RegistryValueName == "EnforcementMode"
| where RegistryValueData == "0"
| where PreviousRegistryValueData == 1