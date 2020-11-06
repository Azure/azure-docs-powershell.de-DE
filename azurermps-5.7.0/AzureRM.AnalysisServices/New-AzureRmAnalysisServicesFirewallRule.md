---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
ms.openlocfilehash: 74a6d563772e84c7356c400b674cbab960ee8dd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500649"
---
# New-AzureRmAnalysisServicesFirewallRule

## Synopsis
Erstellt eine neue Analysis Services-Firewallregel

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureRmAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
```

## Beschreibung
Das New-AzureRmAnalysisServicesFirewallRule erstellt ein neues Firewallregel-Objekt.

## Beispiele

### Beispiel 1
```
PS C:\> New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

Erstellt eine Firewallregel mit dem Namen "rule1" mit dem Anfangsbereich 0.0.0.0 und dem Endbereich 255.255.255.255

## Parameter

### -FirewallRuleName
Name der Firewall-Regel

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RangeStart
Der Bereichsanfang einer Firewallregel

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RangeEnd
Das Bereichsende einer Firewallregel

```yaml
Type: String
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## Eingaben

## Ausgaben

### Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesFirewallRule

## Verwandte Links

[Neu – AzureRmAnalysisServicesFirewallConfig](./New-AzureRmAnalysisServicesFirewallConfig.md)
