---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 15aed0e5a4cca1b67c85cbe651453d64cecc13ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154425"
---
# Get-AzExpressRouteCrossConnectionPeering

## SYNOPSIS
Ruft eine ExpressRoute-übergreifende Peeringkonfiguration ab.

## SYNTAX

```
Get-AzExpressRouteCrossConnectionPeering [-Name <String>]
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzExpressRouteCrossConnectionPeering"** ruft die Konfiguration einer Peeringbeziehung für eine ExpressRoute-Kreuzverbindung ab.

## BEISPIELE

### Beispiel 1: Anzeigen der Peeringkonfiguration für eine ExpressRoute-Kreuzverbindung
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $RG
Get-AzExpressRouteCrossConnectionPeering -Name "AzurePrivatePeering" -ExpressRouteCrossConnection $cc
```

## PARAMETERS

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

### -ExpressRouteCrossConnection
Das ExpressRoute-Kreuzverbindungsobjekt, das die Peeringkonfiguration enthält.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Der Name der abzurufenden Peeringkonfiguration.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### PSExpressRouteCrossConnection
Der Parameter 'ExpressRouteCrossConnection' akzeptiert den Wert des Typs 'PSExpressRouteCrossConnection' aus der Pipeline

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSPeering

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Add-AzExpressRouteCrossConnectionPeering](Add-AzExpressRouteCrossConnectionPeering.md)

[Remove-AzExpressRouteCrossConnectionPeering](Remove-AzExpressRouteCrossConnectionPeering.md)

[Get-AzExpressRouteCrossConnection](Get-AzExpressRouteCrossConnection.md)

[Set-AzExpressRouteCrossConnection](Set-AzExpressRouteCrossConnection.md)
