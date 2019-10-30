---
description: Create a new resource.
---

# New-HPOVResource

### HPE OneView 5.00 Library

### Syntax

```text
New-HPOVResource [-Uri] <String> [-InputObject] <Object> [[-ApplianceConnection] <Object>] [<CommonParameters>]
```

### Description

Create a new resource by passing the URI and the resource details in the form of a PowerShell Object, or `[System.Management.Automation.PSCustomObject]`.  For specific information about an objects properties and allowed values, please reference the HPE OneView REST API documentation.

### Parameters

#### -ApplianceConnection &lt;Object&gt;

Specify one `[HPOneView.Appliance.Connection]` object or Name property value. If Resource object is provided via Pipeline, the `ApplianceConnection` property of the object will be used.

| Aliases | Appliance |
| :--- | :--- |
| Required? | false |
| Position? | 2 |
| Default value | \(${Global:ConnectedSessions} \| ? Default\) |
| Accept pipeline input? | true \(ByPropertyName\) |
| Accept wildcard characters?    | False |

#### -InputObject &lt;Object&gt; 

The new resource that is to be created

| Aliases | Resource |
| :--- | :--- |
| Required? | true |
| Position? | 1 |
| Default value |  |
| Accept pipeline input? | true \(ByValue\) |
| Accept wildcard characters?    | False |

#### -Uri &lt;String&gt; 

The location where the new object is to be created, using the HTTP POST method.

| Aliases | None |
| :--- | :--- |
| Required? | true |
| Position? | 0 |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

&lt;CommonParameters&gt;

This cmdlet supports the common parameters: Verbose, Debug, ErrorAction, ErrorVariable, WarningAction, WarningVariable, OutBuffer, PipelineVariable, and OutVariable. For more information, see about\_CommonParameters \([http://go.microsoft.com/fwlink/?LinkID=113216](http://go.microsoft.com/fwlink/?LinkID=113216)\)

### Input Types

_**System.Management.Automation.PSCustomObject**_

Resource object to create.

### Return Values

_**System.Management.Automation.PSCustomObject**_

The newly created resource, or async task.

### Examples

```text
 -------------------------- EXAMPLE 1 --------------------------
New-HPOVResource /rest/ethernet-networks @{vlanId=2000; purpose="General"; name="VLAN 2000"; smartLink=$true; privateNetwork=$false; type="ethernet-networkV4"}
```

 Create a new Ethernet Network, "VLAN 2000". 

### Related Links 

* [Remove-HPOVResource ](remove-hpovresource.md)
* [Set-HPOVResource](set-hpovresource.md)

## HPE OneView 4.20 Library

### Syntax

```text
New-HPOVResource [-Uri] <String> [-InputObject] <Object> [[-ApplianceConnection] <Object>] [<CommonParameters>]
```

### Description

Create a new resource by passing the URI and the resource details in the form of a PowerShell Object, or `[System.Management.Automation.PSCustomObject]`.  For specific information about an objects properties and allowed values, please reference the HPE OneView REST API documentation.

### Parameters

#### -ApplianceConnection &lt;Object&gt;

Specify one `[HPOneView.Appliance.Connection]` object or Name property value. If Resource object is provided via Pipeline, the `ApplianceConnection` property of the object will be used.

| Aliases | Appliance |
| :--- | :--- |
| Required? | false |
| Position? | 2 |
| Default value | \(${Global:ConnectedSessions} \| ? Default\) |
| Accept pipeline input? | true \(ByPropertyName\) |
| Accept wildcard characters?    | False |

#### -InputObject &lt;Object&gt; 

The new resource that is to be created

| Aliases | Resource |
| :--- | :--- |
| Required? | true |
| Position? | 1 |
| Default value |  |
| Accept pipeline input? | true \(ByValue\) |
| Accept wildcard characters?    | False |

#### -Uri &lt;String&gt; 

The location where the new object is to be created, using the HTTP POST method.

| Aliases | None |
| :--- | :--- |
| Required? | true |
| Position? | 0 |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

&lt;CommonParameters&gt;

This cmdlet supports the common parameters: Verbose, Debug, ErrorAction, ErrorVariable, WarningAction, WarningVariable, OutBuffer, PipelineVariable, and OutVariable. For more information, see about\_CommonParameters \([http://go.microsoft.com/fwlink/?LinkID=113216](http://go.microsoft.com/fwlink/?LinkID=113216)\)

### Input Types

_**System.Management.Automation.PSCustomObject**_

Resource object to create.

### Return Values

_**System.Management.Automation.PSCustomObject**_

The newly created resource, or async task.

### Examples

```text
 -------------------------- EXAMPLE 1 --------------------------
New-HPOVResource /rest/ethernet-networks @{vlanId=2000; purpose="General"; name="VLAN 2000"; smartLink=$true; privateNetwork=$false; type="ethernet-networkV4"}
```

 Create a new Ethernet Network, "VLAN 2000". 

### Related Links 

* [Remove-HPOVResource ](remove-hpovresource.md)
* [Set-HPOVResource](set-hpovresource.md)

## HPE OneView 4.10 Library

### Syntax

```text
New-HPOVResource [-Uri] <String> [-InputObject] <Object> [[-ApplianceConnection] <Object>] [<CommonParameters>]
```

### Description

Create a new resource by passing the URI and the resource details in the form of a PowerShell Object, or `[System.Management.Automation.PSCustomObject]`.  For specific information about an objects properties and allowed values, please reference the HPE OneView REST API documentation.

### Parameters

#### -ApplianceConnection &lt;Object&gt;

Specify one `[HPOneView.Appliance.Connection]` object or Name property value. If Resource object is provided via Pipeline, the `ApplianceConnection` property of the object will be used.

| Aliases | Appliance |
| :--- | :--- |
| Required? | false |
| Position? | 2 |
| Default value | \(${Global:ConnectedSessions} \| ? Default\) |
| Accept pipeline input? | true \(ByPropertyName\) |
| Accept wildcard characters?    | False |

#### -InputObject &lt;Object&gt; 

The new resource that is to be created

| Aliases | Resource |
| :--- | :--- |
| Required? | true |
| Position? | 1 |
| Default value |  |
| Accept pipeline input? | true \(ByValue\) |
| Accept wildcard characters?    | False |

#### -Uri &lt;String&gt; 

The location where the new object is to be created, using the HTTP POST method.

| Aliases | None |
| :--- | :--- |
| Required? | true |
| Position? | 0 |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters?    | False |

&lt;CommonParameters&gt;

This cmdlet supports the common parameters: Verbose, Debug, ErrorAction, ErrorVariable, WarningAction, WarningVariable, OutBuffer, PipelineVariable, and OutVariable. For more information, see about\_CommonParameters \([http://go.microsoft.com/fwlink/?LinkID=113216](http://go.microsoft.com/fwlink/?LinkID=113216)\)

### Input Types

_**System.Management.Automation.PSCustomObject**_

Resource object to create.

### Return Values

_**System.Management.Automation.PSCustomObject**_

The newly created resource, or async task.

### Examples

```text
 -------------------------- EXAMPLE 1 --------------------------
New-HPOVResource /rest/ethernet-networks @{vlanId=2000; purpose="General"; name="VLAN 2000"; smartLink=$true; privateNetwork=$false; type="ethernet-networkV3"}
```

 Create a new Ethernet Network, "VLAN 2000". 

### Related Links 

* [Remove-HPOVResource ](remove-hpovresource.md)
* [Set-HPOVResource](set-hpovresource.md)
