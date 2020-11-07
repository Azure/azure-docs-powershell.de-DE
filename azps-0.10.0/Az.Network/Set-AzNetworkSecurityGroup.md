---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
ms.openlocfilehash: 1c61af223b97ac60dd74f55504ce623b26b5233e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843612"
---
# Set-AzNetworkSecurityGroup

## Synopsis
Legt den Zielstatus für eine Netzwerksicherheitsgruppe fest.

## Syntax

```
Set-AzNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Set-AzNetworkSecurityGroup** " legt den Zielstatus für eine Azure Network Security-Gruppe fest.

## Beispiele

### Beispiel 1: Festlegung des Zielstatus für eine Netzwerksicherheitsgruppe
```
PS C:\>Get-AzNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzNetworkSecurityGroup
```

Dieser Befehl ruft die Azure Network Security-Gruppe mit dem Namen Nsg1 ab und fügt eine Netzwerk Sicherheitsregel mit dem Namen Rdp-Rule hinzu, um den Internet Datenverkehr auf Port 3389 dem abgerufenen Netzwerk Sicherheitsgruppenobjekt mithilfe von Add-AzNetworkSecurityRuleConfig zu ermöglichen.
Der Befehl behält die geänderte Azure Network Security-Gruppe mithilfe von " **AzNetworkSecurityGroup** " bei.

## Parameter

### -AsJob
Ausführen eines Cmdlets im Hintergrund

```yaml
Type: SwitchParameter
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkSecurityGroup
Ein Netzwerk Sicherheitsgruppenobjekt, das den Zielstatus darstellt, zu dem das Cmdlet die Netzwerksicherheitsgruppe festlegt.

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### PSNetworkSecurityGroup
Der Parameter "NetworkSecurityGroup" akzeptiert den Wert vom Typ "PSNetworkSecurityGroup" aus der Pipeline.

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup

## Notizen

## Verwandte Links

[Get-AzNetworkSecurityGroup](./Get-AzNetworkSecurityGroup.md)

[Neu – AzNetworkSecurityGroup](./New-AzNetworkSecurityGroup.md)

[Remove-AzNetworkSecurityGroup](./Remove-AzNetworkSecurityGroup.md)


