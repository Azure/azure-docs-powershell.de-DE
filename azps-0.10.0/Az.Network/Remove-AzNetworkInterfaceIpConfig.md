---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 2ccb5f7117df8f959698c894915cedd3a5d4c7e2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841124"
---
# Remove-AzNetworkInterfaceIpConfig

## Synopsis
Entfernt eine Netzwerkschnittstellen-IP-Konfiguration von einer Netzwerkschnittstelle.

## Syntax

```
Remove-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzNetworkInterfaceIpConfig** entfernt eine Netzwerkschnittstellen-IP-Konfiguration über eine Azure-Netzwerkschnittstelle.

## Beispiele

### 1: Löschen einer IP-Konfiguration über eine Netzwerkschnittstelle
```
$nic = Get-AzNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic
```

Der erste Befehl ruft eine Netzwerkschnittstelle mit dem Namen mynic ab und speichert Sie in der Variablen $NIC. Der zweite Befehl entfernt die IP-Konfiguration mit dem Namen ipconfig-1, die dieser Netzwerkschnittstelle zugeordnet ist.

## Parameter

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

### -Name
Gibt den Namen der zu entfernenden Netzwerkschnittstellen-IP-Konfiguration an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Network Interface
Gibt ein **Network Interface** -Objekt an.
Dieses Objekt enthält die zu entfernende Netzwerkschnittstellen-IP-Konfiguration.

```yaml
Type: PSNetworkInterface
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

### PSNetworkInterface
Der Parameter "Network Interface" akzeptiert den Wert vom Typ "PSNetworkInterface" aus der Pipeline.

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSNetworkInterface

## Notizen
* Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke

## Verwandte Links

[Add-AzNetworkInterfaceIpConfig](./Add-AzNetworkInterfaceIpConfig.md)

[Get-AzNetworkInterfaceIpConfig](./Get-AzNetworkInterfaceIpConfig.md)

[Neu – AzNetworkInterfaceIpConfig](./New-AzNetworkInterfaceIpConfig.md)

[Satz-AzNetworkInterfaceIpConfig](./Set-AzNetworkInterfaceIpConfig.md)


