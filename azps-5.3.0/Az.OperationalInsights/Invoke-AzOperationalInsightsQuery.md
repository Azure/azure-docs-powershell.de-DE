---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/invoke-azoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
ms.openlocfilehash: 0b2b27855e0c8248f0e7ceb9f1c096370a54e2fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473309"
---
# Invoke-AzOperationalInsightsQuery

## SYNOPSIS
Gibt Suchergebnisse basierend auf den angegebenen Parametern zurück.

## SYNTAX

### ByWorkspaceId (Standard)
```
Invoke-AzOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>] [-Wait <Int32>]
 [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByWorkspaceObject
```
Invoke-AzOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Invoke-AzOperationalInsightsQuery** gibt die Suchergebnisse basierend auf den angegebenen Parametern zurück.
Sie können auf den Status der Suche in der Metadateneigenschaft des zurückgegebenen Objekts zugreifen.
Wenn der Status "Ausstehend" ist, wurde die Suche nicht abgeschlossen, und die Ergebnisse werden aus dem Archiv entfernt.
Sie können die Ergebnisse der Suche aus der Eigenschaft "Value" des zurückgegebenen Objekts abrufen.
Sehen Sie sich die allgemeinen Abfragegrenzwerte hier genauer https://docs.microsoft.com/en-us/azure/azure-monitor/service-limits#log-queries-and-language an:

## BEISPIELE

### Beispiel 1: Erhalten von Suchergebnissen mithilfe einer Abfrage
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

Nach dem Aufruf enthält $queryResults.Results alle resultierenden Zeilen aus Ihrer Abfrage.

### Beispiel 2: Konvertieren $results. Ergebnis iEnumerable für eine Matrix
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($queryResults.Results)
...
```

Einige Abfragen können dazu führen, dass sehr große Datensätze zurückgegeben werden. Daher besteht das Standardverhalten des Cmdlets in der Rückgabe eines IEnumerable-Speichers, um die Speicherkosten zu verringern. Wenn Sie ein Array mit Ergebnissen bevorzugen, können Sie die LINQ Enumerable.ToArray()-Erweiterungsmethode verwenden, um IEnumerable in ein Array zu konvertieren.

### Beispiel 3: Erhalten von Suchergebnissen mithilfe einer Abfrage über einen bestimmten Zeitraum
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

Die Ergebnisse dieser Abfrage sind auf die letzten 24 Stunden beschränkt.

### Beispiel 4: Hinzufügen von Render- & in Abfrageergebnisse
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

Weitere [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) Informationen zum Rendern und zur Statistik finden Sie im Detail.

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

### -IncludeRender
Falls angegeben, werden Renderinformationen für metrische Abfragen in die Antwort einbezogen.

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

### -IncludeStatistics
Falls angegeben, werden Abfragestatistiken in die Antwort einbezogen.

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

### -Query
Die auszuführende Abfrage.

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

### -Timespan
Die Zeitspanne, über die die Abfrage gebunden wurde.

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Wait
Legt eine obere Grenze für die Zeit ein, die der Server für die Verarbeitung der Abfrage aufbringt.
Sieh: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts

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

### -Workspace
Der Arbeitsbereich

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WorkspaceId
Die Arbeitsbereichs-ID.

```yaml
Type: System.String
Parameter Sets: ByWorkspaceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace

## AUSGABEN

### Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
