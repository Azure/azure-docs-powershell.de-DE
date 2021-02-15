---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
ms.openlocfilehash: df298b41ea1efa4915cb7556b9fd07b1d8f3e2de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151620"
---
# New-AzPrivateEndpoint

## SYNOPSIS
Erstellt einen privaten Endpunkt.

## SYNTAX

### Alle

```
New-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 -PrivateLinkServiceConnection <PSPrivateLinkServiceConnection[]> [-ByManualRequest] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG

Das **Cmdlet "New-AzPrivateEndpoint"** erstellt einen privaten Endpunkt.

## BEISPIELE

### Beispiel 1: Erstellen eines privaten Endpunkts

Im folgenden Beispiel wird ein privater Endpunkt mit einer bestimmten Dienst-ID für private Verknüpfungen im angegebenen Subnetz in einem virtuellen Netzwerk erstellt.

```powershell
$virtualNetwork = Get-AzVirtualNetwork -ResourceName 'myVirtualNetwork' -ResourceGroupName 'myResourceGroup'
$subnet = $virtualNetwork | Select-Object -ExpandProperty subnets | Where-Object Name -eq 'mySubnet'
$plsConnection= New-AzPrivateLinkServiceConnection -Name 'MyPLSConnections' -PrivateLinkServiceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService' -RequestMessage 'Please Approve my request'
New-AzPrivateEndpoint -Name 'MyPrivateEndpoint' -ResourceGroup 'myResourceGroup' -Location 'centralus' -PrivateLinkServiceConnection $plsConnection -Subnet $subnet
```

## PARAMETERS

### -AsJob

Führen Sie das Cmdlet als Aufgabe im Hintergrund aus.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ByManualRequest

Verwenden Sie die manuelle Anforderung, um die Verbindung herzustellen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Force

Fordern Sie keine Bestätigung zum Überschreiben einer Ressource an.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location

Gibt eine Position für den privaten Endpunkt an. Verwenden [Sie "Get-AzLocation",](/powershell/module/az.resources/get-azlocation) um gültige Werte für diesen Parameter zu ermitteln.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name

Name des privaten Endpunkts.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PrivateLinkServiceConnection

Die Ressourcen-ID zum Verbinden des privaten Endpunkts.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName

Gibt den Namen der Ressourcengruppe an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Subnet

Das Subnetz des privaten Endpunkts.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag

Schlüssel-Wert-Paare in Form einer Hashtabelle. Beispiel: @{key0='value0';key1=$null;key2='value2'}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm

Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Waswenn

Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](/powershell/module/microsoft.powershell.core/about/about_commonparameters)

## EINGABEN

### System.String

### Microsoft.Azure.Commands.Network.Models.PSSubnet

### Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzPrivateEndpoint](./Get-AzPrivateEndpoint.md)

[Remove-AzPrivateEndpoint](./Remove-AzPrivateEndpoint.md)

[New-AzPrivateLinkServiceConnection](./New-AzPrivateLinkServiceConnection.md)