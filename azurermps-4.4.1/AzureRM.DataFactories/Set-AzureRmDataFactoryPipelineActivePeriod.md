---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: D853A91F-95E7-4C36-AC0F-2C10DFCF68F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryPipelineActivePeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryPipelineActivePeriod.md
ms.openlocfilehash: 033b787d444d8a4f97650b93f7621399648b1343
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477185"
---
# Set-AzureRmDataFactoryPipelineActivePeriod

## Synopsis
Konfiguriert den aktiven Zeitraum für Datenslices.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ByFactoryName (Standard)
```
Set-AzureRmDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactoryName] <String>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByFactoryObject
```
Set-AzureRmDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactory] <PSDataFactory>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **festlegen-AzureRmDataFactoryPipelineActivePeriod** " konfiguriert den aktiven Zeitraum für die Datensegmente, die von einer Pipeline in Azure Data Factory verarbeitet werden.
Wenn Sie das Set-AzureRmDataFactorySliceStatus-Cmdlet verwenden, um den Status von Segmenten für ein DataSet zu ändern, stellen Sie sicher, dass sich die Startzeit und die Endzeit für ein Segment im aktiven Zeitraum der Pipeline befinden.

Nachdem Sie eine Pipeline erstellt haben, können Sie den Zeitraum angeben, in dem die Datenverarbeitung erfolgen soll.
Wenn Sie den aktiven Zeitraum für eine Pipeline angeben, wird die Zeitdauer definiert, in der die Datensegmente basierend auf den **Verfügbarkeits** Eigenschaften verarbeitet werden, die für die einzelnen Daten Factory-Datasets definiert wurden.

## Beispiele

### Beispiel 1: Konfigurieren des aktiven Zeitraums
```
PS C:\>Set-AzureRmDataFactoryPipelineActivePeriod -ResourceGroupName "ADF" -PipelineName "DPWikisample" -DataFactoryName "WikiADF" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-22T16:00:00Z
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

### -Enddatum
Gibt das Ende eines Zeitraums als **DateTime** -Objekt an.
Die Datenverarbeitung erfolgt, oder Datenscheiben werden innerhalb dieses Zeitraums verarbeitet.
Wenn Sie weitere Informationen zu **DateTime** -Objekten wünschen, geben Sie `Get-Help Get-Date` .

*Enddatum* muss im ISO8601-Format wie in den folgenden Beispielen angegeben werden: 

2015-01-01z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (Pazifik-Standard Zeit)

Der standardmäßige Zeitzonenbezeichner ist UTC.

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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### System. Boolean

## Notizen
* Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys

## Verwandte Links

[Neu – AzureRmDataFactoryPipeline](./New-AzureRmDataFactoryPipeline.md)

[Satz-AzureRmDataFactorySliceStatus](./Set-AzureRmDataFactorySliceStatus.md)


