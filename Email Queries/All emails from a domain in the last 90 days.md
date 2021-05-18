## Find mail from the specified domain within the last 90 days

let attackerDomain = 'dataminr.com'; #Replace "dataminr.com" with the relevant URL
EmailEvents
| where SenderMailFromDomain contains attackerDomain and Timestamp > ago(90d)
| summarize count() by RecipientEmailAddress  
