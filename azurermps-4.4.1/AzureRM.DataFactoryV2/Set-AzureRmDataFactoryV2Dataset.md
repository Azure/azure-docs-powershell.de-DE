---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Dataset.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 311073fcd840e9d163c1316019e48569f7e59c81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665395"
---
# Set-AzureRmDataFactoryV2Dataset

## Synopsis
Erstellt ein Dataset in Data Factory.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ByFactoryName (Standard)
```
Set-AzureRmDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-WhatIf] [-Confirm]
```

### ByResourceId
```
Set-AzureRmDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## Beschreibung
Das Set-AzureRmDataFactoryV2Dataset-Cmdlet erstellt ein Dataset in Azure Data Factory.
Wenn Sie einen Namen für ein DataSet angeben, das bereits vorhanden ist, werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor das DataSet ersetzt wird.
Wenn Sie den Parameter Force angeben, wird das vorhandene DataSet ohne Bestätigung durch das Cmdlet ersetzt.

Führen Sie diese Vorgänge in der folgenden Reihenfolge aus:

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

Wenn bereits ein DataSet mit dem gleichen Namen in der Data Factory vorhanden ist, werden Sie von diesem Cmdlet aufgefordert, zu bestätigen, ob das vorhandene DataSet mit dem neuen DataSet überschrieben werden soll.
Wenn Sie bestätigen, dass das vorhandene DataSet überschrieben werden soll, wird auch die DataSet-Definition ersetzt.

## Beispiele

### Beispiel 1: Erstellen eines Datasets
```
PS C:\> Set-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

```

Dieser Befehl erstellt ein DataSet mit dem Namen DA_WikipediaClickEvents in der Data Factory mit dem Namen WikiADF.
Der Befehl unterstützt das Dataset auf Informationen in der DAWikipediaClickEvents.jsfür die Datei.

## Parameter

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Datafactoryname
Gibt den Namen einer Data Factory an.
Dieses Cmdlet erstellt ein Dataset in der Data Factory, das dieser Parameter angibt.

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Definitions-Nr.
Der JSON-Dateipfad.

```yaml
Type: String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.

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
Gibt den Namen des zu erstellenden Datasets an.

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Azure-Ressourcengruppe an.
Mit diesem Cmdlet wird ein Dataset in der Gruppe erstellt, das dieser Parameter angibt.

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Resourcen-Nr
Die Azure-Ressourcen-ID.

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## Eingaben

### System. String


## Ausgaben

### Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset


## Notizen
Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys

## Verwandte Links
[Get-AzureRmDataFactoryV2Dataset]()

[Remove-AzureRmDataFactoryV2Dataset]()
