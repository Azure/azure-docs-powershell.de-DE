---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryactivitywindow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
ms.openlocfilehash: 5b18af8890d255dbd5514cccc0279acafe6bd611
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470600"
---
# <span data-ttu-id="d70f1-101">Get-AzDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="d70f1-101">Get-AzDataFactoryActivityWindow</span></span>

## <span data-ttu-id="d70f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d70f1-102">SYNOPSIS</span></span>
<span data-ttu-id="d70f1-103">Ruft Informationen zu Aktivitätsfenstern ab, die einer Daten factory zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d70f1-103">Gets information about activity windows associated with a data factory.</span></span>

## <span data-ttu-id="d70f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d70f1-104">SYNTAX</span></span>

### <span data-ttu-id="d70f1-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d70f1-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d70f1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d70f1-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d70f1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d70f1-107">DESCRIPTION</span></span>
<span data-ttu-id="d70f1-108">Das **Cmdlet "Get-AzDataFactoryActivityWindow"** ruft Informationen zu den Aktivitätsfenstern ab, die einer Datenfactory zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d70f1-108">The **Get-AzDataFactoryActivityWindow** cmdlet gets information about the activity windows associated with a data factory.</span></span>

## <span data-ttu-id="d70f1-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d70f1-109">EXAMPLES</span></span>

### <span data-ttu-id="d70f1-110">Beispiel 1: Erhalten von Aktivitätsfenstern, die einer Daten factory zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="d70f1-110">Example 1: Get activity windows associated with a data factory</span></span>
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

<span data-ttu-id="d70f1-111">Dieser Befehl ruft Informationen zu allen Aktivitätsfenstern ab, die der Daten factory namens WikiADF zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d70f1-111">This command gets information about all activity window associated with the data factory named WikiADF.</span></span>

## <span data-ttu-id="d70f1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d70f1-112">PARAMETERS</span></span>

### <span data-ttu-id="d70f1-113">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="d70f1-113">-ActivityName</span></span>
<span data-ttu-id="d70f1-114">Gibt den Namen der Aktivität an.</span><span class="sxs-lookup"><span data-stu-id="d70f1-114">Specifies the name of the activity.</span></span>
<span data-ttu-id="d70f1-115">Dieses Cmdlet ruft Aktivitätsfenster für die Aktivität ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d70f1-115">This cmdlet gets activity windows for the activity that this parameter specifies.</span></span>

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

### <span data-ttu-id="d70f1-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d70f1-116">-DataFactory</span></span>
<span data-ttu-id="d70f1-117">Gibt ein von **einem Cmdlet zurückgegebenes "PSDataFactory"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="d70f1-117">Specifies a **PSDataFactory** object returned by a cmdlet.</span></span>
<span data-ttu-id="d70f1-118">Dieses Cmdlet ruft Aktivitätsfenster ab, die zu der von diesem Parameter angegebenen Daten factory gehören.</span><span class="sxs-lookup"><span data-stu-id="d70f1-118">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d70f1-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d70f1-119">-DataFactoryName</span></span>
<span data-ttu-id="d70f1-120">Gibt den Namen der Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="d70f1-120">Specifies the name of the data factory.</span></span>
<span data-ttu-id="d70f1-121">Dieses Cmdlet ruft Aktivitätsfenster ab, die zu der von diesem Parameter angegebenen Daten factory gehören.</span><span class="sxs-lookup"><span data-stu-id="d70f1-121">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d70f1-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="d70f1-122">-DatasetName</span></span>
<span data-ttu-id="d70f1-123">Gibt den Namen des Datasets an.</span><span class="sxs-lookup"><span data-stu-id="d70f1-123">Specifies the name of the dataset.</span></span>
<span data-ttu-id="d70f1-124">Dieses Cmdlet ruft Aktivitätsfenster ab, die zu dem von diesem Parameter angegebenen Dataset gehören.</span><span class="sxs-lookup"><span data-stu-id="d70f1-124">This cmdlet gets activity windows that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="d70f1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d70f1-125">-DefaultProfile</span></span>
<span data-ttu-id="d70f1-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d70f1-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d70f1-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="d70f1-127">-Filter</span></span>
<span data-ttu-id="d70f1-128">Gibt das Aktivitätsfenster an, das mithilfe der Azure Search-Filtergrammatik ausgedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="d70f1-128">Specifies the activity window expressed by using Azure Search filter grammar.</span></span>
<span data-ttu-id="d70f1-129">Informationen zur Grammatik finden Sie in der #A0 für Azure Search https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) (in MSDN).</span><span class="sxs-lookup"><span data-stu-id="d70f1-129">For information about the grammar, see OData Expression Syntax for Azure Searchhttps://msdn.microsoft.com/en-us/library/azure/dn798921.aspx (https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span></span>
<span data-ttu-id="d70f1-130">Die Liste der Aktivitätsfenster wird nach der Suchzeichenfolge gefiltert, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d70f1-130">The activity windows list is filtered by the search string that this parameter specifies.</span></span>

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

