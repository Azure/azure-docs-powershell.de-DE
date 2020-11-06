---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
ms.openlocfilehash: ac5735d66a7b44c7183a9af3a32c01445f2b3486
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499621"
---
# <span data-ttu-id="251a5-101">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="251a5-101">Get-AzureRmDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="251a5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="251a5-102">SYNOPSIS</span></span>
<span data-ttu-id="251a5-103">Ruft Informationen zu Pipeline Läufen ab.</span><span class="sxs-lookup"><span data-stu-id="251a5-103">Gets information about pipeline runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="251a5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="251a5-104">SYNTAX</span></span>

### <span data-ttu-id="251a5-105">ByFactoryNameByRunId (Standard)</span><span class="sxs-lookup"><span data-stu-id="251a5-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="251a5-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="251a5-106">ByFactoryObjectByRunId</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="251a5-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="251a5-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="251a5-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="251a5-108">ByFactoryNameByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="251a5-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="251a5-109">DESCRIPTION</span></span>
<span data-ttu-id="251a5-110">Der Befehl " **Get-AzureRmDataFactoryV2PipelineRun** " gibt Informationen zu Läufen für die angegebene Pipeline zurück.</span><span class="sxs-lookup"><span data-stu-id="251a5-110">The **Get-AzureRmDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="251a5-111">Wenn PipelineRunId angegeben ist, werden die Details für die Ausführung mit dieser ID angezeigt.</span><span class="sxs-lookup"><span data-stu-id="251a5-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="251a5-112">Wenn PipelineRunId nicht angegeben ist, werden Informationen zu allen Läufen für die angegebene Pipeline angezeigt, die zwischen den Werten von LastUpdatedAfter und LastUpdatedBefore aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="251a5-112">If the PipelineRunId is not specified, then it shows information about all runs for the specified pipeline that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="251a5-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="251a5-113">EXAMPLES</span></span>

### <span data-ttu-id="251a5-114">Beispiel 1: Abrufen von Informationen für eine Pipeline konzentrieren-Ausführung</span><span class="sxs-lookup"><span data-stu-id="251a5-114">Example 1: Get information for a pipline run</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"

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

<span data-ttu-id="251a5-115">Dieser Befehl ruft Details zur Pipelineausführung mit der ID "61eb095a-FE23-4591-8a97-fade6c65ca72" ab.</span><span class="sxs-lookup"><span data-stu-id="251a5-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="251a5-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="251a5-116">PARAMETERS</span></span>

### <span data-ttu-id="251a5-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="251a5-117">-DataFactory</span></span>
<span data-ttu-id="251a5-118">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="251a5-118">The data factory object.</span></span>

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

### <span data-ttu-id="251a5-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="251a5-119">-DataFactoryName</span></span>
<span data-ttu-id="251a5-120">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="251a5-120">The data factory name.</span></span>

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

### <span data-ttu-id="251a5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="251a5-121">-DefaultProfile</span></span>
<span data-ttu-id="251a5-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="251a5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="251a5-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="251a5-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="251a5-124">Die Zeit, zu der oder nach der die Pipeline ausgeführt wurde, im ISO8601-Format aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="251a5-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="251a5-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="251a5-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="251a5-126">Die Zeit, zu der oder vor der die Pipeline ausgeführt wurde, im ISO8601-Format aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="251a5-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="251a5-127">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="251a5-127">-PipelineName</span></span>
<span data-ttu-id="251a5-128">Der Name der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="251a5-128">The pipeline name.</span></span>

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

### <span data-ttu-id="251a5-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="251a5-129">-PipelineRunId</span></span>
<span data-ttu-id="251a5-130">Die Ausführungs-ID der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="251a5-130">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="251a5-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="251a5-131">-ResourceGroupName</span></span>
<span data-ttu-id="251a5-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="251a5-132">The resource group name.</span></span>

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

### <span data-ttu-id="251a5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="251a5-133">CommonParameters</span></span>
<span data-ttu-id="251a5-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="251a5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="251a5-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="251a5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="251a5-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="251a5-136">INPUTS</span></span>

### <span data-ttu-id="251a5-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="251a5-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="251a5-138">Parameter: DataFactory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="251a5-138">Parameters: DataFactory (ByValue)</span></span>

### <span data-ttu-id="251a5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="251a5-139">System.String</span></span>

## <span data-ttu-id="251a5-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="251a5-140">OUTPUTS</span></span>

### <span data-ttu-id="251a5-141">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="251a5-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="251a5-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="251a5-142">NOTES</span></span>

## <span data-ttu-id="251a5-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="251a5-143">RELATED LINKS</span></span>

[<span data-ttu-id="251a5-144">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="251a5-144">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="251a5-145">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="251a5-145">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

