---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
ms.openlocfilehash: a71ccc37fe1c6b6811b955c5d84353dfecd66c2f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174689"
---
# <span data-ttu-id="098f0-101">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="098f0-101">Get-AzDataFactorySlice</span></span>

## <span data-ttu-id="098f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="098f0-102">SYNOPSIS</span></span>
<span data-ttu-id="098f0-103">Ruft Datenschnitte für ein Dataset in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="098f0-103">Gets data slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="098f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="098f0-104">SYNTAX</span></span>

### <span data-ttu-id="098f0-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="098f0-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="098f0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="098f0-106">ByFactoryObject</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="098f0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="098f0-107">DESCRIPTION</span></span>
<span data-ttu-id="098f0-108">Das **Cmdlet "Get-AzDataFactoryS slice"** ruft Datenschnitte für ein Dataset in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="098f0-108">The **Get-AzDataFactorySlice** cmdlet gets data slices for a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="098f0-109">Geben Sie eine Anfangszeit und eine Endzeit an, um einen Bereich von Datenschnitten zum Anzeigen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="098f0-109">Specify a start time and an end time to define a range of data slices to view.</span></span>
<span data-ttu-id="098f0-110">Der Status eines Datenschnitts ist einer der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="098f0-110">The status of a data slice is one of the following values:</span></span> 
- <span data-ttu-id="098f0-111">PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="098f0-111">PendingExecution.</span></span>
<span data-ttu-id="098f0-112">Die Datenverarbeitung wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="098f0-112">Data processing has not started.</span></span> 
- <span data-ttu-id="098f0-113">InProgress.</span><span class="sxs-lookup"><span data-stu-id="098f0-113">InProgress.</span></span>
<span data-ttu-id="098f0-114">Die Datenverarbeitung wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="098f0-114">Data processing is in progress.</span></span> 
- <span data-ttu-id="098f0-115">"Bereit" aus.</span><span class="sxs-lookup"><span data-stu-id="098f0-115">Ready.</span></span>
<span data-ttu-id="098f0-116">Die Datenverarbeitung ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="098f0-116">Data processing is completed.</span></span>
<span data-ttu-id="098f0-117">Das Datenschnitt kann von abhängigen Segmenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="098f0-117">The data slice is ready for dependent slices to consume it.</span></span> 
- <span data-ttu-id="098f0-118">Fehler.</span><span class="sxs-lookup"><span data-stu-id="098f0-118">Failed.</span></span>
<span data-ttu-id="098f0-119">Die Ausführung, die das Segment erzeugt, ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="098f0-119">The run that produces the slice failed.</span></span> 
- <span data-ttu-id="098f0-120">"Überspringen" aus.</span><span class="sxs-lookup"><span data-stu-id="098f0-120">Skip.</span></span>
<span data-ttu-id="098f0-121">Data Factory überspringt die Verarbeitung des Datenschnitts.</span><span class="sxs-lookup"><span data-stu-id="098f0-121">Data Factory skips processing of the slice.</span></span> 
- <span data-ttu-id="098f0-122">Wiederholen Sie den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="098f0-122">Retry.</span></span>
<span data-ttu-id="098f0-123">Data Factory führt die Ausführung aus, die das Segment erzeugt.</span><span class="sxs-lookup"><span data-stu-id="098f0-123">Data Factory retries the run that produces the slice.</span></span> 
- <span data-ttu-id="098f0-124">"Timed Out" aus. Die Datenverarbeitung ist nicht mehr zeit.</span><span class="sxs-lookup"><span data-stu-id="098f0-124">Timed Out. Data processing has timed out.</span></span> 
- <span data-ttu-id="098f0-125">PendingValidation.</span><span class="sxs-lookup"><span data-stu-id="098f0-125">PendingValidation.</span></span>
<span data-ttu-id="098f0-126">Das Datendatenschnitt wartet auf die Überprüfung, bevor es verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="098f0-126">Data slice is waiting for validation before it is processed.</span></span> 
- <span data-ttu-id="098f0-127">Wiederholen Sie die Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="098f0-127">Retry Validation.</span></span>
<span data-ttu-id="098f0-128">Data Factory rechiert die Überprüfung des Datenschnitts.</span><span class="sxs-lookup"><span data-stu-id="098f0-128">Data Factory retries the validation of the slice.</span></span> 
- <span data-ttu-id="098f0-129">Fehler bei der Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="098f0-129">Failed Validation.</span></span>
<span data-ttu-id="098f0-130">Fehler bei der Überprüfung des Segments.</span><span class="sxs-lookup"><span data-stu-id="098f0-130">Validation of the slice failed.</span></span>
<span data-ttu-id="098f0-131">Für jedes der Segmente werden weitere Informationen zur Ausführung des Segments mithilfe des cmdlets Get-AzDataFactoryRun segmentiert.</span><span class="sxs-lookup"><span data-stu-id="098f0-131">For each of the slices, you can see more information about the run that produces the slice by using the Get-AzDataFactoryRun cmdlet.</span></span>

