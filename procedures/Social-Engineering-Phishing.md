** Social-Engineering (Email Phishing) **


### DETECT

### ANALYZE
* Identify impacted user/mailbox/email address
* Capture phishing email artificact (export/save as EML or MSG file)
* Search Audit Logs, Azure Sign-In data, Message Trace
* Inspect user mailbox rules/forwarding rules

### CONTAIN
* Disable email login
  * O365: 
  * AD/OnPrem Exchange
  * Other system: depentant on application
* Disable/Remove malicious mailbox rules
* 
 

### ERADICATE
#### Purge phishing email from all mailboxes
* Create new Content Search
  * https://protection.office.com/contentsearchbeta?ContentOnly=1
  * Create new search with date-range, subject line, details from message body....(goal is to limit scope)
* Export contents, save to incident file
* Execute Purge (using search form above)
```powershell
Set-ExecutionPolicy RemoteSigned
$UserCredential = Get-Credential
$Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
Import-PSSession $Session -DisableNameChecking
New-ComplianceSearchAction -SearchName "XXX" -Purge -PurgeType HardDelete
```

### RECOVER



