---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsdefaultfunctiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: 1854c2e060dbbc83ba196043debb0ba08c9a933e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178187"
---
# Get-AzStreamAnalyticsDefaultFunctionDefinition

## Synopsis
Ruft die Standard Definition einer Funktion in der Datenstrom Analyse ab.

## Syntax

```
Get-AzStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzStreamAnalyticsDefaultFunctionDefinition** " Ruft die Standard Definition einer Funktion in Azure Stream Analytics ab.
Sie können die Standard Definition und das New-AzStreamAnalyticsFunction-Cmdlet verwenden, um eine Funktion zu erstellen.
Sie können die Standard Definition ändern, bevor Sie eine Funktion erstellen.

## Beispiele

### Beispiel 1: Abrufen der Standard Definition einer Datenstrom Analysefunktion
```
PS C:\>Get-AzStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

Dieser Befehl ruft die Standard Definition der Funktion mit dem Namen ScoreTweet mithilfe der Parameter ab, die in der Datei RetrieveDefaultDefinitionRequest.jsangegeben sind.

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

### -Datei
Gibt den Pfad einer JSON-Datei an, die die JSON-Darstellung (JavaScript Object Notation) des Anforderungstexts für die Abruffunktion der Standard Funktions Definitions Anforderung enthält.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Jobname
Gibt den Namen des Datenstrom Analyse Auftrags an, zu dem Funktionen gehören.
Dieses Cmdlet ruft die Standard Definition für eine Funktion in dem Auftrag ab, die dieser Parameter angibt.

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
Gibt den Namen der Datenstrom Analysefunktion an, für die dieses Cmdlet die Standard Definition abruft.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, zu der Datenstrom Analysefunktionen gehören.
Dieses Cmdlet ruft eine Funktionsdefinition für die Gruppe ab, die dieser Parameter angibt.

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


