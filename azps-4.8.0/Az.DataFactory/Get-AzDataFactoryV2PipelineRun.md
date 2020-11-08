---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 889cffd16c836c5f895a9eb587c14cfbe66a45b3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008557"
---
# <span data-ttu-id="c60e4-101">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="c60e4-101">Get-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="c60e4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c60e4-102">SYNOPSIS</span></span>
<span data-ttu-id="c60e4-103">Ruft Informationen zu Pipeline Läufen ab.</span><span class="sxs-lookup"><span data-stu-id="c60e4-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="c60e4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c60e4-104">SYNTAX</span></span>

### <span data-ttu-id="c60e4-105">ByFactoryNameByRunId (Standard)</span><span class="sxs-lookup"><span data-stu-id="c60e4-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c60e4-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="c60e4-106">ByFactoryObjectByRunId</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c60e4-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="c60e4-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c60e4-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="c60e4-108">ByFactoryNameByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c60e4-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c60e4-109">DESCRIPTION</span></span>
<span data-ttu-id="c60e4-110">Der Befehl " **Get-AzDataFactoryV2PipelineRun** " gibt Informationen zu Läufen für die angegebene Pipeline zurück.</span><span class="sxs-lookup"><span data-stu-id="c60e4-110">The **Get-AzDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="c60e4-111">Wenn PipelineRunId angegeben ist, werden die Details für die Ausführung mit dieser ID angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c60e4-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="c60e4-112">Wenn PipelineRunId nicht angegeben ist, werden Informationen zu allen Läufen für die Pipelines angezeigt, die zwischen den Werten von LastUpdatedAfter und LastUpdatedBefore aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="c60e4-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="c60e4-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c60e4-113">EXAMPLES</span></span>

### <span data-ttu-id="c60e4-114">Beispiel 1: Abrufen von Informationen für eine Pipelineausführung</span><span class="sxs-lookup"><span data-stu-id="c60e4-114">Example 1: Get information for a pipeline run</span></span>
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

<span data-ttu-id="c60e4-115">Dieser Befehl ruft Details zur Pipelineausführung mit der ID "61eb095a-FE23-4591-8a97-fade6c65ca72" ab.</span><span class="sxs-lookup"><span data-stu-id="c60e4-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="c60e4-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="c60e4-116">PARAMETERS</span></span>

### <span data-ttu-id="c60e4-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="c60e4-117">-DataFactory</span></span>
<span data-ttu-id="c60e4-118">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c60e4-118">The data factory object.</span></span>

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

### <span data-ttu-id="c60e4-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="c60e4-119">-DataFactoryName</span></span>
<span data-ttu-id="c60e4-120">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="c60e4-120">The data factory name.</span></span>

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

### <span data-ttu-id="c60e4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c60e4-121">-DefaultProfile</span></span>
<span data-ttu-id="c60e4-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c60e4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c60e4-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="c60e4-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="c60e4-124">Die Zeit, zu der oder nach der die Pipeline ausgeführt wurde, im ISO8601-Format aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c60e4-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="c60e4-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="c60e4-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="c60e4-126">Die Zeit, zu der oder vor der die Pipeline ausgeführt wurde, im ISO8601-Format aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c60e4-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="c60e4-127">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="c60e4-127">-PipelineName</span></span>
<span data-ttu-id="c60e4-128">Der Name der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c60e4-128">The pipeline name.</span></span>

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

### <span data-ttu-id="c60e4-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="c60e4-129">-PipelineRunId</span></span>
<span data-ttu-id="c60e4-130">Die Ausführungs-ID der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c60e4-130">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="c60e4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c60e4-131">-ResourceGroupName</span></span>
<span data-ttu-id="c60e4-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c60e4-132">The resource group name.</span></span>

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

### <span data-ttu-id="c60e4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c60e4-133">CommonParameters</span></span>
<span data-ttu-id="c60e4-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c60e4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c60e4-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c60e4-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c60e4-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c60e4-136">INPUTS</span></span>

### <span data-ttu-id="c60e4-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c60e4-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="c60e4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c60e4-138">System.String</span></span>

## <span data-ttu-id="c60e4-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c60e4-139">OUTPUTS</span></span>

### <span data-ttu-id="c60e4-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="c60e4-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="c60e4-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="c60e4-141">NOTES</span></span>

## <span data-ttu-id="c60e4-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c60e4-142">RELATED LINKS</span></span>

[<span data-ttu-id="c60e4-143">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="c60e4-143">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="c60e4-144">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="c60e4-144">Get-AzDataFactoryV2ActivityRun</span></span>]()

