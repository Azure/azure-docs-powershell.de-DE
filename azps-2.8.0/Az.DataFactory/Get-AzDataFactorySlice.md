---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
ms.openlocfilehash: a4f83bf560af1643d2971ed7644089cee26759c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651774"
---
# <span data-ttu-id="a77b5-101">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="a77b5-101">Get-AzDataFactorySlice</span></span>

## <span data-ttu-id="a77b5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a77b5-102">SYNOPSIS</span></span>
<span data-ttu-id="a77b5-103">Ruft Datensegmente für ein Dataset in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="a77b5-103">Gets data slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="a77b5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a77b5-104">SYNTAX</span></span>

### <span data-ttu-id="a77b5-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a77b5-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a77b5-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a77b5-106">ByFactoryObject</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a77b5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a77b5-107">DESCRIPTION</span></span>
<span data-ttu-id="a77b5-108">Das Cmdlet " **Get-AzDataFactorySlice** " ruft Datensegmente für ein Dataset in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="a77b5-108">The **Get-AzDataFactorySlice** cmdlet gets data slices for a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="a77b5-109">Geben Sie eine Startzeit und eine Endzeit an, um einen Bereich von Datensegmenten zu definieren, die angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a77b5-109">Specify a start time and an end time to define a range of data slices to view.</span></span>
<span data-ttu-id="a77b5-110">Der Status eines Datensegments entspricht einem der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="a77b5-110">The status of a data slice is one of the following values:</span></span> 
- <span data-ttu-id="a77b5-111">PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="a77b5-111">PendingExecution.</span></span>
<span data-ttu-id="a77b5-112">Die Datenverarbeitung wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="a77b5-112">Data processing has not started.</span></span> 
- <span data-ttu-id="a77b5-113">InProgress.</span><span class="sxs-lookup"><span data-stu-id="a77b5-113">InProgress.</span></span>
<span data-ttu-id="a77b5-114">Die Datenverarbeitung wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a77b5-114">Data processing is in progress.</span></span> 
- <span data-ttu-id="a77b5-115">Bereit.</span><span class="sxs-lookup"><span data-stu-id="a77b5-115">Ready.</span></span>
<span data-ttu-id="a77b5-116">Die Datenverarbeitung ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="a77b5-116">Data processing is completed.</span></span>
<span data-ttu-id="a77b5-117">Der Datenslice ist für abhängige Slices bereit, um ihn zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a77b5-117">The data slice is ready for dependent slices to consume it.</span></span> 
- <span data-ttu-id="a77b5-118">Fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="a77b5-118">Failed.</span></span>
<span data-ttu-id="a77b5-119">Fehler beim Ausführen des Segments.</span><span class="sxs-lookup"><span data-stu-id="a77b5-119">The run that produces the slice failed.</span></span> 
- <span data-ttu-id="a77b5-120">Skip.</span><span class="sxs-lookup"><span data-stu-id="a77b5-120">Skip.</span></span>
<span data-ttu-id="a77b5-121">Data Factory überspringt die Verarbeitung des Segments.</span><span class="sxs-lookup"><span data-stu-id="a77b5-121">Data Factory skips processing of the slice.</span></span> 
- <span data-ttu-id="a77b5-122">Wiederholen.</span><span class="sxs-lookup"><span data-stu-id="a77b5-122">Retry.</span></span>
<span data-ttu-id="a77b5-123">Data Factory versucht die Ausführung, die das Segment produziert, erneut.</span><span class="sxs-lookup"><span data-stu-id="a77b5-123">Data Factory retries the run that produces the slice.</span></span> 
- <span data-ttu-id="a77b5-124">Timeout. Die Datenverarbeitung hat ein Zeitlimit überschritten.</span><span class="sxs-lookup"><span data-stu-id="a77b5-124">Timed Out. Data processing has timed out.</span></span> 
- <span data-ttu-id="a77b5-125">PendingValidation.</span><span class="sxs-lookup"><span data-stu-id="a77b5-125">PendingValidation.</span></span>
<span data-ttu-id="a77b5-126">Datenslice wartet auf die Validierung, bevor Sie verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="a77b5-126">Data slice is waiting for validation before it is processed.</span></span> 
- <span data-ttu-id="a77b5-127">Überprüfung erneut versuchen.</span><span class="sxs-lookup"><span data-stu-id="a77b5-127">Retry Validation.</span></span>
<span data-ttu-id="a77b5-128">Data Factory versucht erneut, die Validierung des Segments zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a77b5-128">Data Factory retries the validation of the slice.</span></span> 
- <span data-ttu-id="a77b5-129">Fehler bei der Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="a77b5-129">Failed Validation.</span></span>
<span data-ttu-id="a77b5-130">Fehler bei der Überprüfung des Segments.</span><span class="sxs-lookup"><span data-stu-id="a77b5-130">Validation of the slice failed.</span></span>
<span data-ttu-id="a77b5-131">Für jedes der Segmente können Sie mithilfe des Get-AzDataFactoryRun-Cmdlets Weitere Informationen zur Ausführung des Segments anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a77b5-131">For each of the slices, you can see more information about the run that produces the slice by using the Get-AzDataFactoryRun cmdlet.</span></span>

