---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 8742babd73e28e28797db75952d7eb9e9c8dc4a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499133"
---
# Get-AzureRmDataFactoryV2

## Synopsis
Ruft Informationen zu Data Factory ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>]
```

## Beschreibung
Das Get-AzureRmDataFactoryV2-Cmdlet ruft Informationen zu Daten Factorys in einer Azure-Ressourcengruppe ab.
Wenn Sie den Namen einer Data Factory angeben, ruft dieses Cmdlet Informationen zu dieser Data Factory ab.
Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Daten Factorys in einer Azure-Ressourcengruppe ab.


## Beispiele

### Beispiel 1: Abrufen aller Daten Factorys
```
PS C:\> Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

    DataFactoryName   : WikiADF2
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf2
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          :
    ProvisioningState : Succeeded

```

Zeigt Informationen zu allen Daten Fabriken im Azure-Abonnement an.

### Beispiel 2: Abrufen einer bestimmten Data Factory
```
PS C:\> $DataFactory = Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataF
                        actory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

```

Dieser Befehl zeigt Informationen zur Data Factory mit dem Namen WikiADF im Abonnement für die Ressourcengruppe "ADF" an und speichert Sie dann in der $datafactory-Variablen.
Geben Sie den Parameter DataFactory in nachfolgenden Cmdlets an, um die in $DataFactory gespeicherte Data Factory zu verwenden.

## Parameter

### -Name
Gibt den Namen der Data Factory an, über die Informationen abgerufen werden sollen.

```yaml
Type: String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Azure-Ressourcengruppe an.
Dieses Cmdlet ruft Informationen zu Daten Factorys ab, die zu der Gruppe gehören, die dieser Parameter angibt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## Eingaben

### System. String


## Ausgaben

### System. Collections. Generic. List ' 1 [[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]
Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory


## Notizen
Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys

## Verwandte Links
[Satz-AzureRmDataFactoryV2]()

[Remove-AzureRmDataFactoryV2]()

