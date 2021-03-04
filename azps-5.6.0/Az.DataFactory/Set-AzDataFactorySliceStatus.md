---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
ms.openlocfilehash: 80a471b88856ff4c7425e89fd6e5b73168370789
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942880"
---
# <span data-ttu-id="6f796-101">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="6f796-101">Set-AzDataFactorySliceStatus</span></span>

## <span data-ttu-id="6f796-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f796-102">SYNOPSIS</span></span>
<span data-ttu-id="6f796-103">Legt den Status von Datenschnitten für ein Dataset in Azure Data Factory fest.</span><span class="sxs-lookup"><span data-stu-id="6f796-103">Sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="6f796-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6f796-104">SYNTAX</span></span>

### <span data-ttu-id="6f796-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="6f796-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f796-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6f796-106">ByFactoryObject</span></span>
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f796-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6f796-107">DESCRIPTION</span></span>
<span data-ttu-id="6f796-108">Das **Cmdlet Set-AzDataFactorySliceStatus** legt den Status von Segmenten für ein Dataset in Azure Data Factory fest.</span><span class="sxs-lookup"><span data-stu-id="6f796-108">The **Set-AzDataFactorySliceStatus** cmdlet sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="6f796-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6f796-109">EXAMPLES</span></span>

### <span data-ttu-id="6f796-110">Beispiel 1: Festlegen des Status aller Segmente</span><span class="sxs-lookup"><span data-stu-id="6f796-110">Example 1: Set the status of all slices</span></span>
```
PS C:\>Set-AzDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

<span data-ttu-id="6f796-111">Mit diesem Befehl wird der Status aller Datenschnitte für das Dataset mit dem Namen DAWikiAggregatedData auf Warten in der Daten factory mit dem Namen WikiADF fest.</span><span class="sxs-lookup"><span data-stu-id="6f796-111">This command sets the status of all slices for the dataset named DAWikiAggregatedData to Waiting in the data factory named WikiADF.</span></span>
<span data-ttu-id="6f796-112">Der *Parameter UpdateType* hat den Wert UpstreamInPipeline, und daher legt der Befehl den Status der einzelnen Datenschnitte für das Dataset und alle abhängigen Datasets fest.</span><span class="sxs-lookup"><span data-stu-id="6f796-112">The *UpdateType* parameter has a value of UpstreamInPipeline, and so the command sets the status of each slice for the dataset and all dependent datasets.</span></span>
<span data-ttu-id="6f796-113">Abhängige Datasets werden als Eingabedatensets für Aktivitäten in der Pipeline verwendet.</span><span class="sxs-lookup"><span data-stu-id="6f796-113">Dependent datasets are used as input datasets for activities in the pipeline.</span></span>
<span data-ttu-id="6f796-114">Dieser Befehl gibt einen Wert von $True.</span><span class="sxs-lookup"><span data-stu-id="6f796-114">This command returns a value of $True.</span></span>

## <span data-ttu-id="6f796-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6f796-115">PARAMETERS</span></span>

### <span data-ttu-id="6f796-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="6f796-116">-DataFactory</span></span>
<span data-ttu-id="6f796-117">Gibt ein **PSDataFactory-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="6f796-117">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="6f796-118">Dieses Cmdlet ändert den Status von Segmenten, die zur Daten factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="6f796-118">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6f796-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6f796-119">-DataFactoryName</span></span>
<span data-ttu-id="6f796-120">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="6f796-120">Specifies the name of a data factory.</span></span>
<span data-ttu-id="6f796-121">Dieses Cmdlet ändert den Status von Segmenten, die zur Daten factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="6f796-121">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6f796-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="6f796-122">-DatasetName</span></span>
<span data-ttu-id="6f796-123">Gibt den Namen des Datasets an, für das dieses Cmdlet Segmente ändert.</span><span class="sxs-lookup"><span data-stu-id="6f796-123">Specifies the name of the dataset for which this cmdlet modifies slices.</span></span>

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

### <span data-ttu-id="6f796-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f796-124">-DefaultProfile</span></span>
<span data-ttu-id="6f796-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6f796-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f796-126">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="6f796-126">-EndDateTime</span></span>
<span data-ttu-id="6f796-127">Gibt das Ende eines Zeitraums als **DateTime-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="6f796-127">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="6f796-128">Dieses Mal ist das Ende eines Datenschnitts.</span><span class="sxs-lookup"><span data-stu-id="6f796-128">This time is the end of a data slice.</span></span>
<span data-ttu-id="6f796-129">Weitere Informationen zu **DateTime-Objekten** finden Sie unter `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="6f796-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="6f796-130">*EndDateTime* muss wie in den folgenden Beispielen im ISO8601-Format angegeben werden: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) Der Standardmäßige Zeitzonenentwurfer ist UTC.</span><span class="sxs-lookup"><span data-stu-id="6f796-130">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="6f796-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f796-131">-ResourceGroupName</span></span>
<span data-ttu-id="6f796-132">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="6f796-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="6f796-133">Dieses Cmdlet ändert den Status von Segmenten, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="6f796-133">This cmdlet modifies the status of slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6f796-134">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="6f796-134">-StartDateTime</span></span>
<span data-ttu-id="6f796-135">Gibt den Anfang eines Zeitraums als **DateTime-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="6f796-135">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="6f796-136">Dieses Mal ist der Anfang eines Datenschnitts.</span><span class="sxs-lookup"><span data-stu-id="6f796-136">This time is the beginning of a data slice.</span></span>

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

