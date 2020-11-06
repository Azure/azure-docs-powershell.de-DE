---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermbgpservicecommunity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmBgpServiceCommunity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmBgpServiceCommunity.md
ms.openlocfilehash: f951aab0ab655d073c830d08e2665533c961960a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501126"
---
# Get-AzureRmBgpServiceCommunity

## Synopsis
Enthält eine Liste aller Dienste/Regionen, BGP Communities und zugehöriger Präfixe.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmBgpServiceCommunity [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Dieses Cmdlet enthält eine Liste aller Dienste/Regionen, BGP-Communities und zugehörigen Präfixe.

## Beispiele

### Beispiel 1
```
Get-AzureRmBgpServiceCommunity

...

Name           : AzureCentralIndia
Id             : /subscriptions//resourceGroups//providers/Microsoft.Network/bgpServiceCommunities/AzureCentralIndia
Type           : Microsoft.Network/bgpServiceCommunities
BgpCommunities : [
                   {
                     "ServiceSupportedRegion": "Global",
                     "CommunityName": "Azure Central India",
                     "CommunityValue": "12076:51017",
                     "CommunityPrefixes": [
                       "13.71.0.0/18",
                       "20.190.146.0/25",
                       "40.79.214.0/24",
                       "40.81.224.0/19",
                       "40.87.224.0/22",
                       "40.112.39.0/25",
                       "40.112.39.128/26",
                       "40.126.18.0/25",
                       "52.136.24.0/24",
                       "52.140.64.0/18",
                       "52.159.64.0/19",
                       "52.172.128.0/17",
                       "52.239.135.64/26",
                       "52.239.202.0/24",
                       "52.245.96.0/22",
                       "52.253.168.0/22",
                       "104.47.210.0/23",
                       "104.211.64.0/20",
                       "104.211.81.0/24",
                       "104.211.82.0/23",
                       "104.211.84.0/22",
                       "104.211.88.0/21",
                       "104.211.96.0/19"
                     ],
                     "IsAuthorizedToUse": true,
                     "ServiceGroup": "Azure"
                   }
                 ]
...
```

Dieses Cmdlet enthält eine Liste aller Dienste/Regionen, BGP-Communities und zugehörigen Präfixe.

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

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSBgpServiceCommunity

## Notizen

## Verwandte Links

[Verschieben-AzureRmExpressRouteCircuit](Move-AzureRmExpressRouteCircuit.md)

[Neu – AzureRmExpressRouteCircuit](New-AzureRmExpressRouteCircuit.md)

[Remove-AzureRmExpressRouteCircuit](Remove-AzureRmExpressRouteCircuit.md)

[Satz-AzureRmExpressRouteCircuit](Set-AzureRmExpressRouteCircuit.md)

[Get-AzureRmRouteFilter](Get-AzureRmRouteFilter.md)

[Get-AzureRmRouteFilterRuleConfig](Get-AzureRmRouteFilterRuleConfig.md)

[Remove-AzureRmRouteFilter](Remove-AzureRmRouteFilter.md)

[Remove-AzureRmRouteFilterRuleConfig](Remove-AzureRmRouteFilterRuleConfig.md)

[Satz-AzureRmRouteFilter](Set-AzureRmRouteFilter.md)

[Satz-AzureRmRouteFilterRuleConfig](Set-AzureRmRouteFilterRuleConfig.md)

[Neu – AzureRmRouteFilter](New-AzureRmRouteFilter.md)

[Neu – AzureRmRouteFilterRuleConfig](New-AzureRmRouteFilterRuleConfig.md)
