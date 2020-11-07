---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D853A91F-95E7-4C36-AC0F-2C10DFCF68F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactorypipelineactiveperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
ms.openlocfilehash: edb2e94900d383675bd183c09df16e295828aae1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820343"
---
# Set-AzDataFactoryPipelineActivePeriod

## Synopsis
Konfiguriert den aktiven Zeitraum für Datenslices.

## Syntax

### ByFactoryName (Standard)
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactoryName] <String>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByFactoryObject
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactory] <PSDataFactory>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **festlegen-AzDataFactoryPipelineActivePeriod** " konfiguriert den aktiven Zeitraum für die Datensegmente, die von einer Pipeline in Azure Data Factory verarbeitet werden.
Wenn Sie das Set-AzDataFactorySliceStatus-Cmdlet verwenden, um den Status von Segmenten für ein DataSet zu ändern, stellen Sie sicher, dass sich die Startzeit und die Endzeit für ein Segment im aktiven Zeitraum der Pipeline befinden.
Nachdem Sie eine Pipeline erstellt haben, können Sie den Zeitraum angeben, in dem die Datenverarbeitung erfolgen soll.
Wenn Sie den aktiven Zeitraum für eine Pipeline angeben, wird die Zeitdauer definiert, in der die Datensegmente basierend auf den **Verfügbarkeits** Eigenschaften verarbeitet werden, die für die einzelnen Daten Factory-Datasets definiert wurden.

## Beispiele

### Beispiel 1: Konfigurieren des aktiven Zeitraums
```
PS C:\>Set-AzDataFactoryPipelineActivePeriod -ResourceGroupName "ADF" -PipelineName "DPWikisample" -DataFactoryName "WikiADF" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-22T16:00:00Z
Confirm
Are you sure you want to set pipeline 'DPWikisample' active period from '05/21/2014 16:00:00' to
'05/22/2014 16:00:00'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

Dieser Befehl konfiguriert den aktiven Zeitraum für die Datensegmente, die von der Pipeline mit dem Namen DPWikisample verarbeitet werden.
Der Befehl bietet Anfangs-und Endpunkte für die Datensegmente als Werte.
Der Befehl gibt den Wert $true zurück.

## Parameter

### – Autoresolve
Gibt an, dass dieses Cmdlet die automatische Aufhebung verwendet.

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

### -DataFactory
Gibt ein **PSDataFactory** -Objekt an.
Dieses Cmdlet ändert den aktiven Zeitraum für eine Pipeline, die zu der Data Factory gehört, die dieser Parameter angibt.

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

### -Datafactoryname
Gibt den Namen einer Data Factory an.
Dieses Cmdlet ändert den aktiven Zeitraum für eine Pipeline, die zu der Data Factory gehört, die dieser Parameter angibt.

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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -Enddatum
Gibt das Ende eines Zeitraums als **DateTime** -Objekt an.
Die Datenverarbeitung erfolgt, oder Datenscheiben werden innerhalb dieses Zeitraums verarbeitet.
Wenn Sie weitere Informationen zu **DateTime** -Objekten wünschen, geben Sie `Get-Help Get-Date` .
*Enddatum* muss im ISO8601-Format angegeben werden, wie in den folgenden Beispielen: 2015-01-01z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (Pazifik-Standardzeit) der standardmäßige Zeitzonenbezeichner ist UTC.

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

### -ForceRecalculate
Gibt an, dass dieses Cmdlet Force-Neuberechnung verwendet.

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

### -Pipelinename
Gibt den Namen der Pipeline an.
Mit diesem Cmdlet wird der aktive Zeitraum für die Pipeline festgelegt, den dieser Parameter angibt.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Azure-Ressourcengruppe an.
Dieses Cmdlet ändert den aktiven Zeitraum für eine Pipeline, die zu der Gruppe gehört, die dieser Parameter angibt.

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

### -Startdatum
Gibt den Anfang eines Zeitraums als **DateTime** -Objekt an.
Die Datenverarbeitung erfolgt, oder Datenscheiben werden innerhalb dieses Zeitraums verarbeitet.
Start *Datum* muss im ISO8601-Format angegeben werden.

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

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
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

### System. String

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

## Ausgaben

### System. Boolean

## Notizen
* Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys

## Verwandte Links

[Neu – AzDataFactoryPipeline](./New-AzDataFactoryPipeline.md)

[Satz-AzDataFactorySliceStatus](./Set-AzDataFactorySliceStatus.md)


