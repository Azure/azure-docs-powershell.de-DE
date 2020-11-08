---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: d98366d9bd3fb42be39f68976e131ec644274431
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179849"
---
# Remove-AzExpressRouteCircuitAuthorization

## Synopsis
Entfernt eine vorhandene Express Route-Konfigurations Autorisierung.

## Syntax

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzExpressRouteCircuitAuthorization** entfernt eine Autorisierung, die einem Express Route-Schaltkreis zugewiesen ist. Express Route-Schaltkreise verbinden Ihr lokales Netzwerk mithilfe eines Verbindungs Anbieters anstelle des öffentlichen Internets mit Azure. Der Besitzer eines Express Route-Schaltkreises kann bis zu 10 Berechtigungen für jeden Schaltkreis erstellen. Diese Berechtigungen generieren einen Autorisierungsschlüssel, der von einem virtuellen Netzwerk Besitzer verwendet werden kann, um sein Netzwerk mit dem Schaltkreis zu verbinden. Pro virtuelles Netzwerk kann nur eine Autorisierung vorhanden sein. Der Leitungs Besitzer kann jedoch jederzeit mithilfe von **Remove-AzExpressRouteCircuitAuthorization** die Autorisierung entfernen, die einem virtuellen Netzwerk zugewiesen ist. In diesem Fall ist das entsprechende virtuelle Netzwerk nicht mehr in der Lage, die Express Route-Schaltung zum Herstellen einer Verbindung mit Azure zu verwenden.

## Beispiele

### Beispiel 1: Entfernen einer Schaltkreis Autorisierung von einem Express Route-Schaltkreis
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

In diesem Beispiel wird eine Schaltkreis Autorisierung aus einem Express Route-Schaltkreis entfernt. Der erste Befehl verwendet das Cmdlet " **Get-AzExpressRouteCircuit** ", um einen Objektverweis auf einen Express Route-Schaltkreis mit dem Namen ContosoCircuit zu erstellen und das Ergebnis in der Variablen mit dem Namen $Circuit zu speichern.
Der zweite Befehl kennzeichnet den ContosoCircuitAuthorization für die Schaltkreis Autorisierung zum Entfernen.
Der dritte Befehl verwendet das Set-AzExpressRouteCircuit-Cmdlet, um die Entfernung des in der $Circuit Variablen gespeicherten Express Route-Schaltkreises zu bestätigen.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### -ExpressRouteCircuit
Gibt das ExpressRouteCircuit-Objekt an, das vom Cmdlet entfernt wird.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Gibt den Namen der Schaltkreis Autorisierung an, die vom Cmdlet entfernt wird.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit

## Notizen

## Verwandte Links

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[Neu – AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Satz-AzExpressRouteCircuit](./Set-AzExpressRouteCircuit.md)
