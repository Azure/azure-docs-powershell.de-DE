---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
ms.openlocfilehash: 8e1d189173c9825876018351ef36a2b73f285a24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478522"
---
# <span data-ttu-id="80ac1-101">Set-AzureRmDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="80ac1-101">Set-AzureRmDataFactorySliceStatus</span></span>

## <span data-ttu-id="80ac1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="80ac1-102">SYNOPSIS</span></span>
<span data-ttu-id="80ac1-103">Legt den Status von Segmenten für ein Dataset in Azure Data Factory fest.</span><span class="sxs-lookup"><span data-stu-id="80ac1-103">Sets the status of slices for a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80ac1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="80ac1-104">SYNTAX</span></span>

### <span data-ttu-id="80ac1-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="80ac1-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80ac1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="80ac1-106">ByFactoryObject</span></span>
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80ac1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80ac1-107">DESCRIPTION</span></span>
<span data-ttu-id="80ac1-108">Das Cmdlet " **Set-AzureRmDataFactorySliceStatus** " legt den Status von Segmenten für ein Dataset in Azure Data Factory fest.</span><span class="sxs-lookup"><span data-stu-id="80ac1-108">The **Set-AzureRmDataFactorySliceStatus** cmdlet sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="80ac1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="80ac1-109">EXAMPLES</span></span>

