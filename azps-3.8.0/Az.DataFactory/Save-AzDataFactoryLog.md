---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/save-azdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
ms.openlocfilehash: cf1e0738a01d2b8f3219f2732995182fe7f6959d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847156"
---
# Save-AzDataFactoryLog

## Synopsis
Downloadet Protokolldateien aus Azure HDInsight processing.

## Syntax

### ByFactoryName (Standard)
```
Save-AzDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Save-AzDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Save-AzDataFactoryLog** downloadet Protokolldateien, die der Azure HDInsight-Verarbeitung von Pig-oder Hive-Projekten zugeordnet sind, oder für benutzerdefinierte Aktivitäten auf der lokalen Festplatte.
Sie führen zunächst das Get-AzDataFactoryRun-Cmdlet aus, um eine ID für eine Aktivitätsausführung für einen Datenslice abzurufen, und verwenden Sie dann diese ID, um Protokolldateien aus dem BLOB-Speicher (Binary Large Object) abzurufen, der dem HDInsight-Cluster zugeordnet ist.
Wenn Sie den *DownloadLogs* -Parameter nicht angeben, gibt das Cmdlet nur den Speicherort der Protokolldateien zurück.
Wenn Sie *DownloadLogs* angeben, ohne ein Ausgabeverzeichnis ( *Ausgabe* Parameter) anzugeben, werden die Protokolldateien in den Standardordner "Dokumente" heruntergeladen.
Wenn Sie *DownloadLogs* zusammen mit einem Ausgabeordner ( *Output* ) angeben, werden die Protokolldateien in den angegebenen Ordner heruntergeladen.

## Beispiele

### Beispiel 1: Speichern von Protokolldateien in einem bestimmten Ordner
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

Dieser Befehl speichert Protokolldateien für die Aktivität, die mit der ID von 841b77c9-d56c-48d1-99a3-8c16c3e77d39 ausgeführt wird, wobei die Aktivität zu einer Pipeline in der Data Factory mit dem Namen LogProcessingFactory in der Ressourcengruppe "ADF" gehört.
Die Protokolldateien werden im Ordner C:\test gespeichert.

### Beispiel 2: Speichern von Protokolldateien im Standardordner "Dokumente"
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

Dieser Befehl speichert Protokolldateien in Ordner "Dokumente" (Standard).

### Beispiel 3: Abrufen des Speicherorts von Protokolldateien
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

Dieser Befehl gibt den Speicherort der Protokolldateien zurück.
Beachten Sie, dass *DownloadLogs* nicht angegeben ist.

## Parameter

### -DataFactory
Gibt ein **PSDataFactory** -Objekt an.

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
Dieses Cmdlet downloadet Protokolldateien für die Data Factory, die dieser Parameter angibt.

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

### -DownloadLogs
Gibt an, dass das Cmdlet Protokolldateien auf Ihren lokalen Computer herunterlädt.
Wenn der *Ausgabe* Ordner nicht angegeben ist, werden die Dateien im Ordner Dokumente unter einem Unterordner gespeichert.

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

### -ID
Gibt die ID der Aktivitätsausführung für den Datenslice an.
Verwenden Sie das Get-AzDataFactoryRun-Cmdlet, um eine ID abzurufen.

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

### -Output
Gibt den Ausgabeordner an, in dem die heruntergeladenen Protokolldateien gespeichert werden.

```yaml
Type: System.String
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
Type: System.String
Parameter Sets: ByFactoryName
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

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System. String

## Ausgaben

### Microsoft. Azure. Commands. datafactoring. Models. PSRunLogInfo

## Notizen
* Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys

## Verwandte Links

[Get-AzDataFactoryRun](./Get-AzDataFactoryRun.md)

[Get-AzDataFactoryPipeline](./Get-AzDataFactoryPipeline.md)

[Neu – AzDataFactoryPipeline](./New-AzDataFactoryPipeline.md)

[Remove-AzDataFactoryPipeline](./Remove-AzDataFactoryPipeline.md)

[Satz-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)

[Suspend-AzDataFactoryPipeline](./Suspend-AzDataFactoryPipeline.md)


