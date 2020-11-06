---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: b8065c3b4aa958c9138316488b7ca8a9b982d97c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505097"
---
# <span data-ttu-id="92776-101">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="92776-101">Get-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="92776-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="92776-102">SYNOPSIS</span></span>
<span data-ttu-id="92776-103">Ruft Informationen zu Pipelines in Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="92776-103">Gets information about pipelines in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92776-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="92776-104">SYNTAX</span></span>

### <span data-ttu-id="92776-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="92776-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="92776-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="92776-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
```

## <span data-ttu-id="92776-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92776-107">DESCRIPTION</span></span>
<span data-ttu-id="92776-108">Das Get-AzureRmDataFactoryV2Pipeline-Cmdlet ruft Informationen zu Pipelines in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="92776-108">The Get-AzureRmDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="92776-109">Wenn Sie den Namen einer Pipeline angeben, ruft dieses Cmdlet Informationen zu dieser Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="92776-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="92776-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Pipelines in der Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="92776-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="92776-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="92776-111">EXAMPLES</span></span>

### <span data-ttu-id="92776-112">Beispiel 1: Abrufen von Informationen zu allen Pipelines</span><span class="sxs-lookup"><span data-stu-id="92776-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyWebActivity}
    Parameters        : {[url, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}

    PipelineName      : DPTwittersample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}

```

<span data-ttu-id="92776-113">Dieser Befehl ruft Informationen zu allen Pipelines in der Data Factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="92776-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="92776-114">Sie können entweder einen der folgenden Beispielbefehle verwenden:</span><span class="sxs-lookup"><span data-stu-id="92776-114">You can use either one of the following example commands.</span></span>
<span data-ttu-id="92776-115">Bei der zweiten wird ein DataFactory-Objekt als Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="92776-115">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="92776-116">Beispiel 2: Abrufen von Informationen zu einer bestimmten Pipeline</span><span class="sxs-lookup"><span data-stu-id="92776-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="92776-117">Dieser Befehl ruft Informationen zur Pipeline mit dem Namen DPWikisample in der Data Factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="92776-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="92776-118">Der Befehl übergibt diese Informationen mithilfe des Pipelineoperators an das Format-List-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92776-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="92776-119">Das Windows PowerShell-Cmdlet formatiert die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="92776-119">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="92776-120">Wenn Sie weitere Informationen wünschen, geben Sie Get-Help Format-List ein.</span><span class="sxs-lookup"><span data-stu-id="92776-120">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="92776-121">Beispiel 3: Abrufen der Eigenschaften für eine bestimmte Pipeline</span><span class="sxs-lookup"><span data-stu-id="92776-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Activities

    Source                          : Microsoft.Azure.Management.DataFactory.Models.BlobSource
    Sink                            : Microsoft.Azure.Management.DataFactory.Models.BlobSink
    Translator                      :
    EnableStaging                   :
    StagingSettings                 :
    ParallelCopies                  :
    CloudDataMovementUnits          :
    EnableSkipIncompatibleRow       :
    RedirectIncompatibleRowSettings :
    Inputs                          : {}
    Outputs                         : {}
    LinkedServiceName               :
    Policy                          :
    Name                            : MyCopyActivity_0_0
    Description                     :
    DependsOn                       :

    Source                          : Microsoft.Azure.Management.DataFactory.Models.BlobSource
    Sink                            : Microsoft.Azure.Management.DataFactory.Models.BlobSink
    Translator                      :
    EnableStaging                   :
    StagingSettings                 :
    ParallelCopies                  :
    CloudDataMovementUnits          :
    EnableSkipIncompatibleRow       :
    RedirectIncompatibleRowSettings :
    Inputs                          : {}
    Outputs                         : {}
    LinkedServiceName               :
    Policy                          :
    Name                            : MyCopyActivity_1_0
    Description                     :
    DependsOn                       : {Microsoft.Azure.Management.DataFactory.Models.ActivityDependency}

```

<span data-ttu-id="92776-122">Dieser Befehl ruft Informationen für die Pipeline mit dem Namen DPWikisample in der Data Factory mit dem Namen WikiADF ab und verwendet dann die standardmäßige Punktnotation, um die Aktivitäten-Eigenschaft anzuzeigen, die dieser Pipeline zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="92776-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="92776-123">Beispiel 6: Abrufen von Informationen zu Eingaben für die erste Aktivität</span><span class="sxs-lookup"><span data-stu-id="92776-123">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :

```

<span data-ttu-id="92776-124">Dieser Befehl ruft Informationen für die Pipeline mit dem Namen DPWikisample in der Data Factory mit dem Namen WikiADF ab und verwendet dann die standardmäßige Punktnotation, um die Aktivitäten-Eigenschaft anzuzeigen, die dieser Pipeline zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="92776-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="92776-125">Der Befehl zeigt die Inputs-Eigenschaft des ersten Elements des Activities-Arrays mithilfe des Format-List-Cmdlets an.</span><span class="sxs-lookup"><span data-stu-id="92776-125">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="92776-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="92776-126">PARAMETERS</span></span>

### <span data-ttu-id="92776-127">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="92776-127">-DataFactory</span></span>
<span data-ttu-id="92776-128">Gibt ein PSDataFactory-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="92776-128">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="92776-129">Dieses Cmdlet ruft Pipelines ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="92776-129">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92776-130">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="92776-130">-DataFactoryName</span></span>
<span data-ttu-id="92776-131">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="92776-131">Specifies the name of a data factory.</span></span>
<span data-ttu-id="92776-132">Dieses Cmdlet ruft Pipelines ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="92776-132">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92776-133">-Name</span><span class="sxs-lookup"><span data-stu-id="92776-133">-Name</span></span>
<span data-ttu-id="92776-134">Gibt den Namen der Pipeline an, über die Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="92776-134">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PipelineName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92776-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92776-135">-ResourceGroupName</span></span>
<span data-ttu-id="92776-136">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="92776-136">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="92776-137">Dieses Cmdlet ruft Pipelines ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="92776-137">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="92776-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="92776-138">INPUTS</span></span>

### <span data-ttu-id="92776-139">System. String</span><span class="sxs-lookup"><span data-stu-id="92776-139">System.String</span></span>
<span data-ttu-id="92776-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="92776-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="92776-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="92776-141">OUTPUTS</span></span>

### <span data-ttu-id="92776-142">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="92776-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="92776-143">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="92776-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>


## <span data-ttu-id="92776-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="92776-144">NOTES</span></span>
<span data-ttu-id="92776-145">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="92776-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="92776-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="92776-146">RELATED LINKS</span></span>
[<span data-ttu-id="92776-147">Satz-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="92776-147">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="92776-148">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="92776-148">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="92776-149">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="92776-149">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()
