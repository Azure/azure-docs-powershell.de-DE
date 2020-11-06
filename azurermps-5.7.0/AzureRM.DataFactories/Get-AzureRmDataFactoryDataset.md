---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: BB18EEF3-570A-4667-AF0E-FCEEE17B4905
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryDataset.md
ms.openlocfilehash: 10e4af67d76e6c9d367de4d9b512d003e211ddae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497669"
---
# <span data-ttu-id="11366-101">Get-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="11366-101">Get-AzureRmDataFactoryDataset</span></span>

## <span data-ttu-id="11366-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="11366-102">SYNOPSIS</span></span>
<span data-ttu-id="11366-103">Ruft Informationen zu Datasets in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="11366-103">Gets information about datasets in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11366-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="11366-104">SYNTAX</span></span>

### <span data-ttu-id="11366-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="11366-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11366-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="11366-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11366-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11366-107">DESCRIPTION</span></span>
<span data-ttu-id="11366-108">Das Cmdlet " **Get-AzureRmDataFactoryDataset** " Ruft Informationen zu Datasets in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="11366-108">The **Get-AzureRmDataFactoryDataset** cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="11366-109">Wenn Sie den Namen eines Datasets angeben, ruft dieses Cmdlet Informationen zu diesem DataSet ab.</span><span class="sxs-lookup"><span data-stu-id="11366-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="11366-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Datasets in der Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="11366-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="11366-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="11366-111">EXAMPLES</span></span>

### <span data-ttu-id="11366-112">Beispiel 1: Abrufen von Informationen zu allen Datasets</span><span class="sxs-lookup"><span data-stu-id="11366-112">Example 1: Get information about all datasets</span></span>
```
PS C:\>Get-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 
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

<span data-ttu-id="11366-113">Dieser Befehl ruft Informationen zu allen Datasets in der Data Factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="11366-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="11366-114">Beispiel 2: Abrufen von Informationen zu einem bestimmten Dataset</span><span class="sxs-lookup"><span data-stu-id="11366-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\>Get-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" 
DatasetName       : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

<span data-ttu-id="11366-115">Dieser Befehl ruft Informationen über das DataSet mit dem Namen DAWikipediaClickEvents in der Data Factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="11366-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

### <span data-ttu-id="11366-116">Beispiel 3: Abrufen des Speicherorts für ein bestimmtes Dataset</span><span class="sxs-lookup"><span data-stu-id="11366-116">Example 3: Get the location for a specific dataset</span></span>
```
PS C:\>(Get-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents").Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="11366-117">Dieser Befehl ruft Informationen für das DataSet mit dem Namen DAWikipediaClickEvents in der Data Factory mit dem Namen WikiADF ab und verwendet dann die standardmäßige Punktnotation, um den **Speicherort** anzuzeigen, der diesem DataSet zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="11366-117">This command gets information for the dataset named DAWikipediaClickEvents in the data factory named WikiADF, and then uses standard dot notation to view the **Location** associated with that dataset.</span></span>
<span data-ttu-id="11366-118">Alternativ können Sie die Ausgabe des Cmdlets **Get-AzureRmDataFactoryDataset** einer Variablen zuweisen und dann die Punktnotation verwenden, um die Location-Eigenschaft anzuzeigen, die dem in dieser Variablen gespeicherten DataSet-Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="11366-118">Alternatively, assign the output of the **Get-AzureRmDataFactoryDataset** cmdlet to a variable, and then use dot notation to view the Location property associated with the dataset object stored in that variable.</span></span>

## <span data-ttu-id="11366-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="11366-119">PARAMETERS</span></span>

### <span data-ttu-id="11366-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="11366-120">-DataFactory</span></span>
<span data-ttu-id="11366-121">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="11366-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="11366-122">Dieses Cmdlet ruft Datasets ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="11366-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11366-123">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="11366-123">-DataFactoryName</span></span>
<span data-ttu-id="11366-124">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="11366-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="11366-125">Dieses Cmdlet ruft Datasets ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="11366-125">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="11366-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11366-126">-DefaultProfile</span></span>
<span data-ttu-id="11366-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="11366-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11366-128">-Name</span><span class="sxs-lookup"><span data-stu-id="11366-128">-Name</span></span>
<span data-ttu-id="11366-129">Gibt den Namen des Datasets an, über das dieses Cmdlet Informationen erhält.</span><span class="sxs-lookup"><span data-stu-id="11366-129">Specifies the name of the dataset about which this cmdlet gets information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11366-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11366-130">-ResourceGroupName</span></span>
<span data-ttu-id="11366-131">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="11366-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="11366-132">Dieses Cmdlet ruft Datasets ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="11366-132">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="11366-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11366-133">CommonParameters</span></span>
<span data-ttu-id="11366-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11366-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11366-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11366-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11366-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="11366-136">INPUTS</span></span>

### <span data-ttu-id="11366-137">Keine</span><span class="sxs-lookup"><span data-stu-id="11366-137">None</span></span>
<span data-ttu-id="11366-138">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="11366-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="11366-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="11366-139">OUTPUTS</span></span>

### <span data-ttu-id="11366-140">System. Collections. Generic. List ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataset, Microsoft. WindowsAzure. Commands. Utilities, Version = 0.8.2.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataset</span><span class="sxs-lookup"><span data-stu-id="11366-140">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataset, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataset</span></span>

## <span data-ttu-id="11366-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="11366-141">NOTES</span></span>
* <span data-ttu-id="11366-142">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="11366-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="11366-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="11366-143">RELATED LINKS</span></span>

[<span data-ttu-id="11366-144">Neu – AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="11366-144">New-AzureRmDataFactoryDataset</span></span>](./New-AzureRmDataFactoryDataset.md)

[<span data-ttu-id="11366-145">Remove-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="11366-145">Remove-AzureRmDataFactoryDataset</span></span>](./Remove-AzureRmDataFactoryDataset.md)


