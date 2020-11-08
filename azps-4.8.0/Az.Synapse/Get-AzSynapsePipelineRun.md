---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
ms.openlocfilehash: 365311b156b8bd6f2c61da760c6b82a3b2d5dfb4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165925"
---
# <span data-ttu-id="c485b-101">Get-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="c485b-101">Get-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="c485b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c485b-102">SYNOPSIS</span></span>
<span data-ttu-id="c485b-103">Ruft Informationen zu Pipeline Läufen ab.</span><span class="sxs-lookup"><span data-stu-id="c485b-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="c485b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c485b-104">SYNTAX</span></span>

### <span data-ttu-id="c485b-105">GetByNameAndId (Standard)</span><span class="sxs-lookup"><span data-stu-id="c485b-105">GetByNameAndId (Default)</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c485b-106">GetByNameAndTime</span><span class="sxs-lookup"><span data-stu-id="c485b-106">GetByNameAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c485b-107">GetByObjectAndId</span><span class="sxs-lookup"><span data-stu-id="c485b-107">GetByObjectAndId</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c485b-108">GetByObjectAndTime</span><span class="sxs-lookup"><span data-stu-id="c485b-108">GetByObjectAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c485b-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c485b-109">DESCRIPTION</span></span>
<span data-ttu-id="c485b-110">Der Befehl " **Get-AzSynapsePipelineRun** " gibt Informationen zu Läufen für die angegebene Pipeline zurück.</span><span class="sxs-lookup"><span data-stu-id="c485b-110">The **Get-AzSynapsePipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="c485b-111">Wenn PipelineRunId angegeben ist, werden die Details für die Ausführung mit dieser ID angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c485b-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="c485b-112">Wenn PipelineRunId nicht angegeben ist, werden Informationen zu allen Läufen für die Pipelines angezeigt, die zwischen den Werten von RunStartedAfter und RunStartedBefore aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="c485b-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of RunStartedAfter and RunStartedBefore.</span></span>

## <span data-ttu-id="c485b-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c485b-113">EXAMPLES</span></span>

### <span data-ttu-id="c485b-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c485b-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"
```

<span data-ttu-id="c485b-115">Dieser Befehl ruft Details zur Pipelineausführung mit der ID "61eb095a-FE23-4591-8a97-fade6c65ca72" ab.</span><span class="sxs-lookup"><span data-stu-id="c485b-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="c485b-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="c485b-116">PARAMETERS</span></span>

### <span data-ttu-id="c485b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c485b-117">-DefaultProfile</span></span>
<span data-ttu-id="c485b-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c485b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c485b-119">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="c485b-119">-PipelineName</span></span>
<span data-ttu-id="c485b-120">Der Name der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c485b-120">The pipeline name.</span></span>

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

### <span data-ttu-id="c485b-121">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="c485b-121">-PipelineRunId</span></span>
<span data-ttu-id="c485b-122">Der Pipeline Ausführungs Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="c485b-122">The pipeline run identifier.</span></span>

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

### <span data-ttu-id="c485b-123">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="c485b-123">-RunStartedAfter</span></span>
<span data-ttu-id="c485b-124">Die Zeit, zu der oder nach der das Run-Ereignis im Format "ISO 8601" aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c485b-124">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="c485b-125">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="c485b-125">-RunStartedBefore</span></span>
<span data-ttu-id="c485b-126">Die Zeitspanne, zu der das Run-Ereignis im Format "ISO 8601" aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c485b-126">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="c485b-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c485b-127">-WorkspaceName</span></span>
<span data-ttu-id="c485b-128">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="c485b-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c485b-129">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="c485b-129">-WorkspaceObject</span></span>
<span data-ttu-id="c485b-130">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="c485b-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c485b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c485b-131">CommonParameters</span></span>
<span data-ttu-id="c485b-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c485b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c485b-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c485b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c485b-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c485b-134">INPUTS</span></span>

### <span data-ttu-id="c485b-135">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c485b-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="c485b-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c485b-136">OUTPUTS</span></span>

### <span data-ttu-id="c485b-137">Microsoft. Azure. Commands. Synapse. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="c485b-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="c485b-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="c485b-138">NOTES</span></span>

## <span data-ttu-id="c485b-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c485b-139">RELATED LINKS</span></span>
