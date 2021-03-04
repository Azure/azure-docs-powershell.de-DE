---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/get-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
ms.openlocfilehash: f48fadb740fdca823c2513d68a2f77e0d34c4631
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919976"
---
# Get-AzFrontDoor

## SYNOPSIS
Ladenausgleich für die Eingangstür

## SYNTAX

```
Get-AzFrontDoor [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzFrontDoor-CmdletGet** ruft alle vorhandenen Front Doors im aktuellen Abonnement ab, die den bereitgestellten Informationen entspricht.

## BEISPIELE

### Beispiel 1: Alle FrontDoors im aktuellen Abonnement erhalten.
```powershell
PS C:\> Get-AzFrontDoor

FriendlyName          : frontdoor1
FrontDoorId           : {guid}
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid1}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1

FriendlyName          : frontdoor1
FrontDoorId           : {guid}
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid2}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

Alle FrontDoors im aktuellen Abonnement erhalten.

### Beispiel 2: Alle FrontDoors in der Ressourcengruppe "rg1" im aktuellen Abonnement erhalten.
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1"

FriendlyName          : frontdoor1
FrontDoorId           : {guid}
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1

FriendlyName          : frontdoor2
FrontDoorId           : {guid}
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

Alle FrontDoors in der Ressourcengruppe "rg1" im aktuellen Abonnement.

### Beispiel 3: Holen Sie sich die FrontDoors in der Ressourcengruppe "rg1" mit dem Namen "frontDoor1" im aktuellen Abonnement.
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" -Name "frontDoor1"

FriendlyName          : frontdoor1
FrontDoorId           : {guid}
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

Holen Sie sich die FrontDoors in der Ressourcengruppe "rg1" mit dem Namen "frontDoor1" im aktuellen Abonnement.

## PARAMETER

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Name der Eingangstür.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Frontdoor.Models.PSFrontDoor

## NOTIZEN

## VERWANDTE LINKS

[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
