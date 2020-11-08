---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
ms.openlocfilehash: ceedee89473385202037cfedb23e4373995b6f98
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010358"
---
# Get-AzStreamAnalyticsFunction

## Synopsis
Ruft Funktionen in einem Datenstrom Analyse Auftrag ab.

## Syntax

```
Get-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzStreamAnalyticsFunction** " Ruft eine Liste der Funktionen ab, die in einem Azure Stream-Analyse Auftrag oder Informationen zu einer bestimmten Funktion definiert sind.

## Beispiele

### Beispiel 1: Abrufen aller Datenstrom Analysefunktionen
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

Dieser Befehl ruft die Funktionen ab, die für den Auftrag mit dem Namen StreamJob22 definiert sind.

### Beispiel 2: Abrufen einer bestimmten Datenstrom Analysefunktion
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

Dieser Befehl ruft Informationen zur Funktion ScoreTweet ab, die für den Auftrag mit dem Namen StreamJob22 definiert ist.

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

### -Jobname
Gibt den Namen des Datenstrom Analyse Auftrags an, zu dem Funktionen gehören.
Dieses Cmdlet ruft Funktionen für den Auftrag ab, die dieser Parameter angibt.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen der Datenstrom Analysefunktion an, die dieses Cmdlet erhält.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, zu der Datenstrom Analysefunktionen gehören.
Dieses Cmdlet ruft Funktionen für die Gruppe ab, die dieser Parameter angibt.

```yaml
Type: System.String
Parameter Sets: (All)
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

## Ausgaben

### Microsoft. Azure. Commands. StreamAnalytics. Models. PSFunction

## Notizen

## Verwandte Links

[Neu – AzStreamAnalyticsFunction](./New-AzStreamAnalyticsFunction.md)

[Remove-AzStreamAnalyticsFunction](./Remove-AzStreamAnalyticsFunction.md)

[Test-AzStreamAnalyticsFunction](./Test-AzStreamAnalyticsFunction.md)


