---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
ms.openlocfilehash: 05adb3533604188aa5331d0d4b3f41a2aeba292d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503801"
---
# <span data-ttu-id="685db-101">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="685db-101">Get-AzureRmDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="685db-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="685db-102">SYNOPSIS</span></span>
<span data-ttu-id="685db-103">Ruft Informationen zu Pipeline Läufen ab.</span><span class="sxs-lookup"><span data-stu-id="685db-103">Gets information about pipeline runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="685db-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="685db-104">SYNTAX</span></span>

### <span data-ttu-id="685db-105">ByFactoryNameByRunId (Standard)</span><span class="sxs-lookup"><span data-stu-id="685db-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="685db-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="685db-106">ByFactoryObjectByRunId</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="685db-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="685db-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="685db-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="685db-108">ByFactoryNameByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="685db-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="685db-109">DESCRIPTION</span></span>
<span data-ttu-id="685db-110">Der Befehl " **Get-AzureRmDataFactoryV2PipelineRun** " gibt Informationen zu Läufen für die angegebene Pipeline zurück.</span><span class="sxs-lookup"><span data-stu-id="685db-110">The **Get-AzureRmDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="685db-111">Wenn PipelineRunId angegeben ist, werden die Details für die Ausführung mit dieser ID angezeigt.</span><span class="sxs-lookup"><span data-stu-id="685db-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="685db-112">Wenn PipelineRunId nicht angegeben ist, werden Informationen zu allen Läufen für die angegebene Pipeline angezeigt, die zwischen den Werten von LastUpdatedAfter und LastUpdatedBefore aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="685db-112">If the PipelineRunId is not specified, then it shows information about all runs for the specified pipeline that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="685db-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="685db-113">EXAMPLES</span></span>

### <span data-ttu-id="685db-114">Beispiel 1: Abrufen von Informationen für eine Pipeline konzentrieren-Ausführung</span><span class="sxs-lookup"><span data-stu-id="685db-114">Example 1: Get information for a pipline run</span></span>
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

<span data-ttu-id="685db-115">Dieser Befehl ruft Details zur Pipelineausführung mit der ID "61eb095a-FE23-4591-8a97-fade6c65ca72" ab.</span><span class="sxs-lookup"><span data-stu-id="685db-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="685db-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="685db-116">PARAMETERS</span></span>

### <span data-ttu-id="685db-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="685db-117">-DataFactory</span></span>
<span data-ttu-id="685db-118">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="685db-118">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObjectByRunId, ByFactoryObjectByPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="685db-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="685db-119">-DataFactoryName</span></span>
<span data-ttu-id="685db-120">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="685db-120">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="685db-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="685db-121">-DefaultProfile</span></span>
<span data-ttu-id="685db-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="685db-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="685db-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="685db-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="685db-124">Die Zeit, zu der oder nach der die Pipeline ausgeführt wurde, im ISO8601-Format aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="685db-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="685db-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="685db-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="685db-126">Die Zeit, zu der oder vor der die Pipeline ausgeführt wurde, im ISO8601-Format aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="685db-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="685db-127">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="685db-127">-PipelineName</span></span>
<span data-ttu-id="685db-128">Der Name der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="685db-128">The pipeline name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="685db-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="685db-129">-PipelineRunId</span></span>
<span data-ttu-id="685db-130">Die Ausführungs-ID der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="685db-130">The Run ID of the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByRunId, ByFactoryObjectByRunId
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="685db-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="685db-131">-ResourceGroupName</span></span>
<span data-ttu-id="685db-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="685db-132">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="685db-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="685db-133">CommonParameters</span></span>
<span data-ttu-id="685db-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="685db-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="685db-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="685db-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="685db-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="685db-136">INPUTS</span></span>

### <span data-ttu-id="685db-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="685db-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="685db-138">System. String</span><span class="sxs-lookup"><span data-stu-id="685db-138">System.String</span></span>

## <span data-ttu-id="685db-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="685db-139">OUTPUTS</span></span>

### <span data-ttu-id="685db-140">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipelineRun, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="685db-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="685db-141">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="685db-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="685db-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="685db-142">NOTES</span></span>

## <span data-ttu-id="685db-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="685db-143">RELATED LINKS</span></span>

[<span data-ttu-id="685db-144">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="685db-144">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="685db-145">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="685db-145">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

