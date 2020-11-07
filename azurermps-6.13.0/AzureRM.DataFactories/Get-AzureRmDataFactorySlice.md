---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactorySlice.md
ms.openlocfilehash: 50942dfc9b31b96a796b0a77df8b1ffc1a4cbd36
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664871"
---
# <span data-ttu-id="60c7c-101">Get-AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="60c7c-101">Get-AzureRmDataFactorySlice</span></span>

## <span data-ttu-id="60c7c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="60c7c-102">SYNOPSIS</span></span>
<span data-ttu-id="60c7c-103">Ruft Datensegmente für ein Dataset in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="60c7c-103">Gets data slices for a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60c7c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="60c7c-104">SYNTAX</span></span>

### <span data-ttu-id="60c7c-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="60c7c-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="60c7c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="60c7c-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60c7c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60c7c-107">DESCRIPTION</span></span>
<span data-ttu-id="60c7c-108">Das Cmdlet " **Get-AzureRmDataFactorySlice** " ruft Datensegmente für ein Dataset in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="60c7c-108">The **Get-AzureRmDataFactorySlice** cmdlet gets data slices for a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="60c7c-109">Geben Sie eine Startzeit und eine Endzeit an, um einen Bereich von Datensegmenten zu definieren, die angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="60c7c-109">Specify a start time and an end time to define a range of data slices to view.</span></span>
<span data-ttu-id="60c7c-110">Der Status eines Datensegments entspricht einem der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="60c7c-110">The status of a data slice is one of the following values:</span></span> 
- <span data-ttu-id="60c7c-111">PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="60c7c-111">PendingExecution.</span></span>
<span data-ttu-id="60c7c-112">Die Datenverarbeitung wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="60c7c-112">Data processing has not started.</span></span> 
- <span data-ttu-id="60c7c-113">InProgress.</span><span class="sxs-lookup"><span data-stu-id="60c7c-113">InProgress.</span></span>
<span data-ttu-id="60c7c-114">Die Datenverarbeitung wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="60c7c-114">Data processing is in progress.</span></span> 
- <span data-ttu-id="60c7c-115">Bereit.</span><span class="sxs-lookup"><span data-stu-id="60c7c-115">Ready.</span></span>
<span data-ttu-id="60c7c-116">Die Datenverarbeitung ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="60c7c-116">Data processing is completed.</span></span>
<span data-ttu-id="60c7c-117">Der Datenslice ist für abhängige Slices bereit, um ihn zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="60c7c-117">The data slice is ready for dependent slices to consume it.</span></span> 
- <span data-ttu-id="60c7c-118">Fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="60c7c-118">Failed.</span></span>
<span data-ttu-id="60c7c-119">Fehler beim Ausführen des Segments.</span><span class="sxs-lookup"><span data-stu-id="60c7c-119">The run that produces the slice failed.</span></span> 
- <span data-ttu-id="60c7c-120">Skip.</span><span class="sxs-lookup"><span data-stu-id="60c7c-120">Skip.</span></span>
<span data-ttu-id="60c7c-121">Data Factory überspringt die Verarbeitung des Segments.</span><span class="sxs-lookup"><span data-stu-id="60c7c-121">Data Factory skips processing of the slice.</span></span> 
- <span data-ttu-id="60c7c-122">Wiederholen.</span><span class="sxs-lookup"><span data-stu-id="60c7c-122">Retry.</span></span>
<span data-ttu-id="60c7c-123">Data Factory versucht die Ausführung, die das Segment produziert, erneut.</span><span class="sxs-lookup"><span data-stu-id="60c7c-123">Data Factory retries the run that produces the slice.</span></span> 
- <span data-ttu-id="60c7c-124">Timeout. Die Datenverarbeitung hat ein Zeitlimit überschritten.</span><span class="sxs-lookup"><span data-stu-id="60c7c-124">Timed Out. Data processing has timed out.</span></span> 
- <span data-ttu-id="60c7c-125">PendingValidation.</span><span class="sxs-lookup"><span data-stu-id="60c7c-125">PendingValidation.</span></span>
<span data-ttu-id="60c7c-126">Datenslice wartet auf die Validierung, bevor Sie verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="60c7c-126">Data slice is waiting for validation before it is processed.</span></span> 
- <span data-ttu-id="60c7c-127">Überprüfung erneut versuchen.</span><span class="sxs-lookup"><span data-stu-id="60c7c-127">Retry Validation.</span></span>
<span data-ttu-id="60c7c-128">Data Factory versucht erneut, die Validierung des Segments zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="60c7c-128">Data Factory retries the validation of the slice.</span></span> 
- <span data-ttu-id="60c7c-129">Fehler bei der Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="60c7c-129">Failed Validation.</span></span>
<span data-ttu-id="60c7c-130">Fehler bei der Überprüfung des Segments.</span><span class="sxs-lookup"><span data-stu-id="60c7c-130">Validation of the slice failed.</span></span>
<span data-ttu-id="60c7c-131">Für jedes der Segmente können Sie mithilfe des Get-AzureRmDataFactoryRun-Cmdlets Weitere Informationen zur Ausführung des Segments anzeigen.</span><span class="sxs-lookup"><span data-stu-id="60c7c-131">For each of the slices, you can see more information about the run that produces the slice by using the Get-AzureRmDataFactoryRun cmdlet.</span></span>

