---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
ms.openlocfilehash: 826089ca0db48e89138e9df78f0aa483b110ba30
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471679"
---
# Get-AzStreamAnalyticsJob

## SYNOPSIS
Ruft Daten zu Stream Analytics-Aufträgen ab.

## SYNTAX

### ByResourceGroup
```
Get-AzStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BySubscription
```
Get-AzStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzStreamAnalyticsJob"** listet alle Stream Analytics-Aufträge auf, die im Abonnement von Azure oder einer bestimmten Ressourcengruppe definiert wurden, oder ruft Auftragsinformationen zu einem bestimmten Auftrag innerhalb einer Ressourcengruppe ab.

## BEISPIELE

### BEISPIEL 1: Informationen zu allen Aufträgen in einem Abonnement
```
PS C:\>Get-AzStreamAnalyticsJob
```

Dieser Befehl gibt Informationen zu allen Stream Analytics-Aufträgen im Abonnement von Azure zurück.

### BEISPIEL 2: Erhalten von Informationen zu allen Aufträgen in einer Ressourcengruppe
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

Dieser Befehl gibt Informationen zu allen Stream Analytics-Aufträgen in der Ressourcengruppe "StreamAnalytics-Default-West-US" zurück.

### BEISPIEL 3: Erhalten von Informationen zu einem bestimmten Auftrag in einer Ressourcengruppe
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

Dieser Befehl gibt Informationen über den Stream Analytics-Auftrag "StreamingJob" in der Ressourcengruppe "StreamAnalytics-Default-West-US" zurück.

## PARAMETERS

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

### -Name
Gibt den Namen des abzurufenden Azure Stream Analytics-Auftrags an.

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NoExpand
Gibt an, dass das Cmdlet den Azure Stream Analytics-Auftrag abruft, aber keine Informationen zu seinen Eingaben, Ausgaben und Transformationen zurückgibt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, zu der der Azure Stream Analytics-Auftrag gehört.

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

### System.Management.Automation.SwitchParameter

## AUSGABEN

### Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[New-AzStreamAnalyticsJob](./New-AzStreamAnalyticsJob.md)

[Remove-AzStreamAnalyticsJob](./Remove-AzStreamAnalyticsJob.md)

[Start-AzStreamAnalyticsJob](./Start-AzStreamAnalyticsJob.md)

[Stop-AzStreamAnalyticsJob](./Stop-AzStreamAnalyticsJob.md)


