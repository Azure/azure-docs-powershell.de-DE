---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoormanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorManagedRuleObject.md
ms.openlocfilehash: 236cb9ff263f97ae52ea5d3226f4defec00c662a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663136"
---
# New-AzureRmFrontDoorManagedRuleObject

## Synopsis
Erstellen eines ManagedRule-Objekts für die WAF-Richtlinienerstellung

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureRmFrontDoorManagedRuleObject -Priority <Int32> [-Version <String>]
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Erstellen eines ManagedRule-Objekts für die WAF-Richtlinienerstellung

## Beispiele

### Beispiel 1
```powershell
PS C:\> New-AzureRmFrontDoor
ManagedRuleObject -Priority 1 -Version 0 -RuleGroupOverride $override1

RuleGroupOverrides                                                   Priority Version
------------------                                                   -------- -------
{Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride}        1 0
```

Erstellen eines ManagedRule-Objekts

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

### -Priorität
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

### -RuleGroupOverride
Liste der Überschreibung der Azure Managed Provider-Konfiguration

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version
Version des RuleSet

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### Microsoft. Azure. Commands. Haustür. Models. PSAzureManagedRule

## Notizen

## Verwandte Links

[Neu – AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Satz-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md) 
 [Neu – AzureRmFrontDoorRuleGroupOverrideObject](./Set-AzureRmFrontDoorRuleGroupOverrideObject.md)
