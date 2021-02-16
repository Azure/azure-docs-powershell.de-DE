---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseactivityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
ms.openlocfilehash: fd300a54b3f35aa69a94bfee69cfcf7ca60f95a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162881"
---
# <span data-ttu-id="48564-101">Get-AzSynapseActivityRun</span><span class="sxs-lookup"><span data-stu-id="48564-101">Get-AzSynapseActivityRun</span></span>

## <span data-ttu-id="48564-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48564-102">SYNOPSIS</span></span>
<span data-ttu-id="48564-103">Ruft Informationen zu Aktivitäten ab, die für einen Pipelinelauf ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="48564-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="48564-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48564-104">SYNTAX</span></span>

### <span data-ttu-id="48564-105">GetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="48564-105">GetByName (Default)</span></span>
```
Get-AzSynapseActivityRun -WorkspaceName <String> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48564-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="48564-106">GetByObject</span></span>
```
Get-AzSynapseActivityRun -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48564-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48564-107">DESCRIPTION</span></span>
<span data-ttu-id="48564-108">Das **Cmdlet "Get-AzSynapseActivityRun"** ruft Informationen über die Ausführung im Arbeitsbereich für den angegebenen Pipelinelauf ab, der im angegebenen Zeitrahmen ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="48564-108">The **Get-AzSynapseActivityRun** cmdlet gets information about runs in workspace for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="48564-109">Darüber hinaus können Sie Filter für den Aktivitätsnamen und den Status der Ausführung angeben.</span><span class="sxs-lookup"><span data-stu-id="48564-109">Additionally, you can specify filters for activity name and the status of the run.</span></span>

## <span data-ttu-id="48564-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="48564-110">EXAMPLES</span></span>

### <span data-ttu-id="48564-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="48564-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseActivityRun -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="48564-112">Dieser Befehl ruft Details zu allen Aktivitäten ab, die in der Pipeline namens "ContosoPipeline run" mit der ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" ausgeführt wurden, die zwischen "2018-09-01T21:00" und "2018-09-30T21:00" passiert ist.</span><span class="sxs-lookup"><span data-stu-id="48564-112">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00".</span></span>

### <span data-ttu-id="48564-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="48564-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseActivityRun -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="48564-114">Dieser Befehl ruft Details zu allen Aktivitäten ab, die in der Pipeline namens "ContosoPipeline run" mit der ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" ausgeführt wurden, die zwischen "2018-09-01T21:00" und "2018-09-30T21:00" über die Pipeline passiert ist.</span><span class="sxs-lookup"><span data-stu-id="48564-114">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00" through pipeline.</span></span>

## <span data-ttu-id="48564-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48564-115">PARAMETERS</span></span>

### <span data-ttu-id="48564-116">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="48564-116">-ActivityName</span></span>
<span data-ttu-id="48564-117">Der Name der Aktivität.</span><span class="sxs-lookup"><span data-stu-id="48564-117">The name of the activity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48564-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48564-118">-DefaultProfile</span></span>
<span data-ttu-id="48564-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="48564-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48564-120">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="48564-120">-PipelineName</span></span>
<span data-ttu-id="48564-121">Der Pipelinename.</span><span class="sxs-lookup"><span data-stu-id="48564-121">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48564-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="48564-122">-PipelineRunId</span></span>
<span data-ttu-id="48564-123">Der Pipeline-Ausführungsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="48564-123">The pipeline run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48564-124">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="48564-124">-RunStartedAfter</span></span>
<span data-ttu-id="48564-125">Die Uhrzeit, zu oder nach der das Ausführungsereignis im FORMAT "ISO 8601" aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="48564-125">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48564-126">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="48564-126">-RunStartedBefore</span></span>
<span data-ttu-id="48564-127">Der Zeitpunkt oder vor dem das Ausführungsereignis im FORMAT ISO 8601 aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="48564-127">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48564-128">-Status</span><span class="sxs-lookup"><span data-stu-id="48564-128">-Status</span></span>
<span data-ttu-id="48564-129">Der Status der Pipeline wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="48564-129">The status of the pipeline run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48564-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="48564-130">-WorkspaceName</span></span>
<span data-ttu-id="48564-131">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="48564-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48564-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="48564-132">-WorkspaceObject</span></span>
<span data-ttu-id="48564-133">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="48564-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48564-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48564-134">CommonParameters</span></span>
<span data-ttu-id="48564-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48564-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48564-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48564-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48564-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="48564-137">INPUTS</span></span>

### <span data-ttu-id="48564-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="48564-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="48564-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="48564-139">OUTPUTS</span></span>

### <span data-ttu-id="48564-140">Microsoft.Azure.Commands.Synapse.Models.PSActivityRunsQueryResponse</span><span class="sxs-lookup"><span data-stu-id="48564-140">Microsoft.Azure.Commands.Synapse.Models.PSActivityRunsQueryResponse</span></span>

## <span data-ttu-id="48564-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="48564-141">NOTES</span></span>

## <span data-ttu-id="48564-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="48564-142">RELATED LINKS</span></span>