### <span data-ttu-id="d70f1-131">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="d70f1-131">-OrderBy</span></span>
<span data-ttu-id="d70f1-132">Gibt an, dass die Antwort nach einem der Parameter der Aktivitätsfensterliste geordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d70f1-132">Specifies to order the response by one of the activity window list parameters.</span></span>
<span data-ttu-id="d70f1-133">Dies ist eine Liste der durch Kommas getrennten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d70f1-133">This is a list of comma separated properties.</span></span>
<span data-ttu-id="d70f1-134">Beispiel: WindowStart, PercentComplete.</span><span class="sxs-lookup"><span data-stu-id="d70f1-134">For example: WindowStart, PercentComplete.</span></span>
<span data-ttu-id="d70f1-135">Standardmäßig ist die Reihenfolge ASC (Ascending Order, aufsteigende Reihenfolge).</span><span class="sxs-lookup"><span data-stu-id="d70f1-135">By default, the order is ascending order (ASC).</span></span>
<span data-ttu-id="d70f1-136">Geben Sie "DESC" an, wenn die Liste in absteigender Reihenfolge angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d70f1-136">Specify DESC if you want to order the list in descending order.</span></span>

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

### <span data-ttu-id="d70f1-137">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="d70f1-137">-PipelineName</span></span>
<span data-ttu-id="d70f1-138">Gibt den Namen der Pipeline an.</span><span class="sxs-lookup"><span data-stu-id="d70f1-138">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="d70f1-139">Dieses Cmdlet ruft Aktivitätsfenster ab, die zu der pipeline gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d70f1-139">This cmdlet gets activity windows that belong to the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="d70f1-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d70f1-140">-ResourceGroupName</span></span>
<span data-ttu-id="d70f1-141">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="d70f1-141">Specifies the name of the resource group.</span></span>
<span data-ttu-id="d70f1-142">Dieses Cmdlet ruft Aktivitätsfenster ab, die zu der Ressourcengruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d70f1-142">This cmdlet gets activity windows that belong to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d70f1-143">-RunEnd</span><span class="sxs-lookup"><span data-stu-id="d70f1-143">-RunEnd</span></span>
<span data-ttu-id="d70f1-144">Gibt die Endzeit der Ausführung des Aktivitätsfensters an.</span><span class="sxs-lookup"><span data-stu-id="d70f1-144">Specifies the end time of the activity window run.</span></span>
<span data-ttu-id="d70f1-145">Dieses Cmdlet ruft Aktivitätsfenster ab, deren Laufzeit zwischen *"RunStart"* und *"RunEnd"* liegt.</span><span class="sxs-lookup"><span data-stu-id="d70f1-145">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="d70f1-146">-RunStart</span><span class="sxs-lookup"><span data-stu-id="d70f1-146">-RunStart</span></span>
<span data-ttu-id="d70f1-147">Gibt die Startzeit der Ausführung des Aktivitätsfensters an.</span><span class="sxs-lookup"><span data-stu-id="d70f1-147">Specifies the start time of the activity window run.</span></span>
<span data-ttu-id="d70f1-148">Dieses Cmdlet ruft Aktivitätsfenster ab, deren Laufzeit zwischen *"RunStart"* und *"RunEnd"* liegt.</span><span class="sxs-lookup"><span data-stu-id="d70f1-148">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="d70f1-149">-Top</span><span class="sxs-lookup"><span data-stu-id="d70f1-149">-Top</span></span>
<span data-ttu-id="d70f1-150">Gibt die maximale Anzahl von Aktivitätsfenstern an, die dieses Cmdlet zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d70f1-150">Specifies the maximum number of activity windows that this cmdlet returns.</span></span>

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