## <span data-ttu-id="098f0-132">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="098f0-132">EXAMPLES</span></span>

### <span data-ttu-id="098f0-133">Beispiel 1: Datenschnitte für ein Dataset erhalten</span><span class="sxs-lookup"><span data-stu-id="098f0-133">Example 1: Get data slices for a dataset</span></span>
```powershell
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

<span data-ttu-id="098f0-134">Dieser Befehl ruft alle Datenschnitte für das Dataset mit dem Namen "WikiAggregatedData" in der Daten factory namens WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="098f0-134">This command gets all the data slices for the dataset named WikiAggregatedData in the data factory named WikiADF.</span></span>
<span data-ttu-id="098f0-135">Der Befehl ruft Segmente ab, die nach der vom Parameter "StartDateTime" angegebenen Zeit erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="098f0-135">The command gets slices produced after the time that the StartDateTime parameter specifies.</span></span>
<span data-ttu-id="098f0-136">Der folgende Beispielcode legt die Verfügbarkeit für dieses Dataset stündlich in der JavaScript Object Notation (JSON)-Datei fest.</span><span class="sxs-lookup"><span data-stu-id="098f0-136">The following example code sets the availability for this dataset every hour in the JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="098f0-137">availability: { period: "Hour", periodMultiplier: 1 } Some of the results are Ready, and others are PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="098f0-137">availability: { period: "Hour", periodMultiplier: 1 } Some of the results are Ready and others are PendingExecution.</span></span>
<span data-ttu-id="098f0-138">Fertige Segmente wurden bereits ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="098f0-138">Ready slices have already run.</span></span>
<span data-ttu-id="098f0-139">Die ausstehenden Segmente werden am Ende jeder Stunde in dem vom cmdlet Set-AzDataFactoryPipelineActivePeriod festgelegten Intervall ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="098f0-139">The pending slices are waiting to run at the end of each hour in the interval that the Set-AzDataFactoryPipelineActivePeriod cmdlet specifies.</span></span>
<span data-ttu-id="098f0-140">In diesem Beispiel haben sowohl Start- als auch Endzeiträume für die Pipeline und das Segment einen Wert von einem Tag (24 Stunden).</span><span class="sxs-lookup"><span data-stu-id="098f0-140">In this example, both start and end periods for the pipeline and the slice have a value of one day (24 hours).</span></span>

### <span data-ttu-id="098f0-141">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="098f0-141">Example 2</span></span>

<span data-ttu-id="098f0-142">Ruft Datenschnitte für ein Dataset in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="098f0-142">Gets data slices for a dataset in Azure Data Factory.</span></span> <span data-ttu-id="098f0-143">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="098f0-143">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzDataFactorySlice -DataFactoryName 'WikiADF' -DatasetName 'DAWikiAggregatedData' -EndDateTime 2014-05-22T16:00:00Z -ResourceGroupName 'ADF' -StartDateTime 2014-05-20T10:00:00Z
```

## <span data-ttu-id="098f0-144">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="098f0-144">PARAMETERS</span></span>

