---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7100B5F0-A07B-4305-BF80-1F52647A03AB
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
ms.openlocfilehash: f04f2d2d96dd0b293850ca3150568eb015ab5bbb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472685"
---
# <span data-ttu-id="87fe7-101">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="87fe7-101">Get-AzDataFactoryRun</span></span>

## <span data-ttu-id="87fe7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87fe7-102">SYNOPSIS</span></span>
<span data-ttu-id="87fe7-103">Wird für ein Datendatenschnitt eines Datasets in Azure Data Factory ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="87fe7-103">Gets runs for a data slice of a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="87fe7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87fe7-104">SYNTAX</span></span>

### <span data-ttu-id="87fe7-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="87fe7-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryRun [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87fe7-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="87fe7-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryRun [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87fe7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="87fe7-107">DESCRIPTION</span></span>
<span data-ttu-id="87fe7-108">Das **Cmdlet "Get-AzDataFactoryRun"** ruft die Runs für ein Datendatenschnitt eines Datasets in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="87fe7-108">The **Get-AzDataFactoryRun** cmdlet gets the runs for a data slice of a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="87fe7-109">Ein Dataset in einer Daten factory besteht aus Segmenten über der Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="87fe7-109">A dataset in a data factory is composed of slices over the time axis.</span></span>
<span data-ttu-id="87fe7-110">Die Breite eines Segments wird durch den Zeitplan (stündlich oder täglich) bestimmt.</span><span class="sxs-lookup"><span data-stu-id="87fe7-110">The width of a slice is determined by the schedule, either hourly or daily.</span></span>
<span data-ttu-id="87fe7-111">Eine Ausführung ist eine Verarbeitungseinheit für ein Segment.</span><span class="sxs-lookup"><span data-stu-id="87fe7-111">A run is a unit of processing for a slice.</span></span>
<span data-ttu-id="87fe7-112">Bei Wiederholungen oder für den Fall, dass Sie das Segment aufgrund von Fehlern erneut ausführen, kann mindestens ein Segment ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="87fe7-112">There could be one or more runs for a slice in case of retries or in case you rerun your slice due to failures.</span></span>
<span data-ttu-id="87fe7-113">Ein Segment wird durch seine Startzeit identifiziert.</span><span class="sxs-lookup"><span data-stu-id="87fe7-113">A slice is identified by its start time.</span></span>
<span data-ttu-id="87fe7-114">Verwenden Sie das cmdlet "Get-AzDataFactorySlice", um die Startzeit eines Datenschnitts zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="87fe7-114">To obtain the start time of a slice, use the Get-AzDataFactorySlice cmdlet.</span></span>
<span data-ttu-id="87fe7-115">Um beispielsweise eine Ausführung für das folgende Segment zu erhalten, verwenden Sie die Startzeit 2015-04-02T20:00:00.</span><span class="sxs-lookup"><span data-stu-id="87fe7-115">For example, to get a run for the following slice, use the start time 2015-04-02T20:00:00.</span></span>
<span data-ttu-id="87fe7-116">ResourceGroupName: ADF DataFactoryName: SPDataFactory0924 DatasetName: MarketingStatusaignEffectivenessBlobDataset Start : 02.05.2014 20:00 Uhr Ende: 03.05.2014 20:00: Wiederholungscount: 0 Status: Ready LatencyStatus :</span><span class="sxs-lookup"><span data-stu-id="87fe7-116">ResourceGroupName  : ADF DataFactoryName : SPDataFactory0924 DatasetName : MarketingCampaignEffectivenessBlobDataset Start : 5/2/2014 8:00:00 PM End : 5/3/2014 8:00:00 PM RetryCount : 0 Status : Ready LatencyStatus :</span></span>

## <span data-ttu-id="87fe7-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="87fe7-117">EXAMPLES</span></span>

### <span data-ttu-id="87fe7-118">Beispiel 1: Erhalten eines Datasets</span><span class="sxs-lookup"><span data-stu-id="87fe7-118">Example 1: Get a dataset</span></span>
```
PS C:\>Get-AzDataFactoryRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z
Id                  : a7c4913c-9623-49b3-ae1e-3e45e2b68819
ResourceGroupName   : ADF
DataFactoryName     : WikiADF
DatasetName           : DAWikiAggregatedData
PipelineName        : 249ea141-ca00-8597-fad9-a148e5e7bdba
ActivityId          : fcefe2bd-39b1-2d7a-7b35-bcc2b0432300
ResumptionToken     : a7c4913c-9623-49b3-ae1e-3e45e2b68819
ContinuationToken   : 
ProcessingStartTime : 5/21/2014 5:02:41 PM
ProcessingEndTime   : 5/21/2014 5:04:12 PM
PercentComplete     : 100
DataSliceStart      : 5/21/2014 4:00:00 PM
DataSliceEnd        : 5/21/2014 5:00:00 PM
Status              : Succeeded
Timestamp           : 5/21/2014 5:02:41 PM
RetryAttempt        : 0
Properties          : {[errors, ]} 
ErrorMessage        :
```

