---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
ms.openlocfilehash: 8b2c55a069463120b861f1ea928ac0163a4c37df
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470540"
---
# Set-AzDataFactorySliceStatus

## SYNOPSIS
Legt den Status von Segmenten für ein Dataset in Azure Data Factory fest.

## SYNTAX

### ByFactoryName (Standard)
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Set-AzDataFactoryS status"** legt den Status von Segmenten für ein Dataset in Azure Data Factory fest.

## BEISPIELE

### Beispiel 1: Festlegen des Status aller Segmente
```
PS C:\>Set-AzDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

Mit diesem Befehl wird der Status aller Segmente für das Dataset mit dem Namen "DAWikiAggregatedData" auf "Waiting" in der Daten factory namens "WikiADF" definiert.
Der *Parameter "UpdateType"* hat den Wert "UpstreamInPipeline", und daher legt der Befehl den Status jedes Datenschnitts für das Dataset und alle abhängigen Datasets fest.
Abhängige Datasets werden als Eingabedatensets für Aktivitäten in der Pipeline verwendet.
Dieser Befehl gibt den Wert "$True" $True.

## PARAMETERS

### -DataFactory
Gibt ein **"PSDataFactory"-Objekt** an.
Dieses Cmdlet ändert den Status von Segmenten, die zu der von diesem Parameter angegebenen Daten factory gehören.

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Gibt den Namen einer Daten factory an.
Dieses Cmdlet ändert den Status von Segmenten, die zu der von diesem Parameter angegebenen Daten factory gehören.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DatasetName
Gibt den Namen des Datasets an, für das dieses Cmdlet Segmente ändert.

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

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden

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

### -EndDateTime
Gibt das Ende eines Zeitraums als **"DateTime"-Objekt** an.
Dieses Mal ist das Ende eines Datenschnitts.
Weitere Informationen zu **"DateTime"-Objekten** erhalten Sie, wenn Sie `Get-Help Get-Date` ".
*EndDateTime* muss im ISO8601-Format angegeben werden, wie in den folgenden Beispielen: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) Der Standard-Zeitzonen-Designator ist UTC.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Azure-Ressourcengruppe an.
Dieses Cmdlet ändert den Status von Segmenten, die zu der Gruppe gehören, die dieser Parameter angibt.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartDateTime
Gibt den Anfang eines Zeitraums als **"DateTime"-Objekt** an.
Dieses Mal ist der Anfang eines Datenschnitts.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status
Gibt einen Status an, der dem Datenschnitt zugewiesen werden soll.
Die zulässigen Werte für diesen Parameter sind:
- Warten
Das Datendatenschnitt wartet auf die Überprüfung der Überprüfungsrichtlinien, bevor sie verarbeitet wird. 
- "Bereit".
Die Datenverarbeitung wurde abgeschlossen, und das Datenschnitt ist bereit.
- InProgress.
Die Datenverarbeitung wird ausgeführt. 
- Fehler.
Fehler bei der Datenverarbeitung.
- Übersprungen.
Verarbeitung des Datenschnitts übersprungen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Failed, InProgress, Ready, Skipped, Waiting

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateType
Gibt den Aktualisierungstyp für das Segment an.
Die zulässigen Werte für diesen Parameter sind:
- Einzelperson.
Legt den Status der einzelnen Segmente für das Dataset im angegebenen Zeitraum fest. 
- UpstreamInPipeline.
Legt den Status der einzelnen Segmente für das Dataset und alle abhängigen Datasets fest, die als Eingabedatensets für Aktivitäten in der Pipeline verwendet werden.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Individual, UpstreamInPipeline

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## AUSGABEN

### System.Boolean

## HINWEISE
* Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys

## LINKS ZU VERWANDTEN THEMEN

[Get-AzDataFactorySfactory](./Get-AzDataFactorySlice.md)


