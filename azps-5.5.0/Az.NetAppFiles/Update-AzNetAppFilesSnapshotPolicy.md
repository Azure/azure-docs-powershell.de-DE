---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: edb22cc9945ca665b2e24a4488bf3335faac4f50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161257"
---
# Update-AzNetAppFilesSnapshotPolicy

## SYNOPSIS
Aktualisiert eine Azure NetApp Files (ANF)-Momentaufnahmerichtlinie auf die bereitgestellten optionalen Modifizierer.

## SYNTAX

### ByFieldsParameterSet (Standard)
```
Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByParentObjectParameterSet
```
Update-AzNetAppFilesSnapshotPolicy -Name <String> [-Enabled <Boolean>]
 [-HourlySchedule <PSNetAppFilesHourlySchedule>] [-DailySchedule <PSNetAppFilesDailySchedule>]
 [-WeeklySchedule <PSNetAppFilesWeeklySchedule>] [-MonthlySchedule <PSNetAppFilesMonthlySchedule>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByResourceIdParameterSet
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] -ResourceId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObjectParameterSet
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesSnapshotPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Update-AzNetAppFilesSnapshotPolicy"** ändert eine ANF-Momentaufnahmerichtlinie.

## BEISPIELE

### Beispiel 1
```powershell
$hourlySchedule = @{
        Minute = 1
        SnapshotsToKeep = 3
    }
PS C:\> Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy" -HourlySchedule $hourlySchedule
```

Mit diesem Befehl wird die ANF-Sicherungsrichtlinie "MySnapshotPolicy" so geändert, dass die angegebene "HourlySchedule" vorkommt.

## PARAMETERS

### -AccountName
Der Name des ANF-Kontos

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AccountObject
Das Konto für das neue Snapshotrichtlinienobjekt

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DailySchedule
Hashtablearray, das den täglichen Zeitplan darstellt

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesDailySchedule
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

### -Enabled
Die Eigenschaft, die zu entscheiden ist, ob die Richtlinie aktiviert ist oder nicht

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HourlySchedule
Hashtablearray, das den Stundenplan darstellt

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesHourlySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Das zu entfernende Momentaufnahmeobjekt

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Location
Der Speicherort der Ressource

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonthlySchedule
Hashtablearray, das den montly Schedule darstellt

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesMonthlySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Der Name der ANF-Momentaufnahmerichtlinie

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Die Ressourcengruppe des ANF-Kontos

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Die Ressourcen-ID der ANF-Momentaufnahmerichtlinie

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Hashtablearray, das Ressourcentags darstellt

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WeeklySchedule
Hashtablearray, das den montly Schedule darstellt

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesWeeklySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### System.String

### Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount

### Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy

## AUSGABEN

### Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
