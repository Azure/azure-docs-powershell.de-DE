---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 4079d8b6859a2860116520c52928d13c7e3fa29e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665130"
---
# Remove-AzureRmApplicationGatewayHttpListener

## Synopsis
Entfernt einen HTTP-Listener von einem Anwendungsgateway.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Remove-AzureRmApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureRmApplicationGatewayHttpListener** entfernt einen HTTP-Listener aus einem Azure Application Gateway.

## Beispiele

### Beispiel 1: Entfernen eines Application Gateway HTTP-Listeners
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $AppGw-Variablen.
Mit dem zweiten Befehl wird der HTTP-Listener mit dem Namen Listener02 aus dem Anwendungsgateway entfernt, das in $AppGw gespeichert ist.

## Parameter

### -ApplicationGateway
Gibt das Anwendungsgateway an, aus dem ein HTTP-Listener entfernt werden soll.

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

### -Name
Gibt den Namen des HTTP-Listener an, den dieses Cmdlet entfernt.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. Network. Models. PSApplicationGateway
Parameter: ApplicationGateway (ByValue)

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener

## Notizen

## Verwandte Links

[Add-AzureRmApplicationGatewayHttpListener](./Add-AzureRmApplicationGatewayHttpListener.md)

[Get-AzureRmApplicationGatewayHttpListener](./Get-AzureRmApplicationGatewayHttpListener.md)

[Neu – AzureRmApplicationGatewayHttpListener](./New-AzureRmApplicationGatewayHttpListener.md)

[Satz-AzureRmApplicationGatewayHttpListener](./Set-AzureRmApplicationGatewayHttpListener.md)


