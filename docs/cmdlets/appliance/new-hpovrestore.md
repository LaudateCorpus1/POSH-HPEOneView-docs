---
description: Upload appliance backup file to restore its configuration.
---

# New-HPOVRestore

## HPE OneView 5.00 Library

### Syntax

```text
New-HPOVRestore [-FileName] <System.IO.FileInfo> [[-EncryptionKey] <Object>] [[-ApplianceConnection] <Array>] [[-WhatIf] <SwitchParameter>] [[-Confirm] <SwitchParameter>] [<CommonParameters>]
```

### Description

Using this Cmdlet will initiate a restore of the appliance to the backup file specified. Starts a restore operation from the backup file already uploaded to the appliance. Only one restore operation can run at a time. There is no way to cancel a restore once it has been started. The restore operation is destructive. Any configuration changes not included in the backup file will be lost. The appliance will raise alerts for any inconsistencies detected after the restore. If an unrecoverable error is detected during the restore, then the appliance will be set to the factory reset mode.

{% hint style="danger" %}
Restoring from a backup is a disruptive action:

* The appliance restarts and users cannot log in to the appliance during the restore process. All users are logged out and their work is lost.
* To prevent duplicate identifiers on the network, server hardware configurations are cleared if an associated server profile is not in the backup.
* Server profiles that have been modified since the backup was taken are flagged with this message: "Server profile settings conflict with the server hardware configuration". To reapply the server profile

  configuration and restore network connectivity, you must unassign all flagged server profiles and then

  individually reassign the server profiles to the server hardware.

* To prevent unintentional assignment of duplicate addresses or identifiers, all address and identifier ranges are disabled after the post-restore process completes. The appliance automatically re-creates replacement address and identifier ranges.
{% endhint %}

{% hint style="info" %}
Required permissions: Infrastructure administrator, Software administrator
{% endhint %}

### Parameters

#### -ApplianceConnection &lt;Array&gt; 

Specify one or more \[HPOneView.Appliance.Connection\] object\(s\) or Name property value\(s\).

Default Value: ${Global:ConnectedSessions} \| ? Default

| Aliases | Appliance |
| :--- | :--- |
| Required? | false |
| Position? | named |
| Default value | \(${Global:ConnectedSessions} \| ? Default\) |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

#### -Confirm &lt;SwitchParameter&gt;

| Aliases | cf |
| :--- | :--- |
| Required? | false |
| Position? | named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

#### -EncryptionKey &lt;Object&gt; 

Provide the encryption key file path or file object. When restoring an appliance backup, and after the appliance has been factory reset, the prior encryption key is needed to decrypt the backup file. This is only supported with HPE Synergy Composer 2 appliances.

| Aliases | None |
| :--- | :--- |
| Required? | false |
| Position? | named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

#### -FileName &lt;System.IO.FileInfo&gt; 

The full path and file name of the appliance configuration backup file.

| Aliases | File |
| :--- | :--- |
| Required? | true |
| Position? | named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

#### -WhatIf &lt;SwitchParameter&gt;

| Aliases | wi |
| :--- | :--- |
| Required? | false |
| Position? | named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

&lt;CommonParameters&gt;

