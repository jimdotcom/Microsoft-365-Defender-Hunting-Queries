let attacker = 'n-ueda@kitakyu-hp.or.jp';
EmailEvents | join EmailUrlInfo on NetworkMessageId
| where Timestamp > ago(12h)
| where SenderMailFromAddress contains attacker or SenderFromAddress contains attacker