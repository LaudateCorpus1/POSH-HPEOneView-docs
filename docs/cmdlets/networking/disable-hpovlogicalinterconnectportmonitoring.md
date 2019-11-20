---
description: Disable port monitoring for a logical interconnect.
---

# Disable-HPOVLogicalInterconnectPortMonitoring

## HPE OneView 5.00 Library

### Syntax

```text
Disable-HPOVLogicalInterconnectPortMonitoring [-InputObject] <Object> [[-ApplianceConnection] <Array>] [<CommonParameters>]
```

### Description

Port monitoring enables you to send a copy of every Ethernet or Fibre Channel frame coming in and going out of a downlink \(server-facing\) port to another port. To evaluate network traffic between ports, you can connect debugging equipment, such as a network analyzer. This capability is important in a server environment where there is limited physical access to the network interfaces on the servers.

{% hint style="warning" %}
* You cannot use Virtual Connect to forward captured traffic to a server. For more information, see the HPE Virtual Connect for c-Class BladeSystem User Guide in the Hewlett Packard Enterprise Information Library. 
* You can configure one network analyzer port \(the uplink port\) for up to 16 downlink server ports within a logical interconnect. 
* The HPE Virtual Connect 16Gb 24-Port Fibre Channel Module monitors 1 downlink server port. 
* HPE Virtual Connect 16Gb 24-Port Fibre Channel Module firmware must be 4.00 or later 
{% endhint %}

{% hint style="info" %}
Required Privileges: Network administrator
{% endhint %}

### Parameters

#### -ApplianceConnection &lt;Array&gt; 

Specify one or more \[HPOneView.Appliance.Connection\] object\(s\) or Name property value\(s\).

Default Value: ${Global:ConnectedSessions} \| ? Default

| Aliases | Appliance |
| :--- | :--- |
| Required? | False |
| Position? | named |
| Default value | \(${Global:ConnectedSessions} \| ? Default\) |
| Accept pipeline input? | true \(ByPropertyName\) |
| Accept wildcard characters?    | False |

#### -InputObject &lt;Object&gt; 

The HPOneView.Networking.LogicalInterconnect resource from Get-HPOVLogicalInterconnect.

| Aliases | uri, li, name, Resource |
| :--- | :--- |
| Required? | True |
| Position? | named |
| Default value |  |
| Accept pipeline input? | true \(ByValue\) |
| Accept wildcard characters?    | False |

&lt;CommonParameters&gt;

