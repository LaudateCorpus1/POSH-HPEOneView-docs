﻿---
description: Get available storage volume sets.
---

# Get-OVStorageVolumeSet

## Syntax

```text
Get-OVStorageVolumeSet
    [-Name <string>]
    [-Label <String>]
    [-Scope <Object>]
    [-ApplianceConnection <Object>]
    [<CommonParameters>]
```

## Description

A collection of volumes is referred to as volume set in HPE OneView. Volume sets are used to govern data-protection policies, such as snapshot and replication schedules. For HPE Nimble storage, the corresponding terminology for "volume sets" is "data protection volume collections".  Volumes that hold multiple components of an application, such as databases and transaction logs, can be grouped into a volume set.

This Cmdlet will return the available volume sets from the available storage systems.  Volume sets are created on the storage system.

## Examples

###  Example 1 

```text
Get-OVStorageVolumeSet
```

Get all available storage sets.

###  Example 2 

```text
Get-OVStorageVolumeSet -Name VolumeSets
```

Get the specified "VolumeSets" storage sets.

## Parameters

### -ApplianceConnection &lt;Object&gt;

Specify one or more `[HPEOneView.Appliance.Connection]` object(s) or Name property value(s).

| Aliases | Appliance |
| :--- | :--- |
| Required? | False |
| Position? | Named |
| Default value | (${Global:ConnectedSessions} &vert; ? Default) |
| Accept pipeline input? | true (ByPropertyName) |
| Accept wildcard characters? | False |

### -Label &lt;String&gt;

Specify the label associated with resources.

| Aliases | None |
| :--- | :--- |
| Required? | False |
| Position? | Named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters? | False |

### -Name &lt;string&gt;

Filter for the resource name.

| Aliases | None |
| :--- | :--- |
| Required? | False |
| Position? | Named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters? | False |

### -Scope &lt;Object&gt;

Filter resources based on provided Scope membership.  By default, all resources for the accounts Active Permissions will be displayed.  Allowed values:nr
    * AllResources
    *AllResourcesInScope
    * `[HPEOneView.Appliance.ScopeCollection]`
    * `[HPEOneView.Appliance.ConnectionPermission]`

| Aliases | None |
| :--- | :--- |
| Required? | False |
| Position? | Named |
| Default value | AllResourcesInScope |
| Accept pipeline input? | false |
| Accept wildcard characters? | False |

### &lt;CommonParameters&gt;

This cmdlet supports the common parameters: Verbose, Debug, ErrorAction, ErrorVariable, WarningAction, WarningVariable, OutBuffer, PipelineVariable, and OutVariable. For more information, see about\_CommonParameters \([http://go.microsoft.com/fwlink/?LinkID=113216](http://go.microsoft.com/fwlink/?LinkID=113216)\)

## Input Types

_**None.  You cannot pipe objects to this Cmdlet.**_

## Return Values

_**HPEOneView.Storage.VolumeSet**_

The available storage system volume set.

## Related Links