### <span data-ttu-id="6f796-137">-Status</span><span class="sxs-lookup"><span data-stu-id="6f796-137">-Status</span></span>
<span data-ttu-id="6f796-138">Gibt einen Status an, der dem Datenschnitt zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6f796-138">Specifies a status to assign to the data slice.</span></span>
<span data-ttu-id="6f796-139">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="6f796-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6f796-140">Warten.</span><span class="sxs-lookup"><span data-stu-id="6f796-140">Waiting.</span></span>
<span data-ttu-id="6f796-141">Das Datendatenschnitt wartet auf die Überprüfung der Gültigkeitsprüfungsrichtlinien, bevor es verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="6f796-141">Data slice is waiting for validation against validation policies before being processed.</span></span> 
- <span data-ttu-id="6f796-142">Fertig.</span><span class="sxs-lookup"><span data-stu-id="6f796-142">Ready.</span></span>
<span data-ttu-id="6f796-143">Die Datenverarbeitung ist abgeschlossen, und das Datendatenschnitt ist bereit.</span><span class="sxs-lookup"><span data-stu-id="6f796-143">Data processing has completed and the data slice is ready.</span></span>
- <span data-ttu-id="6f796-144">InProgress.</span><span class="sxs-lookup"><span data-stu-id="6f796-144">InProgress.</span></span>
<span data-ttu-id="6f796-145">Die Datenverarbeitung wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6f796-145">Data processing is in-progress.</span></span> 
- <span data-ttu-id="6f796-146">Fehler.</span><span class="sxs-lookup"><span data-stu-id="6f796-146">Failed.</span></span>
<span data-ttu-id="6f796-147">Fehler bei der Datenverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="6f796-147">Data processing failed.</span></span>
- <span data-ttu-id="6f796-148">Übersprungen.</span><span class="sxs-lookup"><span data-stu-id="6f796-148">Skipped.</span></span>
<span data-ttu-id="6f796-149">Die Verarbeitung des Datenschnitts wurde übersprungen.</span><span class="sxs-lookup"><span data-stu-id="6f796-149">Skipped processing the data slice.</span></span>

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

### <span data-ttu-id="6f796-150">-UpdateType</span><span class="sxs-lookup"><span data-stu-id="6f796-150">-UpdateType</span></span>
<span data-ttu-id="6f796-151">Gibt den Aktualisierungstyp für das Segment an.</span><span class="sxs-lookup"><span data-stu-id="6f796-151">Specifies the type of update to the slice.</span></span>
<span data-ttu-id="6f796-152">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="6f796-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6f796-153">Individuell.</span><span class="sxs-lookup"><span data-stu-id="6f796-153">Individual.</span></span>
<span data-ttu-id="6f796-154">Legt den Status der einzelnen Datenschnitte für das Dataset im angegebenen Zeitraum fest.</span><span class="sxs-lookup"><span data-stu-id="6f796-154">Sets the status of each slice for the dataset in the specified time range.</span></span> 
- <span data-ttu-id="6f796-155">UpstreamInPipeline.</span><span class="sxs-lookup"><span data-stu-id="6f796-155">UpstreamInPipeline.</span></span>
<span data-ttu-id="6f796-156">Legt den Status der einzelnen Datenschnitte für das Dataset und aller abhängigen Datasets fest, die als Eingabesets für Aktivitäten in der Pipeline verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6f796-156">Sets the status of each slice for the dataset and all the dependent datasets, which are used as input datasets for activities in the pipeline.</span></span>

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

### <span data-ttu-id="6f796-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f796-157">CommonParameters</span></span>
<span data-ttu-id="6f796-158">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f796-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f796-159">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f796-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f796-160">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6f796-160">INPUTS</span></span>

### <span data-ttu-id="6f796-161">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="6f796-161">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="6f796-162">System.String</span><span class="sxs-lookup"><span data-stu-id="6f796-162">System.String</span></span>

## <span data-ttu-id="6f796-163">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6f796-163">OUTPUTS</span></span>

### <span data-ttu-id="6f796-164">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6f796-164">System.Boolean</span></span>

## <span data-ttu-id="6f796-165">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6f796-165">NOTES</span></span>
* <span data-ttu-id="6f796-166">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factory</span><span class="sxs-lookup"><span data-stu-id="6f796-166">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="6f796-167">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6f796-167">RELATED LINKS</span></span>

[<span data-ttu-id="6f796-168">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="6f796-168">Get-AzDataFactorySlice</span></span>](./Get-AzDataFactorySlice.md)


