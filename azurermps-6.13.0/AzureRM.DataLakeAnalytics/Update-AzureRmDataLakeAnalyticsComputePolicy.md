---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/update-azurermdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 860b58ce3be37eb2ef2277b627971adb301a02af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499594"
---
# Update-AzureRmDataLakeAnalyticsComputePolicy

## Synopsis
Aktualisiert eine Data Lake Analytics-Compute-Richtlinienregel für eine bestimmte Aad-Entität.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Update-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das **Update-AzureRmDataLakeAnalyticsComputePolicy** aktualisiert die angegebene Compute-Richtlinienregel für eine bestimmte Aad-Entität in einem Azure Data Lake Analytics-Konto.

## Beispiele

### Beispiel 1: Aktualisieren einer Regel in einer COMPUTE-Richtlinie
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5
```

Mit diesem Befehl wird eine Richtlinie mit dem Namen "meine Richtlinie" im Konto "contosoadla" aktualisiert, um sicherzustellen, dass der Benutzer keine Aufträge mit mehr als 5 Analyseeinheiten übermitteln kann.

### Beispiel 2: Erstellen einer COMPUTE-Richtlinie mit beiden Regel Updates
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

Mit diesem Befehl wird eine Richtlinie mit dem Namen "meine Richtlinie" im Konto "contosoadla" erstellt, um sicherzustellen, dass der Benutzer keine Aufträge mit mehr als 5 Analyseeinheiten oder mit einer Priorität unter 100 senden kann.

## Parameter

### -Konto
Der Name des Kontos, in dem die Compute-Richtlinie aktualisiert werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -MaxAnalyticsUnitsPerJob
Die maximal unterstützten Analyseeinheiten pro Auftrag für diese Richtlinie. Entweder this, MinPriorityPerJob oder beide Parameter müssen angegeben werden.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelismPerJob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MinPriorityPerJob
Die minimale unterstützte Priorität pro Auftrag für diese Richtlinie. Entweder this, MaxAnalyticsUnitsPerJob oder beide Parameter müssen angegeben werden.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Der Name der zu aktualisierende Compute-Richtlinie.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Name der Ressourcengruppe, unter der Sie das Konto vorhanden sind.
Optional und versucht, festzustellen, wenn Sie nicht bereitgestellt werden.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

### System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

## Ausgaben

### Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy

## Notizen

## Verwandte Links
