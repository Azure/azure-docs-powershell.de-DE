---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 43B2A4FD-DA74-403A-89D0-40FE9A3E5A7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/new-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 7b18513a6a9e7ebbf82892500344d13f9cbc8185
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498665"
---
# New-AzureRmStreamAnalyticsOutput

## Synopsis
Erstellt oder aktualisiert Ausgaben für einen Datenstrom Analyse Auftrag.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureRmStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmStreamAnalyticsOutput** erstellt eine Ausgabe innerhalb eines Datenstrom Analyse Auftrags oder aktualisiert eine vorhandene Ausgabe.
Der Name der Ausgabe kann in der angegeben werden. JSON-Datei oder in der Befehlszeile.
Wenn beide angegeben sind, muss der Name in der Befehlszeile mit dem Namen in der Datei übereinstimmen.

Wenn Sie eine Ausgabe angeben, die bereits vorhanden ist, und den Parameter *Force* nicht angeben, fragt das Cmdlet, ob die vorhandene Ausgabe ersetzt werden soll.

Wenn Sie den Parameter *Force* angeben und einen vorhandenen Ausgabe Namen angeben, wird die Ausgabe ohne Bestätigung ersetzt.

## Beispiele

### Beispiel 1: Hinzufügen einer Ausgabe zu einem Auftrag
```
PS C:\>New-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output"
```

Dieser Befehl erstellt eine neue Ausgabe namens Output im Auftrag namens StreamingJob.
Wenn eine vorhandene Ausgabe mit diesem Namen bereits definiert ist, fragt das Cmdlet, ob Sie ersetzt werden soll.

### Beispiel 2: Ersetzen einer Auftragsausgabe Definition
```
PS C:\>New-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output" -Force
```

Dieser Befehl ersetzt die Definition für die Ausgabe im Job namens StreamingJob ohne Bestätigung.

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
Gibt den Pfad zu einer JSON-Datei an, die die JSON-Darstellung der zu erstellende Azure-Stream-Analyseausgabe enthält.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
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

### -Jobname
Gibt den Namen des Azure Stream Analytics-Auftrags an, unter dem die Azure Stream Analytics-Ausgabe erstellt werden soll.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen der zu erstellende Azure-Datenstrom Analyseausgabe an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, unter der die Azure Stream Analytics-Ausgabe erstellt werden soll.

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

### Microsoft. Azure. Commands. StreamAnalytics. Models. PSOutput

## Notizen

## Verwandte Links

[Get-AzureRmStreamAnalyticsOutput](./Get-AzureRmStreamAnalyticsOutput.md)

[Remove-AzureRmStreamAnalyticsOutput](./Remove-AzureRmStreamAnalyticsOutput.md)

[Test-AzureRmStreamAnalyticsOutput](./Test-AzureRmStreamAnalyticsOutput.md)


