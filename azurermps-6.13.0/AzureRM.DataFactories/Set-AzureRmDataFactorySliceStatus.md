---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
ms.openlocfilehash: ce1d81fc0226c7c44682d67cb666e3e63dfd5816
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496277"
---
# <span data-ttu-id="ea715-101">Set-AzureRmDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="ea715-101">Set-AzureRmDataFactorySliceStatus</span></span>

## <span data-ttu-id="ea715-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ea715-102">SYNOPSIS</span></span>
<span data-ttu-id="ea715-103">Legt den Status von Segmenten für ein Dataset in Azure Data Factory fest.</span><span class="sxs-lookup"><span data-stu-id="ea715-103">Sets the status of slices for a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea715-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea715-104">SYNTAX</span></span>

### <span data-ttu-id="ea715-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ea715-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea715-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ea715-106">ByFactoryObject</span></span>
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea715-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ea715-107">DESCRIPTION</span></span>
<span data-ttu-id="ea715-108">Das Cmdlet " **Set-AzureRmDataFactorySliceStatus** " legt den Status von Segmenten für ein Dataset in Azure Data Factory fest.</span><span class="sxs-lookup"><span data-stu-id="ea715-108">The **Set-AzureRmDataFactorySliceStatus** cmdlet sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="ea715-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ea715-109">EXAMPLES</span></span>

