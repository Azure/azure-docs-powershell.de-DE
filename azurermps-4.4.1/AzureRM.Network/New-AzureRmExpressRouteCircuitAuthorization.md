---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 2fec428adb2ba8621d09a1f0ae5e762cdbe4b913
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664249"
---
# New-AzureRmExpressRouteCircuitAuthorization

## Synopsis
Erstellt eine Express Route-Schaltkreis Autorisierung.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureRmExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmExpressRouteCircuitAuthorization** erstellt eine Schaltkreis Autorisierung, die einem Express Route-Schaltkreis hinzugefügt werden kann. Express Route-Schaltkreise verbinden Ihr lokales Netzwerk mit der Microsoft-Cloud, indem Sie einen Verbindungsanbieter anstelle des öffentlichen Internets verwenden. Der Besitzer eines Express Route-Schaltkreises kann bis zu 10 Berechtigungen für jeden Schaltkreis erstellen. Diese Berechtigungen generieren einen Autorisierungsschlüssel, der von einem virtuellen Netzwerk Besitzer verwendet werden kann, um ein Netzwerk mit dem Schaltkreis zu verbinden. Pro virtuelles Netzwerk kann nur eine Autorisierung vorhanden sein.

Nachdem Sie einen Express Route-Schaltkreis erstellt haben, können Sie **Add-AzureRmExpressRouteCircuitAuthorization** verwenden, um dieser Schaltkreis eine Autorisierung hinzuzufügen.
Alternativ können Sie auch **New-AzureRmExpressRouteCircuitAuthorization** verwenden, um eine Autorisierung zu erstellen, die gleichzeitig zu einem neuen Schaltkreis hinzugefügt werden kann, wenn der Schaltkreis erstellt wird.

## Beispiele

### Beispiel 1: Erstellen einer neuen Schaltkreis Autorisierung
```
$Authorization = New-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

Dieser Befehl erstellt eine neue Schaltkreis Autorisierung mit dem Namen "ContosoCircuitAuthorization" und speichert dieses Objekt dann in einer Variablen mit dem Namen "$Authorization". Das Speichern des Objekts in einer Variablen ist wichtig: Obwohl **New-AzureRmExpressRouteCircuitAuthorization** eine Schaltkreis Autorisierung erstellen kann, kann diese Berechtigung nicht zu einer leitungsroute hinzugefügt werden. Stattdessen wird die Variable $Authorization New-AzureRmExpressRouteCircuit beim Erstellen eines brandneuen Express Route-Schaltkreises verwendet.

Weitere Informationen finden Sie in der Dokumentation zum New-AzureRmExpressRouteCircuit-Cmdlet.

## Parameter

### -Name
Gibt einen eindeutigen Namen für die neue Express Route-Schaltkreis Autorisierung an.

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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Pipeline-Eingabe.

## Ausgaben

### PSExpressRouteCircuitAuthorization
Dieses Cmdlet erstellt Instanzen des **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization** -Objekts.

## Notizen

## Verwandte Links

[Add-AzureRmExpressRouteCircuitAuthorization](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[Get-AzureRmExpressRouteCircuitAuthorization](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[Remove-AzureRmExpressRouteCircuitAuthorization](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