This cmdlet supports the common parameters: Verbose, Debug, ErrorAction, ErrorVariable, WarningAction, WarningVariable, OutBuffer, PipelineVariable, and OutVariable. For more information, see about\_CommonParameters \([http://go.microsoft.com/fwlink/?LinkID=113216](http://go.microsoft.com/fwlink/?LinkID=113216)\)

### Input Types

_**HPoneView.Networking.LogicalInterconnect \[System.Management.Automation.PSCustomObject\]**_

Logical Interconnect resource object from Get-HPOVLogicalInterconnect

### Return Values

_**HPOneView.Appliance.TaskResource \[System.Management.Automation.PSCustomObject\]**_

Async task Resource object for configuring port monitoring on the requested logical intercinnect.

### Examples

```text
 -------------------------- EXAMPLE 1 --------------------------
Get-HPOVLogicalInterconnect -Name "Encl1" -ErrorAction Stop | Disable-HPOVLogicalInterconnectPortMonitoring
```

Disable port monitoring for the specified logical interconnect resource. 

### Related Links 

* [Enable-HPOVLogicalInterconnectPortMonitoring](https://github.com/HewlettPackard/POSH-HPOneView/wiki/Enable-HPOVLogicalInterconnectPortMonitoring) 
* [Get-HPOVLogicalInterconnectPortMonitoring](https://github.com/HewlettPackard/POSH-HPOneView/wiki/Get-HPOVLogicalInterconnectPortMonitoring) 

## HPE OneView 4.20 Library

### Syntax

```text
Disable-HPOVLogicalInterconnectPortMonitoring [-InputObject] <Object> [[-ApplianceConnection] <Array>] [<CommonParameters>]
```

### Description

Port monitoring enables you to send a copy of every Ethernet or Fibre Channel frame coming in and going out of a downlink \(server-facing\) port to another port. To evaluate network traffic between ports, you can connect debugging equipment, such as a network analyzer. This capability is important in a server environment where there is limited physical access to the network interfaces on the servers.

{% hint style="warning" %}
* You cannot use Virtual Connect to forward captured traffic to a server. For more information, see the HPE Virtual Connect for c-Class BladeSystem User Guide in the Hewlett Packard Enterprise Information Library. 
* You can configure one network analyzer port \(the uplink port\) for up to 16 downlink server ports within a logical interconnect. 
* The HPE Virtual Connect 16Gb 24-Port Fibre Channel Module monitors 1 downlink server port. 
* HPE Virtual Connect 16Gb 24-Port Fibre Channel Module firmware must be 4.00 or later 
{% endhint %}

{% hint style="info" %}
Required Privileges: Network administrator
{% endhint %}

### Parameters

#### -ApplianceConnection &lt;Array&gt; 

Specify one or more \[HPOneView.Appliance.Connection\] object\(s\) or Name property value\(s\).

Default Value: ${Global:ConnectedSessions} \| ? Default

| Aliases | Appliance |
| :--- | :--- |
| Required? | False |
| Position? | named |
| Default value | \(${Global:ConnectedSessions} \| ? Default\) |
| Accept pipeline input? | true \(ByPropertyName\) |
| Accept wildcard characters?    | False |

#### -InputObject &lt;Object&gt; 

The HPOneView.Networking.LogicalInterconnect resource from Get-HPOVLogicalInterconnect.

| Aliases | uri, li, name, Resource |
| :--- | :--- |
| Required? | True |
| Position? | named |
| Default value |  |
| Accept pipeline input? | true \(ByValue\) |
| Accept wildcard characters?    | False |

&lt;CommonParameters&gt;

This cmdlet supports the common parameters: Verbose, Debug, ErrorAction, ErrorVariable, WarningAction, WarningVariable, OutBuffer, PipelineVariable, and OutVariable. For more information, see about\_CommonParameters \([http://go.microsoft.com/fwlink/?LinkID=113216](http://go.microsoft.com/fwlink/?LinkID=113216)\)

### Input Types

_**HPoneView.Networking.LogicalInterconnect \[System.Management.Automation.PSCustomObject\]**_

Logical Interconnect resource object from Get-HPOVLogicalInterconnect

### Return Values

_**HPOneView.Appliance.TaskResource \[System.Management.Automation.PSCustomObject\]**_

Async task Resource object for configuring port monitoring on the requested logical intercinnect.

### Examples

```text
 -------------------------- EXAMPLE 1 --------------------------
Get-HPOVLogicalInterconnect -Name "Encl1" -ErrorAction Stop | Disable-HPOVLogicalInterconnectPortMonitoring
```

Disable port monitoring for the specified logical interconnect resource. 

### Related Links 

* [Enable-HPOVLogicalInterconnectPortMonitoring](https://github.com/HewlettPackard/POSH-HPOneView/wiki/Enable-HPOVLogicalInterconnectPortMonitoring) 
* [Get-HPOVLogicalInterconnectPortMonitoring](https://github.com/HewlettPackard/POSH-HPOneView/wiki/Get-HPOVLogicalInterconnectPortMonitoring) 

## HPE OneView 4.10 Library

### Syntax

```text
Disable-HPOVLogicalInterconnectPortMonitoring [-InputObject] <Object> [[-ApplianceConnection] <Array>] [<CommonParameters>]
```

### Description

Port monitoring enables you to send a copy of every Ethernet or Fibre Channel frame coming in and going out of a downlink \(server-facing\) port to another port. To evaluate network traffic between ports, you can connect debugging equipment, such as a network analyzer. This capability is important in a server environment where there is limited physical access to the network interfaces on the servers.

{% hint style="warning" %}
* You cannot use Virtual Connect to forward captured traffic to a server. For more information, see the HPE Virtual Connect for c-Class BladeSystem User Guide in the Hewlett Packard Enterprise Information Library. 
* You can configure one network analyzer port \(the uplink port\) for up to 16 downlink server ports within a logical interconnect. 
* The HPE Virtual Connect 16Gb 24-Port Fibre Channel Module monitors 1 downlink server port. 
* HPE Virtual Connect 16Gb 24-Port Fibre Channel Module firmware must be 4.00 or later 
{% endhint %}

{% hint style="info" %}
Required Privileges: Network administrator
{% endhint %}

### Parameters

#### -ApplianceConnection &lt;Array&gt; 

Specify one or more \[HPOneView.Appliance.Connection\] object\(s\) or Name property value\(s\).

Default Value: ${Global:ConnectedSessions} \| ? Default

| Aliases | Appliance |
| :--- | :--- |
| Required? | False |
| Position? | named |
| Default value | \(${Global:ConnectedSessions} \| ? Default\) |
| Accept pipeline input? | true \(ByPropertyName\) |
| Accept wildcard characters?    | False |

#### -InputObject &lt;Object&gt; 

The HPOneView.Networking.LogicalInterconnect resource from Get-HPOVLogicalInterconnect.

| Aliases | uri, li, name, Resource |
| :--- | :--- |
| Required? | True |
| Position? | named |
| Default value |  |
| Accept pipeline input? | true \(ByValue\) |
| Accept wildcard characters?    | False |

&lt;CommonParameters&gt;

This cmdlet supports the common parameters: Verbose, Debug, ErrorAction, ErrorVariable, WarningAction, WarningVariable, OutBuffer, PipelineVariable, and OutVariable. For more information, see about\_CommonParameters \([http://go.microsoft.com/fwlink/?LinkID=113216](http://go.microsoft.com/fwlink/?LinkID=113216)\)

### Input Types

_**HPoneView.Networking.LogicalInterconnect \[System.Management.Automation.PSCustomObject\]**_

Logical Interconnect resource object from Get-HPOVLogicalInterconnect

### Return Values

_**HPOneView.Appliance.TaskResource \[System.Management.Automation.PSCustomObject\]**_

Async task Resource object for configuring port monitoring on the requested logical intercinnect.

### Examples

```text
 -------------------------- EXAMPLE 1 --------------------------
Get-HPOVLogicalInterconnect -Name "Encl1" -ErrorAction Stop | Disable-HPOVLogicalInterconnectPortMonitoring
```

Disable port monitoring for the specified logical interconnect resource. 

### Related Links 

* [Enable-HPOVLogicalInterconnectPortMonitoring](https://github.com/HewlettPackard/POSH-HPOneView/wiki/Enable-HPOVLogicalInterconnectPortMonitoring) 
* [Get-HPOVLogicalInterconnectPortMonitoring](https://github.com/HewlettPackard/POSH-HPOneView/wiki/Get-HPOVLogicalInterconnectPortMonitoring) 


