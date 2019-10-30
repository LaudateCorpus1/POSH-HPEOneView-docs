---
description: Add X.509 SSL certificates to appliance trusted store.
---

# Add-HPOVApplianceTrustedCertificate

## HPE OneView 5.00 Library

### Syntax

```text
Add-HPOVApplianceTrustedCertificate [-Path] <System.IO.FileInfo> [[-AliasName] <String>] [[-Force] <SwitchParameter>] [[-Async] <SwitchParameter>] [[-ApplianceConnection] <Object>] [<CommonParameters>]
```

```text
Add-HPOVApplianceTrustedCertificate [-CertObject] <Object> [[-AliasName] <String>] [[-Force] <SwitchParameter>] [[-Async] <SwitchParameter>] [[-ApplianceConnection] <Object>] [<CommonParameters>]
```

```text
Add-HPOVApplianceTrustedCertificate [-ComputerName] <String> [[-Port] <Int>] [[-AliasName] <String>] [[-Force] <SwitchParameter>] [[-Async] <SwitchParameter>] [[-ApplianceConnection] <Object>] [<CommonParameters>]
```

### Detailed Description

This Cmdlet will allow the Infrastructure Administrator to add X.509 compliant SSL certificates to the appliance trusted store.

### Parameters

#### -AliasName &lt;String&gt; 

Specify an alias name of the certificate stored on the appliance. By default, the Subject name will be used.

| Aliases | None |
| :--- | :--- |
| Required? | False |
| Position? | named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

#### -ApplianceConnection &lt;Object&gt;

Specify one or more `[HPOneView.Appliance.Connection]` objects or Name property values.

| Aliases | Appliance |
| :--- | :--- |
| Required? | false |
| Position? | named |
| Default value | \(${Global:ConnectedSessions} \| ? Default\) |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

#### -Async &lt;SwitchParameter&gt; 

Use this parameter to immediately return the async task. By default, the Cmdlet will wait for the task to complete.

| Aliases | None |
| :--- | :--- |
| Required? | False |
| Position? | named |
| Default value | False |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

#### -CertObject &lt;Object&gt; 

Specify the public Base64 encoded string X.509 certificate of the remote endpoint to add to the appliances internal trust store.

| Aliases | None |
| :--- | :--- |
| Required? | True |
| Position? | named |
| Default value |  |
| Accept pipeline input? | true \(ByValue\) |
| Accept wildcard characters?    | False |

#### -ComputerName &lt;String&gt; 

The remote endpoint Computer Name or IP Address. This should match either the X.509 Subject or Subject Alternative Name fields with in the cert object. If omitting the -CertObject parameter, the Cmdlet will initiate a TCP connection in order to retrieve the certificate. Use the -Port parameter to specify the correct TCP port the SSL/TLS service is listening on.

| Aliases | None |
| :--- | :--- |
| Required? | False |
| Position? | named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

#### -Force &lt;SwitchParameter&gt; 

Use to force add an untrusted \(self-signed or a certificate authority certificate has not been added to the appliance\) certificate into the appliances trust store.

| Aliases | None |
| :--- | :--- |
| Required? | False |
| Position? | named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

#### -Path &lt;System.IO.FileInfo&gt; 

The filesystem object of the X.509 public SSL certificate to add.

| Aliases | None |
| :--- | :--- |
| Required? | true |
| Position? | named |
| Default value |  |
| Accept pipeline input? | true \(ByValue\) |
| Accept wildcard characters?    | False |

#### -Port &lt;Int&gt; 

Specify the TCP port where the TLS/SSL service is bound and listening on. Use with the -ComputerName parameter.

| Aliases | None |
| :--- | :--- |
| Required? | False |
| Position? | named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

&lt;CommonParameters&gt;

