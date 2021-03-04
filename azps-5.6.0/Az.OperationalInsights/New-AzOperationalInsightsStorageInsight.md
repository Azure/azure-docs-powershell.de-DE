---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: f3ab3c381e36c766e6d4bdb24476f6bd1cd69df3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937960"
---
# New-AzOperationalInsightsStorageInsight

## SYNOPSIS
Erstellt eine Speicherinblicke innerhalb eines Arbeitsbereichs.

## SYNTAX

### ByWorkspaceName (Standard)
```
New-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByWorkspaceObject
```
New-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet New-AzOperationalInsightsStorageInsight** erstellt einen neuen Speichereinblick in einem vorhandenen Arbeitsbereich.

## BEISPIELE

### Beispiel 1: Erstellen einer Speicheraufschlussansicht nach Name
```
PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

Der erste Befehl verwendet das Get-AzStorageAccount-Cmdlet, um das Speicherkonto namens ContosoStorage zu erhalten, und speichert es dann in der $Storage Variablen.
Der zweite Befehl übergibt das Speicherkonto in $Storage mithilfe des Pipelineoperators an das Get-AzStorageAccountKey-Cmdlet, um den angegebenen Speicherkontoschlüssel zu erhalten, und speichert ihn dann in der variablen $StorageKey. In diesem Beispiel wird der erste Schlüssel abgerufen. Verwenden Sie zum Abrufen des anderen Werts[1] anstelle von Wert[0].
Mit dem letzten Befehl wird eine Speichereinsicht mit dem Namen "MyStorageInsight" im Arbeitsbereich mit dem Namen "MyWorkspace" erstellt.
Diese Speicheraufschlussinformationen nutzen Daten aus der Tabelle WADWindowsEventLogsTable in der angegebenen Speicherkontoressource.

### Beispiel 2: Erstellen einer Speicheraufschlussansicht mithilfe eines Arbeitsbereichsobjekts
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

Der erste Befehl verwendet das Get-AzOperationalInsightsWorkspace-Cmdlet, um den Arbeitsbereich mit dem Namen MyWorkspace zu erhalten, und speichert ihn dann in der $Workspace-Variable.
Der zweite Befehl verwendet das Get-AzStorageAccount-Cmdlet, um das angegebene Speicherkonto zu erhalten, und speichert es dann in der $Storage Variablen.
Der dritte Befehl übergibt das Speicherkonto in $Storage mithilfe des Pipelineoperators an das Get-AzStorageAccountKey-Cmdlet, um den angegebenen Schlüssel zu erhalten, und speichert ihn dann in der variablen $StorageKey. In diesem Beispiel wird der erste Schlüssel abgerufen. Verwenden Sie zum Abrufen des anderen Werts[1] anstelle von Wert[0].
Mit dem letzten Befehl wird eine Speichereinsicht namens "MyStorageInsight" in dem arbeitsbereich erstellt, der in $Workspace.
Die Storage Insight verwendet Daten aus der Tabelle WADWindowsEventLogsTable in der angegebenen Speicherkontoressource.

## PARAMETER

### -Container
Gibt die Liste der Container an, die die Daten enthalten.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden

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

### -Erzwingen
Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen der Speicheraufschluss-Datei an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Azure-Ressourcengruppe an, die einen Arbeitsbereich enthält.

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountKey
Gibt den Zugriffsschlüssel für das Speicherkonto an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountResourceId
Gibt die Azure-Ressource eines Speicherkontos an.
Dies kann abgerufen werden, indem das cmdlet Get-AzStorageAccount ausgeführt wird und auf den Parameter *Id* des Ergebnisses zugegriffen wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tabellen
Gibt die Liste der Tabellen an, die die Daten bereitstellen.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Arbeitsbereich
Gibt den Arbeitsbereich für die neue Storage Insight an.

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WorkspaceName
Gibt den Namen eines vorhandenen Arbeitsbereichs an.

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace

### System.String

### System.String[]

## AUSGABEN

### Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight

## NOTIZEN

## VERWANDTE LINKS

[Azure Operational Insights-Cmdlets](./Az.OperationalInsights.md)

[Get-AzOperationalInsightsWorkspace](./Get-AzOperationalInsightsWorkspace.md)


