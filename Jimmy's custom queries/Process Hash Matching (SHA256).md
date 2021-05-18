//Search across these event types
find in (DeviceProcessEvents , DeviceFileEvents, DeviceRegistryEvents , DeviceLogonEvents, DeviceImageLoadEvents, DeviceEvents)
//Search SHA256 hash values from comma separated list below:
where InitiatingProcessSHA256 has_any ("EAF3D06BFE9E87CF055128CFEF4AC83700D663D333E66F50CFE74536F8C78FE9",
"BA9FA197E8B99BB5BAE0AA498DC0054E16C38D6AA4D00005358A20C698A93147")