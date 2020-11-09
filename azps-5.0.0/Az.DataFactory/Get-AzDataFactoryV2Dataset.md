---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 5af8053f3d504cfc3eb28a2f8ad71f83492f0e3e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298539"
---
# <span data-ttu-id="1dbbb-101">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="1dbbb-101">Get-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="1dbbb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1dbbb-102">SYNOPSIS</span></span>
<span data-ttu-id="1dbbb-103">Ruft Informationen zu Datasets in Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="1dbbb-103">Gets information about datasets in Data Factory.</span></span>

## <span data-ttu-id="1dbbb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1dbbb-104">SYNTAX</span></span>

### <span data-ttu-id="1dbbb-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="1dbbb-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dbbb-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1dbbb-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dbbb-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1dbbb-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Dataset [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1dbbb-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1dbbb-108">DESCRIPTION</span></span>
<span data-ttu-id="1dbbb-109">Das Get-AzDataFactoryV2Dataset-Cmdlet ruft Informationen zu Datasets in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="1dbbb-109">The Get-AzDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="1dbbb-110">Wenn Sie den Namen eines Datasets angeben, ruft dieses Cmdlet Informationen zu diesem DataSet ab.</span><span class="sxs-lookup"><span data-stu-id="1dbbb-110">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="1dbbb-111">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Datasets in der Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="1dbbb-111">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="1dbbb-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1dbbb-112">EXAMPLES</span></span>

### <span data-ttu-id="1dbbb-113">Beispiel 1: Abrufen von Informationen zu allen Datasets</span><span class="sxs-lookup"><span data-stu-id="1dbbb-113">Example 1: Get information about all datasets</span></span>
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

<span data-ttu-id="1dbbb-114">Dieser Befehl ruft Informationen zu allen Datasets in der Data Factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="1dbbb-114">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="1dbbb-115">Beispiel 2: Abrufen von Informationen zu einem bestimmten Dataset</span><span class="sxs-lookup"><span data-stu-id="1dbbb-115">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="1dbbb-116">Dieser Befehl ruft Informationen über das DataSet mit dem Namen DAWikipediaClickEvents in der Data Factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="1dbbb-116">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="1dbbb-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="1dbbb-117">PARAMETERS</span></span>

### <span data-ttu-id="1dbbb-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1dbbb-118">-DataFactory</span></span>
<span data-ttu-id="1dbbb-119">Gibt ein PSDataFactory-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="1dbbb-119">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="1dbbb-120">Dieses Cmdlet ruft Datasets ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="1dbbb-120">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1dbbb-121">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="1dbbb-121">-DataFactoryName</span></span>
<span data-ttu-id="1dbbb-122">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="1dbbb-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="1dbbb-123">Dieses Cmdlet ruft Datasets ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="1dbbb-123">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1dbbb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dbbb-124">-DefaultProfile</span></span>
<span data-ttu-id="1dbbb-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1dbbb-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dbbb-126">-Name</span><span class="sxs-lookup"><span data-stu-id="1dbbb-126">-Name</span></span>
<span data-ttu-id="1dbbb-127">Gibt den Namen des Datasets an, für das Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1dbbb-127">Specifies the name of the dataset about which to get information.</span></span>

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

### <span data-ttu-id="1dbbb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dbbb-128">-ResourceGroupName</span></span>
<span data-ttu-id="1dbbb-129">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1dbbb-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1dbbb-130">Dieses Cmdlet ruft Datasets ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="1dbbb-130">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1dbbb-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1dbbb-131">-ResourceId</span></span>
<span data-ttu-id="1dbbb-132">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="1dbbb-132">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1dbbb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dbbb-133">CommonParameters</span></span>
<span data-ttu-id="1dbbb-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dbbb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dbbb-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dbbb-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dbbb-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1dbbb-136">INPUTS</span></span>

### <span data-ttu-id="1dbbb-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1dbbb-137">System.String</span></span>

### <span data-ttu-id="1dbbb-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1dbbb-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="1dbbb-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1dbbb-139">OUTPUTS</span></span>

### <span data-ttu-id="1dbbb-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="1dbbb-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="1dbbb-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="1dbbb-141">NOTES</span></span>
<span data-ttu-id="1dbbb-142">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="1dbbb-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1dbbb-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1dbbb-143">RELATED LINKS</span></span>

[<span data-ttu-id="1dbbb-144">Satz-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="1dbbb-144">Set-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="1dbbb-145">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="1dbbb-145">Remove-AzDataFactoryV2Dataset</span></span>]()
