---
applicable: Lync Server 2010, Lync Server 2013, Skype for Business Server 2015
schema: 2.0.0
---

# Get-CsLisPort

## SYNOPSIS
**Below Content Applies To:** Lync Server 2010

Retrieves one or more ports from the location configuration database.
Each port can be associated with a location, in which case this cmdlet will also retrieve the location information of the ports.
This location association is used in an Enhanced 9-1-1 (E9-1-1) Enterprise Voice implementation to notify an emergency services operator of the caller's location.

**Below Content Applies To:** Lync Server 2013, Skype for Business Server 2015

Retrieves one or more ports from the location configuration database.
Each port can be associated with a location, in which case this cmdlet will also retrieve the location information of the ports.
This location association is used in an Enhanced 9-1-1 (E9-1-1) Enterprise Voice implementation to notify an emergency services operator of the caller's location.
This cmdlet was introduced in Lync Server 2010.



## SYNTAX

```
Get-CsLisPort [<CommonParameters>]
```

## DESCRIPTION
**Below Content Applies To:** Lync Server 2010, Lync Server 2013

Enhanced 9-1-1 allows an emergency operator to identify the location of a caller without having to ask the caller for that information.
In the case where a caller is calling from a Voice over Internet Protocol (VoIP) connection, that information must be extracted based on various connection factors.
The VoIP administrator must configure a location map (called a wiremap) that will determine a caller's location.
This cmdlet retrieves information on associations between physical locations and the port through which the client is connected.

This cmdlet does not take any parameters (other than the Windows PowerShell common parameters).
The cmdlet will retrieve all instances of port to location mappings.
To narrow down the information retrieved, you must pipe the output from this cmdlet to another Windows PowerShell cmdlet such as Where-Object or Select-Object.

Who can run this cmdlet: By default, members of the following groups are authorized to run the Get-CsLisPort cmdlet locally: RTCUniversalServerAdmins.
To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:

Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Get-CsLisPort"}

**Below Content Applies To:** Skype for Business Server 2015

Enhanced 9-1-1 allows an emergency operator to identify the location of a caller without having to ask the caller for that information.
In the case where a caller is calling from a Voice over Internet Protocol (VoIP) connection, that information must be extracted based on various connection factors.
The VoIP administrator must configure a location map (called a wiremap) that will determine a caller's location.
This cmdlet retrieves information on associations between physical locations and the port through which the client is connected.

This cmdlet does not take any parameters (other than the Windows PowerShell common parameters).
The cmdlet will retrieve all instances of port to location mappings.
To narrow down the information retrieved, you must pipe the output from this cmdlet to another Windows PowerShell cmdlet such as the Where-Object cmdlet or the Select-Object cmdlet.



## EXAMPLES

### -------------------------- Example 1 -------------------------- (Lync Server 2010)
```
Get-CsLisPort
```

Example 1 retrieves all Location Information Server (LIS) ports and any associated locations that have been defined in the Microsoft Lync Server 2010 deployment.

### -------------------------- EXAMPLE 1 -------------------------- (Lync Server 2013)
```

```

Example 1 retrieves all Location Information Server (LIS) ports and any associated locations that have been defined in the Lync Server deployment.

Get-CsLisPort

### -------------------------- EXAMPLE 1 -------------------------- (Skype for Business Server 2015)
```

```

Example 1 retrieves all Location Information Server (LIS) ports and any associated locations that have been defined in the Skype for Business Server 2015 deployment.

Get-CsLisPort

### -------------------------- Example 2 -------------------------- (Lync Server 2010)
```
Get-CsLisPort | Where-Object {$_.City -eq "Redmond"}
```

This example retrieves all information for all ports that have been associated with a location in the city of Redmond.
The command begins by calling Get-CsLisPort to retrieve all port location associations.
This collection of port locations is piped to the Where-Object cmdlet.
Where-Object checks the City property of each item in the collection to determine whether the value is equal to (-eq) Redmond.

### -------------------------- EXAMPLE 2 -------------------------- (Lync Server 2013)
```

```

This example retrieves all information for all ports that have been associated with a location in the city of Redmond.
The command begins by calling Get-CsLisPort to retrieve all port location associations.
This collection of port locations is piped to the Where-Object cmdlet.
Where-Object checks the City property of each item in the collection to determine whether the value is equal to (-eq) Redmond.

Get-CsLisPort | Where-Object {$_.City -eq "Redmond"}

### -------------------------- EXAMPLE 2 -------------------------- (Skype for Business Server 2015)
```

```

This example retrieves all information for all ports that have been associated with a location in the city of Redmond.
The command begins by calling the Get-CsLisPort cmdlet to retrieve all port location associations.
This collection of port locations is piped to the Where-Object cmdlet.
The Where-Object cmdlet checks the City property of each item in the collection to determine whether the value is equal to (-eq) Redmond.

Get-CsLisPort | Where-Object {$_.City -eq "Redmond"}

## PARAMETERS

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

###  
None.

## OUTPUTS

###  
This cmdlet retrieves one or more objects of type System.Management.Automation.PSCustomObject.

## NOTES

## RELATED LINKS

[Online Version](http://technet.microsoft.com/EN-US/library/c755aa8c-e842-4bb8-bdbf-d61a364eb0bc(OCS.14).aspx)

[Remove-CsLisPort]()

[Set-CsLisPort]()

[Online Version](http://technet.microsoft.com/EN-US/library/c755aa8c-e842-4bb8-bdbf-d61a364eb0bc(OCS.15).aspx)

[Online Version](http://technet.microsoft.com/EN-US/library/c755aa8c-e842-4bb8-bdbf-d61a364eb0bc(OCS.16).aspx)
