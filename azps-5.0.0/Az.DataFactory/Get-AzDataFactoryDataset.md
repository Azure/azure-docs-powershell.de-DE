---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: BB18EEF3-570A-4667-AF0E-FCEEE17B4905
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
ms.openlocfilehash: 44db491986f42bc37df250f5949690efe874c997
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298605"
---
# <span data-ttu-id="1caef-101">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="1caef-101">Get-AzDataFactoryDataset</span></span>

## <span data-ttu-id="1caef-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1caef-102">SYNOPSIS</span></span>
<span data-ttu-id="1caef-103">Ruft Informationen zu Datasets in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="1caef-103">Gets information about datasets in Azure Data Factory.</span></span>

## <span data-ttu-id="1caef-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1caef-104">SYNTAX</span></span>

### <span data-ttu-id="1caef-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="1caef-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1caef-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1caef-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1caef-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1caef-107">DESCRIPTION</span></span>
<span data-ttu-id="1caef-108">Das Cmdlet " **Get-AzDataFactoryDataset** " Ruft Informationen zu Datasets in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="1caef-108">The **Get-AzDataFactoryDataset** cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="1caef-109">Wenn Sie den Namen eines Datasets angeben, ruft dieses Cmdlet Informationen zu diesem DataSet ab.</span><span class="sxs-lookup"><span data-stu-id="1caef-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="1caef-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Datasets in der Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="1caef-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="1caef-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1caef-111">EXAMPLES</span></span>

### <span data-ttu-id="1caef-112">Beispiel 1: Abrufen von Informationen zu allen Datasets</span><span class="sxs-lookup"><span data-stu-id="1caef-112">Example 1: Get information about all datasets</span></span>
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

<span data-ttu-id="1caef-113">Dieser Befehl ruft Informationen zu allen Datasets in der Data Factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="1caef-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="1caef-114">Beispiel 2: Abrufen von Informationen zu einem bestimmten Dataset</span><span class="sxs-lookup"><span data-stu-id="1caef-114">Example 2: Get information about a specific dataset</span></span>
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

<span data-ttu-id="1caef-115">Dieser Befehl ruft Informationen über das DataSet mit dem Namen DAWikipediaClickEvents in der Data Factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="1caef-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

### <span data-ttu-id="1caef-116">Beispiel 3: Abrufen des Speicherorts für ein bestimmtes Dataset</span><span class="sxs-lookup"><span data-stu-id="1caef-116">Example 3: Get the location for a specific dataset</span></span>
```
PS C:\>(Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents").Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="1caef-117">Dieser Befehl ruft Informationen für das DataSet mit dem Namen DAWikipediaClickEvents in der Data Factory mit dem Namen WikiADF ab und verwendet dann die standardmäßige Punktnotation, um den **Speicherort** anzuzeigen, der diesem DataSet zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1caef-117">This command gets information for the dataset named DAWikipediaClickEvents in the data factory named WikiADF, and then uses standard dot notation to view the **Location** associated with that dataset.</span></span>
<span data-ttu-id="1caef-118">Alternativ können Sie die Ausgabe des Cmdlets **Get-AzDataFactoryDataset** einer Variablen zuweisen und dann die Punktnotation verwenden, um die Location-Eigenschaft anzuzeigen, die dem in dieser Variablen gespeicherten DataSet-Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1caef-118">Alternatively, assign the output of the **Get-AzDataFactoryDataset** cmdlet to a variable, and then use dot notation to view the Location property associated with the dataset object stored in that variable.</span></span>

## <span data-ttu-id="1caef-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="1caef-119">PARAMETERS</span></span>

### <span data-ttu-id="1caef-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1caef-120">-DataFactory</span></span>
<span data-ttu-id="1caef-121">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="1caef-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="1caef-122">Dieses Cmdlet ruft Datasets ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="1caef-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1caef-123">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="1caef-123">-DataFactoryName</span></span>
<span data-ttu-id="1caef-124">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="1caef-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="1caef-125">Dieses Cmdlet ruft Datasets ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="1caef-125">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1caef-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1caef-126">-DefaultProfile</span></span>
<span data-ttu-id="1caef-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1caef-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1caef-128">-Name</span><span class="sxs-lookup"><span data-stu-id="1caef-128">-Name</span></span>
<span data-ttu-id="1caef-129">Gibt den Namen des Datasets an, über das dieses Cmdlet Informationen erhält.</span><span class="sxs-lookup"><span data-stu-id="1caef-129">Specifies the name of the dataset about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="1caef-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1caef-130">-ResourceGroupName</span></span>
<span data-ttu-id="1caef-131">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1caef-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1caef-132">Dieses Cmdlet ruft Datasets ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="1caef-132">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1caef-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1caef-133">CommonParameters</span></span>
<span data-ttu-id="1caef-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1caef-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1caef-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1caef-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1caef-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1caef-136">INPUTS</span></span>

### <span data-ttu-id="1caef-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1caef-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="1caef-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1caef-138">System.String</span></span>

## <span data-ttu-id="1caef-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1caef-139">OUTPUTS</span></span>

### <span data-ttu-id="1caef-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="1caef-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="1caef-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="1caef-141">NOTES</span></span>
* <span data-ttu-id="1caef-142">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="1caef-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1caef-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1caef-143">RELATED LINKS</span></span>

[<span data-ttu-id="1caef-144">Neu – AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="1caef-144">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)

[<span data-ttu-id="1caef-145">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="1caef-145">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)