### <span data-ttu-id="ea715-110">Beispiel 1: Einstellen des Status aller Segmente</span><span class="sxs-lookup"><span data-stu-id="ea715-110">Example 1: Set the status of all slices</span></span>
```
PS C:\>Set-AzureRmDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

<span data-ttu-id="ea715-111">Mit diesem Befehl wird der Status aller Segmente für das DataSet mit dem Namen DAWikiAggregatedData auf Waiting in der Data Factory mit dem Namen WikiADF festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ea715-111">This command sets the status of all slices for the dataset named DAWikiAggregatedData to Waiting in the data factory named WikiADF.</span></span>
<span data-ttu-id="ea715-112">Der *UpdateType* -Parameter hat den Wert UpstreamInPipeline, und der Befehl legt den Status jedes Segments für das DataSet und alle abhängigen Datasets fest.</span><span class="sxs-lookup"><span data-stu-id="ea715-112">The *UpdateType* parameter has a value of UpstreamInPipeline, and so the command sets the status of each slice for the dataset and all dependent datasets.</span></span>
<span data-ttu-id="ea715-113">Abhängige Datasets werden als Eingabedatasets für Aktivitäten in der Pipeline verwendet.</span><span class="sxs-lookup"><span data-stu-id="ea715-113">Dependent datasets are used as input datasets for activities in the pipeline.</span></span>
<span data-ttu-id="ea715-114">Dieser Befehl gibt den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="ea715-114">This command returns a value of $True.</span></span>

## <span data-ttu-id="ea715-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea715-115">PARAMETERS</span></span>

### <span data-ttu-id="ea715-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ea715-116">-DataFactory</span></span>
<span data-ttu-id="ea715-117">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="ea715-117">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="ea715-118">Dieses Cmdlet ändert den Status von Segmenten, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ea715-118">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ea715-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="ea715-119">-DataFactoryName</span></span>
<span data-ttu-id="ea715-120">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="ea715-120">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ea715-121">Dieses Cmdlet ändert den Status von Segmenten, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ea715-121">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ea715-122">-DataSetName</span><span class="sxs-lookup"><span data-stu-id="ea715-122">-DatasetName</span></span>
<span data-ttu-id="ea715-123">Gibt den Namen des Datasets an, für das dieses Cmdlet Slices ändert.</span><span class="sxs-lookup"><span data-stu-id="ea715-123">Specifies the name of the dataset for which this cmdlet modifies slices.</span></span>

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

### <span data-ttu-id="ea715-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea715-124">-DefaultProfile</span></span>
<span data-ttu-id="ea715-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ea715-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea715-126">-Enddatum</span><span class="sxs-lookup"><span data-stu-id="ea715-126">-EndDateTime</span></span>
<span data-ttu-id="ea715-127">Gibt das Ende eines Zeitraums als **DateTime** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="ea715-127">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="ea715-128">Dieses Mal ist das Ende eines Datensegments.</span><span class="sxs-lookup"><span data-stu-id="ea715-128">This time is the end of a data slice.</span></span>
<span data-ttu-id="ea715-129">Wenn Sie weitere Informationen zu **DateTime** -Objekten wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="ea715-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="ea715-130">*Enddatum* muss im ISO8601-Format angegeben werden, wie in den folgenden Beispielen: 2015-01-01z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (Pazifik-Standardzeit) der standardmäßige Zeitzonenbezeichner ist UTC.</span><span class="sxs-lookup"><span data-stu-id="ea715-130">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea715-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea715-131">-ResourceGroupName</span></span>
<span data-ttu-id="ea715-132">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ea715-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ea715-133">Dieses Cmdlet ändert den Status von Segmenten, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ea715-133">This cmdlet modifies the status of slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ea715-134">-Startdatum</span><span class="sxs-lookup"><span data-stu-id="ea715-134">-StartDateTime</span></span>
<span data-ttu-id="ea715-135">Gibt den Anfang eines Zeitraums als **DateTime** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="ea715-135">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="ea715-136">Dieser Zeitpunkt ist der Anfang eines Datensegments.</span><span class="sxs-lookup"><span data-stu-id="ea715-136">This time is the beginning of a data slice.</span></span>

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

### <span data-ttu-id="ea715-137">-Status</span><span class="sxs-lookup"><span data-stu-id="ea715-137">-Status</span></span>
<span data-ttu-id="ea715-138">Gibt einen Status an, der dem Datenslice zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ea715-138">Specifies a status to assign to the data slice.</span></span>
<span data-ttu-id="ea715-139">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ea715-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ea715-140">Warten.</span><span class="sxs-lookup"><span data-stu-id="ea715-140">Waiting.</span></span>
<span data-ttu-id="ea715-141">Der Datenslice wartet vor der Verarbeitung auf die Validierung anhand von Validierungsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="ea715-141">Data slice is waiting for validation against validation policies before being processed.</span></span> 
- <span data-ttu-id="ea715-142">Bereit.</span><span class="sxs-lookup"><span data-stu-id="ea715-142">Ready.</span></span>
<span data-ttu-id="ea715-143">Die Datenverarbeitung ist abgeschlossen, und der Datenslice ist fertig.</span><span class="sxs-lookup"><span data-stu-id="ea715-143">Data processing has completed and the data slice is ready.</span></span>
- <span data-ttu-id="ea715-144">InProgress.</span><span class="sxs-lookup"><span data-stu-id="ea715-144">InProgress.</span></span>
<span data-ttu-id="ea715-145">Die Datenverarbeitung ist in Bearbeitung.</span><span class="sxs-lookup"><span data-stu-id="ea715-145">Data processing is in-progress.</span></span> 
- <span data-ttu-id="ea715-146">Fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="ea715-146">Failed.</span></span>
<span data-ttu-id="ea715-147">Fehler bei der Datenverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="ea715-147">Data processing failed.</span></span>
- <span data-ttu-id="ea715-148">Übersprungen.</span><span class="sxs-lookup"><span data-stu-id="ea715-148">Skipped.</span></span>
<span data-ttu-id="ea715-149">Die Verarbeitung des Datensegments wurde übersprungen.</span><span class="sxs-lookup"><span data-stu-id="ea715-149">Skipped processing the data slice.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Failed, InProgress, Ready, Skipped, Waiting

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea715-150">-UpdateType</span><span class="sxs-lookup"><span data-stu-id="ea715-150">-UpdateType</span></span>
<span data-ttu-id="ea715-151">Gibt den Typ des Updates für das Segment an.</span><span class="sxs-lookup"><span data-stu-id="ea715-151">Specifies the type of update to the slice.</span></span>
<span data-ttu-id="ea715-152">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ea715-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ea715-153">Einzelnen.</span><span class="sxs-lookup"><span data-stu-id="ea715-153">Individual.</span></span>
<span data-ttu-id="ea715-154">Legt den Status der einzelnen Segmente für das Dataset im angegebenen Zeitbereich fest.</span><span class="sxs-lookup"><span data-stu-id="ea715-154">Sets the status of each slice for the dataset in the specified time range.</span></span> 
- <span data-ttu-id="ea715-155">UpstreamInPipeline.</span><span class="sxs-lookup"><span data-stu-id="ea715-155">UpstreamInPipeline.</span></span>
<span data-ttu-id="ea715-156">Legt den Status jedes Segments für das DataSet und alle abhängigen Datasets fest, die als Eingabedatasets für Aktivitäten in der Pipeline verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea715-156">Sets the status of each slice for the dataset and all the dependent datasets, which are used as input datasets for activities in the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Individual, UpstreamInPipeline

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea715-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea715-157">CommonParameters</span></span>
<span data-ttu-id="ea715-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea715-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea715-159">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea715-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea715-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ea715-160">INPUTS</span></span>

### <span data-ttu-id="ea715-161">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ea715-161">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="ea715-162">System. String</span><span class="sxs-lookup"><span data-stu-id="ea715-162">System.String</span></span>

## <span data-ttu-id="ea715-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ea715-163">OUTPUTS</span></span>

### <span data-ttu-id="ea715-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ea715-164">System.Boolean</span></span>

## <span data-ttu-id="ea715-165">Notizen</span><span class="sxs-lookup"><span data-stu-id="ea715-165">NOTES</span></span>
* <span data-ttu-id="ea715-166">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="ea715-166">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ea715-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ea715-167">RELATED LINKS</span></span>

[<span data-ttu-id="ea715-168">Get-AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="ea715-168">Get-AzureRmDataFactorySlice</span></span>](./Get-AzureRmDataFactorySlice.md)


