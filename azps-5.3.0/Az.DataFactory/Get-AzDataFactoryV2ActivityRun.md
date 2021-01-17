---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2activityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
ms.openlocfilehash: cdee786d338dce2663bf99916c6b6c2b250e22b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470590"
---
# <span data-ttu-id="efcb9-101">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="efcb9-101">Get-AzDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="efcb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efcb9-102">SYNOPSIS</span></span>
<span data-ttu-id="efcb9-103">Ruft Informationen zu Aktivitäten ab, die für einen Pipelinelauf ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="efcb9-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="efcb9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="efcb9-104">SYNTAX</span></span>

### <span data-ttu-id="efcb9-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="efcb9-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efcb9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="efcb9-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efcb9-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="efcb9-107">DESCRIPTION</span></span>
<span data-ttu-id="efcb9-108">Das **Cmdlet "Get-AzDataFactoryV2ActivityRun"** ruft Informationen zu den Ausführungsläufen in Azure Data Factory für den angegebenen Pipelinelauf ab, der im angegebenen Zeitrahmen ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="efcb9-108">The **Get-AzDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="efcb9-109">Darüber hinaus können Sie Filter für den Aktivitätsnamen, den namen des verknüpften Diensts, der die Ausführung ausgeführt hat, und den Status der Ausführung angeben.</span><span class="sxs-lookup"><span data-stu-id="efcb9-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="efcb9-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="efcb9-110">EXAMPLES</span></span>

### <span data-ttu-id="efcb9-111">Beispiel 1: Alle Aktivitäten für einen Pipelinelauf ausführen</span><span class="sxs-lookup"><span data-stu-id="efcb9-111">Example 1: Get all activity runs for a pipeline run</span></span>
```
PS C:\> Get-AzDataFactoryV2ActivityRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter "2017-09-01" -RunStartedBefore "2017-09-30"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    ActivityName      : MyWebActivity
    PipelineRunId     : f288712d-fb08-4cb8-96ef-82d3b9b30621
    PipelineName      : DPWikisample
    Input             : {method, url, headers, body...}
    Output            : {operationstatus}
    ActivityRunStart  : 9/14/2017 12:20:57 AM
    ActivityRunEnd    : 9/14/2017 12:21:00 AM
    DurationInMs      : 2768
    Status            : Succeeded
    Error             : {errorCode, message, failureType, target}
```

<span data-ttu-id="efcb9-112">Dieser Befehl ruft Details zu allen Aktivitäten ab, die bei der Ausführung der Pipeline mit der ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" zwischen "2017-09-01" und "2017-09-30" passiert sind.</span><span class="sxs-lookup"><span data-stu-id="efcb9-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="efcb9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efcb9-113">PARAMETERS</span></span>

### <span data-ttu-id="efcb9-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="efcb9-114">-ActivityName</span></span>
<span data-ttu-id="efcb9-115">Der Name der Aktivität.</span><span class="sxs-lookup"><span data-stu-id="efcb9-115">The name of the activity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efcb9-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="efcb9-116">-DataFactory</span></span>
<span data-ttu-id="efcb9-117">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="efcb9-117">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efcb9-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="efcb9-118">-DataFactoryName</span></span>
<span data-ttu-id="efcb9-119">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="efcb9-119">The data factory name.</span></span>

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

### <span data-ttu-id="efcb9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efcb9-120">-DefaultProfile</span></span>
<span data-ttu-id="efcb9-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="efcb9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efcb9-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="efcb9-122">-PipelineRunId</span></span>
<span data-ttu-id="efcb9-123">Die Ausführungs-ID der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="efcb9-123">The Run ID of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efcb9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efcb9-124">-ResourceGroupName</span></span>
<span data-ttu-id="efcb9-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="efcb9-125">The resource group name.</span></span>

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

### <span data-ttu-id="efcb9-126">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="efcb9-126">-RunStartedAfter</span></span>
<span data-ttu-id="efcb9-127">Der Zeitpunkt, zu dem oder nach dem die Ausführung der Pipeline gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="efcb9-127">The time at or after which the pipeline run started to execute.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efcb9-128">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="efcb9-128">-RunStartedBefore</span></span>
<span data-ttu-id="efcb9-129">Der Zeitpunkt, zu dem oder vor dem die Ausführung der Pipeline gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="efcb9-129">The time at or before which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="efcb9-130">-Status</span><span class="sxs-lookup"><span data-stu-id="efcb9-130">-Status</span></span>
<span data-ttu-id="efcb9-131">Der Status der Pipeline wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="efcb9-131">The status of the pipeline run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efcb9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efcb9-132">CommonParameters</span></span>
<span data-ttu-id="efcb9-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efcb9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efcb9-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efcb9-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efcb9-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="efcb9-135">INPUTS</span></span>

### <span data-ttu-id="efcb9-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="efcb9-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="efcb9-137">System.String</span><span class="sxs-lookup"><span data-stu-id="efcb9-137">System.String</span></span>

## <span data-ttu-id="efcb9-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="efcb9-138">OUTPUTS</span></span>

### <span data-ttu-id="efcb9-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span><span class="sxs-lookup"><span data-stu-id="efcb9-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>

## <span data-ttu-id="efcb9-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="efcb9-140">NOTES</span></span>

## <span data-ttu-id="efcb9-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="efcb9-141">RELATED LINKS</span></span>

[<span data-ttu-id="efcb9-142">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="efcb9-142">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="efcb9-143">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="efcb9-143">Get-AzDataFactoryV2PipelineRun</span></span>]()

