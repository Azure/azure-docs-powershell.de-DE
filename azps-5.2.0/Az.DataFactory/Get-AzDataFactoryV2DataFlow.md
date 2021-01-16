---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: b4af5eae61e47d8617eb270451f406f349162f50
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307427"
---
# Get-AzDataFactoryV2DataFlow

## SYNOPSIS
Ruft Informationen zu Datenflüssen in Data Factory ab.

## SYNTAX

### ByFactoryName (Standard)
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByResourceId
```
Get-AzDataFactoryV2DataFlow [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das Get-AzDataFactoryV2DataFlow Cmdlet ruft Informationen zu Datenflüssen in Azure Data Factory ab.
Wenn Sie den Namen eines Datenflusses angeben, ruft dieses Cmdlet Informationen zu diesem Datenfluss ab.
Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Datenflüssen in der Daten factory ab.

## BEISPIELE
### Beispiel 1: Informationen zu allen Datenflüssen
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow3                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

Dieser Befehl ruft Informationen zu allen Datenflüssen in der Daten factory namens WikiADF ab.

### Beispiel 2: Erhalten von Informationen zu einem bestimmten Datenfluss
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "dataflow1"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

Dieser Befehl ruft Informationen über den Datenfluss namens "dataflow1" in der Daten factory namens WikiADF ab.

## PARAMETERS

### -DataFactory
Das Data Factory-Objekt.

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DataFactoryName
Der Name der Daten factory.

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

### -Name
Der Datenflussname.

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: DataFlowName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

### Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory

## AUSGABEN

### Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow

## HINWEISE
Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys

## LINKS ZU VERWANDTEN THEMEN

[Set-AzDataFactoryDataFlow](./Set-AzDataFactoryDataFlow.md)

[Remove-AzDataFactoryDataFlow](./Remove-AzDataFactoryDataFlow.md)