This cmdlet supports the common parameters: Verbose, Debug, ErrorAction, ErrorVariable, WarningAction, WarningVariable, OutBuffer, PipelineVariable, and OutVariable. For more information, see about\_CommonParameters \([http://go.microsoft.com/fwlink/?LinkID=113216](http://go.microsoft.com/fwlink/?LinkID=113216)\)

### Input Types

_**None. You cannot pipe objects to this cmdlet.**_

### Return Values

_**System.Management.Automation.PSCustomObject**_

The restore process object. This is not an Async Task

### Examples

```text
 -------------------------- EXAMPLE 1 --------------------------
New-HPOVRestore -FileName "C:\Users\me\Documents\appliance_backup_2013-11-01_110203.bkp"
```

Upload a backup file to restore in the appliance.

```text
 -------------------------- EXAMPLE 2 --------------------------
New-HPOVRestore -FileName "C:\Users\me\Documents\appliance_backup_2013-11-01_110203.bkp -EncryptionKey "C:\Path\to\encryptionkey.aek""
```

Upload a backup file to restore in the appliance, supplying the path to the encryption key file. 

#### Related Links 

* [New-HPOVBackup ](new-hpovbackup.md#hpe-oneview-5-00-library)
* [Save-HPOVApplianceDataAtRestEncryptionKey](https://github.com/HewlettPackard/POSH-HPOneView/wiki/Save-HPOVApplianceDataAtRestEncryptionKey) 

## HPE OneView 4.20 Library

### Syntax

```text
New-HPOVRestore [-FileName] <System.IO.FileInfo> [[-ApplianceConnection] <Array>] [[-WhatIf] <SwitchParameter>] [[-Confirm] <SwitchParameter>] [<CommonParameters>]
```

### Description

Using this Cmdlet will initiate a restore of the appliance to the backup file specified. Starts a restore operation from the backup file already uploaded to the appliance. Only one restore operation can run at a time. There is no way to cancel a restore once it has been started. The restore operation is destructive. Any configuration changes not included in the backup file will be lost. The appliance will raise alerts for any inconsistencies detected after the restore. If an unrecoverable error is detected during the restore, then the appliance will be set to the factory reset mode.

{% hint style="danger" %}
Restoring from a backup is a disruptive action:

* The appliance restarts and users cannot log in to the appliance during the restore process. All users are logged out and their work is lost.
* To prevent duplicate identifiers on the network, server hardware configurations are cleared if an associated server profile is not in the backup.
* Server profiles that have been modified since the backup was taken are flagged with this message: "Server profile settings conflict with the server hardware configuration". To reapply the server profile

  configuration and restore network connectivity, you must unassign all flagged server profiles and then

  individually reassign the server profiles to the server hardware.

* To prevent unintentional assignment of duplicate addresses or identifiers, all address and identifier ranges are disabled after the post-restore process completes. The appliance automatically re-creates replacement address and identifier ranges.
{% endhint %}

{% hint style="info" %}
Required permissions: Infrastructure administrator, Software administrator
{% endhint %}

### Parameters

#### -ApplianceConnection &lt;Array&gt; 

Specify one or more \[HPOneView.Appliance.Connection\] object\(s\) or Name property value\(s\).

Default Value: ${Global:ConnectedSessions} \| ? Default

| Aliases | Appliance |
| :--- | :--- |
| Required? | false |
| Position? | named |
| Default value | \(${Global:ConnectedSessions} \| ? Default\) |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

#### -Confirm &lt;SwitchParameter&gt;

| Aliases | cf |
| :--- | :--- |
| Required? | false |
| Position? | named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

#### -FileName &lt;System.IO.FileInfo&gt; 

The full path and file name of the appliance configuration backup file.

| Aliases | File |
| :--- | :--- |
| Required? | true |
| Position? | named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

#### -WhatIf &lt;SwitchParameter&gt;

| Aliases | wi |
| :--- | :--- |
| Required? | false |
| Position? | named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

&lt;CommonParameters&gt;

This cmdlet supports the common parameters: Verbose, Debug, ErrorAction, ErrorVariable, WarningAction, WarningVariable, OutBuffer, PipelineVariable, and OutVariable. For more information, see about\_CommonParameters \([http://go.microsoft.com/fwlink/?LinkID=113216](http://go.microsoft.com/fwlink/?LinkID=113216)\)

### Input Types

_**None. You cannot pipe objects to this cmdlet.**_

### Return Values

_**System.Management.Automation.PSCustomObject**_

The restore process object. This is not an Async Task

### Examples

```text
 -------------------------- EXAMPLE 1 --------------------------
New-HPOVRestore -FileName "C:\Users\me\Documents\appliance_backup_2013-11-01_110203.bkp"
```

Upload a backup file to restore in the appliance.

#### Related Links 

* [New-HPOVBackup ](new-hpovbackup.md#hpe-oneview-4-20-library)
* [Save-HPOVApplianceDataAtRestEncryptionKey](https://github.com/HewlettPackard/POSH-HPOneView/wiki/Save-HPOVApplianceDataAtRestEncryptionKey) 

## HPE OneView 4.10 Library

### Syntax

```text
New-HPOVRestore [-FileName] <System.IO.FileInfo> [[-ApplianceConnection] <Array> [[-WhatIf] <SwitchParameter>] [[-Confirm] <SwitchParameter>] [<CommonParameters>]
```

### Description

Using this Cmdlet will initiate a restore of the appliance to the backup file specified. Starts a restore operation from the backup file already uploaded to the appliance. Only one restore operation can run at a time. There is no way to cancel a restore once it has been started. The restore operation is destructive. Any configuration changes not included in the backup file will be lost. The appliance will raise alerts for any inconsistencies detected after the restore. If an unrecoverable error is detected during the restore, then the appliance will be set to the factory reset mode.

{% hint style="danger" %}
Restoring from a backup is a disruptive action:

* The appliance restarts and users cannot log in to the appliance during the restore process. All users are logged out and their work is lost.
* To prevent duplicate identifiers on the network, server hardware configurations are cleared if an associated server profile is not in the backup.
* Server profiles that have been modified since the backup was taken are flagged with this message: "Server profile settings conflict with the server hardware configuration". To reapply the server profile

  configuration and restore network connectivity, you must unassign all flagged server profiles and then

  individually reassign the server profiles to the server hardware.

* To prevent unintentional assignment of duplicate addresses or identifiers, all address and identifier ranges are disabled after the post-restore process completes. The appliance automatically re-creates replacement address and identifier ranges.
{% endhint %}

{% hint style="info" %}
Required permissions: Infrastructure administrator, Software administrator
{% endhint %}

### Parameters

#### -ApplianceConnection &lt;Array&gt; 

Specify one or more \[HPOneView.Appliance.Connection\] object\(s\) or Name property value\(s\).

Default Value: ${Global:ConnectedSessions} \| ? Default

| Aliases | Appliance |
| :--- | :--- |
| Required? | false |
| Position? | named |
| Default value | \(${Global:ConnectedSessions} \| ? Default\) |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

#### -Confirm &lt;SwitchParameter&gt;

| Aliases | cf |
| :--- | :--- |
| Required? | false |
| Position? | named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

#### -FileName &lt;System.IO.FileInfo&gt; 

The full path and file name of the appliance configuration backup file.

| Aliases | File |
| :--- | :--- |
| Required? | true |
| Position? | named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

#### -WhatIf &lt;SwitchParameter&gt;

| Aliases | wi |
| :--- | :--- |
| Required? | false |
| Position? | named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

&lt;CommonParameters&gt;

This cmdlet supports the common parameters: Verbose, Debug, ErrorAction, ErrorVariable, WarningAction, WarningVariable, OutBuffer, PipelineVariable, and OutVariable. For more information, see about\_CommonParameters \([http://go.microsoft.com/fwlink/?LinkID=113216](http://go.microsoft.com/fwlink/?LinkID=113216)\)

### Input Types

_**None. You cannot pipe objects to this cmdlet.**_

### Return Values

_**System.Management.Automation.PSCustomObject**_

The restore process object. This is not an Async Task

### Examples

```text
 -------------------------- EXAMPLE 1 --------------------------
New-HPOVRestore -FileName "C:\Users\me\Documents\appliance_backup_2013-11-01_110203.bkp"
```

Upload a backup file to restore in the appliance.

#### Related Links 

* [New-HPOVBackup ](new-hpovbackup.md#hpe-oneview-4-10-library)
* [Save-HPOVApplianceDataAtRestEncryptionKey](https://github.com/HewlettPackard/POSH-HPOneView/wiki/Save-HPOVApplianceDataAtRestEncryptionKey) 
