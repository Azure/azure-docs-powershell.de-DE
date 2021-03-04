---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: cd110ebf3b8467e1590ddf52a28d822eebe17092
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930192"
---
# <span data-ttu-id="e8393-101">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e8393-101">Get-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="e8393-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8393-102">SYNOPSIS</span></span>
<span data-ttu-id="e8393-103">Ruft Informationen zu Pipelines in Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="e8393-103">Gets information about pipelines in Data Factory.</span></span>

## <span data-ttu-id="e8393-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8393-104">SYNTAX</span></span>

### <span data-ttu-id="e8393-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="e8393-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8393-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e8393-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8393-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e8393-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Pipeline [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8393-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e8393-108">DESCRIPTION</span></span>
<span data-ttu-id="e8393-109">Das Get-AzDataFactoryV2Pipeline-Cmdlet ruft Informationen zu Pipelines in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="e8393-109">The Get-AzDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="e8393-110">Wenn Sie den Namen einer Pipeline angeben, ruft dieses Cmdlet Informationen zu dieser Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="e8393-110">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="e8393-111">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Pipelines in der Daten factory ab.</span><span class="sxs-lookup"><span data-stu-id="e8393-111">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="e8393-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e8393-112">EXAMPLES</span></span>

### <span data-ttu-id="e8393-113">Beispiel 1: Informationen zu allen Pipelines erhalten</span><span class="sxs-lookup"><span data-stu-id="e8393-113">Example 1: Get information about all pipelines</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 

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

<span data-ttu-id="e8393-114">Dieser Befehl ruft Informationen zu allen Pipelines in der Daten factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="e8393-114">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="e8393-115">Sie können einen der folgenden Beispielbefehle verwenden.</span><span class="sxs-lookup"><span data-stu-id="e8393-115">You can use either one of the following example commands.</span></span>
<span data-ttu-id="e8393-116">Im zweiten wird ein DataFactory-Objekt als Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="e8393-116">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="e8393-117">Beispiel 2: Informationen zu einer bestimmten Pipeline erhalten</span><span class="sxs-lookup"><span data-stu-id="e8393-117">Example 2: Get information about a specific pipeline</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="e8393-118">Dieser Befehl ruft Informationen zur Pipeline mit dem Namen DPWikisample in der Daten factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="e8393-118">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="e8393-119">Der Befehl übergibt diese Informationen mithilfe des Pipelineoperators an Format-List-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8393-119">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e8393-120">Damit Windows PowerShell cmdlet die Ergebnisse formatiert.</span><span class="sxs-lookup"><span data-stu-id="e8393-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="e8393-121">Wenn Sie weitere Informationen erhalten möchten, geben Sie Get-Help Formatliste ein.</span><span class="sxs-lookup"><span data-stu-id="e8393-121">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="e8393-122">Beispiel 3: Erhalten der Eigenschaften für eine bestimmte Pipeline</span><span class="sxs-lookup"><span data-stu-id="e8393-122">Example 3: Get the properties for a specific pipeline</span></span>
```powershell
PS C:\> (Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Activities

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

<span data-ttu-id="e8393-123">Dieser Befehl ruft Informationen für die Pipeline mit dem Namen DPWikisample in der Daten factory mit dem Namen WikiADF ab und verwendet dann die Standardpunkt-Notation, um die der Pipeline zugeordnete Activities-Eigenschaft anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="e8393-123">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="e8393-124">Beispiel 4: Informationen zu Eingaben für die erste Aktivität</span><span class="sxs-lookup"><span data-stu-id="e8393-124">Example 4: Get information about inputs for the first activity</span></span>
```powershell
PS C:\> (Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :
```

<span data-ttu-id="e8393-125">Dieser Befehl ruft Informationen für die Pipeline mit dem Namen DPWikisample in der Daten factory mit dem Namen WikiADF ab und verwendet dann die Standardpunkt-Notation, um die der Pipeline zugeordnete Activities-Eigenschaft anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="e8393-125">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="e8393-126">Der Befehl zeigt die Input-Eigenschaft des ersten Elements des Arrays Aktivitäten mithilfe des cmdlets Format-List an.</span><span class="sxs-lookup"><span data-stu-id="e8393-126">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="e8393-127">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e8393-127">PARAMETERS</span></span>

### <span data-ttu-id="e8393-128">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="e8393-128">-DataFactory</span></span>
<span data-ttu-id="e8393-129">Gibt ein PSDataFactory-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="e8393-129">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="e8393-130">Dieses Cmdlet ruft Pipelines ab, die zur daten factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="e8393-130">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8393-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e8393-131">-DataFactoryName</span></span>
<span data-ttu-id="e8393-132">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="e8393-132">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e8393-133">Dieses Cmdlet ruft Pipelines ab, die zur daten factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="e8393-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8393-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8393-134">-DefaultProfile</span></span>
<span data-ttu-id="e8393-135">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e8393-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8393-136">-Name</span><span class="sxs-lookup"><span data-stu-id="e8393-136">-Name</span></span>
<span data-ttu-id="e8393-137">Gibt den Namen der Pipeline an, über die Informationen zu erhalten sind.</span><span class="sxs-lookup"><span data-stu-id="e8393-137">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: PipelineName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8393-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8393-138">-ResourceGroupName</span></span>
<span data-ttu-id="e8393-139">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e8393-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e8393-140">Dieses Cmdlet ruft Pipelines ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="e8393-140">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8393-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8393-141">-ResourceId</span></span>
<span data-ttu-id="e8393-142">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="e8393-142">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8393-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8393-143">CommonParameters</span></span>
<span data-ttu-id="e8393-144">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8393-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8393-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8393-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8393-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e8393-146">INPUTS</span></span>

### <span data-ttu-id="e8393-147">System.String</span><span class="sxs-lookup"><span data-stu-id="e8393-147">System.String</span></span>

### <span data-ttu-id="e8393-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e8393-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="e8393-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e8393-149">OUTPUTS</span></span>

### <span data-ttu-id="e8393-150">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="e8393-150">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="e8393-151">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e8393-151">NOTES</span></span>
<span data-ttu-id="e8393-152">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factory</span><span class="sxs-lookup"><span data-stu-id="e8393-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e8393-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e8393-153">RELATED LINKS</span></span>

[<span data-ttu-id="e8393-154">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e8393-154">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="e8393-155">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e8393-155">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="e8393-156">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e8393-156">Invoke-AzDataFactoryV2Pipeline</span></span>]()
