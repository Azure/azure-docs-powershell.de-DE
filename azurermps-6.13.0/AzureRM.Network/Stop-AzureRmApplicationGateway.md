---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
ms.openlocfilehash: a235ae8ad4467e135e85599300869bcb36805a30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662994"
---
# Stop-AzureRmApplicationGateway

## Synopsis
Beenden eines Anwendungs Gateways

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Stop-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Stop-AzureRmApplicationGateway** beendet ein Anwendungsgateway.

## Beispiele

### Beispiel 1: Beenden eines Anwendungs Gateways
```
PS C:\>Stop-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

Mit diesem Befehl wird das in der $AppGw-Variable gespeicherte Anwendungsgateway angehalten.

## Parameter

### -ApplicationGateway
Gibt das Anwendungsgateway an, das mit diesem Cmdlet beendet wird.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AsJob
Ausführen eines Cmdlets im Hintergrund

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

### Microsoft. Azure. Commands. Network. Models. PSApplicationGateway
Parameter: ApplicationGateway (ByValue)

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSApplicationGateway

## Notizen

## Verwandte Links

[Get-AzureRmApplicationGateway](./Get-AzureRmApplicationGateway.md)

[Neu – AzureRmApplicationGateway](./New-AzureRmApplicationGateway.md)

[Remove-AzureRmApplicationGateway](./Remove-AzureRmApplicationGateway.md)

[Satz-AzureRmApplicationGateway](./Set-AzureRmApplicationGateway.md)

[Anfang-AzureRmApplicationGateway](./Start-AzureRmApplicationGateway.md)


