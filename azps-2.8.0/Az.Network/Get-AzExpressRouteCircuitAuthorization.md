---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 3d14a82cf387d85644870766cf92d1ede0c50b9b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821868"
---
# Get-AzExpressRouteCircuitAuthorization

## Synopsis
Ruft Informationen zu Express Route-Schaltkreis Berechtigungen ab.

## Syntax

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzExpressRouteCircuitAuthorization** " Ruft Informationen zu den Berechtigungen ab, die einem Express Route-Schaltkreis zugewiesen sind. Express Route-Schaltkreise verbinden Ihr lokales Netzwerk mit der Microsoft-Cloud, indem Sie einen Verbindungsanbieter anstelle des öffentlichen Internets verwenden. Der Besitzer eines Express Route-Schaltkreises kann bis zu 10 Berechtigungen für jeden Schaltkreis erstellen. Diese Berechtigungen generieren einen Autorisierungsschlüssel, der von einem virtuellen Netzwerk Besitzer verwendet werden kann, um sein Netzwerk mit dem Schaltkreis (eine Autorisierung pro virtuelles Netzwerk) zu verbinden. Autorisierungsschlüssel sowie weitere Informationen zur Autorisierung können jederzeit angezeigt werden, indem **Sie Get-AzExpressRouteCircuitAuthorization** ausführen.

## Beispiele

### Beispiel 1: Abrufen aller Express Route-Berechtigungen
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

Diese Befehle geben Informationen zu allen Express Route-Berechtigungen zurück, die einem Express Route-Schaltkreis zugeordnet sind. Der erste Befehl verwendet das Cmdlet " **Get-AzExpressRouteCircuit** ", um einen Objektverweis auf einen Schaltkreis mit dem Namen ContosoCircuit zu erstellen. dieser Objektverweis wird in der Variablen $Circuit gespeichert. Der zweite Befehl verwendet dann diesen Objektverweis und das Cmdlet " **Get-AzExpressRouteCircuitAuthorization** ", um Informationen zu den Berechtigungen zurückzugeben, die mit ContosoCircuit verknüpft sind.

### Beispiel 2: Abrufen aller Express Route-Berechtigungen mithilfe des Where-Object-Cmdlets
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

Diese Befehle stellen eine Variation der in Beispiel 1 verwendeten Befehle dar. In diesem Fall werden Informationen jedoch nur für diejenigen Berechtigungen zurückgegeben, die für die Verwendung verfügbar sind (also für Berechtigungen, die nicht einem virtuellen Netzwerk zugewiesen wurden). Zu diesem Zweck werden die Informationen zur Schaltkreis Autorisierung in Befehl 2 zurückgegeben und an das Cmdlet **Where-Object** umgeleitet.
**Where-Object** wählt dann nur die Berechtigungen aus, bei denen die *AuthorizationUseStatus* -Eigenschaft auf available festgesetzt ist. Verwenden Sie diese Syntax für die WHERE-Klausel, um nur die nicht verfügbaren Berechtigungen aufzulisten: `{$_.AuthorizationUseStatus -ne "Available"}`

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
Gibt die Express Route-Schaltkreis Autorisierung an.

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
Gibt den Namen der Express Route-Schaltkreis Autorisierung an, die dieses Cmdlet erhält.
-Name "ContosoCircuitAuthorization"

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization

## Notizen

## Verwandte Links

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[Neu – AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)
