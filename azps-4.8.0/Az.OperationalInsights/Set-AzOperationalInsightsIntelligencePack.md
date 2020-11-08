---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: a8d799cec6278149cb4c08faf68584fb7968f85e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165071"
---
# Set-AzOperationalInsightsIntelligencePack

## Synopsis
Aktiviert oder deaktiviert das angegebene Intelligence Pack.

## Syntax

```
Set-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Set-AzOperationalInsightsIntelligencePack** " aktiviert das angegebene Intelligence Pack, wenn *Enabled* auf "$true" festgelegt ist und deaktiviert ist, wenn " *Enabled* " auf "$false" festgelegt ist.

## Beispiele

### Beispiel 1: Einrichten von Intelligence Packs
```
PS C:\>Set-AzOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

Mit diesem Befehl wird das angegebene Intelligence Pack aktiviert.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -Aktiviert
```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IntelligencePackName
Gibt den Namen des Intelligence-Pakets an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WorkspaceName
Gibt den Namen des Arbeitsbereichs an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

### System. Boolean

## Ausgaben

### Microsoft. Azure. Commands. OperationalInsights. Models. PSIntelligencePack

## Notizen

## Verwandte Links

[Azure-Cmdlets für operationelle Einblicke](./Az.OperationalInsights.md)