This cmdlet supports the common parameters: Verbose, Debug, ErrorAction, ErrorVariable, WarningAction, WarningVariable, OutBuffer, PipelineVariable, and OutVariable. For more information, see about\_CommonParameters \([http://go.microsoft.com/fwlink/?LinkID=113216](http://go.microsoft.com/fwlink/?LinkID=113216)\)

### Input Types

_**System.IO.FileInfo**_

The filesystem object of the X.509 public SSL certificate to add.

### Return Values

_**HPOneView.Appliance.TaskResource \[System.Management.Automation.PSCustomObject\]**_

Asyncronous task resource to monitor.

### Examples

```text
 -------------------------- EXAMPLE 1 --------------------------
Get-ChildItem C:\Path\srv1-pub.cer | Add-HPOVApplianceTrustedCertificate
```

 Add the provided offline certificate to the appliance trust store.

```text
 -------------------------- EXAMPLE 2 --------------------------
Add-HPOVApplianceTrustedCertificate -ComputerName $RemoteBackupHostname -Port 443 -AliasName backupserver -Async -Outvariable Task
```

 Use the Cmdlet to add the remote certificate to the appliance trust store without waiting for the task to complete.

```text
 -------------------------- EXAMPLE 3 --------------------------
Add-HPOVApplianceTrustedCertificate -ComputerName server1-ilo.domain.com -AliasName server1iLo -force
```

 Use the Cmdlet to add the self-signed iLO certificate to the appliance. 

### Related Links 

* [Get-HPOVApplianceTrustedCertificate](https://github.com/HewlettPackard/POSH-HPOneView/wiki/Get-HPOVApplianceTrustedCertificate) 
* [Remove-HPOVApplianceTrustedCertificate](https://github.com/HewlettPackard/POSH-HPOneView/wiki/Remove-HPOVApplianceTrustedCertificate) 

## HPE OneView 4.20 Library

### Syntax

```text
Add-HPOVApplianceTrustedCertificate [-Path] <System.IO.FileInfo> [[-AliasName] <String>] [[-Force] <SwitchParameter>] [[-Async] <SwitchParameter>] [[-ApplianceConnection] <Object>] [<CommonParameters>]
```

```text
Add-HPOVApplianceTrustedCertificate [-CertObject] <Object> [[-AliasName] <String>] [[-Force] <SwitchParameter>] [[-Async] <SwitchParameter>] [[-ApplianceConnection] <Object>] [<CommonParameters>]
```

```text
Add-HPOVApplianceTrustedCertificate [-ComputerName] <String> [[-Port] <Int>] [[-AliasName] <String>] [[-Force] <SwitchParameter>] [[-Async] <SwitchParameter>] [[-ApplianceConnection] <Object>] [<CommonParameters>]
```

### Detailed Description

This Cmdlet will allow the Infrastructure Administrator to add X.509 compliant SSL certificates to the appliance trusted store.

### Parameters

#### -AliasName &lt;String&gt; 

Specify an alias name of the certificate stored on the appliance. By default, the Subject name will be used.

| Aliases | None |
| :--- | :--- |
| Required? | False |
| Position? | named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

#### -ApplianceConnection &lt;Object&gt;

Specify one or more `[HPOneView.Appliance.Connection]` objects or Name property values.

| Aliases | Appliance |
| :--- | :--- |
| Required? | false |
| Position? | named |
| Default value | \(${Global:ConnectedSessions} \| ? Default\) |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

#### -Async &lt;SwitchParameter&gt; 

Use this parameter to immediately return the async task. By default, the Cmdlet will wait for the task to complete.

| Aliases | None |
| :--- | :--- |
| Required? | False |
| Position? | named |
| Default value | False |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

#### -CertObject &lt;Object&gt; 

Specify the public Base64 encoded string X.509 certificate of the remote endpoint to add to the appliances internal trust store.

| Aliases | None |
| :--- | :--- |
| Required? | True |
| Position? | named |
| Default value |  |
| Accept pipeline input? | true \(ByValue\) |
| Accept wildcard characters?    | False |

#### -ComputerName &lt;String&gt; 

The remote endpoint Computer Name or IP Address. This should match either the X.509 Subject or Subject Alternative Name fields with in the cert object. If omitting the -CertObject parameter, the Cmdlet will initiate a TCP connection in order to retrieve the certificate. Use the -Port parameter to specify the correct TCP port the SSL/TLS service is listening on.

| Aliases | None |
| :--- | :--- |
| Required? | False |
| Position? | named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

#### -Force &lt;SwitchParameter&gt; 

Use to force add an untrusted \(self-signed or a certificate authority certificate has not been added to the appliance\) certificate into the appliances trust store.

| Aliases | None |
| :--- | :--- |
| Required? | False |
| Position? | named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

#### -Path &lt;System.IO.FileInfo&gt; 

The filesystem object of the X.509 public SSL certificate to add.

| Aliases | None |
| :--- | :--- |
| Required? | true |
| Position? | named |
| Default value |  |
| Accept pipeline input? | true \(ByValue\) |
| Accept wildcard characters?    | False |

#### -Port &lt;Int&gt; 

Specify the TCP port where the TLS/SSL service is bound and listening on. Use with the -ComputerName parameter.

| Aliases | None |
| :--- | :--- |
| Required? | False |
| Position? | named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

&lt;CommonParameters&gt;

This cmdlet supports the common parameters: Verbose, Debug, ErrorAction, ErrorVariable, WarningAction, WarningVariable, OutBuffer, PipelineVariable, and OutVariable. For more information, see about\_CommonParameters \([http://go.microsoft.com/fwlink/?LinkID=113216](http://go.microsoft.com/fwlink/?LinkID=113216)\)

### Input Types

_**System.IO.FileInfo**_

The filesystem object of the X.509 public SSL certificate to add.

### Return Values

_**HPOneView.Appliance.TaskResource \[System.Management.Automation.PSCustomObject\]**_

Asyncronous task resource to monitor.

### Examples

```text
 -------------------------- EXAMPLE 1 --------------------------
Get-ChildItem C:\Path\srv1-pub.cer | Add-HPOVApplianceTrustedCertificate
```

 Add the provided offline certificate to the appliance trust store.

```text
 -------------------------- EXAMPLE 2 --------------------------
Add-HPOVApplianceTrustedCertificate -ComputerName $RemoteBackupHostname -Port 443 -AliasName backupserver -Async -Outvariable Task
```

 Use the Cmdlet to add the remote certificate to the appliance trust store without waiting for the task to complete.

```text
 -------------------------- EXAMPLE 3 --------------------------
Add-HPOVApplianceTrustedCertificate -ComputerName server1-ilo.domain.com -AliasName server1iLo -force
```

 Use the Cmdlet to add the self-signed iLO certificate to the appliance. 

### Related Links 

* [Get-HPOVApplianceTrustedCertificate](https://github.com/HewlettPackard/POSH-HPOneView/wiki/Get-HPOVApplianceTrustedCertificate) 
* [Remove-HPOVApplianceTrustedCertificate](https://github.com/HewlettPackard/POSH-HPOneView/wiki/Remove-HPOVApplianceTrustedCertificate) 

## HPE OneView 4.10 Library

### Syntax

```text
Add-HPOVApplianceTrustedCertificate [-Path] <System.IO.FileInfo> [[-AliasName] <String>] [[-Force] <SwitchParameter>] [[-Async] <SwitchParameter>] [[-ApplianceConnection] <Object>] [<CommonParameters>]
```

```text
Add-HPOVApplianceTrustedCertificate [-CertObject] <Object> [[-AliasName] <String>] [[-Force] <SwitchParameter>] [[-Async] <SwitchParameter>] [[-ApplianceConnection] <Object>] [<CommonParameters>]
```

```text
Add-HPOVApplianceTrustedCertificate [-ComputerName] <String> [[-Port] <Int>] [[-AliasName] <String>] [[-Force] <SwitchParameter>] [[-Async] <SwitchParameter>] [[-ApplianceConnection] <Object>] [<CommonParameters>]
```

### Detailed Description

This Cmdlet will allow the Infrastructure Administrator to add X.509 compliant SSL certificates to the appliance trusted store.

### Parameters

#### -AliasName &lt;String&gt; 

Specify an alias name of the certificate stored on the appliance. By default, the Subject name will be used.

| Aliases | None |
| :--- | :--- |
| Required? | False |
| Position? | named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

#### -ApplianceConnection &lt;Object&gt;

Specify one or more `[HPOneView.Appliance.Connection]` objects or Name property values.

| Aliases | Appliance |
| :--- | :--- |
| Required? | false |
| Position? | named |
| Default value | \(${Global:ConnectedSessions} \| ? Default\) |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

#### -Async &lt;SwitchParameter&gt; 

Use this parameter to immediately return the async task. By default, the Cmdlet will wait for the task to complete.

| Aliases | None |
| :--- | :--- |
| Required? | False |
| Position? | named |
| Default value | False |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

#### -CertObject &lt;Object&gt; 

Specify the public Base64 encoded string X.509 certificate of the remote endpoint to add to the appliances internal trust store.

| Aliases | None |
| :--- | :--- |
| Required? | True |
| Position? | named |
| Default value |  |
| Accept pipeline input? | true \(ByValue\) |
| Accept wildcard characters?    | False |

#### -ComputerName &lt;String&gt; 

The remote endpoint Computer Name or IP Address. This should match either the X.509 Subject or Subject Alternative Name fields with in the cert object. If omitting the -CertObject parameter, the Cmdlet will initiate a TCP connection in order to retrieve the certificate. Use the -Port parameter to specify the correct TCP port the SSL/TLS service is listening on.

| Aliases | None |
| :--- | :--- |
| Required? | False |
| Position? | named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

#### -Force &lt;SwitchParameter&gt; 

Use to force add an untrusted \(self-signed or a certificate authority certificate has not been added to the appliance\) certificate into the appliances trust store.

| Aliases | None |
| :--- | :--- |
| Required? | False |
| Position? | named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

#### -Path &lt;System.IO.FileInfo&gt; 

The filesystem object of the X.509 public SSL certificate to add.

| Aliases | None |
| :--- | :--- |
| Required? | true |
| Position? | named |
| Default value |  |
| Accept pipeline input? | true \(ByValue\) |
| Accept wildcard characters?    | False |

#### -Port &lt;Int&gt; 

Specify the TCP port where the TLS/SSL service is bound and listening on. Use with the -ComputerName parameter.

| Aliases | None |
| :--- | :--- |
| Required? | False |
| Position? | named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

&lt;CommonParameters&gt;

This cmdlet supports the common parameters: Verbose, Debug, ErrorAction, ErrorVariable, WarningAction, WarningVariable, OutBuffer, PipelineVariable, and OutVariable. For more information, see about\_CommonParameters \([http://go.microsoft.com/fwlink/?LinkID=113216](http://go.microsoft.com/fwlink/?LinkID=113216)\)

### Input Types

_**System.IO.FileInfo**_

The filesystem object of the X.509 public SSL certificate to add.

### Return Values

_**HPOneView.Appliance.TaskResource \[System.Management.Automation.PSCustomObject\]**_

Asyncronous task resource to monitor.

### Examples

```text
 -------------------------- EXAMPLE 1 --------------------------
Get-ChildItem C:\Path\srv1-pub.cer | Add-HPOVApplianceTrustedCertificate
```

 Add the provided offline certificate to the appliance trust store.

```text
 -------------------------- EXAMPLE 2 --------------------------
Add-HPOVApplianceTrustedCertificate -ComputerName $RemoteBackupHostname -Port 443 -AliasName backupserver -Async -Outvariable Task
```

 Use the Cmdlet to add the remote certificate to the appliance trust store without waiting for the task to complete.

```text
 -------------------------- EXAMPLE 3 --------------------------
Add-HPOVApplianceTrustedCertificate -ComputerName server1-ilo.domain.com -AliasName server1iLo -force
```

 Use the Cmdlet to add the self-signed iLO certificate to the appliance. 

### Related Links 

* [Get-HPOVApplianceTrustedCertificate](https://github.com/HewlettPackard/POSH-HPOneView/wiki/Get-HPOVApplianceTrustedCertificate) 
* [Remove-HPOVApplianceTrustedCertificate](https://github.com/HewlettPackard/POSH-HPOneView/wiki/Remove-HPOVApplianceTrustedCertificate) 
