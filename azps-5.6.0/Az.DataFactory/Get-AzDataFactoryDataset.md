---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: BB18EEF3-570A-4667-AF0E-FCEEE17B4905
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
ms.openlocfilehash: c31a8bb3ef09eb190a7a4c77aef0c44fadbf8960
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939616"
---
# <span data-ttu-id="413cc-101">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="413cc-101">Get-AzDataFactoryDataset</span></span>

## <span data-ttu-id="413cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="413cc-102">SYNOPSIS</span></span>
<span data-ttu-id="413cc-103">Ruft Informationen zu Datasets in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="413cc-103">Gets information about datasets in Azure Data Factory.</span></span>

## <span data-ttu-id="413cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="413cc-104">SYNTAX</span></span>

### <span data-ttu-id="413cc-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="413cc-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="413cc-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="413cc-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="413cc-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="413cc-107">DESCRIPTION</span></span>
<span data-ttu-id="413cc-108">Das **Get-AzDataFactoryDataset-Cmdlet** ruft Informationen zu Datasets in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="413cc-108">The **Get-AzDataFactoryDataset** cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="413cc-109">Wenn Sie den Namen eines Datasets angeben, ruft dieses Cmdlet Informationen zu diesem Dataset ab.</span><span class="sxs-lookup"><span data-stu-id="413cc-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="413cc-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Datasets in der Daten factory ab.</span><span class="sxs-lookup"><span data-stu-id="413cc-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="413cc-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="413cc-111">EXAMPLES</span></span>

### <span data-ttu-id="413cc-112">Beispiel 1: Informationen zu allen Datasets</span><span class="sxs-lookup"><span data-stu-id="413cc-112">Example 1: Get information about all datasets</span></span>
```
PS C:\>Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 
DatasetName       : DACuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}

DatasetName       : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}

DatasetName         : DAWikiAggregatedData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}
```

<span data-ttu-id="413cc-113">Dieser Befehl ruft Informationen zu allen Datasets in der Daten factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="413cc-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="413cc-114">Beispiel 2: Informationen zu einem bestimmten Dataset erhalten</span><span class="sxs-lookup"><span data-stu-id="413cc-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\>Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" 
DatasetName       : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

<span data-ttu-id="413cc-115">Dieser Befehl ruft Informationen zum Dataset mit dem Namen DAWikipediaClickEvents in der Daten factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="413cc-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

### <span data-ttu-id="413cc-116">Beispiel 3: Speicherort für ein bestimmtes Dataset</span><span class="sxs-lookup"><span data-stu-id="413cc-116">Example 3: Get the location for a specific dataset</span></span>
```
PS C:\>(Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents").Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="413cc-117">Dieser Befehl ruft Informationen für das Dataset mit dem Namen DAWikipediaClickEvents in der Daten factory  mit dem Namen WikiADF ab und verwendet dann die Standardpunkt-Notation, um die dem Dataset zugeordnete Position anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="413cc-117">This command gets information for the dataset named DAWikipediaClickEvents in the data factory named WikiADF, and then uses standard dot notation to view the **Location** associated with that dataset.</span></span>
<span data-ttu-id="413cc-118">Alternativ können Sie die Ausgabe des **Get-AzDataFactoryDataset-Cmdlets** einer Variablen zuweisen und dann die Dot-Notation verwenden, um die Position-Eigenschaft anzuzeigen, die dem dataset-Objekt zugeordnet ist, das in dieser Variable gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="413cc-118">Alternatively, assign the output of the **Get-AzDataFactoryDataset** cmdlet to a variable, and then use dot notation to view the Location property associated with the dataset object stored in that variable.</span></span>

## <span data-ttu-id="413cc-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="413cc-119">PARAMETERS</span></span>

### <span data-ttu-id="413cc-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="413cc-120">-DataFactory</span></span>
<span data-ttu-id="413cc-121">Gibt ein **PSDataFactory-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="413cc-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="413cc-122">Dieses Cmdlet ruft Datasets ab, die zur daten factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="413cc-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="413cc-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="413cc-123">-DataFactoryName</span></span>
<span data-ttu-id="413cc-124">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="413cc-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="413cc-125">Dieses Cmdlet ruft Datasets ab, die zur daten factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="413cc-125">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="413cc-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="413cc-126">-DefaultProfile</span></span>
<span data-ttu-id="413cc-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="413cc-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="413cc-128">-Name</span><span class="sxs-lookup"><span data-stu-id="413cc-128">-Name</span></span>
<span data-ttu-id="413cc-129">Gibt den Namen des Datasets an, über das dieses Cmdlet Informationen erhält.</span><span class="sxs-lookup"><span data-stu-id="413cc-129">Specifies the name of the dataset about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="413cc-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="413cc-130">-ResourceGroupName</span></span>
<span data-ttu-id="413cc-131">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="413cc-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="413cc-132">Dieses Cmdlet ruft Datasets ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="413cc-132">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="413cc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="413cc-133">CommonParameters</span></span>
<span data-ttu-id="413cc-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="413cc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="413cc-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="413cc-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="413cc-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="413cc-136">INPUTS</span></span>

### <span data-ttu-id="413cc-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="413cc-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="413cc-138">System.String</span><span class="sxs-lookup"><span data-stu-id="413cc-138">System.String</span></span>

## <span data-ttu-id="413cc-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="413cc-139">OUTPUTS</span></span>

### <span data-ttu-id="413cc-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="413cc-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="413cc-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="413cc-141">NOTES</span></span>
* <span data-ttu-id="413cc-142">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factory</span><span class="sxs-lookup"><span data-stu-id="413cc-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="413cc-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="413cc-143">RELATED LINKS</span></span>

[<span data-ttu-id="413cc-144">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="413cc-144">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)

[<span data-ttu-id="413cc-145">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="413cc-145">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)


