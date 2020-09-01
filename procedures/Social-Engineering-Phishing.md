** Virus or Malicous Code Procedure **


### DETECT

### ANALYZE

### CONTAIN

### EREDICATE
#### Purge phishing email from all mailboxes
##### Create new Content Search
##### Execute Purge (using search form above)
```powershell
Set-ExecutionPolicy RemoteSigned
$UserCredential = Get-Credential
$Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
Import-PSSession $Session -DisableNameChecking
New-ComplianceSearchAction -SearchName "XXX" -Purge -PurgeType HardDelete
```

### RECOVER



