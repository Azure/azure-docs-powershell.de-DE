---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/invoke-azurermoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Invoke-AzureRmOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Invoke-AzureRmOperationalInsightsQuery.md
ms.openlocfilehash: e3bfdd771413f17d4dd560a350d45fdb3f47c5a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479646"
---
# Invoke-AzureRmOperationalInsightsQuery

## Synopsis
Gibt Suchergebnisse basierend auf den angegebenen Parametern zurück.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ByWorkspaceId (Standard)
```
Invoke-AzureRmOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByWorkspaceObject
```
Invoke-AzureRmOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Invoke-AzureRmOperationalInsightsQuery** gibt die Suchergebnisse auf der Grundlage der angegebenen Parameter zurück.

Sie können auf den Status der Suche in der Metadata-Eigenschaft des zurückgegebenen Objekts zugreifen.
Wenn der Status Ausstehend ist, wurde die Suche nicht abgeschlossen, und die Ergebnisse werden aus dem Archiv angezeigt.

Sie können die Suchergebnisse aus der Value-Eigenschaft des zurückgegebenen Objekts abrufen.

## Beispiele

### Beispiel 1: Abrufen von Suchergebnissen mithilfe einer Abfrage
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

Sobald aufgerufen, enthält $queryResults. results alle resultierenden Zeilen aus der Abfrage.

### Beispiel 2: Konvertieren von $results. Ergebnis-IEnumberable zu einem Array
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($results.Results)
...
```

Einige Abfragen können dazu führen, dass sehr große Datensätze zurückgegeben werden. Aus diesem Grund ist das Standardverhalten des Cmdlets, ein IEnumerable zurückzugeben, um die Speicherkosten zu reduzieren. Wenn Sie ein Array von Ergebnissen bevorzugen, können Sie die IEnumerable-Methode Enumerable. ToArray () verwenden, um die IEnumerable in ein Array zu konvertieren.

### Beispiel 3: Abrufen von Suchergebnissen mithilfe einer Abfrage über einen bestimmten Zeitraum
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

Die Ergebnisse dieser Abfrage sind auf die letzten 24 Stunden limitiert.

### Beispiel 4: Rendern & Statistiken in Abfrageergebnis einbeziehen
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

[https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions)Details zu den Render-und Statistikinformationen finden Sie unter.

## Parameter

### -AsJob
Ausführen eines Cmdlets im Hintergrund
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeRender
Wenn angegeben, werden Renderinginformationen für metrische Abfragen in die Antwort aufgenommen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeStatistics
Wenn angegeben, werden Abfragestatistiken in der Antwort berücksichtigt.

```yaml
Type: SwitchParameter
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
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TimeSpan
Die TimeSpan, an die die Abfrage gebunden werden soll.

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Wait
Legt eine Obergrenze für die Zeitspanne an, die der Server für die Verarbeitung der Abfrage aufwendet.
Sieh: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Arbeitsbereich
Der Arbeitsbereich

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Arbeitsbereichs-Nr
Die Arbeitsbereichs-ID.

```yaml
Type: String
Parameter Sets: ByWorkspaceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace
Wenn die Arbeitsbereichs-ID weitergeleitet wird, wird Sie aus dem PSWorkspace extrahiert. Andernfalls können Sie den Workspace-Parameter verwenden, um die Arbeitsbereichs-ID manuell anzugeben.

## Ausgaben

### Microsoft. Azure. Commands. OperationalInsights. Models. PSQueryResponse
Die ***PSQueryResponse*** enthält die Ergebnisse, Render & Statistiken der Abfrage.

## Notizen

## Verwandte Links

