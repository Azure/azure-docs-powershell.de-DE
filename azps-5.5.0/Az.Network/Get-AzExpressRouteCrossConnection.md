---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3efb6270-f908-4734-bdb1-6c7e4e4eb382
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
ms.openlocfilehash: a6a3b973a893e3588b5df77700318a725bde11b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154441"
---
# Get-AzExpressRouteCrossConnection

## SYNOPSIS
Ruft eine Azure -ExpressRoute-Kreuzverbindung aus Azure ab.

## SYNTAX

```
Get-AzExpressRouteCrossConnection [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzExpressRouteCrossConnection"** wird verwendet, um ein ExpressRoute-Kreuzverbindungsobjekt aus Ihrem Abonnement abzurufen.
AzureRmExpressRouteCrossConnection

## BEISPIELE

### Beispiel 1: Herstellen der ExpressRoute-Querverbindung
```
Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
```

### Beispiel 2: Auflisten der ExpressRoute-Kreuzverbindungen mithilfe eines Filters
```
Get-AzExpressRouteCrossConnection -Name test*
```

Dieses Cmdlet listet alle ExpressRoute-Kreuzverbindungen auf, die mit "Test" beginnen.

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

### -Name
Der Name der ExpressRoute-Kreuzverbindung.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -ResourceGroupName
Der Name der Ressourcengruppe, die die ExpressRoute-Kreuzverbindung enthält.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Set-AzExpressRouteCrossConnection](Set-AzExpressRouteCrossConnection.md)