---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 68c524f2c8712b0da0600abda2fa8035dd5a979c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930184"
---
# <span data-ttu-id="99e87-101">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="99e87-101">Get-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="99e87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99e87-102">SYNOPSIS</span></span>
<span data-ttu-id="99e87-103">Ruft Informationen zu Pipelineläufen ab.</span><span class="sxs-lookup"><span data-stu-id="99e87-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="99e87-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99e87-104">SYNTAX</span></span>

### <span data-ttu-id="99e87-105">ByFactoryNameByRunId (Standard)</span><span class="sxs-lookup"><span data-stu-id="99e87-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99e87-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="99e87-106">ByFactoryObjectByRunId</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99e87-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="99e87-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="99e87-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="99e87-108">ByFactoryNameByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99e87-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="99e87-109">DESCRIPTION</span></span>
<span data-ttu-id="99e87-110">Der **Befehl Get-AzDataFactoryV2PipelineRun** gibt Informationen zu den Ausgeführt für die angegebene Pipeline zurück.</span><span class="sxs-lookup"><span data-stu-id="99e87-110">The **Get-AzDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="99e87-111">Wenn PipelineRunId angegeben ist, werden Details für die Ausführung mit dieser ID gezeigt.</span><span class="sxs-lookup"><span data-stu-id="99e87-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="99e87-112">Wenn die PipelineRunId nicht angegeben ist, werden Informationen zu allen Ausgeführten für die Pipelines angezeigt, die zwischen den Werten von LastUpdatedAfter und LastUpdatedBefore ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="99e87-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="99e87-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="99e87-113">EXAMPLES</span></span>

### <span data-ttu-id="99e87-114">Beispiel 1: Informationen für einen Pipelinelauf erhalten</span><span class="sxs-lookup"><span data-stu-id="99e87-114">Example 1: Get information for a pipeline run</span></span>
```
PS C:\> Get-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    RunId             : 61eb095a-fe23-4591-8a97-fade6c65ca72
    PipelineName      : DPWikisample
    LastUpdated       : 9/14/2017 12:21:02 AM
    Parameters        : {[url, http://adfsamplewebapi.azurewebsites.net/api/execute/sample]}
    RunStart          : 9/14/2017 12:20:54 AM
    RunEnd            : 9/14/2017 12:21:02 AM
    DurationInMs      : 8246
    Status            : Succeeded
    Message           :
```

<span data-ttu-id="99e87-115">Dieser Befehl ruft Details zur Ausführung der Pipeline mit der ID "61eb095a-fe23-4591-8a97-fade6c65ca72" ab.</span><span class="sxs-lookup"><span data-stu-id="99e87-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="99e87-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="99e87-116">PARAMETERS</span></span>

### <span data-ttu-id="99e87-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="99e87-117">-DataFactory</span></span>
<span data-ttu-id="99e87-118">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="99e87-118">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObjectByRunId, ByFactoryObjectByPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99e87-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="99e87-119">-DataFactoryName</span></span>
<span data-ttu-id="99e87-120">Der Name der Datenfabrik.</span><span class="sxs-lookup"><span data-stu-id="99e87-120">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99e87-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99e87-121">-DefaultProfile</span></span>
<span data-ttu-id="99e87-122">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="99e87-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99e87-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="99e87-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="99e87-124">Die Zeit, zu der oder nach der die Pipeline ausgeführt wurde, wurde im ISO8601-Format aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="99e87-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99e87-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="99e87-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="99e87-126">Die Zeit, zu der oder vor der die Pipeline ausgeführt wurde, wurde im ISO8601-Format aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="99e87-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99e87-127">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="99e87-127">-PipelineName</span></span>
<span data-ttu-id="99e87-128">Der Name der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="99e87-128">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99e87-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="99e87-129">-PipelineRunId</span></span>
<span data-ttu-id="99e87-130">Die Ausführungs-ID der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="99e87-130">The Run ID of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByRunId, ByFactoryObjectByRunId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99e87-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99e87-131">-ResourceGroupName</span></span>
<span data-ttu-id="99e87-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="99e87-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99e87-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99e87-133">CommonParameters</span></span>
<span data-ttu-id="99e87-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99e87-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99e87-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99e87-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99e87-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="99e87-136">INPUTS</span></span>

### <span data-ttu-id="99e87-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="99e87-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="99e87-138">System.String</span><span class="sxs-lookup"><span data-stu-id="99e87-138">System.String</span></span>

## <span data-ttu-id="99e87-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="99e87-139">OUTPUTS</span></span>

### <span data-ttu-id="99e87-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="99e87-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="99e87-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="99e87-141">NOTES</span></span>

## <span data-ttu-id="99e87-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="99e87-142">RELATED LINKS</span></span>

[<span data-ttu-id="99e87-143">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="99e87-143">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="99e87-144">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="99e87-144">Get-AzDataFactoryV2ActivityRun</span></span>]()