<span data-ttu-id="87fe7-119">Dieser Befehl ruft alle Segmente des Datasets namens "DAWikiAggregatedData" in der Daten factory namens WikiADF ab 16:00 Uhr GMT am 21.05.2014 ab.</span><span class="sxs-lookup"><span data-stu-id="87fe7-119">This command gets all runs for slices of the dataset named DAWikiAggregatedData in the data factory named WikiADF that start from 4 PM GMT on 05/21/2014.</span></span>

## <span data-ttu-id="87fe7-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87fe7-120">PARAMETERS</span></span>

### <span data-ttu-id="87fe7-121">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="87fe7-121">-DataFactory</span></span>
<span data-ttu-id="87fe7-122">Gibt ein **"PSDataFactory"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="87fe7-122">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="87fe7-123">Dieses Cmdlet wird für Segmente ausgeführt, die zu der von diesem Parameter angegebenen Daten factory gehören.</span><span class="sxs-lookup"><span data-stu-id="87fe7-123">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="87fe7-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="87fe7-124">-DataFactoryName</span></span>
<span data-ttu-id="87fe7-125">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="87fe7-125">Specifies the name of a data factory.</span></span>
<span data-ttu-id="87fe7-126">Dieses Cmdlet wird für Segmente ausgeführt, die zu der von diesem Parameter angegebenen Daten factory gehören.</span><span class="sxs-lookup"><span data-stu-id="87fe7-126">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="87fe7-127">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="87fe7-127">-DatasetName</span></span>
<span data-ttu-id="87fe7-128">Gibt den Namen des Datasets an.</span><span class="sxs-lookup"><span data-stu-id="87fe7-128">Specifies the name of the dataset.</span></span>
<span data-ttu-id="87fe7-129">Dieses Cmdlet wird für Segmente ausgeführt, die zu dem von diesem Parameter angegebenen Dataset gehören.</span><span class="sxs-lookup"><span data-stu-id="87fe7-129">This cmdlet gets runs for slices that belong to the dataset that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87fe7-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87fe7-130">-DefaultProfile</span></span>
<span data-ttu-id="87fe7-131">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="87fe7-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87fe7-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87fe7-132">-ResourceGroupName</span></span>
<span data-ttu-id="87fe7-133">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="87fe7-133">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="87fe7-134">Dieses Cmdlet ruft Factoryläufe für Segmente ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="87fe7-134">This cmdlet gets factory runs for slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="87fe7-135">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="87fe7-135">-StartDateTime</span></span>
<span data-ttu-id="87fe7-136">Gibt den Anfang eines Zeitraums als **"DateTime"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="87fe7-136">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="87fe7-137">Dieses Cmdlet wird für die Datenschnitte ausgeführt, die diesem Zeitraum entsprechen.</span><span class="sxs-lookup"><span data-stu-id="87fe7-137">This cmdlet gets runs for the data slices that match this time period.</span></span>
<span data-ttu-id="87fe7-138">*StartDateTime* muss im ISO8601-Format angegeben werden, wie in den folgenden Beispielen: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) Der Standardentwurf für die Zeitzone ist UTC.</span><span class="sxs-lookup"><span data-stu-id="87fe7-138">*StartDateTime* must be specified in the ISO8601 format, as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87fe7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87fe7-139">CommonParameters</span></span>
<span data-ttu-id="87fe7-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87fe7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87fe7-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87fe7-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87fe7-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="87fe7-142">INPUTS</span></span>

### <span data-ttu-id="87fe7-143">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="87fe7-143">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="87fe7-144">System.String</span><span class="sxs-lookup"><span data-stu-id="87fe7-144">System.String</span></span>

## <span data-ttu-id="87fe7-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="87fe7-145">OUTPUTS</span></span>

### <span data-ttu-id="87fe7-146">Microsoft.Azure.Commands.DataFactories.Models.PSDataSverbinderRun</span><span class="sxs-lookup"><span data-stu-id="87fe7-146">Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun</span></span>

## <span data-ttu-id="87fe7-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="87fe7-147">NOTES</span></span>
* <span data-ttu-id="87fe7-148">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="87fe7-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="87fe7-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="87fe7-149">RELATED LINKS</span></span>

[<span data-ttu-id="87fe7-150">Get-AzDataFactorySfactory</span><span class="sxs-lookup"><span data-stu-id="87fe7-150">Get-AzDataFactorySlice</span></span>](./Get-AzDataFactorySlice.md)


