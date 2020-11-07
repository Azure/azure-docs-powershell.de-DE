---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
ms.openlocfilehash: 9991829a70029366086a58020aa53f839db8b6c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658386"
---
# Update-AzActionRule

## Synopsis
Aktualisiert Aktionsregel Eigenschaften.

## Syntax

### ByNameSimplifiedPatch (Standard)
```
Update-AzActionRule -Name <String> -ResourceGroupName <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByResourceId
```
Update-AzActionRule -ResourceId <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObject
```
Update-AzActionRule -InputObject <PSActionRule> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
**Update-AzActionRule** -Cmdlet aktualisiert Aktionsregel Eigenschaften – Status und Kategorien.

## Beispiele

### Beispiel 1
```powershell
PS C:\> Update-AzActionRule -ResourceGroupName "test-rg" -Name "Test-ActionRule" -Status "Disabled"
```

Mit diesem Cmdlet wird die Aktionsregel deaktiviert. 

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

### -Inputobject
Die Ressource "Aktionsregel"

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Name der Aktionsregel

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Name der Aktionsregel

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Resourcen-Nr
Die Ressourcen-ID der Aktionsregel

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Status
Aktionsregel Status

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

### -Tag
Aktionsregel Kategorien

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

### Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule

## Ausgaben

### Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule

## Notizen

## Verwandte Links
