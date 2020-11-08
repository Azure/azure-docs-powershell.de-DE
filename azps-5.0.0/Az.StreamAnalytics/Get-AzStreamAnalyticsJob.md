---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
ms.openlocfilehash: 826089ca0db48e89138e9df78f0aa483b110ba30
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176819"
---
# Get-AzStreamAnalyticsJob

## Synopsis
Ruft Informationen zu Datenstrom Analyse Aufträgen ab.

## Syntax

### ByResourceGroup
```
Get-AzStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BySubscription
```
Get-AzStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzStreamAnalyticsJob** " listet alle Datenstrom Analyse Aufträge auf, die im Azure-Abonnement oder der angegebenen Ressourcengruppe definiert sind, oder es werden Auftragsinformationen zu einem bestimmten Auftrag innerhalb einer Ressourcengruppe abgerufen.

## Beispiele

### Beispiel 1: Abrufen von Informationen zu allen Aufträgen in einem Abonnement
```
PS C:\>Get-AzStreamAnalyticsJob
```

Dieser Befehl gibt Informationen zu allen Datenstrom Analyse Aufträgen im Azure-Abonnement zurück.

### Beispiel 2: Abrufen von Informationen zu allen Aufträgen in einer Ressourcengruppe
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

Dieser Befehl gibt Informationen zu allen Datenstrom Analyse Aufträgen in der Ressourcengruppe StreamAnalytics-default-West-US zurück.

### Beispiel 3: Abrufen von Informationen zu einem bestimmten Job in einer Ressourcengruppe
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

Dieser Befehl gibt Informationen zum Datenstrom Analyse-Auftrags StreamingJob in der Ressourcengruppe StreamAnalytics-default-West-US zurück.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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
Gibt den Namen des abzurufenden Azure-Stream-Analyse Auftrags an.

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

### -NOEXPAND
Gibt an, dass das Cmdlet den Azure-Stream-Analyse Auftrag abruft, aber keine Informationen zu den Eingaben, Ausgaben und der Transformation zurückgibt.

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
Gibt den Namen der Ressourcengruppe an, zu der der Azure-Stream-Analyse Auftrag gehört.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

### System. Management. Automation. Switchparameter

## Ausgaben

### Microsoft. Azure. Commands. StreamAnalytics. Models. PSJob

## Notizen

## Verwandte Links

[Neu – AzStreamAnalyticsJob](./New-AzStreamAnalyticsJob.md)

[Remove-AzStreamAnalyticsJob](./Remove-AzStreamAnalyticsJob.md)

[Anfang-AzStreamAnalyticsJob](./Start-AzStreamAnalyticsJob.md)

[Stopp-AzStreamAnalyticsJob](./Stop-AzStreamAnalyticsJob.md)


