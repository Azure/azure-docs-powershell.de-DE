---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryActivityWindow.md
ms.openlocfilehash: 95d0ce0ffe48f845c15f7f00de59a70bfc466fe3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662436"
---
# <span data-ttu-id="5df16-101">Get-AzureRmDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="5df16-101">Get-AzureRmDataFactoryActivityWindow</span></span>

## <span data-ttu-id="5df16-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5df16-102">SYNOPSIS</span></span>
<span data-ttu-id="5df16-103">Ruft Informationen zu Aktivitäts Fenstern ab, die einer Data Factory zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="5df16-103">Gets information about activity windows associated with a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5df16-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5df16-104">SYNTAX</span></span>

### <span data-ttu-id="5df16-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="5df16-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5df16-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5df16-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5df16-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5df16-107">DESCRIPTION</span></span>
<span data-ttu-id="5df16-108">Das Cmdlet " **Get-AzureRmDataFactoryActivityWindow** " Ruft Informationen zu den Aktivitäts Fenstern ab, die einer Data Factory zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="5df16-108">The **Get-AzureRmDataFactoryActivityWindow** cmdlet gets information about the activity windows associated with a data factory.</span></span>

## <span data-ttu-id="5df16-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5df16-109">EXAMPLES</span></span>

### <span data-ttu-id="5df16-110">Beispiel 1: Abrufen von Aktivitäts Fenstern, die einer Data Factory zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="5df16-110">Example 1: Get activity windows associated with a data factory</span></span>
```
PS C:\>Get-AzureRmDataFactoryActivityWindow -DataFactoryName "WikiADF" -ResourceGroupName "ADF" -Top 3
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

<span data-ttu-id="5df16-111">Dieser Befehl ruft Informationen zu allen Aktivitäts Fenstern ab, die der Data Factory mit dem Namen WikiADF zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="5df16-111">This command gets information about all activity window associated with the data factory named WikiADF.</span></span>

## <span data-ttu-id="5df16-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5df16-112">PARAMETERS</span></span>

### <span data-ttu-id="5df16-113">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="5df16-113">-ActivityName</span></span>
<span data-ttu-id="5df16-114">Gibt den Namen der Aktivität an.</span><span class="sxs-lookup"><span data-stu-id="5df16-114">Specifies the name of the activity.</span></span>
<span data-ttu-id="5df16-115">Dieses Cmdlet ruft Aktivitätsfenster für die Aktivität ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="5df16-115">This cmdlet gets activity windows for the activity that this parameter specifies.</span></span>

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

### <span data-ttu-id="5df16-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="5df16-116">-DataFactory</span></span>
<span data-ttu-id="5df16-117">Gibt ein von einem Cmdlet zurückgegebenes **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="5df16-117">Specifies a **PSDataFactory** object returned by a cmdlet.</span></span>
<span data-ttu-id="5df16-118">Dieses Cmdlet ruft Aktivitätsfenster ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="5df16-118">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="5df16-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="5df16-119">-DataFactoryName</span></span>
<span data-ttu-id="5df16-120">Gibt den Namen der Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="5df16-120">Specifies the name of the data factory.</span></span>
<span data-ttu-id="5df16-121">Dieses Cmdlet ruft Aktivitätsfenster ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="5df16-121">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="5df16-122">-DataSetName</span><span class="sxs-lookup"><span data-stu-id="5df16-122">-DatasetName</span></span>
<span data-ttu-id="5df16-123">Gibt den Namen des Datasets an.</span><span class="sxs-lookup"><span data-stu-id="5df16-123">Specifies the name of the dataset.</span></span>
<span data-ttu-id="5df16-124">Dieses Cmdlet ruft Aktivitätsfenster ab, die zu dem DataSet gehören, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="5df16-124">This cmdlet gets activity windows that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="5df16-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="5df16-125">-Filter</span></span>
<span data-ttu-id="5df16-126">Gibt das Aktivitätsfenster an, das mithilfe der Azure-Suchfilter Grammatik ausgedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="5df16-126">Specifies the activity window expressed by using Azure Search filter grammar.</span></span>
<span data-ttu-id="5df16-127">Informationen zur Grammatik finden Sie unter Syntax für OData-Ausdrücke für Azure Search https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span><span class="sxs-lookup"><span data-stu-id="5df16-127">For information about the grammar, see OData Expression Syntax for Azure Searchhttps://msdn.microsoft.com/en-us/library/azure/dn798921.aspx (https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span></span>
<span data-ttu-id="5df16-128">Die Liste der Aktivitätsfenster wird nach der Suchzeichenfolge gefiltert, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="5df16-128">The activity windows list is filtered by the search string that this parameter specifies.</span></span>

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

### <span data-ttu-id="5df16-129">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="5df16-129">-OrderBy</span></span>
<span data-ttu-id="5df16-130">Gibt an, dass die Antwort durch einen der Parameter der Aktivitätsfenster Liste angeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5df16-130">Specifies to order the response by one of the activity window list parameters.</span></span>
<span data-ttu-id="5df16-131">Hierbei handelt es sich um eine Liste mit durch Kommas getrennten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5df16-131">This is a list of comma separated properties.</span></span>
<span data-ttu-id="5df16-132">Beispiel: WindowStart, PercentComplete.</span><span class="sxs-lookup"><span data-stu-id="5df16-132">For example: WindowStart, PercentComplete.</span></span>

<span data-ttu-id="5df16-133">Standardmäßig ist die Reihenfolge in aufsteigender Reihenfolge (ASC).</span><span class="sxs-lookup"><span data-stu-id="5df16-133">By default, the order is ascending order (ASC).</span></span>
<span data-ttu-id="5df16-134">Geben Sie DESC an, wenn Sie die Liste in absteigender Reihenfolge sortieren möchten.</span><span class="sxs-lookup"><span data-stu-id="5df16-134">Specify DESC if you want to order the list in descending order.</span></span>

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

### <span data-ttu-id="5df16-135">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="5df16-135">-PipelineName</span></span>
<span data-ttu-id="5df16-136">Gibt den Namen der Pipeline an.</span><span class="sxs-lookup"><span data-stu-id="5df16-136">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="5df16-137">Dieses Cmdlet ruft Aktivitätsfenster ab, die zu der Pipeline gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="5df16-137">This cmdlet gets activity windows that belong to the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="5df16-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5df16-138">-ResourceGroupName</span></span>
<span data-ttu-id="5df16-139">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="5df16-139">Specifies the name of the resource group.</span></span>
<span data-ttu-id="5df16-140">Dieses Cmdlet ruft Aktivitätsfenster ab, die zu der Ressourcengruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="5df16-140">This cmdlet gets activity windows that belong to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5df16-141">-RunEnd</span><span class="sxs-lookup"><span data-stu-id="5df16-141">-RunEnd</span></span>
<span data-ttu-id="5df16-142">Gibt die Endzeit des ausgeführten Aktivitäts Fensters an.</span><span class="sxs-lookup"><span data-stu-id="5df16-142">Specifies the end time of the activity window run.</span></span>
<span data-ttu-id="5df16-143">Dieses Cmdlet ruft Aktivitätsfenster ab, deren Ausführungszeiten zwischen *RunStart* -und *RunEnd* -Zeiten liegen.</span><span class="sxs-lookup"><span data-stu-id="5df16-143">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="5df16-144">-RunStart</span><span class="sxs-lookup"><span data-stu-id="5df16-144">-RunStart</span></span>
<span data-ttu-id="5df16-145">Gibt die Startzeit des ausgeführten Aktivitäts Fensters an.</span><span class="sxs-lookup"><span data-stu-id="5df16-145">Specifies the start time of the activity window run.</span></span>
<span data-ttu-id="5df16-146">Dieses Cmdlet ruft Aktivitätsfenster ab, deren Ausführungszeiten zwischen *RunStart* -und *RunEnd* -Zeiten liegen.</span><span class="sxs-lookup"><span data-stu-id="5df16-146">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="5df16-147">-Top</span><span class="sxs-lookup"><span data-stu-id="5df16-147">-Top</span></span>
<span data-ttu-id="5df16-148">Gibt die maximale Anzahl von Aktivitäts Fenstern an, die dieses Cmdlet zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="5df16-148">Specifies the maximum number of activity windows that this cmdlet returns.</span></span>

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

### <span data-ttu-id="5df16-149">-WindowEnd</span><span class="sxs-lookup"><span data-stu-id="5df16-149">-WindowEnd</span></span>
<span data-ttu-id="5df16-150">Gibt das Fenster Endzeit des Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="5df16-150">Specifies the end time of activity window.</span></span>
<span data-ttu-id="5df16-151">Dieses Cmdlet ruft Aktivitätsfenster ab, deren Zeiten zwischen *WindowStart* -und *WindowEnd* -Zeiten liegen.</span><span class="sxs-lookup"><span data-stu-id="5df16-151">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="5df16-152">-WindowStart</span><span class="sxs-lookup"><span data-stu-id="5df16-152">-WindowStart</span></span>
<span data-ttu-id="5df16-153">Gibt das Fenster Startzeit der Aktivität an.</span><span class="sxs-lookup"><span data-stu-id="5df16-153">Specifies the start time of activity window.</span></span>
<span data-ttu-id="5df16-154">Dieses Cmdlet ruft Aktivitätsfenster ab, deren Zeiten zwischen *WindowStart* -und *WindowEnd* -Zeiten liegen.</span><span class="sxs-lookup"><span data-stu-id="5df16-154">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="5df16-155">-WindowState</span><span class="sxs-lookup"><span data-stu-id="5df16-155">-WindowState</span></span>
<span data-ttu-id="5df16-156">Gibt den Zustand des Aktivitäts Fensters an.</span><span class="sxs-lookup"><span data-stu-id="5df16-156">Specifies the state of the activity window.</span></span>
<span data-ttu-id="5df16-157">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5df16-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5df16-158">Keine</span><span class="sxs-lookup"><span data-stu-id="5df16-158">None</span></span>
- <span data-ttu-id="5df16-159">Warten</span><span class="sxs-lookup"><span data-stu-id="5df16-159">Waiting</span></span>
- <span data-ttu-id="5df16-160">InProgress</span><span class="sxs-lookup"><span data-stu-id="5df16-160">InProgress</span></span>
- <span data-ttu-id="5df16-161">Bereit</span><span class="sxs-lookup"><span data-stu-id="5df16-161">Ready</span></span>
- <span data-ttu-id="5df16-162">Fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="5df16-162">Failed</span></span>
- <span data-ttu-id="5df16-163">Übersprungen</span><span class="sxs-lookup"><span data-stu-id="5df16-163">Skipped</span></span>

<span data-ttu-id="5df16-164">Dieses Cmdlet ruft Aktivitätsfenster ab, die sich in dem Zustand befinden, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="5df16-164">This cmdlet gets activity windows that are in the state that this parameter specifies.</span></span>

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

### <span data-ttu-id="5df16-165">-WindowSubstate</span><span class="sxs-lookup"><span data-stu-id="5df16-165">-WindowSubstate</span></span>
<span data-ttu-id="5df16-166">Gibt den unter Status des Aktivitäts Fensters an.</span><span class="sxs-lookup"><span data-stu-id="5df16-166">Specifies the substate of the activity window.</span></span>
<span data-ttu-id="5df16-167">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5df16-167">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5df16-168">Storniert</span><span class="sxs-lookup"><span data-stu-id="5df16-168">Canceled</span></span>
- <span data-ttu-id="5df16-169">TimedOut</span><span class="sxs-lookup"><span data-stu-id="5df16-169">timedOut</span></span>
- <span data-ttu-id="5df16-170">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="5df16-170">Validating</span></span>

<span data-ttu-id="5df16-171">Dieses Cmdlet ruft Aktivitätsfenster ab, die sich im unter Zustand befinden, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="5df16-171">This cmdlet gets activity windows that are in the substate that this parameter specifies.</span></span>

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

### <span data-ttu-id="5df16-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5df16-172">-DefaultProfile</span></span>
<span data-ttu-id="5df16-173">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5df16-173">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5df16-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5df16-174">CommonParameters</span></span>
<span data-ttu-id="5df16-175">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5df16-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5df16-176">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5df16-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5df16-177">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5df16-177">INPUTS</span></span>

## <span data-ttu-id="5df16-178">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5df16-178">OUTPUTS</span></span>

### <span data-ttu-id="5df16-179">System. Collections. Generic. List ' 1 [[Microsoft. WindowsAzure. Commands. Utilities. PSActivyWindow, Microsoft. WindowsAzure. Commands. Utilities, Version = 0.8.2.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="5df16-179">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSActivyWindow, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="5df16-180">Notizen</span><span class="sxs-lookup"><span data-stu-id="5df16-180">NOTES</span></span>

## <span data-ttu-id="5df16-181">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5df16-181">RELATED LINKS</span></span>

[<span data-ttu-id="5df16-182">Azure Data Factories-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="5df16-182">Azure Data Factories Cmdlets</span></span>](./AzureRM.DataFactories.md)