## <span data-ttu-id="60c7c-132">Beispiele</span><span class="sxs-lookup"><span data-stu-id="60c7c-132">EXAMPLES</span></span>

### <span data-ttu-id="60c7c-133">Beispiel 1: Abrufen von Datensegmenten für ein DataSet</span><span class="sxs-lookup"><span data-stu-id="60c7c-133">Example 1: Get data slices for a dataset</span></span>
```
PS C:\>Get-AzureRmDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 1:00:00 AM
End               : 5/21/2014 2:00:00 AM
RetryCount        : 0
Status            : Ready

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 2:00:00 AM
End               : 5/21/2014 3:00:00 AM
RetryCount        : 0
Status            : Ready

. . . 

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 8:00:00 PM
End               : 5/21/2014 9:00:00 PM
RetryCount        : 0
Status            : PendingExecution

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 9:00:00 PM
End               : 5/21/2014 10:00:00 PM
RetryCount        : 0
Status            : PendingExecution

. . .
```

<span data-ttu-id="60c7c-134">Dieser Befehl ruft alle Datensegmente für das DataSet mit dem Namen WikiAggregatedData in der Data Factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="60c7c-134">This command gets all the data slices for the dataset named WikiAggregatedData in the data factory named WikiADF.</span></span>
<span data-ttu-id="60c7c-135">Der Befehl ruft die Segmente ab, die nach dem Zeitpunkt erstellt wurden, an dem der Parameter StartDate Time angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="60c7c-135">The command gets slices produced after the time that the StartDateTime parameter specifies.</span></span>
<span data-ttu-id="60c7c-136">Im folgenden Beispielcode wird die Verfügbarkeit für dieses DataSet stündlich in der JSON-Datei (JavaScript Object Notation) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="60c7c-136">The following example code sets the availability for this dataset every hour in the JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="60c7c-137">Verfügbarkeit: {period: "Hour", periodMultiplier: 1} einige Ergebnisse sind bereit, andere sind PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="60c7c-137">availability: { period: "Hour", periodMultiplier: 1 } Some of the results are Ready and others are PendingExecution.</span></span>
<span data-ttu-id="60c7c-138">Fertige Slices wurden bereits ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="60c7c-138">Ready slices have already run.</span></span>
<span data-ttu-id="60c7c-139">Die ausstehenden Segmente warten auf die Ausführung am Ende jeder Stunde in dem Intervall, das das Set-AzureRmDataFactoryPipelineActivePeriod-Cmdlet angibt.</span><span class="sxs-lookup"><span data-stu-id="60c7c-139">The pending slices are waiting to run at the end of each hour in the interval that the Set-AzureRmDataFactoryPipelineActivePeriod cmdlet specifies.</span></span>
<span data-ttu-id="60c7c-140">In diesem Beispiel haben Start-und endzeiträume für die Pipeline und das Segment einen Wert von einem Tag (24 Stunden).</span><span class="sxs-lookup"><span data-stu-id="60c7c-140">In this example, both start and end periods for the pipeline and the slice have a value of one day (24 hours).</span></span>

## <span data-ttu-id="60c7c-141">Parameter</span><span class="sxs-lookup"><span data-stu-id="60c7c-141">PARAMETERS</span></span>

