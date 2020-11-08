---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 8152cf778cabed1c4a8a346ac86b708266058fc6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003529"
---
# Get-AzNetworkInterfaceIpConfig

## Synopsis
Ruft eine Netzwerkschnittstellen-IP-Konfiguration für eine Netzwerkschnittstelle ab.

## Syntax

```
Get-AzNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzNetworkInterfaceIPConfig** " Ruft eine Netzwerkschnittstellen-IP-Konfiguration über eine Azure-Netzwerkschnittstelle ab.

## Beispiele

### 1: Abrufen einer IP-Konfiguration einer Netzwerkschnittstelle
```
$nic1 = Get-AzNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

Der erste Befehl ruft eine vorhandene Netzwerkschnittstelle namens mynic ab und speichert Sie in der Variablen $NIC 1. Der zweite Befehl ruft die IP-Konfiguration mit dem Namen ipconfig1 dieser Netzwerkschnittstelle ab.
    

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

### -Name
Gibt den Namen der Netzwerk-IP-Konfiguration an, die dieses Cmdlet erhält.

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

### -Network Interface
Gibt ein **Network Interface** -Objekt an, das die Netzwerk-IP-Konfiguration enthält, die dieses Cmdlet erhält.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. Commands. Network. Models. PSNetworkInterface

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration

## Notizen
* Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke

## Verwandte Links

[Add-AzNetworkInterfaceIpConfig](./Add-AzNetworkInterfaceIpConfig.md)

[Neu – AzNetworkInterfaceIpConfig](./New-AzNetworkInterfaceIpConfig.md)

[Remove-AzNetworkInterfaceIpConfig](./Remove-AzNetworkInterfaceIpConfig.md)

[Satz-AzNetworkInterfaceIpConfig](./Set-AzNetworkInterfaceIpConfig.md)


