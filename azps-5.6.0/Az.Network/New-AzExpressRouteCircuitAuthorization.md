---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 9c247784a9f890d97aee301383656f97ef9c7dd4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941080"
---
# New-AzExpressRouteCircuitAuthorization

## SYNOPSIS
Erstellt eine ExpressRoute-Schaltkreisautorisierung.

## SYNTAX

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet New-AzExpressRouteCircuitAuthorization** erstellt eine Schaltungsautorisierung, die einem ExpressRoute-Schaltkreis hinzugefügt werden kann. ExpressRoute-Schaltkreise verbinden Ihr lokales Netzwerk mit der Microsoft-Cloud, indem sie einen Konnektivitätsanbieter anstelle des öffentlichen Internets verwenden. Der Besitzer eines #A0 kann bis zu 10 Berechtigungen für jeden Schaltkreis erstellen. Diese Autorisierungen generieren einen Autorisierungsschlüssel, der von einem Besitzer eines virtuellen Netzwerks verwendet werden kann, um ein Netzwerk mit dem Schaltkreis zu verbinden. Pro virtuellem Netzwerk kann nur eine Autorisierung ausgeführt werden.
Nachdem Sie einen ExpressRoute-Schaltkreis erstellt haben, können Sie **Add-AzExpressRouteCircuitAuthorization** verwenden, um dieser Schaltung eine Autorisierung hinzuzufügen.
Alternativ können Sie **new-AzExpressRouteCircuitAuthorization** verwenden, um eine Autorisierung zu erstellen, die gleichzeitig mit der Erstellung des Schaltkreises einem neuen Schaltkreis hinzugefügt werden kann.

## BEISPIELE

### Beispiel 1: Erstellen einer neuen Schaltkreisautorisierung
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

Dieser Befehl erstellt eine neue Schaltkreisautorisierung namens ContosoCircuitAuthorization und speichert dieses Objekt dann in einer Variablen namens $Authorization. Das Speichern des Objekts in einer Variablen ist wichtig: Obwohl **New-AzExpressRouteCircuitAuthorization** eine Schaltungsautorisierung erstellen kann, kann diese Autorisierung nicht zu einer Stromkreisroute hinzugefügt werden. Stattdessen wird die Variable $Authorization verwendet, New-AzExpressRouteCircuit beim Erstellen eines brandneuen ExpressRoute-Schaltkreises verwendet wird.
Weitere Informationen finden Sie in der Dokumentation zum New-AzExpressRouteCircuit Cmdlet.

## PARAMETER

### -DefaultProfile
Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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
Gibt einen eindeutigen Namen für die neue ExpressRoute-Schaltungsautorisierung an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization

## NOTIZEN

## VERWANDTE LINKS

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)

