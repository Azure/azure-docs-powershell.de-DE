---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 171431e317b9edbafe83f7c0c836f5543fcbd65d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496613"
---
# <span data-ttu-id="6f986-101">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="6f986-101">Get-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="6f986-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6f986-102">SYNOPSIS</span></span>
<span data-ttu-id="6f986-103">Ruft Informationen zu Datasets in Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="6f986-103">Gets information about datasets in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f986-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f986-104">SYNTAX</span></span>

### <span data-ttu-id="6f986-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="6f986-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f986-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6f986-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f986-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6f986-107">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2Dataset -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6f986-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6f986-108">DESCRIPTION</span></span>
<span data-ttu-id="6f986-109">Das Get-AzureRmDataFactoryV2Dataset-Cmdlet ruft Informationen zu Datasets in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="6f986-109">The Get-AzureRmDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="6f986-110">Wenn Sie den Namen eines Datasets angeben, ruft dieses Cmdlet Informationen zu diesem DataSet ab.</span><span class="sxs-lookup"><span data-stu-id="6f986-110">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="6f986-111">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Datasets in der Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="6f986-111">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="6f986-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6f986-112">EXAMPLES</span></span>

### <span data-ttu-id="6f986-113">Beispiel 1: Abrufen von Informationen zu allen Datasets</span><span class="sxs-lookup"><span data-stu-id="6f986-113">Example 1: Get information about all datasets</span></span>
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

<span data-ttu-id="6f986-114">Dieser Befehl ruft Informationen zu allen Datasets in der Data Factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="6f986-114">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="6f986-115">Beispiel 2: Abrufen von Informationen zu einem bestimmten Dataset</span><span class="sxs-lookup"><span data-stu-id="6f986-115">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="6f986-116">Dieser Befehl ruft Informationen über das DataSet mit dem Namen DAWikipediaClickEvents in der Data Factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="6f986-116">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="6f986-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f986-117">PARAMETERS</span></span>

### <span data-ttu-id="6f986-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="6f986-118">-DataFactory</span></span>
<span data-ttu-id="6f986-119">Gibt ein PSDataFactory-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="6f986-119">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="6f986-120">Dieses Cmdlet ruft Datasets ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="6f986-120">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>


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

### <span data-ttu-id="6f986-121">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="6f986-121">-DataFactoryName</span></span>
<span data-ttu-id="6f986-122">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="6f986-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="6f986-123">Dieses Cmdlet ruft Datasets ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="6f986-123">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6f986-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f986-124">-DefaultProfile</span></span>
<span data-ttu-id="6f986-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6f986-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f986-126">-Name</span><span class="sxs-lookup"><span data-stu-id="6f986-126">-Name</span></span>
<span data-ttu-id="6f986-127">Gibt den Namen des Datasets an, für das Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6f986-127">Specifies the name of the dataset about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f986-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f986-128">-ResourceGroupName</span></span>
<span data-ttu-id="6f986-129">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="6f986-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="6f986-130">Dieses Cmdlet ruft Datasets ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="6f986-130">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6f986-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6f986-131">-ResourceId</span></span>
<span data-ttu-id="6f986-132">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="6f986-132">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f986-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f986-133">CommonParameters</span></span>
<span data-ttu-id="6f986-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f986-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f986-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f986-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f986-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6f986-136">INPUTS</span></span>

### <span data-ttu-id="6f986-137">System. String</span><span class="sxs-lookup"><span data-stu-id="6f986-137">System.String</span></span>
<span data-ttu-id="6f986-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="6f986-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="6f986-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6f986-139">OUTPUTS</span></span>

### <span data-ttu-id="6f986-140">System. Collections. Generic. List ' 1 [[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6f986-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="6f986-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="6f986-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="6f986-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="6f986-142">NOTES</span></span>
<span data-ttu-id="6f986-143">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="6f986-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="6f986-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6f986-144">RELATED LINKS</span></span>

[<span data-ttu-id="6f986-145">Satz-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="6f986-145">Set-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="6f986-146">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="6f986-146">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
