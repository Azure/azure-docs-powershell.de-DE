---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
ms.openlocfilehash: da4907200bef198afa1d57b51069c6379d28c8f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156012"
---
# Set-AzSynapseNotebook

## SYNOPSIS
Erstellt oder aktualisiert ein Notizbuch in einem Arbeitsbereich.

## SYNTAX

### SetByName (Standard)
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByNameAndSparkPool
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -SparkPoolName <String> [-ExecutorSize <String>]
 -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetByObject
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByObjectAndSparkPool
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -SparkPoolName <String>
 [-ExecutorSize <String>] -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Set-AzSynapseNotebook"** erstellt oder aktualisiert ein Notizbuch in einem Arbeitsbereich.

## BEISPIELE

### Beispiel 1
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb"

    WorkspaceName : ContosoWorkspace
    Properties    : Microsoft.Azure.Commands.Synapse.Models.PSNotebook
    Name          : notebook
```

Mit diesem Befehl wird ein Notizbuch aus der Datei "notebook.ipynb" im Arbeitsbereich "ContosoWorkspace" erstellt oder aktualisiert.

### Beispiel 2
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseNotebook -DefinitionFile "C:\\samples\\notebook.ipynb"
```

Mit diesem Befehl wird ein Notizbuch aus der Datei "notebook.ipynb" im Arbeitsbereich "ContosoWorkspace" über die Pipeline erstellt oder aktualisiert.

### Beispiel 3
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb" -SparkPoolName ContosoSparkPool -ExecutorCount 2
```

Mit diesem Befehl wird ein Notizbuch aus der Datei "notebook.ipynb" erstellt oder aktualisiert, das an "ContosoSparkPool" anfügen und zwei Ausführungsgeber im Arbeitsbereich "ContosoWorkspace" verwendet.

## PARAMETERS

### -AsJob
Ausführen des Cmdlets im Hintergrund

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

### -DefinitionFile
Der JSON-Dateipfad.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExecutorCount
Die Anzahl der Ausführungsgeber, die im angegebenen Sparkpool für den Auftrag zugeordnet werden sollen.

```yaml
Type: System.Int32
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExecutorSize
Die Anzahl des Kerns und des Arbeitsspeichers, der für die Ausführungsgeber verwendet werden soll, die im angegebenen Sparkpool für den Auftrag zugeordnet sind.

```yaml
Type: System.String
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:
Accepted values: Small, Medium, Large

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Der Notizbuchname.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NotebookName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SparkPoolName
Name des Synapse Spark-Pools.

```yaml
Type: System.String
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceName
Name des Synapse-Arbeitsbereichs.

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceObject
Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

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

### -Waswenn
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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace

## AUSGABEN

### Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
