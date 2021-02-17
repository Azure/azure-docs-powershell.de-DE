---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
ms.openlocfilehash: 365311b156b8bd6f2c61da760c6b82a3b2d5dfb4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164609"
---
# <span data-ttu-id="6433d-101">Get-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="6433d-101">Get-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="6433d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6433d-102">SYNOPSIS</span></span>
<span data-ttu-id="6433d-103">Ruft Informationen zu Pipelineläufen ab.</span><span class="sxs-lookup"><span data-stu-id="6433d-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="6433d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6433d-104">SYNTAX</span></span>

### <span data-ttu-id="6433d-105">GetByNameAndId (Standard)</span><span class="sxs-lookup"><span data-stu-id="6433d-105">GetByNameAndId (Default)</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6433d-106">GetByNameAndTime</span><span class="sxs-lookup"><span data-stu-id="6433d-106">GetByNameAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6433d-107">GetByObjectAndId</span><span class="sxs-lookup"><span data-stu-id="6433d-107">GetByObjectAndId</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6433d-108">GetByObjectAndTime</span><span class="sxs-lookup"><span data-stu-id="6433d-108">GetByObjectAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6433d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6433d-109">DESCRIPTION</span></span>
<span data-ttu-id="6433d-110">Der **Befehl "Get-AzSynapsePipelineRun"** gibt Informationen zu den Ausgeführten für die angegebene Pipeline zurück.</span><span class="sxs-lookup"><span data-stu-id="6433d-110">The **Get-AzSynapsePipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="6433d-111">Wenn "PipelineRunId" angegeben ist, werden Details für die Ausführung mit dieser ID angegeben.</span><span class="sxs-lookup"><span data-stu-id="6433d-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="6433d-112">Wenn "PipelineRunId" nicht angegeben ist, werden Informationen zu allen Ausgeführten für die Pipelines angezeigt, die zwischen den Werten von "RunStartedAfter" und "RunStartedBefore" ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="6433d-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of RunStartedAfter and RunStartedBefore.</span></span>

## <span data-ttu-id="6433d-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6433d-113">EXAMPLES</span></span>

### <span data-ttu-id="6433d-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6433d-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"
```

<span data-ttu-id="6433d-115">Dieser Befehl ruft Details zum Pipelinelauf mit der ID "61eb095a-fe23-4591-8a97-fade6c65ca72" ab.</span><span class="sxs-lookup"><span data-stu-id="6433d-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="6433d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6433d-116">PARAMETERS</span></span>

### <span data-ttu-id="6433d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6433d-117">-DefaultProfile</span></span>
<span data-ttu-id="6433d-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6433d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6433d-119">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="6433d-119">-PipelineName</span></span>
<span data-ttu-id="6433d-120">Der Pipelinename.</span><span class="sxs-lookup"><span data-stu-id="6433d-120">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6433d-121">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="6433d-121">-PipelineRunId</span></span>
<span data-ttu-id="6433d-122">Der Pipeline-Ausführungsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="6433d-122">The pipeline run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndId, GetByObjectAndId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6433d-123">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="6433d-123">-RunStartedAfter</span></span>
<span data-ttu-id="6433d-124">Die Uhrzeit, zu oder nach der das Ausführungsereignis im FORMAT "ISO 8601" aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="6433d-124">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6433d-125">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="6433d-125">-RunStartedBefore</span></span>
<span data-ttu-id="6433d-126">Der Zeitpunkt oder vor dem das Ausführungsereignis im FORMAT ISO 8601 aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="6433d-126">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6433d-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6433d-127">-WorkspaceName</span></span>
<span data-ttu-id="6433d-128">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="6433d-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndId, GetByNameAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6433d-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6433d-129">-WorkspaceObject</span></span>
<span data-ttu-id="6433d-130">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="6433d-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObjectAndId, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6433d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6433d-131">CommonParameters</span></span>
<span data-ttu-id="6433d-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6433d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6433d-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6433d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6433d-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6433d-134">INPUTS</span></span>

### <span data-ttu-id="6433d-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6433d-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="6433d-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6433d-136">OUTPUTS</span></span>

### <span data-ttu-id="6433d-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="6433d-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="6433d-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6433d-138">NOTES</span></span>

## <span data-ttu-id="6433d-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6433d-139">RELATED LINKS</span></span>
