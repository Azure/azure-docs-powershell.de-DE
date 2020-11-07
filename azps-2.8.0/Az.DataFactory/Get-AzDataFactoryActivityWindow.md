---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryactivitywindow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
ms.openlocfilehash: 3e79f4c11a5df5da8c01c323405f78c36aa5245b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651791"
---
# <span data-ttu-id="54eda-101">Get-AzDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="54eda-101">Get-AzDataFactoryActivityWindow</span></span>

## <span data-ttu-id="54eda-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="54eda-102">SYNOPSIS</span></span>
<span data-ttu-id="54eda-103">Ruft Informationen zu Aktivitäts Fenstern ab, die einer Data Factory zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="54eda-103">Gets information about activity windows associated with a data factory.</span></span>

## <span data-ttu-id="54eda-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="54eda-104">SYNTAX</span></span>

### <span data-ttu-id="54eda-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="54eda-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54eda-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="54eda-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="54eda-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="54eda-107">DESCRIPTION</span></span>
<span data-ttu-id="54eda-108">Das Cmdlet " **Get-AzDataFactoryActivityWindow** " Ruft Informationen zu den Aktivitäts Fenstern ab, die einer Data Factory zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="54eda-108">The **Get-AzDataFactoryActivityWindow** cmdlet gets information about the activity windows associated with a data factory.</span></span>

## <span data-ttu-id="54eda-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="54eda-109">EXAMPLES</span></span>

### <span data-ttu-id="54eda-110">Beispiel 1: Abrufen von Aktivitäts Fenstern, die einer Data Factory zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="54eda-110">Example 1: Get activity windows associated with a data factory</span></span>
```
PS C:\>Get-AzDataFactoryActivityWindow -DataFactoryName "WikiADF" -ResourceGroupName "ADF" -Top 3
ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : BlobToSqlCopyActivity
ActivityType      : Copy
LinkedServiceName : 
WindowState       : Waiting
WindowSubstate    : ConcurrencyLimit
Duration          : 00:00:00
InputDatasets     : {DA_CuratedWikiData}
OutputDatasets    : {DA_WikiAggregatedData}
PercentComplete   : 0
RunAttempts       : 1
RunStart          : 8/17/2016 10:05:51 PM
RunEnd            : 8/17/2016 10:05:51 PM
WindowStart       : 8/17/2016 6:00:00 AM
WindowEnd         : 8/17/2016 7:00:00 AM


ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : BlobToSqlCopyActivity
ActivityType      : Copy
LinkedServiceName : 
WindowState       : Waiting
WindowSubstate    : ConcurrencyLimit
Duration          : 00:00:00
InputDatasets     : {DA_CuratedWikiData}
OutputDatasets    : {DA_WikiAggregatedData}
PercentComplete   : 0
RunAttempts       : 1
RunStart          : 8/17/2016 10:05:51 PM
RunEnd            : 8/17/2016 10:05:51 PM
WindowStart       : 8/16/2016 10:00:00 PM
WindowEnd         : 8/16/2016 11:00:00 PM


ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : WikiHiveActivity
ActivityType      : HDInsightHive
LinkedServiceName : HDILinkedService
WindowState       : Ready
WindowSubstate    : 
Duration          : 00:03:37.8020000
InputDatasets     : {DA_WikipediaClickEvents}
OutputDatasets    : {DA_CuratedWikiData}
PercentComplete   : 100
RunAttempts       : 1
RunStart          : 8/17/2016 11:09:23 PM
RunEnd            : 8/17/2016 11:13:01 PM
WindowStart       : 8/17/2016 3:00:00 AM
WindowEnd         : 8/17/2016 4:00:00 AM
```

<span data-ttu-id="54eda-111">Dieser Befehl ruft Informationen zu allen Aktivitäts Fenstern ab, die der Data Factory mit dem Namen WikiADF zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="54eda-111">This command gets information about all activity window associated with the data factory named WikiADF.</span></span>

## <span data-ttu-id="54eda-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="54eda-112">PARAMETERS</span></span>

