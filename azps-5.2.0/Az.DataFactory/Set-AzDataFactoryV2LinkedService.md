---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: d6fd12e96a98d0771a984aa5234013dbe4a548af
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357704"
---
# Set-AzDataFactoryV2LinkedService

## SYNOPSIS
Verknüpft einen Datenspeicher oder einen Clouddienst mit Data Factory.

## SYNTAX

### ByFactoryName (Standard)
```
Set-AzDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByResourceId
```
Set-AzDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das Set-AzDataFactoryV2LinkedService verknüpft einen Datenspeicher oder einen Clouddienst mit Azure Data Factory.
Wenn Sie einen Namen für einen verknüpften Dienst angeben, der bereits vorhanden ist, werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor der verknüpfte Dienst ersetzt wird.
Wenn Sie den Parameter "Erzwingen" angeben, ersetzt das Cmdlet den vorhandenen verknüpften Dienst ohne Bestätigung.
Führen Sie diese Vorgänge in der folgenden Reihenfolge aus: -- Erstellen Sie eine Daten factory.
- Verknüpfte Dienste erstellen.
– Erstellen sie Datasets.
– Erstellen Sie eine Pipeline.

## BEISPIELE

### Beispiel 1: Erstellen eines verknüpften Diensts
```
PS C:\> Set-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

Mit diesem Befehl wird ein verknüpfter Dienst mit dem Namen "LinkedServiceCuratedWikiData" in der Daten factory namens "WikiADF" erstellt.
Dieser verknüpfte Dienst verknüpft einen Azure-BLOB-Speicher, der in der Datei angegeben ist, mit der Daten factory namens WikiADF.
Der Befehl übergibt das Ergebnis mithilfe des Pipelineoperators Format-List an das Format-List Cmdlet.
Auf Windows PowerShell cmdlet werden die Ergebnisse formatiert.
Weitere Informationen erhalten Sie, wenn Sie Get-Help "Format-Liste" eingeben.

## PARAMETERS

### -DataFactoryName
Gibt den Namen einer Daten factory an.
Dieses Cmdlet erstellt einen verknüpften Dienst für die Daten factory, den dieser Parameter angibt.

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
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -DefinitionFile
Der JSON-Dateipfad.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Führt das Cmdlet ohne Bestätigungsaufforderung aus.

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

### -Name
Gibt den Namen des verknüpften Diensts an, der erstellt werden soll.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Azure-Ressourcengruppe an.
Dieses Cmdlet erstellt einen verknüpften Dienst für die Gruppe, den dieser Parameter angibt.

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

### -ResourceId
Die Azure-Ressourcen-ID.

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Waswenn
Zeigt, was geschieht, wenn das Cmdlet ausgeführt, aber nicht ausgeführt wird.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService

## HINWEISE
Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys

## LINKS ZU VERWANDTEN THEMEN

[Get-AzDataFactoryV2LinkedService]()

[Remove-AzDataFactoryV2LinkedService]()