### <span data-ttu-id="60c7c-142">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="60c7c-142">-DataFactory</span></span>
<span data-ttu-id="60c7c-143">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="60c7c-143">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="60c7c-144">Dieses Cmdlet ruft Segmente ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="60c7c-144">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="60c7c-145">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="60c7c-145">-DataFactoryName</span></span>
<span data-ttu-id="60c7c-146">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="60c7c-146">Specifies the name of a data factory.</span></span>
<span data-ttu-id="60c7c-147">Dieses Cmdlet ruft Segmente ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="60c7c-147">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="60c7c-148">-DataSetName</span><span class="sxs-lookup"><span data-stu-id="60c7c-148">-DatasetName</span></span>
<span data-ttu-id="60c7c-149">Gibt den Namen des Datasets an, für das dieses Cmdlet Slices erhält.</span><span class="sxs-lookup"><span data-stu-id="60c7c-149">Specifies the name of the dataset for which this cmdlet gets slices.</span></span>

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

### <span data-ttu-id="60c7c-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60c7c-150">-DefaultProfile</span></span>
<span data-ttu-id="60c7c-151">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="60c7c-151">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60c7c-152">-Enddatum</span><span class="sxs-lookup"><span data-stu-id="60c7c-152">-EndDateTime</span></span>
<span data-ttu-id="60c7c-153">Gibt das Ende eines Zeitraums als **DateTime** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="60c7c-153">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="60c7c-154">Dieses Cmdlet ruft Segmente ab, die vor dem von diesem Parameter festgelegten Zeitpunkt erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="60c7c-154">This cmdlet gets slices produced before the time that this parameter specifies.</span></span>
<span data-ttu-id="60c7c-155">Wenn Sie weitere Informationen zu **DateTime** -Objekten wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="60c7c-155">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="60c7c-156">*Enddatum* muss im ISO8601-Format angegeben werden, wie in den folgenden Beispielen: 2015-01-01z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (Pazifik-Standardzeit) der standardmäßige Zeitzonenbezeichner ist UTC.</span><span class="sxs-lookup"><span data-stu-id="60c7c-156">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="60c7c-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60c7c-157">-ResourceGroupName</span></span>
<span data-ttu-id="60c7c-158">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="60c7c-158">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="60c7c-159">Dieses Cmdlet ruft Segmente ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="60c7c-159">This cmdlet gets slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="60c7c-160">-Startdatum</span><span class="sxs-lookup"><span data-stu-id="60c7c-160">-StartDateTime</span></span>
<span data-ttu-id="60c7c-161">Gibt den Anfang eines Zeitraums als **DateTime** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="60c7c-161">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="60c7c-162">Dieses Cmdlet ruft Segmente ab, die nach dem von diesem Parameter festgelegten Zeitpunkt erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="60c7c-162">This cmdlet gets slices produced after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="60c7c-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60c7c-163">CommonParameters</span></span>
<span data-ttu-id="60c7c-164">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60c7c-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60c7c-165">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60c7c-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60c7c-166">Eingaben</span><span class="sxs-lookup"><span data-stu-id="60c7c-166">INPUTS</span></span>

### <span data-ttu-id="60c7c-167">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="60c7c-167">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="60c7c-168">System. String</span><span class="sxs-lookup"><span data-stu-id="60c7c-168">System.String</span></span>

## <span data-ttu-id="60c7c-169">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="60c7c-169">OUTPUTS</span></span>

### <span data-ttu-id="60c7c-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span><span class="sxs-lookup"><span data-stu-id="60c7c-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span></span>

## <span data-ttu-id="60c7c-171">Notizen</span><span class="sxs-lookup"><span data-stu-id="60c7c-171">NOTES</span></span>
* <span data-ttu-id="60c7c-172">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="60c7c-172">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="60c7c-173">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="60c7c-173">RELATED LINKS</span></span>

[<span data-ttu-id="60c7c-174">Satz-AzureRmDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="60c7c-174">Set-AzureRmDataFactorySliceStatus</span></span>](./Set-AzureRmDataFactorySliceStatus.md)

[<span data-ttu-id="60c7c-175">Get-AzureRmDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="60c7c-175">Get-AzureRmDataFactoryRun</span></span>](./Get-AzureRmDataFactoryRun.md)

[<span data-ttu-id="60c7c-176">Satz-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="60c7c-176">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)


