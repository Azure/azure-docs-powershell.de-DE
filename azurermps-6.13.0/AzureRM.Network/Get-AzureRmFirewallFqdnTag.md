---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewallFqdnTag.md
ms.openlocfilehash: 33482ff6686409c62a2aeffbf616f62074b1984e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664824"
---
# Get-AzureRmFirewallFqdnTag

## Synopsis
Ruft die verfügbaren Azure Firewall-FQDN-Tags ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmFirewallFqdnTag** " Ruft die Liste der FQDN-Tags ab, die für Azure Firewall-Anwendungsregeln verwendet werden können.

## Beispiele

### 1: Abrufen aller verfügbaren FQDN-Tags
```
Get-AzureRmFirewallFqdnTag
```

In diesem Beispiel werden alle verfügbaren FQDN-Tags abgerufen.

### 2: Verwenden des ersten verfügbaren FQDN-Tags in einer Anwendungsregel
```
$fqdnTags = Get-AzureRmFirewallFqdnTag
New-AzureRmFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

In diesem Beispiel wird eine Firewall-Anwendungsregel mit dem ersten verfügbaren FQDN-Tag erstellt

## Parameter

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
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSAzureFirewallFqdnTag

## Notizen

## Verwandte Links

[Neu – AzureRmFirewallApplicationRule](./New-AzureRmFirewallApplicationRule.md)

[Neu – AzureRmFirewall](./New-AzureRmFirewall.md)