### <span data-ttu-id="54eda-113">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="54eda-113">-ActivityName</span></span>
<span data-ttu-id="54eda-114">Gibt den Namen der Aktivität an.</span><span class="sxs-lookup"><span data-stu-id="54eda-114">Specifies the name of the activity.</span></span>
<span data-ttu-id="54eda-115">Dieses Cmdlet ruft Aktivitätsfenster für die Aktivität ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="54eda-115">This cmdlet gets activity windows for the activity that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54eda-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="54eda-116">-DataFactory</span></span>
<span data-ttu-id="54eda-117">Gibt ein von einem Cmdlet zurückgegebenes **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="54eda-117">Specifies a **PSDataFactory** object returned by a cmdlet.</span></span>
<span data-ttu-id="54eda-118">Dieses Cmdlet ruft Aktivitätsfenster ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="54eda-118">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="54eda-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="54eda-119">-DataFactoryName</span></span>
<span data-ttu-id="54eda-120">Gibt den Namen der Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="54eda-120">Specifies the name of the data factory.</span></span>
<span data-ttu-id="54eda-121">Dieses Cmdlet ruft Aktivitätsfenster ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="54eda-121">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="54eda-122">-DataSetName</span><span class="sxs-lookup"><span data-stu-id="54eda-122">-DatasetName</span></span>
<span data-ttu-id="54eda-123">Gibt den Namen des Datasets an.</span><span class="sxs-lookup"><span data-stu-id="54eda-123">Specifies the name of the dataset.</span></span>
<span data-ttu-id="54eda-124">Dieses Cmdlet ruft Aktivitätsfenster ab, die zu dem DataSet gehören, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="54eda-124">This cmdlet gets activity windows that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="54eda-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54eda-125">-DefaultProfile</span></span>
<span data-ttu-id="54eda-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="54eda-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54eda-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="54eda-127">-Filter</span></span>
<span data-ttu-id="54eda-128">Gibt das Aktivitätsfenster an, das mithilfe der Azure-Suchfilter Grammatik ausgedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="54eda-128">Specifies the activity window expressed by using Azure Search filter grammar.</span></span>
<span data-ttu-id="54eda-129">Informationen zur Grammatik finden Sie unter Syntax für OData-Ausdrücke für Azure Search https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span><span class="sxs-lookup"><span data-stu-id="54eda-129">For information about the grammar, see OData Expression Syntax for Azure Searchhttps://msdn.microsoft.com/en-us/library/azure/dn798921.aspx (https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span></span>
<span data-ttu-id="54eda-130">Die Liste der Aktivitätsfenster wird nach der Suchzeichenfolge gefiltert, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="54eda-130">The activity windows list is filtered by the search string that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54eda-131">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="54eda-131">-OrderBy</span></span>
<span data-ttu-id="54eda-132">Gibt an, dass die Antwort durch einen der Parameter der Aktivitätsfenster Liste angeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="54eda-132">Specifies to order the response by one of the activity window list parameters.</span></span>
<span data-ttu-id="54eda-133">Hierbei handelt es sich um eine Liste mit durch Kommas getrennten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="54eda-133">This is a list of comma separated properties.</span></span>
<span data-ttu-id="54eda-134">Beispiel: WindowStart, PercentComplete.</span><span class="sxs-lookup"><span data-stu-id="54eda-134">For example: WindowStart, PercentComplete.</span></span>
<span data-ttu-id="54eda-135">Standardmäßig ist die Reihenfolge in aufsteigender Reihenfolge (ASC).</span><span class="sxs-lookup"><span data-stu-id="54eda-135">By default, the order is ascending order (ASC).</span></span>
<span data-ttu-id="54eda-136">Geben Sie DESC an, wenn Sie die Liste in absteigender Reihenfolge sortieren möchten.</span><span class="sxs-lookup"><span data-stu-id="54eda-136">Specify DESC if you want to order the list in descending order.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54eda-137">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="54eda-137">-PipelineName</span></span>
<span data-ttu-id="54eda-138">Gibt den Namen der Pipeline an.</span><span class="sxs-lookup"><span data-stu-id="54eda-138">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="54eda-139">Dieses Cmdlet ruft Aktivitätsfenster ab, die zu der Pipeline gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="54eda-139">This cmdlet gets activity windows that belong to the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="54eda-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54eda-140">-ResourceGroupName</span></span>
<span data-ttu-id="54eda-141">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="54eda-141">Specifies the name of the resource group.</span></span>
<span data-ttu-id="54eda-142">Dieses Cmdlet ruft Aktivitätsfenster ab, die zu der Ressourcengruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="54eda-142">This cmdlet gets activity windows that belong to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="54eda-143">-RunEnd</span><span class="sxs-lookup"><span data-stu-id="54eda-143">-RunEnd</span></span>
<span data-ttu-id="54eda-144">Gibt die Endzeit des ausgeführten Aktivitäts Fensters an.</span><span class="sxs-lookup"><span data-stu-id="54eda-144">Specifies the end time of the activity window run.</span></span>
<span data-ttu-id="54eda-145">Dieses Cmdlet ruft Aktivitätsfenster ab, deren Ausführungszeiten zwischen *RunStart* -und *RunEnd* -Zeiten liegen.</span><span class="sxs-lookup"><span data-stu-id="54eda-145">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54eda-146">-RunStart</span><span class="sxs-lookup"><span data-stu-id="54eda-146">-RunStart</span></span>
<span data-ttu-id="54eda-147">Gibt die Startzeit des ausgeführten Aktivitäts Fensters an.</span><span class="sxs-lookup"><span data-stu-id="54eda-147">Specifies the start time of the activity window run.</span></span>
<span data-ttu-id="54eda-148">Dieses Cmdlet ruft Aktivitätsfenster ab, deren Ausführungszeiten zwischen *RunStart* -und *RunEnd* -Zeiten liegen.</span><span class="sxs-lookup"><span data-stu-id="54eda-148">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54eda-149">-Top</span><span class="sxs-lookup"><span data-stu-id="54eda-149">-Top</span></span>
<span data-ttu-id="54eda-150">Gibt die maximale Anzahl von Aktivitäts Fenstern an, die dieses Cmdlet zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="54eda-150">Specifies the maximum number of activity windows that this cmdlet returns.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54eda-151">-WindowEnd</span><span class="sxs-lookup"><span data-stu-id="54eda-151">-WindowEnd</span></span>
<span data-ttu-id="54eda-152">Gibt das Fenster Endzeit des Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="54eda-152">Specifies the end time of activity window.</span></span>
<span data-ttu-id="54eda-153">Dieses Cmdlet ruft Aktivitätsfenster ab, deren Zeiten zwischen *WindowStart* -und *WindowEnd* -Zeiten liegen.</span><span class="sxs-lookup"><span data-stu-id="54eda-153">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54eda-154">-WindowStart</span><span class="sxs-lookup"><span data-stu-id="54eda-154">-WindowStart</span></span>
<span data-ttu-id="54eda-155">Gibt das Fenster Startzeit der Aktivität an.</span><span class="sxs-lookup"><span data-stu-id="54eda-155">Specifies the start time of activity window.</span></span>
<span data-ttu-id="54eda-156">Dieses Cmdlet ruft Aktivitätsfenster ab, deren Zeiten zwischen *WindowStart* -und *WindowEnd* -Zeiten liegen.</span><span class="sxs-lookup"><span data-stu-id="54eda-156">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54eda-157">-WindowState</span><span class="sxs-lookup"><span data-stu-id="54eda-157">-WindowState</span></span>
<span data-ttu-id="54eda-158">Gibt den Zustand des Aktivitäts Fensters an.</span><span class="sxs-lookup"><span data-stu-id="54eda-158">Specifies the state of the activity window.</span></span>
<span data-ttu-id="54eda-159">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="54eda-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="54eda-160">Keine</span><span class="sxs-lookup"><span data-stu-id="54eda-160">None</span></span>
- <span data-ttu-id="54eda-161">Warten</span><span class="sxs-lookup"><span data-stu-id="54eda-161">Waiting</span></span>
- <span data-ttu-id="54eda-162">InProgress</span><span class="sxs-lookup"><span data-stu-id="54eda-162">InProgress</span></span>
- <span data-ttu-id="54eda-163">Bereit</span><span class="sxs-lookup"><span data-stu-id="54eda-163">Ready</span></span>
- <span data-ttu-id="54eda-164">Fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="54eda-164">Failed</span></span>
- <span data-ttu-id="54eda-165">Übersprungen dieses Cmdlet ruft Aktivitätsfenster ab, die sich in dem Zustand befinden, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="54eda-165">Skipped This cmdlet gets activity windows that are in the state that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54eda-166">-WindowSubstate</span><span class="sxs-lookup"><span data-stu-id="54eda-166">-WindowSubstate</span></span>
<span data-ttu-id="54eda-167">Gibt den unter Status des Aktivitäts Fensters an.</span><span class="sxs-lookup"><span data-stu-id="54eda-167">Specifies the substate of the activity window.</span></span>
<span data-ttu-id="54eda-168">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="54eda-168">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="54eda-169">Storniert</span><span class="sxs-lookup"><span data-stu-id="54eda-169">Canceled</span></span>
- <span data-ttu-id="54eda-170">TimedOut</span><span class="sxs-lookup"><span data-stu-id="54eda-170">timedOut</span></span>
- <span data-ttu-id="54eda-171">Beim Überprüfen dieses Cmdlets werden Aktivitätsfenster abgerufen, die sich in dem unter Zustand befinden, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="54eda-171">Validating This cmdlet gets activity windows that are in the substate that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54eda-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54eda-172">CommonParameters</span></span>
<span data-ttu-id="54eda-173">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54eda-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54eda-174">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54eda-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54eda-175">Eingaben</span><span class="sxs-lookup"><span data-stu-id="54eda-175">INPUTS</span></span>

### <span data-ttu-id="54eda-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="54eda-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="54eda-177">System. String</span><span class="sxs-lookup"><span data-stu-id="54eda-177">System.String</span></span>

### <span data-ttu-id="54eda-178">System. Nullable ' 1 [[System. DateTime, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="54eda-178">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="54eda-179">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="54eda-179">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="54eda-180">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="54eda-180">OUTPUTS</span></span>

### <span data-ttu-id="54eda-181">Microsoft. Azure. Commands. datafactoring. Models. PSActivityWindow</span><span class="sxs-lookup"><span data-stu-id="54eda-181">Microsoft.Azure.Commands.DataFactories.Models.PSActivityWindow</span></span>

## <span data-ttu-id="54eda-182">Notizen</span><span class="sxs-lookup"><span data-stu-id="54eda-182">NOTES</span></span>

## <span data-ttu-id="54eda-183">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="54eda-183">RELATED LINKS</span></span>

[<span data-ttu-id="54eda-184">Azure Data Factories-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="54eda-184">Azure Data Factories Cmdlets</span></span>](./Az.DataFactory.md)