## <span data-ttu-id="a77b5-132">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a77b5-132">EXAMPLES</span></span>

### <span data-ttu-id="a77b5-133">Beispiel 1: Abrufen von Datensegmenten für ein DataSet</span><span class="sxs-lookup"><span data-stu-id="a77b5-133">Example 1: Get data slices for a dataset</span></span>
```
PS C:\>Get-AzDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
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

<span data-ttu-id="a77b5-134">Dieser Befehl ruft alle Datensegmente für das DataSet mit dem Namen WikiAggregatedData in der Data Factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="a77b5-134">This command gets all the data slices for the dataset named WikiAggregatedData in the data factory named WikiADF.</span></span>
<span data-ttu-id="a77b5-135">Der Befehl ruft die Segmente ab, die nach dem Zeitpunkt erstellt wurden, an dem der Parameter StartDate Time angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="a77b5-135">The command gets slices produced after the time that the StartDateTime parameter specifies.</span></span>
<span data-ttu-id="a77b5-136">Im folgenden Beispielcode wird die Verfügbarkeit für dieses DataSet stündlich in der JSON-Datei (JavaScript Object Notation) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a77b5-136">The following example code sets the availability for this dataset every hour in the JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="a77b5-137">Verfügbarkeit: {period: "Hour", periodMultiplier: 1} einige Ergebnisse sind bereit, andere sind PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="a77b5-137">availability: { period: "Hour", periodMultiplier: 1 } Some of the results are Ready and others are PendingExecution.</span></span>
<span data-ttu-id="a77b5-138">Fertige Slices wurden bereits ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a77b5-138">Ready slices have already run.</span></span>
<span data-ttu-id="a77b5-139">Die ausstehenden Segmente warten auf die Ausführung am Ende jeder Stunde in dem Intervall, das das Set-AzDataFactoryPipelineActivePeriod-Cmdlet angibt.</span><span class="sxs-lookup"><span data-stu-id="a77b5-139">The pending slices are waiting to run at the end of each hour in the interval that the Set-AzDataFactoryPipelineActivePeriod cmdlet specifies.</span></span>
<span data-ttu-id="a77b5-140">In diesem Beispiel haben Start-und endzeiträume für die Pipeline und das Segment einen Wert von einem Tag (24 Stunden).</span><span class="sxs-lookup"><span data-stu-id="a77b5-140">In this example, both start and end periods for the pipeline and the slice have a value of one day (24 hours).</span></span>

## <span data-ttu-id="a77b5-141">Parameter</span><span class="sxs-lookup"><span data-stu-id="a77b5-141">PARAMETERS</span></span>

### <span data-ttu-id="a77b5-142">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a77b5-142">-DataFactory</span></span>
<span data-ttu-id="a77b5-143">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a77b5-143">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="a77b5-144">Dieses Cmdlet ruft Segmente ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a77b5-144">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a77b5-145">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="a77b5-145">-DataFactoryName</span></span>
<span data-ttu-id="a77b5-146">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="a77b5-146">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a77b5-147">Dieses Cmdlet ruft Segmente ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a77b5-147">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a77b5-148">-DataSetName</span><span class="sxs-lookup"><span data-stu-id="a77b5-148">-DatasetName</span></span>
<span data-ttu-id="a77b5-149">Gibt den Namen des Datasets an, für das dieses Cmdlet Slices erhält.</span><span class="sxs-lookup"><span data-stu-id="a77b5-149">Specifies the name of the dataset for which this cmdlet gets slices.</span></span>

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

### <span data-ttu-id="a77b5-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a77b5-150">-DefaultProfile</span></span>
<span data-ttu-id="a77b5-151">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a77b5-151">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a77b5-152">-Enddatum</span><span class="sxs-lookup"><span data-stu-id="a77b5-152">-EndDateTime</span></span>
<span data-ttu-id="a77b5-153">Gibt das Ende eines Zeitraums als **DateTime** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a77b5-153">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="a77b5-154">Dieses Cmdlet ruft Segmente ab, die vor dem von diesem Parameter festgelegten Zeitpunkt erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="a77b5-154">This cmdlet gets slices produced before the time that this parameter specifies.</span></span>
<span data-ttu-id="a77b5-155">Wenn Sie weitere Informationen zu **DateTime** -Objekten wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="a77b5-155">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="a77b5-156">*Enddatum* muss im ISO8601-Format angegeben werden, wie in den folgenden Beispielen: 2015-01-01z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (Pazifik-Standardzeit) der standardmäßige Zeitzonenbezeichner ist UTC.</span><span class="sxs-lookup"><span data-stu-id="a77b5-156">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="a77b5-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a77b5-157">-ResourceGroupName</span></span>
<span data-ttu-id="a77b5-158">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="a77b5-158">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a77b5-159">Dieses Cmdlet ruft Segmente ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a77b5-159">This cmdlet gets slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a77b5-160">-Startdatum</span><span class="sxs-lookup"><span data-stu-id="a77b5-160">-StartDateTime</span></span>
<span data-ttu-id="a77b5-161">Gibt den Anfang eines Zeitraums als **DateTime** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a77b5-161">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="a77b5-162">Dieses Cmdlet ruft Segmente ab, die nach dem von diesem Parameter festgelegten Zeitpunkt erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="a77b5-162">This cmdlet gets slices produced after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="a77b5-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a77b5-163">CommonParameters</span></span>
<span data-ttu-id="a77b5-164">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a77b5-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a77b5-165">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a77b5-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a77b5-166">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a77b5-166">INPUTS</span></span>

### <span data-ttu-id="a77b5-167">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a77b5-167">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="a77b5-168">System. String</span><span class="sxs-lookup"><span data-stu-id="a77b5-168">System.String</span></span>

## <span data-ttu-id="a77b5-169">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a77b5-169">OUTPUTS</span></span>

### <span data-ttu-id="a77b5-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span><span class="sxs-lookup"><span data-stu-id="a77b5-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span></span>

## <span data-ttu-id="a77b5-171">Notizen</span><span class="sxs-lookup"><span data-stu-id="a77b5-171">NOTES</span></span>
* <span data-ttu-id="a77b5-172">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="a77b5-172">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a77b5-173">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a77b5-173">RELATED LINKS</span></span>

[<span data-ttu-id="a77b5-174">Satz-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="a77b5-174">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)

[<span data-ttu-id="a77b5-175">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="a77b5-175">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="a77b5-176">Satz-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="a77b5-176">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


