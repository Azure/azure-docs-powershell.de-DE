---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/save-azdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
ms.openlocfilehash: cf1e0738a01d2b8f3219f2732995182fe7f6959d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144388"
---
# Save-AzDataFactoryLog

## SYNOPSIS
Lädt Protokolldateien aus Azure HDInsight Processing herunter.

## SYNTAX

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

## BESCHREIBUNG
Das **Cmdlet "Save-AzDataFactoryLog"** lädt Protokolldateien herunter, die mit der Azure -HDInsight-Verarbeitung von Schwein- oder Strukturprojekten oder für benutzerdefinierte Aktivitäten auf Ihrer lokalen Festplatte verknüpft sind.
Zuerst führen Sie das Cmdlet Get-AzDataFactoryRun aus, um eine ID für eine Aktivität abzurufen, die für ein Datendatenschnitt ausgeführt wird, und verwenden sie dann zum Abrufen von Protokolldateien aus dem BLOB (Binary Large Object)-Speicher, der dem Cluster "HDInsight" zugeordnet ist.
Wenn Sie den Parameter *"DownloadLogs"* nicht angeben, gibt das Cmdlet einfach den Speicherort der Protokolldateien zurück.
Wenn Sie *"DownloadLogs"* angeben, ohne ein Ausgabeverzeichnis *(Ausgabeparameter)* anzugeben, werden die Protokolldateien in den Standardordner "Dokumente" heruntergeladen.
Wenn Sie *DownloadLogs* zusammen mit einem Ausgabeordner *(Ausgabe)* angeben, werden die Protokolldateien in den angegebenen Ordner heruntergeladen.

## BEISPIELE

### Beispiel 1: Speichern von Protokolldateien in einem bestimmten Ordner
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

Dieser Befehl speichert Protokolldateien für die Aktivität, die mit der ID 841b77c9-d56c-48d1-99a3-8c16c3e77d39 ausgeführt wird, wobei die Aktivität zu einer Pipeline in der Datenfactory mit dem Namen "LogProcessingFactory" in der Ressourcengruppe mit dem Namen ADF gehört.
Die Protokolldateien werden im Ordner "C:\Test" gespeichert.

### Beispiel 2: Speichern von Protokolldateien im Standardordner "Dokumente"
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

Dieser Befehl speichert Protokolldateien im Ordner "Dokumente" (Standard).

### Beispiel 3: Herunterladen des Speicherorts von Protokolldateien
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

Dieser Befehl gibt den Speicherort der Protokolldateien zurück.
Beachten Sie, *dass "DownloadLogs"* nicht angegeben ist.

## PARAMETERS

### -DataFactory
Gibt ein **"PSDataFactory"-Objekt** an.

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
Dieses Cmdlet lädt Protokolldateien für die Daten factory herunter, die dieser Parameter angibt.

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

### -DownloadLogs
Gibt an, dass dieses Cmdlet Protokolldateien auf Ihren lokalen Computer herunterlädt.
Wenn *der* Ordner "Ausgabe" nicht angegeben ist, werden Dateien im Ordner "Dokumente" unter einem Unterordner gespeichert.

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
Gibt die ID der Aktivität an, die für das Datenschnitt ausgeführt wird.
Verwenden Sie das Get-AzDataFactoryRun Cmdlet, um eine ID zu erhalten.

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
Dieses Cmdlet erstellt eine Daten factory, die zu der Gruppe gehört, die dieser Parameter angibt.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo

## HINWEISE
* Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys

## LINKS ZU VERWANDTEN THEMEN

[Get-AzDataFactoryRun](./Get-AzDataFactoryRun.md)

[Get-AzDataFactoryPipeline](./Get-AzDataFactoryPipeline.md)

[New-AzDataFactoryPipeline](./New-AzDataFactoryPipeline.md)

[Remove-AzDataFactoryPipeline](./Remove-AzDataFactoryPipeline.md)

[Set-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)

[Suspend-AzDataFactoryPipeline](./Suspend-AzDataFactoryPipeline.md)


