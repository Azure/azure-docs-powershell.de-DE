---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseactivityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
ms.openlocfilehash: fd300a54b3f35aa69a94bfee69cfcf7ca60f95a8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176711"
---
# <span data-ttu-id="393f0-101">Get-AzSynapseActivityRun</span><span class="sxs-lookup"><span data-stu-id="393f0-101">Get-AzSynapseActivityRun</span></span>

## <span data-ttu-id="393f0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="393f0-102">SYNOPSIS</span></span>
<span data-ttu-id="393f0-103">Ruft Informationen zu Aktivitäts Läufen für eine Pipelineausführung ab.</span><span class="sxs-lookup"><span data-stu-id="393f0-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="393f0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="393f0-104">SYNTAX</span></span>

### <span data-ttu-id="393f0-105">GetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="393f0-105">GetByName (Default)</span></span>
```
Get-AzSynapseActivityRun -WorkspaceName <String> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="393f0-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="393f0-106">GetByObject</span></span>
```
Get-AzSynapseActivityRun -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="393f0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="393f0-107">DESCRIPTION</span></span>
<span data-ttu-id="393f0-108">Das Cmdlet " **Get-AzSynapseActivityRun** " Ruft Informationen zu ausgeführten Läufen im Arbeitsbereich für den angegebenen Pipeline Durchlauf ab, der im angegebenen Zeitrahmen stattgefunden hat.</span><span class="sxs-lookup"><span data-stu-id="393f0-108">The **Get-AzSynapseActivityRun** cmdlet gets information about runs in workspace for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="393f0-109">Darüber hinaus können Sie Filter für den Aktivitätsnamen und den Status der Ausführung angeben.</span><span class="sxs-lookup"><span data-stu-id="393f0-109">Additionally, you can specify filters for activity name and the status of the run.</span></span>

## <span data-ttu-id="393f0-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="393f0-110">EXAMPLES</span></span>

### <span data-ttu-id="393f0-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="393f0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseActivityRun -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="393f0-112">Dieser Befehl ruft Details zu allen Aktivitäten ab, die in der Pipeline namens "ContosoPipeline Run" mit der ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" ausgeführt werden, die zwischen "2018-09-01T21:00" und "2018-09-30T21:00" erfolgte.</span><span class="sxs-lookup"><span data-stu-id="393f0-112">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00".</span></span>

### <span data-ttu-id="393f0-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="393f0-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseActivityRun -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="393f0-114">Dieser Befehl ruft Details zu allen Aktivitäten ab, die in der Pipeline namens ContosoPipeline ausgeführt werden und mit der ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" ausgeführt werden, die zwischen "2018-09-01T21:00" und "2018-09-30T21:00" durch Pipeline erfolgte.</span><span class="sxs-lookup"><span data-stu-id="393f0-114">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00" through pipeline.</span></span>

## <span data-ttu-id="393f0-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="393f0-115">PARAMETERS</span></span>

### <span data-ttu-id="393f0-116">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="393f0-116">-ActivityName</span></span>
<span data-ttu-id="393f0-117">Der Name der Aktivität.</span><span class="sxs-lookup"><span data-stu-id="393f0-117">The name of the activity.</span></span>

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

### <span data-ttu-id="393f0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="393f0-118">-DefaultProfile</span></span>
<span data-ttu-id="393f0-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="393f0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="393f0-120">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="393f0-120">-PipelineName</span></span>
<span data-ttu-id="393f0-121">Der Name der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="393f0-121">The pipeline name.</span></span>

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

### <span data-ttu-id="393f0-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="393f0-122">-PipelineRunId</span></span>
<span data-ttu-id="393f0-123">Der Pipeline Ausführungs Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="393f0-123">The pipeline run identifier.</span></span>

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

### <span data-ttu-id="393f0-124">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="393f0-124">-RunStartedAfter</span></span>
<span data-ttu-id="393f0-125">Die Zeit, zu der oder nach der das Run-Ereignis im Format "ISO 8601" aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="393f0-125">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="393f0-126">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="393f0-126">-RunStartedBefore</span></span>
<span data-ttu-id="393f0-127">Die Zeitspanne, zu der das Run-Ereignis im Format "ISO 8601" aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="393f0-127">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="393f0-128">-Status</span><span class="sxs-lookup"><span data-stu-id="393f0-128">-Status</span></span>
<span data-ttu-id="393f0-129">Der Status der Pipelineausführung.</span><span class="sxs-lookup"><span data-stu-id="393f0-129">The status of the pipeline run.</span></span>

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

### <span data-ttu-id="393f0-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="393f0-130">-WorkspaceName</span></span>
<span data-ttu-id="393f0-131">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="393f0-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="393f0-132">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="393f0-132">-WorkspaceObject</span></span>
<span data-ttu-id="393f0-133">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="393f0-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="393f0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="393f0-134">CommonParameters</span></span>
<span data-ttu-id="393f0-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="393f0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="393f0-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="393f0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="393f0-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="393f0-137">INPUTS</span></span>

### <span data-ttu-id="393f0-138">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="393f0-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="393f0-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="393f0-139">OUTPUTS</span></span>

### <span data-ttu-id="393f0-140">Microsoft. Azure. Commands. Synapse. Models. PSActivityRunsQueryResponse</span><span class="sxs-lookup"><span data-stu-id="393f0-140">Microsoft.Azure.Commands.Synapse.Models.PSActivityRunsQueryResponse</span></span>

## <span data-ttu-id="393f0-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="393f0-141">NOTES</span></span>

## <span data-ttu-id="393f0-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="393f0-142">RELATED LINKS</span></span>
