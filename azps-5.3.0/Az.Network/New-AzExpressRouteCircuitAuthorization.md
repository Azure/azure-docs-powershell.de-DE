---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 28b45f5368fb7a63450276c054654313d7e1c517
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459968"
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
Das **Cmdlet "New-AzExpressRouteCircuitAuthorization"** erstellt eine Schaltkreisautorisierung, die einem Leitungen hinzugefügt werden kann. ExpressRoute-Schaltkreise verbinden Ihr lokales Netzwerk mit der Microsoft-Cloud, indem anstelle des öffentlichen Internets ein Konnektivitätsanbieter verwendet wird. Der Besitzer eines #A0 kann bis zu 10 Autorisierungen für jeden Schaltkreis erstellen. diese Autorisierungen generieren einen Autorisierungsschlüssel, der von einem virtuellen Netzwerkbesitzer verwendet werden kann, um ein Netzwerk mit dem Schaltkreis zu verbinden. Pro virtuellem Netzwerk kann es nur eine Autorisierung gibt.
Nachdem Sie einen "ExpressRoute"-Schaltkreis erstellt haben, können Sie **"Add-AzExpressRouteCircuitAuthorization"** verwenden, um dem Schaltkreis eine Autorisierung hinzuzufügen.
Alternativ können Sie **"New-AzExpressRouteCircuitAuthorization"** verwenden, um eine Autorisierung zu erstellen, die gleichzeitig mit der Erstellung des Schaltkreises einem neuen Schaltkreis hinzugefügt werden kann.

## BEISPIELE

### Beispiel 1: Erstellen einer neuen Schaltkreisautorisierung
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

Mit diesem Befehl wird eine neue Schaltkreisautorisierung namens "ContosoCircuitAuthorization" erstellt und dieses Objekt dann in einer Variablen namens "$Authorization. Das Speichern des Objekts in einer Variablen ist wichtig: Obwohl **"New-AzExpressRouteCircuitAuthorization"** eine Schaltkreisautorisierung erstellen kann, kann diese Autorisierung einer Schaltkreisroute nicht hinzugefügt werden. Stattdessen wird die variable $Authorization beim New-AzExpressRouteCircuit erstellen eines völlig neuen "ExpressRoute"-Schaltkreises verwendet.
Weitere Informationen finden Sie in der Dokumentation zum New-AzExpressRouteCircuit Cmdlet.

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
Gibt einen eindeutigen Namen für die neue ExpressRoute-Schaltkreisautorisierung an.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)

