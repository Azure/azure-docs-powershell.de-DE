---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
ms.openlocfilehash: 292a288850371a834f938143cf2ec4380504091b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307499"
---
# Get-AzDataFactoryHub

## SYNOPSIS
Ruft Informationen zu Hubs in Azure Data Factory ab.

## SYNTAX

### ByFactoryName (Standard)
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzDataFactoryHub-Cmdlet** ruft Informationen zu Hubs in Azure Data Factory ab.
Wenn Sie den Namen eines Hubs angeben, ruft dieses Cmdlet Informationen zu diesem Hub ab.
Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Hubs in einer Daten factory ab.

## BEISPIELE

### Beispiel 1: Alle Datenhubs erhalten
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

Dieser Befehl ruft alle Datenhubs in der Azure-Ressourcengruppe mit dem Namen ADFResourceGroup und der Datenfactory mit dem Namen ADFDataFactory ab.

### Beispiel 2: Erhalten eines bestimmten Datenhubs
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

Dieser Befehl ruft Informationen über den Hub mit dem Namen "MyDataHub" in der Azure-Ressourcengruppe mit dem Namen ADFResourceGroup und der Datenfactory mit dem Namen ADFDataFactory ab.

## PARAMETERS

### -DataFactory
Gibt ein **"PSDataFactory"-Objekt** an.
Dieses Cmdlet ruft Informationen zu Hubs in der Daten factory ab, die dieser Parameter angibt.

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
Dieses Cmdlet ruft Informationen zu Hubs in der Daten factory ab, die dieser Parameter angibt.

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

### -Name
Gibt den Namen des Hubs an, über den Informationen angezeigt werden.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Azure-Ressourcengruppe an.
Dieses Cmdlet ruft Informationen zu Hubs ab, die zu der Gruppe gehören, die dieser Parameter angibt.

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

### System.String

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

## AUSGABEN

### Microsoft.Azure.Commands.DataFactories.Models.PSHub

## HINWEISE
* Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys

## LINKS ZU VERWANDTEN THEMEN

[New-AzDataFactoryHub](./New-AzDataFactoryHub.md)

[Remove-AzDataFactoryHub](./Remove-AzDataFactoryHub.md)


