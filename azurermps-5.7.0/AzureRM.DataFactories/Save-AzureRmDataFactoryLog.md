---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/save-azurermdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Save-AzureRmDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Save-AzureRmDataFactoryLog.md
ms.openlocfilehash: 696e2de560b67db78f24dea7e8512d85c3640902
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478541"
---
# Save-AzureRmDataFactoryLog

## Synopsis
Downloadet Protokolldateien aus Azure HDInsight processing.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ByFactoryName (Standard)
```
Save-AzureRmDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Save-AzureRmDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Save-AzureRmDataFactoryLog** downloadet Protokolldateien, die der Azure HDInsight-Verarbeitung von Pig-oder Hive-Projekten zugeordnet sind, oder für benutzerdefinierte Aktivitäten auf der lokalen Festplatte.
Sie führen zunächst das Get-AzureRmDataFactoryRun-Cmdlet aus, um eine ID für eine Aktivitätsausführung für einen Datenslice abzurufen, und verwenden Sie dann diese ID, um Protokolldateien aus dem BLOB-Speicher (Binary Large Object) abzurufen, der dem HDInsight-Cluster zugeordnet ist.

Wenn Sie den *DownloadLogs* -Parameter nicht angeben, gibt das Cmdlet nur den Speicherort der Protokolldateien zurück.

Wenn Sie *DownloadLogs* angeben, ohne ein Ausgabeverzeichnis ( *Ausgabe* Parameter) anzugeben, werden die Protokolldateien in den Standardordner "Dokumente" heruntergeladen.

Wenn Sie *DownloadLogs* zusammen mit einem Ausgabeordner ( *Output* ) angeben, werden die Protokolldateien in den angegebenen Ordner heruntergeladen.

## Beispiele

### Beispiel 1: Speichern von Protokolldateien in einem bestimmten Ordner
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

Dieser Befehl speichert Protokolldateien für die Aktivität, die mit der ID von 841b77c9-d56c-48d1-99a3-8c16c3e77d39 ausgeführt wird, wobei die Aktivität zu einer Pipeline in der Data Factory mit dem Namen LogProcessingFactory in der Ressourcengruppe "ADF" gehört.
Die Protokolldateien werden im Ordner C:\test gespeichert.

### Beispiel 2: Speichern von Protokolldateien im Standardordner "Dokumente"
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

Dieser Befehl speichert Protokolldateien in Ordner "Dokumente" (Standard).

### Beispiel 3: Abrufen des Speicherorts von Protokolldateien
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

Dieser Befehl gibt den Speicherort der Protokolldateien zurück.
Beachten Sie, dass *DownloadLogs* nicht angegeben ist.

## Parameter

### -DataFactory
Gibt ein **PSDataFactory** -Objekt an.

```yaml
Type: PSDataFactory
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
Dieses Cmdlet downloadet Protokolldateien für die Data Factory, die dieser Parameter angibt.

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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -DownloadLogs
Gibt an, dass das Cmdlet Protokolldateien auf Ihren lokalen Computer herunterlädt.
Wenn der Ordner *Ouptut* nicht angegeben ist, werden die Dateien im Ordner Dokumente unter einem Unterordner gespeichert.

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

### -ID
Gibt die ID der Aktivitätsausführung für den Datenslice an.
Verwenden Sie das Get-AzureRmDataFactoryRun-Cmdlet, um eine ID abzurufen.

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

### -Output
Gibt den Ausgabeordner an, in dem die heruntergeladenen Protokolldateien gespeichert werden.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Azure-Ressourcengruppe an.
Mit diesem Cmdlet wird eine Data Factory erstellt, die zu der Gruppe gehört, die dieser Parameter angibt.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Microsoft. Azure. Commands. datafactoring. Models. PSRunLogInfo

## Notizen
* Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys

## Verwandte Links

[Get-AzureRmDataFactoryRun](./Get-AzureRmDataFactoryRun.md)

[Get-AzureRmDataFactoryPipeline](./Get-AzureRmDataFactoryPipeline.md)

[Neu – AzureRmDataFactoryPipeline](./New-AzureRmDataFactoryPipeline.md)

[Remove-AzureRmDataFactoryPipeline](./Remove-AzureRmDataFactoryPipeline.md)

[Satz-AzureRmDataFactoryPipelineActivePeriod](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[Suspend-AzureRmDataFactoryPipeline](./Suspend-AzureRmDataFactoryPipeline.md)


