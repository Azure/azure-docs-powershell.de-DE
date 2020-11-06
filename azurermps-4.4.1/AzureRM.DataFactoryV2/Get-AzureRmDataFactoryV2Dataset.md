---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
gitcommit: https://github.com/Azure/azure-powershell/blob/c396953644d237789e0f4e1f726b553913186d34
ms.openlocfilehash: ec66f865c4a511935599b81b672cd60d6da78485
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505106"
---
# <span data-ttu-id="4b44b-101">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="4b44b-101">Get-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="4b44b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4b44b-102">SYNOPSIS</span></span>
<span data-ttu-id="4b44b-103">Ruft Informationen zu Datasets in Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="4b44b-103">Gets information about datasets in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b44b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b44b-104">SYNTAX</span></span>

### <span data-ttu-id="4b44b-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="4b44b-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="4b44b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4b44b-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
```

## <span data-ttu-id="4b44b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b44b-107">DESCRIPTION</span></span>
<span data-ttu-id="4b44b-108">Das Get-AzureRmDataFactoryV2Dataset-Cmdlet ruft Informationen zu Datasets in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="4b44b-108">The Get-AzureRmDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="4b44b-109">Wenn Sie den Namen eines Datasets angeben, ruft dieses Cmdlet Informationen zu diesem DataSet ab.</span><span class="sxs-lookup"><span data-stu-id="4b44b-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="4b44b-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Datasets in der Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="4b44b-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="4b44b-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4b44b-111">EXAMPLES</span></span>

### <span data-ttu-id="4b44b-112">Beispiel 1: Abrufen von Informationen zu allen Datasets</span><span class="sxs-lookup"><span data-stu-id="4b44b-112">Example 1: Get information about all datasets</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

    DatasetName       : DACuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

    DatasetName       : DAWikiAggregatedData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

```

<span data-ttu-id="4b44b-113">Dieser Befehl ruft Informationen zu allen Datasets in der Data Factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="4b44b-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="4b44b-114">Beispiel 2: Abrufen von Informationen zu einem bestimmten Dataset</span><span class="sxs-lookup"><span data-stu-id="4b44b-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

```

<span data-ttu-id="4b44b-115">Dieser Befehl ruft Informationen über das DataSet mit dem Namen DAWikipediaClickEvents in der Data Factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="4b44b-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="4b44b-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b44b-116">PARAMETERS</span></span>

### <span data-ttu-id="4b44b-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="4b44b-117">-DataFactory</span></span>
<span data-ttu-id="4b44b-118">Gibt ein PSDataFactory-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="4b44b-118">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="4b44b-119">Dieses Cmdlet ruft Datasets ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="4b44b-119">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>


```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b44b-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="4b44b-120">-DataFactoryName</span></span>
<span data-ttu-id="4b44b-121">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="4b44b-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="4b44b-122">Dieses Cmdlet ruft Datasets ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="4b44b-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4b44b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="4b44b-123">-Name</span></span>
<span data-ttu-id="4b44b-124">Gibt den Namen des Datasets an, für das Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4b44b-124">Specifies the name of the dataset about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b44b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b44b-125">-ResourceGroupName</span></span>
<span data-ttu-id="4b44b-126">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4b44b-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4b44b-127">Dieses Cmdlet ruft Datasets ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="4b44b-127">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

## <span data-ttu-id="4b44b-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4b44b-128">INPUTS</span></span>

### <span data-ttu-id="4b44b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4b44b-129">System.String</span></span>
<span data-ttu-id="4b44b-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4b44b-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="4b44b-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4b44b-131">OUTPUTS</span></span>

### <span data-ttu-id="4b44b-132">System. Collections. Generic. List ' 1 [[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4b44b-132">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="4b44b-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="4b44b-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>


## <span data-ttu-id="4b44b-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="4b44b-134">NOTES</span></span>
<span data-ttu-id="4b44b-135">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="4b44b-135">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4b44b-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4b44b-136">RELATED LINKS</span></span>
[<span data-ttu-id="4b44b-137">Satz-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="4b44b-137">Set-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="4b44b-138">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="4b44b-138">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
