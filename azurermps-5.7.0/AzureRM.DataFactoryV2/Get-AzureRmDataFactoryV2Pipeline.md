---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: bce1969ed951f196b1ff2c6d5bcc359ee68bc3ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503802"
---
# <span data-ttu-id="41402-101">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="41402-101">Get-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="41402-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="41402-102">SYNOPSIS</span></span>
<span data-ttu-id="41402-103">Ruft Informationen zu Pipelines in Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="41402-103">Gets information about pipelines in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41402-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="41402-104">SYNTAX</span></span>

### <span data-ttu-id="41402-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="41402-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41402-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="41402-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41402-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="41402-107">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2Pipeline -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="41402-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="41402-108">DESCRIPTION</span></span>
<span data-ttu-id="41402-109">Das Get-AzureRmDataFactoryV2Pipeline-Cmdlet ruft Informationen zu Pipelines in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="41402-109">The Get-AzureRmDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="41402-110">Wenn Sie den Namen einer Pipeline angeben, ruft dieses Cmdlet Informationen zu dieser Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="41402-110">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="41402-111">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Pipelines in der Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="41402-111">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="41402-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="41402-112">EXAMPLES</span></span>

### <span data-ttu-id="41402-113">Beispiel 1: Abrufen von Informationen zu allen Pipelines</span><span class="sxs-lookup"><span data-stu-id="41402-113">Example 1: Get information about all pipelines</span></span>
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

<span data-ttu-id="41402-114">Dieser Befehl ruft Informationen zu allen Pipelines in der Data Factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="41402-114">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="41402-115">Sie können entweder einen der folgenden Beispielbefehle verwenden:</span><span class="sxs-lookup"><span data-stu-id="41402-115">You can use either one of the following example commands.</span></span>
<span data-ttu-id="41402-116">Bei der zweiten wird ein DataFactory-Objekt als Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="41402-116">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="41402-117">Beispiel 2: Abrufen von Informationen zu einer bestimmten Pipeline</span><span class="sxs-lookup"><span data-stu-id="41402-117">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="41402-118">Dieser Befehl ruft Informationen zur Pipeline mit dem Namen DPWikisample in der Data Factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="41402-118">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="41402-119">Der Befehl übergibt diese Informationen mithilfe des Pipelineoperators an das Format-List-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41402-119">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="41402-120">Das Windows PowerShell-Cmdlet formatiert die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="41402-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="41402-121">Wenn Sie weitere Informationen wünschen, geben Sie Get-Help Format-List ein.</span><span class="sxs-lookup"><span data-stu-id="41402-121">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="41402-122">Beispiel 3: Abrufen der Eigenschaften für eine bestimmte Pipeline</span><span class="sxs-lookup"><span data-stu-id="41402-122">Example 3: Get the properties for a specific pipeline</span></span>
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

<span data-ttu-id="41402-123">Dieser Befehl ruft Informationen für die Pipeline mit dem Namen DPWikisample in der Data Factory mit dem Namen WikiADF ab und verwendet dann die standardmäßige Punktnotation, um die Aktivitäten-Eigenschaft anzuzeigen, die dieser Pipeline zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="41402-123">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="41402-124">Beispiel 6: Abrufen von Informationen zu Eingaben für die erste Aktivität</span><span class="sxs-lookup"><span data-stu-id="41402-124">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :
```

<span data-ttu-id="41402-125">Dieser Befehl ruft Informationen für die Pipeline mit dem Namen DPWikisample in der Data Factory mit dem Namen WikiADF ab und verwendet dann die standardmäßige Punktnotation, um die Aktivitäten-Eigenschaft anzuzeigen, die dieser Pipeline zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="41402-125">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="41402-126">Der Befehl zeigt die Inputs-Eigenschaft des ersten Elements des Activities-Arrays mithilfe des Format-List-Cmdlets an.</span><span class="sxs-lookup"><span data-stu-id="41402-126">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="41402-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="41402-127">PARAMETERS</span></span>

### <span data-ttu-id="41402-128">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="41402-128">-DataFactory</span></span>
<span data-ttu-id="41402-129">Gibt ein PSDataFactory-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="41402-129">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="41402-130">Dieses Cmdlet ruft Pipelines ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="41402-130">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="41402-131">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="41402-131">-DataFactoryName</span></span>
<span data-ttu-id="41402-132">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="41402-132">Specifies the name of a data factory.</span></span>
<span data-ttu-id="41402-133">Dieses Cmdlet ruft Pipelines ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="41402-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="41402-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41402-134">-DefaultProfile</span></span>
<span data-ttu-id="41402-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="41402-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41402-136">-Name</span><span class="sxs-lookup"><span data-stu-id="41402-136">-Name</span></span>
<span data-ttu-id="41402-137">Gibt den Namen der Pipeline an, über die Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="41402-137">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: PipelineName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41402-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41402-138">-ResourceGroupName</span></span>
<span data-ttu-id="41402-139">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="41402-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="41402-140">Dieses Cmdlet ruft Pipelines ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="41402-140">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="41402-141">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="41402-141">-ResourceId</span></span>
<span data-ttu-id="41402-142">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="41402-142">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41402-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41402-143">CommonParameters</span></span>
<span data-ttu-id="41402-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41402-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41402-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41402-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41402-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="41402-146">INPUTS</span></span>

### <span data-ttu-id="41402-147">System. String</span><span class="sxs-lookup"><span data-stu-id="41402-147">System.String</span></span>
<span data-ttu-id="41402-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="41402-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="41402-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="41402-149">OUTPUTS</span></span>

### <span data-ttu-id="41402-150">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="41402-150">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="41402-151">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="41402-151">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="41402-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="41402-152">NOTES</span></span>
<span data-ttu-id="41402-153">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="41402-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="41402-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="41402-154">RELATED LINKS</span></span>

[<span data-ttu-id="41402-155">Satz-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="41402-155">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="41402-156">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="41402-156">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="41402-157">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="41402-157">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()
