---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: 9cb5a19adaf5c9d7371196a5ed917a557ef7c6e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481829"
---
# Set-AzureRmNetworkSecurityGroup

## Synopsis
Legt den Zielstatus für eine Netzwerksicherheitsgruppe fest.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Set-AzureRmNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Set-AzureRmNetworkSecurityGroup** " legt den Zielstatus für eine Azure Network Security-Gruppe fest.

## Beispiele

### Beispiel 1: Festlegung des Zielstatus für eine Netzwerksicherheitsgruppe
```
PS C:\>Get-AzureRmNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzureRmNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzureRmNetworkSecurityGroup
```

Dieser Befehl ruft die Azure Network Security-Gruppe mit dem Namen Nsg1 ab und fügt eine Netzwerk Sicherheitsregel mit dem Namen Rdp-Rule hinzu, um den Internet Datenverkehr auf Port 3389 dem abgerufenen Netzwerk Sicherheitsgruppenobjekt mithilfe von Add-AzureRmNetworkSecurityRuleConfig zu ermöglichen.
Der Befehl behält die geänderte Azure Network Security-Gruppe mithilfe von " **AzureRmNetworkSecurityGroup** " bei.

## Parameter

### -NetworkSecurityGroup
Ein Netzwerk Sicherheitsgruppenobjekt, das den Zielstatus darstellt, zu dem das Cmdlet die Netzwerksicherheitsgruppe festlegt.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### PSNetworkSecurityGroup
Der Parameter "NetworkSecurityGroup" akzeptiert den Wert vom Typ "PSNetworkSecurityGroup" aus der Pipeline.

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup

## Notizen

## Verwandte Links

[Get-AzureRmNetworkSecurityGroup](./Get-AzureRmNetworkSecurityGroup.md)

[Neu – AzureRmNetworkSecurityGroup](./New-AzureRmNetworkSecurityGroup.md)

[Remove-AzureRmNetworkSecurityGroup](./Remove-AzureRmNetworkSecurityGroup.md)


