---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: BB18EEF3-570A-4667-AF0E-FCEEE17B4905
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
ms.openlocfilehash: 44db491986f42bc37df250f5949690efe874c997
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148289"
---
# <span data-ttu-id="87b12-101">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="87b12-101">Get-AzDataFactoryDataset</span></span>

## <span data-ttu-id="87b12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87b12-102">SYNOPSIS</span></span>
<span data-ttu-id="87b12-103">Ruft Informationen zu Datasets in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="87b12-103">Gets information about datasets in Azure Data Factory.</span></span>

## <span data-ttu-id="87b12-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87b12-104">SYNTAX</span></span>

### <span data-ttu-id="87b12-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="87b12-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87b12-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="87b12-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87b12-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="87b12-107">DESCRIPTION</span></span>
<span data-ttu-id="87b12-108">Das **Cmdlet "Get-AzDataFactoryDataset"** ruft Informationen zu Datasets in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="87b12-108">The **Get-AzDataFactoryDataset** cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="87b12-109">Wenn Sie den Namen eines Datasets angeben, ruft dieses Cmdlet Informationen zu diesem Dataset ab.</span><span class="sxs-lookup"><span data-stu-id="87b12-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="87b12-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Datasets in der Daten factory ab.</span><span class="sxs-lookup"><span data-stu-id="87b12-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="87b12-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="87b12-111">EXAMPLES</span></span>

### <span data-ttu-id="87b12-112">Beispiel 1: Informationen zu allen Datasets</span><span class="sxs-lookup"><span data-stu-id="87b12-112">Example 1: Get information about all datasets</span></span>
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

<span data-ttu-id="87b12-113">Dieser Befehl ruft Informationen zu allen Datasets in der Daten factory namens WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="87b12-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="87b12-114">Beispiel 2: Erhalten von Informationen zu einem bestimmten Dataset</span><span class="sxs-lookup"><span data-stu-id="87b12-114">Example 2: Get information about a specific dataset</span></span>
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

<span data-ttu-id="87b12-115">Dieser Befehl ruft Informationen über das Dataset mit dem Namen "DAWikipediaClickEvents" in der Daten factory namens WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="87b12-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

### <span data-ttu-id="87b12-116">Beispiel 3: Den Speicherort für ein bestimmtes Dataset erhalten</span><span class="sxs-lookup"><span data-stu-id="87b12-116">Example 3: Get the location for a specific dataset</span></span>
```
PS C:\>(Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents").Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="87b12-117">Dieser Befehl ruft Informationen für das Dataset mit dem Namen DAWikipediaClickEvents in der Daten factory  namens WikiADF ab und verwendet dann die Standardmäßige Punktformatierung, um den Mit diesem Dataset verknüpften Speicherort anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="87b12-117">This command gets information for the dataset named DAWikipediaClickEvents in the data factory named WikiADF, and then uses standard dot notation to view the **Location** associated with that dataset.</span></span>
<span data-ttu-id="87b12-118">Weisen Sie alternativ die Ausgabe des **Cmdlets "Get-AzDataFactoryDataset"** einer Variablen zu, und verwenden Sie dann die Punkt-Notation, um die Standorteigenschaft anzuzeigen, die dem in dieser Variable gespeicherten Datasetobjekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="87b12-118">Alternatively, assign the output of the **Get-AzDataFactoryDataset** cmdlet to a variable, and then use dot notation to view the Location property associated with the dataset object stored in that variable.</span></span>

## <span data-ttu-id="87b12-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87b12-119">PARAMETERS</span></span>

### <span data-ttu-id="87b12-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="87b12-120">-DataFactory</span></span>
<span data-ttu-id="87b12-121">Gibt ein **"PSDataFactory"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="87b12-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="87b12-122">Dieses Cmdlet ruft Datasets ab, die zu der von diesem Parameter angegebenen Daten factory gehören.</span><span class="sxs-lookup"><span data-stu-id="87b12-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="87b12-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="87b12-123">-DataFactoryName</span></span>
<span data-ttu-id="87b12-124">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="87b12-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="87b12-125">Dieses Cmdlet ruft Datasets ab, die zu der von diesem Parameter angegebenen Daten factory gehören.</span><span class="sxs-lookup"><span data-stu-id="87b12-125">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="87b12-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87b12-126">-DefaultProfile</span></span>
<span data-ttu-id="87b12-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="87b12-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87b12-128">-Name</span><span class="sxs-lookup"><span data-stu-id="87b12-128">-Name</span></span>
<span data-ttu-id="87b12-129">Gibt den Namen des Datasets an, über das dieses Cmdlet Informationen erhält.</span><span class="sxs-lookup"><span data-stu-id="87b12-129">Specifies the name of the dataset about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="87b12-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87b12-130">-ResourceGroupName</span></span>
<span data-ttu-id="87b12-131">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="87b12-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="87b12-132">Dieses Cmdlet ruft Datasets ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="87b12-132">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="87b12-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87b12-133">CommonParameters</span></span>
<span data-ttu-id="87b12-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87b12-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87b12-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87b12-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87b12-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="87b12-136">INPUTS</span></span>

### <span data-ttu-id="87b12-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="87b12-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="87b12-138">System.String</span><span class="sxs-lookup"><span data-stu-id="87b12-138">System.String</span></span>

## <span data-ttu-id="87b12-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="87b12-139">OUTPUTS</span></span>

### <span data-ttu-id="87b12-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="87b12-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="87b12-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="87b12-141">NOTES</span></span>
* <span data-ttu-id="87b12-142">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="87b12-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="87b12-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="87b12-143">RELATED LINKS</span></span>

[<span data-ttu-id="87b12-144">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="87b12-144">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)

[<span data-ttu-id="87b12-145">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="87b12-145">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)


