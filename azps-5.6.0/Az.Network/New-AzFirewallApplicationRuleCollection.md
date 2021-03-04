---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallapplicationrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
ms.openlocfilehash: c82b150dd10a293bda1a001e4b930bcc2fe7989b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950131"
---
# New-AzFirewallApplicationRuleCollection

## SYNOPSIS
Erstellt eine Sammlung von Firewallanwendungsregeln.

## SYNTAX

```
New-AzFirewallApplicationRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallApplicationRule[]> -ActionType <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet New-AzFirewallApplicationRuleCollection** erstellt eine Sammlung von Firewallanwendungsregeln.

## BEISPIELE

### Beispiel 1: Erstellen einer Sammlung mit einer Regel
```powershell
$rule1 = New-AzFirewallApplicationRule -Name "httpsRule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 1000 -Rule $rule1 -ActionType "Allow"
```

In diesem Beispiel wird eine Sammlung mit einer Regel erstellt. Der datenverkehr, der den in $rule 1 genannten Bedingungen entspricht, ist zulässig.
Die erste Regel gilt für den ganzen HTTPS-Datenverkehr auf Port 443 von 10.0.0.0. Wenn es eine andere Anwendungsregelsammlung mit höherer Priorität (kleinere Zahl) gibt, die auch dem in $rule 1 identifizierten Datenverkehr entspricht, wird stattdessen die Aktion der Regelsammlung mit höherer Priorität wirksam. 

### Beispiel 2: Hinzufügen einer Regel zu einer Regelsammlung
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection.AddRule($rule2)
```

In diesem Beispiel wird eine neue Anwendungsregelsammlung mit einer Regel erstellt, und dann wird der Regelsammlung mithilfe von Methoden-AddRule für das Regelsammlungsobjekt eine zweite Regel hinzugefügt. Jeder Regelname in einer bestimmten Regelsammlung muss einen eindeutigen Namen haben und die Groß-/Kleinschreibung nicht beachtet werden.

### Beispiel 3: Erhalten einer Regel aus einer Regelsammlung
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("r1")
```

In diesem Beispiel wird eine neue Anwendungsregelsammlung mit einer Regel erstellt, und dann wird die Regel nach Name und aufruft die -Methode GetRuleByName für das Regelsammlungsobjekt. Der Regelname für die Methode GetRuleByName ist groß-/kleinschreibungsunabhängiger.

### Beispiel 4: Entfernen einer Regel aus einer Regelsammlung
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1, $rule1 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("r1")
```

In diesem Beispiel wird eine neue Anwendungsregelsammlung mit zwei Regeln erstellt und dann die erste Regel aus der Regelsammlung entfernt, indem die Methode RemoveRuleByName für das Regelsammlungsobjekt aufruft. Der Regelname für die Methode RemoveRuleByName ist groß- und kleinschreibungsunabhängiger.

## PARAMETER

### -ActionType
Die Aktion der Regelsammlung

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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
Gibt den Namen dieser Anwendungsregel an. Der Name muss innerhalb einer Regelsammlung eindeutig sein.

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

### -Priorität
Gibt die Priorität dieser Regel an. Priorität ist eine Zahl zwischen 100 und 65000. Je kleiner die Zahl, desto größer die Priorität.

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Regel
Gibt die Liste der Regeln an, die unter dieser Auflistung zu gruppieren sind.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bestätigen
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection

## NOTIZEN

## VERWANDTE LINKS

[New-AzFirewallApplicationRule](./New-AzFirewallApplicationRule.md)

[New-AzFirewall](./New-AzFirewall.md)

[Get-AzFirewall](./Get-AzFirewall.md)
