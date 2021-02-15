---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorCustomRuleObject.md
ms.openlocfilehash: 8602bd4636e3e6034552f48a6f6514a453b816a0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400670"
---
# New-AzFrontDoorCustomRuleObject

## SYNOPSIS
Erstellen eines Benutzerdefinierten Objekts für die Erstellung einer WAF-Richtlinie

## SYNTAX

```
New-AzFrontDoorCustomRuleObject -Name <String> -RuleType <PSCustomRuleType>
 -MatchCondition <PSMatchCondition[]> -Action <PSAction> -Priority <Int32>
 [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Erstellen eines Benutzerdefinierten Objekts für die Erstellung einer WAF-Richtlinie

## BEISPIELE

### Beispiel 1
```powershell
PS C:\> New-AzFrontDoorCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

Erstellen eines CustomRule-Objekts

## PARAMETERS

### -Action
Aktionstyp.
Mögliche Werte sind: "Zulassen", "Blockieren", "Protokoll".

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log, Redirect

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -MatchCondition
Liste der Übereinstimmungsbedingungen.

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Name der Regel

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

### -Priority
Beschreibt die Priorität der Regel.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RateLimitDurationInMinutes
Dauer des Satzlimits. Standard – 1 Minute

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RateLimitThreshold
Satzlimit wird überschritten

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RuleType
Typ der Regel.
Mögliche Werte sind: 'MatchRule', 'RateLimitRule'

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRuleType
Parameter Sets: (All)
Aliases:
Accepted values: RateLimitRule, MatchRule

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.FrontDando.Models.PSCustomRule

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[New-AzFrontD firewallWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Update-AzFrontD firewallWallPolicy](./Update-AzFrontDoorFireWallPolicy.md)
