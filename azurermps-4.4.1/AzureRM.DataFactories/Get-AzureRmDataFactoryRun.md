---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 7100B5F0-A07B-4305-BF80-1F52647A03AB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryRun.md
ms.openlocfilehash: db3992a8df2cbd27c560827a702f9562e64ddcb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665086"
---
# <span data-ttu-id="4e30e-101">Get-AzureRmDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="4e30e-101">Get-AzureRmDataFactoryRun</span></span>

## <span data-ttu-id="4e30e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4e30e-102">SYNOPSIS</span></span>
<span data-ttu-id="4e30e-103">Ruft Runs für ein Datensegment eines Datasets in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="4e30e-103">Gets runs for a data slice of a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e30e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e30e-104">SYNTAX</span></span>

### <span data-ttu-id="4e30e-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="4e30e-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryRun [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e30e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4e30e-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryRun [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e30e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4e30e-107">DESCRIPTION</span></span>
<span data-ttu-id="4e30e-108">Das Cmdlet " **Get-AzureRmDataFactoryRun** " Ruft die Läufe für ein Datensegment eines Datasets in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="4e30e-108">The **Get-AzureRmDataFactoryRun** cmdlet gets the runs for a data slice of a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="4e30e-109">Ein Dataset in einer Data Factory besteht aus Segmenten auf der Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="4e30e-109">A dataset in a data factory is composed of slices over the time axis.</span></span>
<span data-ttu-id="4e30e-110">Die Breite eines Segments wird durch den Zeitplan entweder stündlich oder täglich bestimmt.</span><span class="sxs-lookup"><span data-stu-id="4e30e-110">The width of a slice is determined by the schedule, either hourly or daily.</span></span>
<span data-ttu-id="4e30e-111">Ein Run ist eine Verarbeitungseinheit für ein Segment.</span><span class="sxs-lookup"><span data-stu-id="4e30e-111">A run is a unit of processing for a slice.</span></span>
<span data-ttu-id="4e30e-112">Es kann eine oder mehrere Läufe für ein Segment im Fall von Wiederholungen geben, oder falls Sie Ihr Segment aufgrund von Fehlern erneut ausführen.</span><span class="sxs-lookup"><span data-stu-id="4e30e-112">There could be one or more runs for a slice in case of retries or in case you rerun your slice due to failures.</span></span>
<span data-ttu-id="4e30e-113">Ein Segment wird durch seine Startzeit identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4e30e-113">A slice is identified by its start time.</span></span>
<span data-ttu-id="4e30e-114">Wenn Sie die Startzeit eines Segments abrufen möchten, verwenden Sie das Cmdlet Get-AzureRmDataFactorySlice.</span><span class="sxs-lookup"><span data-stu-id="4e30e-114">To obtain the start time of a slice, use the Get-AzureRmDataFactorySlice cmdlet.</span></span>

<span data-ttu-id="4e30e-115">Wenn Sie beispielsweise einen Run für das folgende Segment erhalten möchten, verwenden Sie die Startzeit 2015-04-02T20:00:00.</span><span class="sxs-lookup"><span data-stu-id="4e30e-115">For example, to get a run for the following slice, use the start time 2015-04-02T20:00:00.</span></span>

<span data-ttu-id="4e30e-116">ResourceGroupName: ADF datafactoryname: SPDataFactory0924 DataSetName: MarketingCampaignEffectivenessBlobDataset Anfang: 5/2/2014 8:00:00 Uhr Ende: 5/3/2014 8:00:00 Uhr RetryCount: 0 Status: Ready LatencyStatus:</span><span class="sxs-lookup"><span data-stu-id="4e30e-116">ResourceGroupName  : ADF DataFactoryName : SPDataFactory0924 DatasetName : MarketingCampaignEffectivenessBlobDataset Start : 5/2/2014 8:00:00 PM End : 5/3/2014 8:00:00 PM RetryCount : 0 Status : Ready LatencyStatus :</span></span>

## <span data-ttu-id="4e30e-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4e30e-117">EXAMPLES</span></span>

