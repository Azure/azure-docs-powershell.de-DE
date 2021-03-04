---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/invoke-azoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
ms.openlocfilehash: bdba6d4da6df49d1975e2cfd1cc6e47f6ce6d776
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947760"
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
Sie können in der Metadateneigenschaft des zurückgegebenen Objekts auf den Status der Suche zugreifen.
Wenn der Status ausstehend ist, wurde die Suche noch nicht abgeschlossen, und die Ergebnisse werden aus dem Archiv angezeigt.
Sie können die Ergebnisse der Suche aus der Wert-Eigenschaft des zurückgegebenen Objekts abrufen.
Bitte überprüfen Sie die Details der allgemeinen Abfragebeschränkungen hier: https://docs.microsoft.com/azure/azure-monitor/service-limits#log-queries-and-language .

## BEISPIELE

### Beispiel 1: Erhalten von Suchergebnissen mithilfe einer Abfrage
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

Nach dem Aufrufen $queryResults.Results alle resultierenden Zeilen aus ihrer Abfrage.

### Beispiel 2: Konvertieren $results. Ergebnis IEnumerable für ein Array
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($queryResults.Results)
...
```

Einige Abfragen können dazu führen, dass sehr große Datensätze zurückgegeben werden. Aus diesem Grund besteht das Standardverhalten des Cmdlets in der Rückgabe eines IEnumerables, um die Speicherkosten zu verringern. Wenn Sie ein Array mit Ergebnissen bevorzugen, können Sie die LINQ Enumerable.ToArray()-Erweiterungsmethode verwenden, um das IEnumerable in ein Array zu konvertieren.

### Beispiel 3: Erhalten von Suchergebnissen mithilfe einer Abfrage über einen bestimmten Zeitrahmen
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

Die Ergebnisse dieser Abfrage sind auf die letzten 24 Stunden beschränkt.

### Beispiel 4: Hinzufügen von Render- & Statistiken in das Abfrageergebnis
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

Weitere [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) Informationen zu Render- und Statistikinformationen finden Sie unter.

## PARAMETER

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

### -IncludeRender
Wenn angegeben, werden Renderinformationen für Metrikabfragen in die Antwort einbezogen.

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
Wenn angegeben, werden Abfragestatistiken in die Antwort einbezogen.

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

### -Zeitspanne
Die Zeitspanne, an die die Abfrage gebunden werden soll.

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
Legt eine Obergrenze für die Zeit ein, die der Server für die Verarbeitung der Abfrage auf sich nimmt.
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

### -Arbeitsbereich
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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace

## AUSGABEN

### Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse

## NOTIZEN

## VERWANDTE LINKS