### <span data-ttu-id="098f0-145">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="098f0-145">-DataFactory</span></span>
<span data-ttu-id="098f0-146">Gibt ein **"PSDataFactory"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="098f0-146">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="098f0-147">Dieses Cmdlet ruft Segmente ab, die zu der von diesem Parameter angegebenen Daten factory gehören.</span><span class="sxs-lookup"><span data-stu-id="098f0-147">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="098f0-148">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="098f0-148">-DataFactoryName</span></span>
<span data-ttu-id="098f0-149">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="098f0-149">Specifies the name of a data factory.</span></span>
<span data-ttu-id="098f0-150">Dieses Cmdlet ruft Segmente ab, die zu der von diesem Parameter angegebenen Daten factory gehören.</span><span class="sxs-lookup"><span data-stu-id="098f0-150">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="098f0-151">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="098f0-151">-DatasetName</span></span>
<span data-ttu-id="098f0-152">Gibt den Namen des Datasets an, für das dieses Cmdlet Segmente erhält.</span><span class="sxs-lookup"><span data-stu-id="098f0-152">Specifies the name of the dataset for which this cmdlet gets slices.</span></span>

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

### <span data-ttu-id="098f0-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="098f0-153">-DefaultProfile</span></span>
<span data-ttu-id="098f0-154">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="098f0-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="098f0-155">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="098f0-155">-EndDateTime</span></span>
<span data-ttu-id="098f0-156">Gibt das Ende eines Zeitraums als **"DateTime"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="098f0-156">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="098f0-157">Dieses Cmdlet ruft Segmente ab, die vor dem von diesem Parameter angegebenen Zeitpunkt erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="098f0-157">This cmdlet gets slices produced before the time that this parameter specifies.</span></span>
<span data-ttu-id="098f0-158">Weitere Informationen zu **"DateTime"-Objekten** erhalten Sie, wenn Sie `Get-Help Get-Date` ".</span><span class="sxs-lookup"><span data-stu-id="098f0-158">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="098f0-159">*EndDateTime* muss im ISO8601-Format angegeben werden, wie in den folgenden Beispielen: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) Der Standard-Zeitzonen-Designator ist UTC.</span><span class="sxs-lookup"><span data-stu-id="098f0-159">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="098f0-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="098f0-160">-ResourceGroupName</span></span>
<span data-ttu-id="098f0-161">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="098f0-161">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="098f0-162">Dieses Cmdlet ruft Segmente ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="098f0-162">This cmdlet gets slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="098f0-163">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="098f0-163">-StartDateTime</span></span>
<span data-ttu-id="098f0-164">Gibt den Anfang eines Zeitraums als **"DateTime"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="098f0-164">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="098f0-165">Dieses Cmdlet ruft Segmente nach dem von diesem Parameter angegebenen Zeitpunkt ab.</span><span class="sxs-lookup"><span data-stu-id="098f0-165">This cmdlet gets slices produced after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="098f0-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="098f0-166">CommonParameters</span></span>
<span data-ttu-id="098f0-167">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="098f0-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="098f0-168">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="098f0-168">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="098f0-169">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="098f0-169">INPUTS</span></span>

### <span data-ttu-id="098f0-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="098f0-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="098f0-171">System.String</span><span class="sxs-lookup"><span data-stu-id="098f0-171">System.String</span></span>

## <span data-ttu-id="098f0-172">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="098f0-172">OUTPUTS</span></span>

### <span data-ttu-id="098f0-173">Microsoft.Azure.Commands.DataFactories.Models.PSDataSverbinder</span><span class="sxs-lookup"><span data-stu-id="098f0-173">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span></span>

## <span data-ttu-id="098f0-174">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="098f0-174">NOTES</span></span>
* <span data-ttu-id="098f0-175">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="098f0-175">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="098f0-176">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="098f0-176">RELATED LINKS</span></span>

[<span data-ttu-id="098f0-177">Set-AzDataFactorySstatus</span><span class="sxs-lookup"><span data-stu-id="098f0-177">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)

[<span data-ttu-id="098f0-178">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="098f0-178">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="098f0-179">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="098f0-179">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


