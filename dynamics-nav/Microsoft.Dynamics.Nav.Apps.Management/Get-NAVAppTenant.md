---
external help file: Microsoft.Dynamics.Nav.Apps.Management.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-NAVAppTenant

## SYNOPSIS
Gets the tenants where the specified NAV App is installed.

## SYNTAX

### Properties (Default)
```
Get-NAVAppTenant [-ServerInstance] <String> [-Name <String>] [-Publisher <String>] [-Version <Version>]
```

### Path
```
Get-NAVAppTenant [-ServerInstance] <String> -Path <String>
```

## DESCRIPTION
Use the Get-NAVAppTenant cmdlet to get the tenants where the specified NAV App is installed.
You can specify the NAV App by name, publisher, or version.
You can use the returned list of tenants to apply general changes, such as uninstalling the NAV App for all tenants that currently have it installed.

## EXAMPLES

### EXAMPLE 1
```
Get-NavAppTenant -ServerInstance DynamicsNAV90 -Name 'ProseWare SmartApp' -Version 2.3.4.500

          Id                    State
          ----                  ---------
          Tenant1               Mounted
          Tenant2               Mounted
          Tenant4               Mounted
```

Description

-----------

This example gets the tenants on the DynamicsNAV90 server instance that have the version 2.3.4.500 of the Proseware SmartApp installed.

### EXAMPLE 2
```
Get-NavAppTenant -ServerInstance DynamicsNAV90 -Name 'ProseWare SmartApp' -Version 2.3.4.500 | Uninstall-NAVApp -ServerInstance DynamicsNAV90 -Name 'Proseware SmartApp' -Version 2.3.4.500
```

Description

-----------

This example gets the tenants on the DynamicsNAV90 server instance that have the version 2.3.4.500 of the Proseware SmartApp installed and then uninstalls that NAV App for each of those tenants by passing the tenants to the Uninstall-NAVApp cmdlet.

## PARAMETERS

### -Name
Specifies the name of the NAV App that you want to see a list of tenants where it is installed.

```yaml
Type: String
Parameter Sets: Properties
Aliases: AppName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Specifies the path to a NAV App package file for the NAV App that you want to see a list of tenants where it is installed.

```yaml
Type: String
Parameter Sets: Path
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Publisher
Specifies the publisher of the NAV App that you want to see a list of tenants where it is installed.

```yaml
Type: String
Parameter Sets: Properties
Aliases: AppPublisher

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerInstance
Specifies the Microsoft Dynamics NAV server instance that the NAV App is deployed to, such as DynamicsNAV90.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Version
Specifies the version of the NAV App that you want to see a list of tenants where it is installed.

```yaml
Type: Version
Parameter Sets: Properties
Aliases: AppVersion

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES
## RELATED LINKS
