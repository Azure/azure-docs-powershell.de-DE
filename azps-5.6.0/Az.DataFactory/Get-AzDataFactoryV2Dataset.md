---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 938b51b6025a420570ad62b4e9ce815fe832c4cb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930251"
---
# <span data-ttu-id="889b6-101">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="889b6-101">Get-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="889b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="889b6-102">SYNOPSIS</span></span>
<span data-ttu-id="889b6-103">Ruft Informationen zu Datasets in Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="889b6-103">Gets information about datasets in Data Factory.</span></span>

## <span data-ttu-id="889b6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="889b6-104">SYNTAX</span></span>

### <span data-ttu-id="889b6-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="889b6-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="889b6-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="889b6-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="889b6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="889b6-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Dataset [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="889b6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="889b6-108">DESCRIPTION</span></span>
<span data-ttu-id="889b6-109">Das Get-AzDataFactoryV2Dataset-Cmdlet ruft Informationen zu Datasets in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="889b6-109">The Get-AzDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="889b6-110">Wenn Sie den Namen eines Datasets angeben, ruft dieses Cmdlet Informationen zu diesem Dataset ab.</span><span class="sxs-lookup"><span data-stu-id="889b6-110">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="889b6-111">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Datasets in der Daten factory ab.</span><span class="sxs-lookup"><span data-stu-id="889b6-111">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="889b6-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="889b6-112">EXAMPLES</span></span>

### <span data-ttu-id="889b6-113">Beispiel 1: Informationen zu allen Datasets</span><span class="sxs-lookup"><span data-stu-id="889b6-113">Example 1: Get information about all datasets</span></span>
```
PS C:\> Get-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

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

<span data-ttu-id="889b6-114">Dieser Befehl ruft Informationen zu allen Datasets in der Daten factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="889b6-114">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="889b6-115">Beispiel 2: Informationen zu einem bestimmten Dataset erhalten</span><span class="sxs-lookup"><span data-stu-id="889b6-115">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="889b6-116">Dieser Befehl ruft Informationen zum Dataset mit dem Namen DAWikipediaClickEvents in der Daten factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="889b6-116">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="889b6-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="889b6-117">PARAMETERS</span></span>

### <span data-ttu-id="889b6-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="889b6-118">-DataFactory</span></span>
<span data-ttu-id="889b6-119">Gibt ein PSDataFactory-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="889b6-119">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="889b6-120">Dieses Cmdlet ruft Datasets ab, die zur daten factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="889b6-120">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="889b6-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="889b6-121">-DataFactoryName</span></span>
<span data-ttu-id="889b6-122">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="889b6-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="889b6-123">Dieses Cmdlet ruft Datasets ab, die zur daten factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="889b6-123">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="889b6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="889b6-124">-DefaultProfile</span></span>
<span data-ttu-id="889b6-125">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="889b6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="889b6-126">-Name</span><span class="sxs-lookup"><span data-stu-id="889b6-126">-Name</span></span>
<span data-ttu-id="889b6-127">Gibt den Namen des Datasets an, über das Informationen angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="889b6-127">Specifies the name of the dataset about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="889b6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="889b6-128">-ResourceGroupName</span></span>
<span data-ttu-id="889b6-129">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="889b6-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="889b6-130">Dieses Cmdlet ruft Datasets ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="889b6-130">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="889b6-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="889b6-131">-ResourceId</span></span>
<span data-ttu-id="889b6-132">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="889b6-132">The Azure resource ID.</span></span>

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

### <span data-ttu-id="889b6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="889b6-133">CommonParameters</span></span>
<span data-ttu-id="889b6-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="889b6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="889b6-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="889b6-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="889b6-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="889b6-136">INPUTS</span></span>

### <span data-ttu-id="889b6-137">System.String</span><span class="sxs-lookup"><span data-stu-id="889b6-137">System.String</span></span>

### <span data-ttu-id="889b6-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="889b6-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="889b6-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="889b6-139">OUTPUTS</span></span>

### <span data-ttu-id="889b6-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="889b6-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="889b6-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="889b6-141">NOTES</span></span>
<span data-ttu-id="889b6-142">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factory</span><span class="sxs-lookup"><span data-stu-id="889b6-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="889b6-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="889b6-143">RELATED LINKS</span></span>

[<span data-ttu-id="889b6-144">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="889b6-144">Set-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="889b6-145">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="889b6-145">Remove-AzDataFactoryV2Dataset</span></span>]()