### <span data-ttu-id="d70f1-151">-WindowEnd</span><span class="sxs-lookup"><span data-stu-id="d70f1-151">-WindowEnd</span></span>
<span data-ttu-id="d70f1-152">Gibt die Endzeit des Aktivitätsfensters an.</span><span class="sxs-lookup"><span data-stu-id="d70f1-152">Specifies the end time of activity window.</span></span>
<span data-ttu-id="d70f1-153">Dieses Cmdlet ruft Aktivitätsfenster ab, deren Zeiten zwischen *"WindowStart"* und *"WindowEnd"* liegen.</span><span class="sxs-lookup"><span data-stu-id="d70f1-153">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="d70f1-154">-WindowStart</span><span class="sxs-lookup"><span data-stu-id="d70f1-154">-WindowStart</span></span>
<span data-ttu-id="d70f1-155">Gibt die Startzeit des Aktivitätsfensters an.</span><span class="sxs-lookup"><span data-stu-id="d70f1-155">Specifies the start time of activity window.</span></span>
<span data-ttu-id="d70f1-156">Dieses Cmdlet ruft Aktivitätsfenster ab, deren Zeiten zwischen *"WindowStart"* und *"WindowEnd"* liegen.</span><span class="sxs-lookup"><span data-stu-id="d70f1-156">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="d70f1-157">-WindowState</span><span class="sxs-lookup"><span data-stu-id="d70f1-157">-WindowState</span></span>
<span data-ttu-id="d70f1-158">Gibt den Status des Aktivitätsfensters an.</span><span class="sxs-lookup"><span data-stu-id="d70f1-158">Specifies the state of the activity window.</span></span>
<span data-ttu-id="d70f1-159">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="d70f1-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d70f1-160">Keine</span><span class="sxs-lookup"><span data-stu-id="d70f1-160">None</span></span>
- <span data-ttu-id="d70f1-161">Warten</span><span class="sxs-lookup"><span data-stu-id="d70f1-161">Waiting</span></span>
- <span data-ttu-id="d70f1-162">InProgress</span><span class="sxs-lookup"><span data-stu-id="d70f1-162">InProgress</span></span>
- <span data-ttu-id="d70f1-163">Bereit</span><span class="sxs-lookup"><span data-stu-id="d70f1-163">Ready</span></span>
- <span data-ttu-id="d70f1-164">Fehler</span><span class="sxs-lookup"><span data-stu-id="d70f1-164">Failed</span></span>
- <span data-ttu-id="d70f1-165">Übersprungen Dieses Cmdlet ruft Aktivitätsfenster ab, die den von diesem Parameter angegebenen Zustand haben.</span><span class="sxs-lookup"><span data-stu-id="d70f1-165">Skipped This cmdlet gets activity windows that are in the state that this parameter specifies.</span></span>

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

### <span data-ttu-id="d70f1-166">-WindowSubstate</span><span class="sxs-lookup"><span data-stu-id="d70f1-166">-WindowSubstate</span></span>
<span data-ttu-id="d70f1-167">Gibt den Unterzustand des Aktivitätsfensters an.</span><span class="sxs-lookup"><span data-stu-id="d70f1-167">Specifies the substate of the activity window.</span></span>
<span data-ttu-id="d70f1-168">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="d70f1-168">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d70f1-169">Storniert</span><span class="sxs-lookup"><span data-stu-id="d70f1-169">Canceled</span></span>
- <span data-ttu-id="d70f1-170">timedOut</span><span class="sxs-lookup"><span data-stu-id="d70f1-170">timedOut</span></span>
- <span data-ttu-id="d70f1-171">Die Validierung dieses Cmdlets ruft Aktivitätsfenster ab, die sich in dem von diesem Parameter angegebenen Unterzustand befinden.</span><span class="sxs-lookup"><span data-stu-id="d70f1-171">Validating This cmdlet gets activity windows that are in the substate that this parameter specifies.</span></span>

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

### <span data-ttu-id="d70f1-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d70f1-172">CommonParameters</span></span>
<span data-ttu-id="d70f1-173">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d70f1-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d70f1-174">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d70f1-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d70f1-175">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d70f1-175">INPUTS</span></span>

### <span data-ttu-id="d70f1-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d70f1-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="d70f1-177">System.String</span><span class="sxs-lookup"><span data-stu-id="d70f1-177">System.String</span></span>

### <span data-ttu-id="d70f1-178">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d70f1-178">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d70f1-179">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d70f1-179">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d70f1-180">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d70f1-180">OUTPUTS</span></span>

### <span data-ttu-id="d70f1-181">Microsoft.Azure.Commands.DataFactories.Models.PSActivityWindow</span><span class="sxs-lookup"><span data-stu-id="d70f1-181">Microsoft.Azure.Commands.DataFactories.Models.PSActivityWindow</span></span>

## <span data-ttu-id="d70f1-182">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d70f1-182">NOTES</span></span>

## <span data-ttu-id="d70f1-183">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d70f1-183">RELATED LINKS</span></span>

[<span data-ttu-id="d70f1-184">Cmdlets für Azure Data Factorys</span><span class="sxs-lookup"><span data-stu-id="d70f1-184">Azure Data Factories Cmdlets</span></span>](./Az.DataFactory.md)