### <span data-ttu-id="4e30e-118">Beispiel 1: Abrufen eines Datasets</span><span class="sxs-lookup"><span data-stu-id="4e30e-118">Example 1: Get a dataset</span></span>
```
PS C:\>Get-AzureRmDataFactoryRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z
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

<span data-ttu-id="4e30e-119">Dieser Befehl ruft alle Läufe für Segmente des Datasets mit dem Namen DAWikiAggregatedData in der Data Factory mit dem Namen WikiADF ab, die ab 16.00 Uhr GMT auf 05/21/2014 beginnen.</span><span class="sxs-lookup"><span data-stu-id="4e30e-119">This command gets all runs for slices of the dataset named DAWikiAggregatedData in the data factory named WikiADF that start from 4 PM GMT on 05/21/2014.</span></span>

## <span data-ttu-id="4e30e-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e30e-120">PARAMETERS</span></span>

### <span data-ttu-id="4e30e-121">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="4e30e-121">-DataFactory</span></span>
<span data-ttu-id="4e30e-122">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="4e30e-122">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="4e30e-123">Dieses Cmdlet ruft Läufe für Segmente ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="4e30e-123">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4e30e-124">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="4e30e-124">-DataFactoryName</span></span>
<span data-ttu-id="4e30e-125">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="4e30e-125">Specifies the name of a data factory.</span></span>
<span data-ttu-id="4e30e-126">Dieses Cmdlet ruft Läufe für Segmente ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="4e30e-126">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4e30e-127">-DataSetName</span><span class="sxs-lookup"><span data-stu-id="4e30e-127">-DatasetName</span></span>
<span data-ttu-id="4e30e-128">Gibt den Namen des Datasets an.</span><span class="sxs-lookup"><span data-stu-id="4e30e-128">Specifies the name of the dataset.</span></span>
<span data-ttu-id="4e30e-129">Dieses Cmdlet ruft Läufe für Segmente ab, die zu dem DataSet gehören, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="4e30e-129">This cmdlet gets runs for slices that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="4e30e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e30e-130">-ResourceGroupName</span></span>
<span data-ttu-id="4e30e-131">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4e30e-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4e30e-132">Dieses Cmdlet ruft Factory-Läufe für Segmente ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="4e30e-132">This cmdlet gets factory runs for slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4e30e-133">-Startdatum</span><span class="sxs-lookup"><span data-stu-id="4e30e-133">-StartDateTime</span></span>
<span data-ttu-id="4e30e-134">Gibt den Anfang eines Zeitraums als **DateTime** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="4e30e-134">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="4e30e-135">Dieses Cmdlet ruft Läufe für die Datensegmente ab, die diesem Zeitraum entsprechen.</span><span class="sxs-lookup"><span data-stu-id="4e30e-135">This cmdlet gets runs for the data slices that match this time period.</span></span>

<span data-ttu-id="4e30e-136">Start *Datum* muss im ISO8601-Format angegeben werden, wie in den folgenden Beispielen:</span><span class="sxs-lookup"><span data-stu-id="4e30e-136">*StartDateTime* must be specified in the ISO8601 format, as in the following examples:</span></span> 

<span data-ttu-id="4e30e-137">2015-01-01z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (Pazifik-Standard Zeit)</span><span class="sxs-lookup"><span data-stu-id="4e30e-137">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time)</span></span>

<span data-ttu-id="4e30e-138">Der standardmäßige Zeitzonenbezeichner ist UTC.</span><span class="sxs-lookup"><span data-stu-id="4e30e-138">The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="4e30e-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e30e-139">-DefaultProfile</span></span>
<span data-ttu-id="4e30e-140">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4e30e-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e30e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e30e-141">CommonParameters</span></span>
<span data-ttu-id="4e30e-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e30e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e30e-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e30e-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e30e-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4e30e-144">INPUTS</span></span>

## <span data-ttu-id="4e30e-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4e30e-145">OUTPUTS</span></span>

### <span data-ttu-id="4e30e-146">System. Collections. Generic. List ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataSliceRun, Microsoft. WindowsAzure. Commands. Utilities, Version = 0.8.2.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="4e30e-146">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataSliceRun, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="4e30e-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="4e30e-147">NOTES</span></span>
* <span data-ttu-id="4e30e-148">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="4e30e-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4e30e-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4e30e-149">RELATED LINKS</span></span>

[<span data-ttu-id="4e30e-150">Get-AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="4e30e-150">Get-AzureRmDataFactorySlice</span></span>](./Get-AzureRmDataFactorySlice.md)


