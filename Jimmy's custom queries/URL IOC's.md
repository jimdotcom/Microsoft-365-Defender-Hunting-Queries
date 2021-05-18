# Replace the list of IOC's below with content from advisory notices to scan monitored endpoints in Defender 365.

find in (EmailUrlInfo, DeviceNetworkEvents, DeviceEvents)
where RemoteUrl in ("https://api.onedrive.com/v1.0/shares/s!Ajp1Jcp4TBtmgRyuTf0Ow-_r40_x/driveitem/content",
    "https://www.dropbox.com/s/qf15ewsstzk4qoz/Thesis%20Information%20to%20be%20referenced%20from.ppt?dl=0",
    "https://uceaf62bf364381a378c816b41ba.dl.dropboxusercontent.com/cd/0/get/A2Vm2UTAy5MCwUTkAgc7zFzIQyACqaHZ2yiX2ORjm3twvsr6cvxtZv0ARG5lyIZq4N60QtQgVm5JL5pTbto45FtwfTs8d9-QuL3_YsAukrIOoZLpoOKRi_DRl5Wxq6TQHIk/file?dl=1",
    "https://login.contact.cybersecuritiesinc.net/",
    "https://login.microsoftonline.com/common/oauth2/v2.0/authorize?response_type=code&client_id=8f43aaa9-d9d7-4eb1-8172-0669dae105aa&redirect_uri=https://www.mailguardonline.net/oauth/api/microsoft/callback&scope=offline_access user.read mail.readwrite&state=EmERFnNRcD2DbezEvK245MXBEokQh6&response_mode=form_post",
    "https://www.mailguardonline.net/oauth/api/microsoft/callback")