### <span data-ttu-id="80ac1-110">Beispiel 1: Einstellen des Status aller Segmente</span><span class="sxs-lookup"><span data-stu-id="80ac1-110">Example 1: Set the status of all slices</span></span>
```
PS C:\>Set-AzureRmDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

<span data-ttu-id="80ac1-111">Mit diesem Befehl wird der Status aller Segmente für das DataSet mit dem Namen DAWikiAggregatedData auf Waiting in der Data Factory mit dem Namen WikiADF festgelegt.</span><span class="sxs-lookup"><span data-stu-id="80ac1-111">This command sets the status of all slices for the dataset named DAWikiAggregatedData to Waiting in the data factory named WikiADF.</span></span>
<span data-ttu-id="80ac1-112">Der *UpdateType* -Parameter hat den Wert UpstreamInPipeline, und der Befehl legt den Status jedes Segments für das DataSet und alle abhängigen Datasets fest.</span><span class="sxs-lookup"><span data-stu-id="80ac1-112">The *UpdateType* parameter has a value of UpstreamInPipeline, and so the command sets the status of each slice for the dataset and all dependent datasets.</span></span>
<span data-ttu-id="80ac1-113">Abhängige Datasets werden als Eingabedatasets für Aktivitäten in der Pipeline verwendet.</span><span class="sxs-lookup"><span data-stu-id="80ac1-113">Dependent datasets are used as input datasets for activities in the pipeline.</span></span>
<span data-ttu-id="80ac1-114">Dieser Befehl gibt den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="80ac1-114">This command returns a value of $True.</span></span>

## <span data-ttu-id="80ac1-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="80ac1-115">PARAMETERS</span></span>

### <span data-ttu-id="80ac1-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="80ac1-116">-DataFactory</span></span>
<span data-ttu-id="80ac1-117">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="80ac1-117">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="80ac1-118">Dieses Cmdlet ändert den Status von Segmenten, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="80ac1-118">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="80ac1-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="80ac1-119">-DataFactoryName</span></span>
<span data-ttu-id="80ac1-120">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="80ac1-120">Specifies the name of a data factory.</span></span>
<span data-ttu-id="80ac1-121">Dieses Cmdlet ändert den Status von Segmenten, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="80ac1-121">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="80ac1-122">-DataSetName</span><span class="sxs-lookup"><span data-stu-id="80ac1-122">-DatasetName</span></span>
<span data-ttu-id="80ac1-123">Gibt den Namen des Datasets an, für das dieses Cmdlet Slices ändert.</span><span class="sxs-lookup"><span data-stu-id="80ac1-123">Specifies the name of the dataset for which this cmdlet modifies slices.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80ac1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80ac1-124">-DefaultProfile</span></span>
<span data-ttu-id="80ac1-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="80ac1-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80ac1-126">-Enddatum</span><span class="sxs-lookup"><span data-stu-id="80ac1-126">-EndDateTime</span></span>
<span data-ttu-id="80ac1-127">Gibt das Ende eines Zeitraums als **DateTime** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="80ac1-127">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="80ac1-128">Dieses Mal ist das Ende eines Datensegments.</span><span class="sxs-lookup"><span data-stu-id="80ac1-128">This time is the end of a data slice.</span></span>
<span data-ttu-id="80ac1-129">Wenn Sie weitere Informationen zu **DateTime** -Objekten wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="80ac1-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="80ac1-130">*Enddatum* muss im ISO8601-Format wie in den folgenden Beispielen angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="80ac1-130">*EndDateTime* must be specified in the ISO8601 format as in the following examples:</span></span> 

<span data-ttu-id="80ac1-131">2015-01-01z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (Pazifik-Standard Zeit)</span><span class="sxs-lookup"><span data-stu-id="80ac1-131">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time)</span></span>

<span data-ttu-id="80ac1-132">Der standardmäßige Zeitzonenbezeichner ist UTC.</span><span class="sxs-lookup"><span data-stu-id="80ac1-132">The default time zone designator is UTC.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ac1-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80ac1-133">-ResourceGroupName</span></span>
<span data-ttu-id="80ac1-134">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="80ac1-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="80ac1-135">Dieses Cmdlet ändert den Status von Segmenten, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="80ac1-135">This cmdlet modifies the status of slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="80ac1-136">-Startdatum</span><span class="sxs-lookup"><span data-stu-id="80ac1-136">-StartDateTime</span></span>
<span data-ttu-id="80ac1-137">Gibt den Anfang eines Zeitraums als **DateTime** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="80ac1-137">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="80ac1-138">Dieser Zeitpunkt ist der Anfang eines Datensegments.</span><span class="sxs-lookup"><span data-stu-id="80ac1-138">This time is the beginning of a data slice.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ac1-139">-Status</span><span class="sxs-lookup"><span data-stu-id="80ac1-139">-Status</span></span>
<span data-ttu-id="80ac1-140">Gibt einen Status an, der dem Datenslice zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="80ac1-140">Specifies a status to assign to the data slice.</span></span>
<span data-ttu-id="80ac1-141">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="80ac1-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="80ac1-142">Warten.</span><span class="sxs-lookup"><span data-stu-id="80ac1-142">Waiting.</span></span>
<span data-ttu-id="80ac1-143">Der Datenslice wartet vor der Verarbeitung auf die Validierung anhand von Validierungsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="80ac1-143">Data slice is waiting for validation against validation policies before being processed.</span></span> 
- <span data-ttu-id="80ac1-144">Bereit.</span><span class="sxs-lookup"><span data-stu-id="80ac1-144">Ready.</span></span>
<span data-ttu-id="80ac1-145">Die Datenverarbeitung ist abgeschlossen, und der Datenslice ist fertig.</span><span class="sxs-lookup"><span data-stu-id="80ac1-145">Data processing has completed and the data slice is ready.</span></span>
- <span data-ttu-id="80ac1-146">InProgress.</span><span class="sxs-lookup"><span data-stu-id="80ac1-146">InProgress.</span></span>
<span data-ttu-id="80ac1-147">Die Datenverarbeitung ist in Bearbeitung.</span><span class="sxs-lookup"><span data-stu-id="80ac1-147">Data processing is in-progress.</span></span> 
- <span data-ttu-id="80ac1-148">Fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="80ac1-148">Failed.</span></span>
<span data-ttu-id="80ac1-149">Fehler bei der Datenverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="80ac1-149">Data processing failed.</span></span>
- <span data-ttu-id="80ac1-150">Übersprungen.</span><span class="sxs-lookup"><span data-stu-id="80ac1-150">Skipped.</span></span>
<span data-ttu-id="80ac1-151">Die Verarbeitung des Datensegments wurde übersprungen.</span><span class="sxs-lookup"><span data-stu-id="80ac1-151">Skipped processing the data slice.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Failed, InProgress, Ready, Skipped, Waiting

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ac1-152">-UpdateType</span><span class="sxs-lookup"><span data-stu-id="80ac1-152">-UpdateType</span></span>
<span data-ttu-id="80ac1-153">Gibt den Typ des Updates für das Segment an.</span><span class="sxs-lookup"><span data-stu-id="80ac1-153">Specifies the type of update to the slice.</span></span>
<span data-ttu-id="80ac1-154">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="80ac1-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="80ac1-155">Einzelnen.</span><span class="sxs-lookup"><span data-stu-id="80ac1-155">Individual.</span></span>
<span data-ttu-id="80ac1-156">Legt den Status der einzelnen Segmente für das Dataset im angegebenen Zeitbereich fest.</span><span class="sxs-lookup"><span data-stu-id="80ac1-156">Sets the status of each slice for the dataset in the specified time range.</span></span> 
- <span data-ttu-id="80ac1-157">UpstreamInPipeline.</span><span class="sxs-lookup"><span data-stu-id="80ac1-157">UpstreamInPipeline.</span></span>
<span data-ttu-id="80ac1-158">Legt den Status jedes Segments für das DataSet und alle abhängigen Datasets fest, die als Eingabedatasets für Aktivitäten in der Pipeline verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="80ac1-158">Sets the status of each slice for the dataset and all the dependent datasets, which are used as input datasets for activities in the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Individual, UpstreamInPipeline

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ac1-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80ac1-159">CommonParameters</span></span>
<span data-ttu-id="80ac1-160">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80ac1-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80ac1-161">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80ac1-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80ac1-162">Eingaben</span><span class="sxs-lookup"><span data-stu-id="80ac1-162">INPUTS</span></span>

### <span data-ttu-id="80ac1-163">Keine</span><span class="sxs-lookup"><span data-stu-id="80ac1-163">None</span></span>
<span data-ttu-id="80ac1-164">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="80ac1-164">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="80ac1-165">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="80ac1-165">OUTPUTS</span></span>

### <span data-ttu-id="80ac1-166">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="80ac1-166">System.Boolean</span></span>

## <span data-ttu-id="80ac1-167">Notizen</span><span class="sxs-lookup"><span data-stu-id="80ac1-167">NOTES</span></span>
* <span data-ttu-id="80ac1-168">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="80ac1-168">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="80ac1-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="80ac1-169">RELATED LINKS</span></span>

[<span data-ttu-id="80ac1-170">Get-AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="80ac1-170">Get-AzureRmDataFactorySlice</span></span>](./Get-AzureRmDataFactorySlice.md)


