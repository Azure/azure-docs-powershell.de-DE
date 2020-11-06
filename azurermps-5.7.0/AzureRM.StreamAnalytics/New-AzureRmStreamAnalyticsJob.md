---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: F281B351-F7C7-47D1-9745-FFE4BAA840FD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/new-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: b17eb98ec8dc1aa64760a61ee731f67cf7b05139
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498669"
---
# New-AzureRmStreamAnalyticsJob

## Synopsis
Erstellt oder aktualisiert einen Datenstrom Analyse Auftrag.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureRmStreamAnalyticsJob [[-Name] <String>] [-File] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmStreamAnalyticsJob** erstellt einen neuen Datenstrom Analyse Auftrag in Azure oder aktualisiert die Definition eines vorhandenen angegebenen Auftrags.
Der Name des Auftrags kann in der angegeben werden. JSON-Datei oder in der Befehlszeile.
Wenn beide angegeben sind, muss der Name in der Befehlszeile mit dem Namen in der Datei übereinstimmen.

Wenn Sie einen Auftragsnamen angeben, der bereits vorhanden ist, und den Parameter *Force* nicht angeben, fragt das Cmdlet, ob der vorhandene Auftrag ersetzt werden soll.

Wenn Sie den Parameter *Force* angeben und einen vorhandenen Auftragsnamen angeben, wird die Auftragsdefinition ohne Bestätigung ersetzt.

## Beispiele

### Beispiel 1: Erstellen eines Auftrags
```
PS C:\>New-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json"
```

Mit diesem Befehl wird ein Auftrag aus der Definition in JobDefinition.jsauf erstellt.
Wenn ein vorhandener Auftrag mit dem angegebenen Namen in der Auftragsdefinitionsdatei bereits definiert ist, fragt das Cmdlet, ob er ersetzt werden soll.

### Beispiel 2: Ersetzen einer Auftragsdefinition
```
PS C:\>New-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json" -Name "StreamingJob" -Force
```

Dieser Befehl ersetzt die Auftragsdefinition für StreamingJob ohne Bestätigung.

## Parameter

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

### -Datei
Gibt den Pfad zu einer JSON-Datei an, die die JSON-Darstellung des zu erstellende Azure Stream Analytics-Auftrags enthält.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.

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

### -Name
Gibt den Namen des zu erstellende Azure Stream Analytics-Auftrags an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, zu der der Azure-Stream-Analyse Auftrag gehören soll.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Microsoft. Azure. Commands. StreamAnalytics. Models. PSJob

## Notizen

## Verwandte Links

[Get-AzureRmStreamAnalyticsJob](./Get-AzureRmStreamAnalyticsJob.md)

[Remove-AzureRmStreamAnalyticsJob](./Remove-AzureRmStreamAnalyticsJob.md)

[Anfang-AzureRmStreamAnalyticsJob](./Start-AzureRmStreamAnalyticsJob.md)

[Stopp-AzureRmStreamAnalyticsJob](./Stop-AzureRmStreamAnalyticsJob.md)

[Stopp-AzureRmStreamAnalyticsJob](./Stop-AzureRmStreamAnalyticsJob.md)


