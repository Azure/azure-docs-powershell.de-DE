---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 6605fa005d8ca5c41c0ea60ee21a15c0196ae832
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294575"
---
# <span data-ttu-id="7138a-101">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="7138a-101">Get-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="7138a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7138a-102">SYNOPSIS</span></span>
<span data-ttu-id="7138a-103">Ruft Informationen zu Pipelines in Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="7138a-103">Gets information about pipelines in Data Factory.</span></span>

## <span data-ttu-id="7138a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7138a-104">SYNTAX</span></span>

### <span data-ttu-id="7138a-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7138a-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7138a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7138a-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7138a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7138a-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Pipeline [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7138a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7138a-108">DESCRIPTION</span></span>
<span data-ttu-id="7138a-109">Das Get-AzDataFactoryV2Pipeline Cmdlet ruft Informationen zu Pipelines in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="7138a-109">The Get-AzDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="7138a-110">Wenn Sie den Namen einer Pipeline angeben, ruft dieses Cmdlet Informationen zu dieser Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="7138a-110">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="7138a-111">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Pipelines in der Daten factory ab.</span><span class="sxs-lookup"><span data-stu-id="7138a-111">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="7138a-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7138a-112">EXAMPLES</span></span>

### <span data-ttu-id="7138a-113">Beispiel 1: Informationen zu allen Pipelines</span><span class="sxs-lookup"><span data-stu-id="7138a-113">Example 1: Get information about all pipelines</span></span>
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

<span data-ttu-id="7138a-114">Dieser Befehl ruft Informationen zu allen Pipelines in der Daten factory namens WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="7138a-114">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="7138a-115">Sie können einen der folgenden Beispielbefehle verwenden.</span><span class="sxs-lookup"><span data-stu-id="7138a-115">You can use either one of the following example commands.</span></span>
<span data-ttu-id="7138a-116">Im zweiten Parameter wird ein DataFactory-Objekt als Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="7138a-116">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="7138a-117">Beispiel 2: Informationen zu einer bestimmten Pipeline</span><span class="sxs-lookup"><span data-stu-id="7138a-117">Example 2: Get information about a specific pipeline</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="7138a-118">Dieser Befehl ruft Informationen über die Pipeline mit dem Namen DPWikisample in der Daten factory namens WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="7138a-118">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="7138a-119">Der Befehl übergibt diese Informationen mithilfe des Pipelineoperators Format-List an das Format-List Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7138a-119">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7138a-120">Auf Windows PowerShell cmdlet werden die Ergebnisse formatiert.</span><span class="sxs-lookup"><span data-stu-id="7138a-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="7138a-121">Weitere Informationen erhalten Sie, wenn Sie Get-Help "Format-Liste" eingeben.</span><span class="sxs-lookup"><span data-stu-id="7138a-121">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="7138a-122">Beispiel 3: Erhalten der Eigenschaften für eine bestimmte Pipeline</span><span class="sxs-lookup"><span data-stu-id="7138a-122">Example 3: Get the properties for a specific pipeline</span></span>
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

<span data-ttu-id="7138a-123">Dieser Befehl ruft Informationen für die Pipeline mit dem Namen DPWikisample in der Daten factory mit dem Namen WikiADF ab und verwendet dann die standardmäßige Punkt-Notation, um die dieser Pipeline zugeordnete Eigenschaft "Activities" anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7138a-123">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="7138a-124">Beispiel 4: Informationen zu Eingaben für die erste Aktivität</span><span class="sxs-lookup"><span data-stu-id="7138a-124">Example 4: Get information about inputs for the first activity</span></span>
```powershell
PS C:\> (Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :
```

<span data-ttu-id="7138a-125">Dieser Befehl ruft Informationen für die Pipeline mit dem Namen DPWikisample in der Daten factory mit dem Namen WikiADF ab und verwendet dann die standardmäßige Punkt-Notation, um die dieser Pipeline zugeordnete Eigenschaft "Activities" anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7138a-125">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="7138a-126">Der Befehl zeigt die Eingabeeigenschaft des ersten Elements des Array "Aktivitäten" mithilfe des cmdlets Format-List an.</span><span class="sxs-lookup"><span data-stu-id="7138a-126">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="7138a-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7138a-127">PARAMETERS</span></span>

### <span data-ttu-id="7138a-128">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="7138a-128">-DataFactory</span></span>
<span data-ttu-id="7138a-129">Gibt ein "PSDataFactory"-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="7138a-129">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="7138a-130">Dieses Cmdlet ruft Pipelines ab, die zu der von diesem Parameter angegebenen Daten factory gehören.</span><span class="sxs-lookup"><span data-stu-id="7138a-130">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7138a-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7138a-131">-DataFactoryName</span></span>
<span data-ttu-id="7138a-132">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="7138a-132">Specifies the name of a data factory.</span></span>
<span data-ttu-id="7138a-133">Dieses Cmdlet ruft Pipelines ab, die zu der von diesem Parameter angegebenen Daten factory gehören.</span><span class="sxs-lookup"><span data-stu-id="7138a-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7138a-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7138a-134">-DefaultProfile</span></span>
<span data-ttu-id="7138a-135">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7138a-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7138a-136">-Name</span><span class="sxs-lookup"><span data-stu-id="7138a-136">-Name</span></span>
<span data-ttu-id="7138a-137">Gibt den Namen der Pipeline an, über die Informationen angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7138a-137">Specifies the name of the pipeline about which to get information.</span></span>

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

### <span data-ttu-id="7138a-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7138a-138">-ResourceGroupName</span></span>
<span data-ttu-id="7138a-139">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="7138a-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="7138a-140">Dieses Cmdlet ruft Pipelines ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="7138a-140">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7138a-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7138a-141">-ResourceId</span></span>
<span data-ttu-id="7138a-142">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="7138a-142">The Azure resource ID.</span></span>

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

### <span data-ttu-id="7138a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7138a-143">CommonParameters</span></span>
<span data-ttu-id="7138a-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7138a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7138a-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7138a-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7138a-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7138a-146">INPUTS</span></span>

### <span data-ttu-id="7138a-147">System.String</span><span class="sxs-lookup"><span data-stu-id="7138a-147">System.String</span></span>

### <span data-ttu-id="7138a-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="7138a-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="7138a-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7138a-149">OUTPUTS</span></span>

### <span data-ttu-id="7138a-150">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="7138a-150">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="7138a-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7138a-151">NOTES</span></span>
<span data-ttu-id="7138a-152">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="7138a-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7138a-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7138a-153">RELATED LINKS</span></span>

[<span data-ttu-id="7138a-154">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="7138a-154">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="7138a-155">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="7138a-155">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="7138a-156">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="7138a-156">Invoke-AzDataFactoryV2Pipeline</span></span>]()
