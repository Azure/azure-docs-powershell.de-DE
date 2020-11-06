---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: e0abd64298d74c52f2081e6d36f42b1ad2dee913
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479334"
---
# <span data-ttu-id="ff5d0-101">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="ff5d0-101">Get-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="ff5d0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ff5d0-102">SYNOPSIS</span></span>
<span data-ttu-id="ff5d0-103">Ruft Informationen zu Pipelines in Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="ff5d0-103">Gets information about pipelines in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff5d0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff5d0-104">SYNTAX</span></span>

### <span data-ttu-id="ff5d0-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ff5d0-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff5d0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ff5d0-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff5d0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ff5d0-107">DESCRIPTION</span></span>
<span data-ttu-id="ff5d0-108">Das Get-AzureRmDataFactoryV2Pipeline-Cmdlet ruft Informationen zu Pipelines in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="ff5d0-108">The Get-AzureRmDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="ff5d0-109">Wenn Sie den Namen einer Pipeline angeben, ruft dieses Cmdlet Informationen zu dieser Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="ff5d0-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="ff5d0-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Pipelines in der Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="ff5d0-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="ff5d0-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ff5d0-111">EXAMPLES</span></span>

### <span data-ttu-id="ff5d0-112">Beispiel 1: Abrufen von Informationen zu allen Pipelines</span><span class="sxs-lookup"><span data-stu-id="ff5d0-112">Example 1: Get information about all pipelines</span></span>
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

<span data-ttu-id="ff5d0-113">Dieser Befehl ruft Informationen zu allen Pipelines in der Data Factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="ff5d0-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="ff5d0-114">Sie können entweder einen der folgenden Beispielbefehle verwenden:</span><span class="sxs-lookup"><span data-stu-id="ff5d0-114">You can use either one of the following example commands.</span></span>
<span data-ttu-id="ff5d0-115">Bei der zweiten wird ein DataFactory-Objekt als Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="ff5d0-115">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="ff5d0-116">Beispiel 2: Abrufen von Informationen zu einer bestimmten Pipeline</span><span class="sxs-lookup"><span data-stu-id="ff5d0-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="ff5d0-117">Dieser Befehl ruft Informationen zur Pipeline mit dem Namen DPWikisample in der Data Factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="ff5d0-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="ff5d0-118">Der Befehl übergibt diese Informationen mithilfe des Pipelineoperators an das Format-List-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff5d0-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ff5d0-119">Das Windows PowerShell-Cmdlet formatiert die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="ff5d0-119">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="ff5d0-120">Wenn Sie weitere Informationen wünschen, geben Sie Get-Help Format-List ein.</span><span class="sxs-lookup"><span data-stu-id="ff5d0-120">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="ff5d0-121">Beispiel 3: Abrufen der Eigenschaften für eine bestimmte Pipeline</span><span class="sxs-lookup"><span data-stu-id="ff5d0-121">Example 3: Get the properties for a specific pipeline</span></span>
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

<span data-ttu-id="ff5d0-122">Dieser Befehl ruft Informationen für die Pipeline mit dem Namen DPWikisample in der Data Factory mit dem Namen WikiADF ab und verwendet dann die standardmäßige Punktnotation, um die Aktivitäten-Eigenschaft anzuzeigen, die dieser Pipeline zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ff5d0-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="ff5d0-123">Beispiel 6: Abrufen von Informationen zu Eingaben für die erste Aktivität</span><span class="sxs-lookup"><span data-stu-id="ff5d0-123">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :
```

<span data-ttu-id="ff5d0-124">Dieser Befehl ruft Informationen für die Pipeline mit dem Namen DPWikisample in der Data Factory mit dem Namen WikiADF ab und verwendet dann die standardmäßige Punktnotation, um die Aktivitäten-Eigenschaft anzuzeigen, die dieser Pipeline zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ff5d0-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="ff5d0-125">Der Befehl zeigt die Inputs-Eigenschaft des ersten Elements des Activities-Arrays mithilfe des Format-List-Cmdlets an.</span><span class="sxs-lookup"><span data-stu-id="ff5d0-125">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="ff5d0-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff5d0-126">PARAMETERS</span></span>

### <span data-ttu-id="ff5d0-127">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ff5d0-127">-DataFactory</span></span>
<span data-ttu-id="ff5d0-128">Gibt ein PSDataFactory-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="ff5d0-128">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="ff5d0-129">Dieses Cmdlet ruft Pipelines ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ff5d0-129">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ff5d0-130">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="ff5d0-130">-DataFactoryName</span></span>
<span data-ttu-id="ff5d0-131">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="ff5d0-131">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ff5d0-132">Dieses Cmdlet ruft Pipelines ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ff5d0-132">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ff5d0-133">-Name</span><span class="sxs-lookup"><span data-stu-id="ff5d0-133">-Name</span></span>
<span data-ttu-id="ff5d0-134">Gibt den Namen der Pipeline an, über die Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ff5d0-134">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff5d0-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff5d0-135">-ResourceGroupName</span></span>
<span data-ttu-id="ff5d0-136">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ff5d0-136">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ff5d0-137">Dieses Cmdlet ruft Pipelines ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ff5d0-137">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ff5d0-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff5d0-138">-DefaultProfile</span></span>
<span data-ttu-id="ff5d0-139">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ff5d0-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff5d0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff5d0-140">CommonParameters</span></span>
<span data-ttu-id="ff5d0-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff5d0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff5d0-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff5d0-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff5d0-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ff5d0-143">INPUTS</span></span>

### <span data-ttu-id="ff5d0-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ff5d0-144">System.String</span></span>
<span data-ttu-id="ff5d0-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ff5d0-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="ff5d0-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ff5d0-146">OUTPUTS</span></span>

### <span data-ttu-id="ff5d0-147">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ff5d0-147">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="ff5d0-148">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="ff5d0-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="ff5d0-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="ff5d0-149">NOTES</span></span>
<span data-ttu-id="ff5d0-150">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="ff5d0-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ff5d0-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ff5d0-151">RELATED LINKS</span></span>

[<span data-ttu-id="ff5d0-152">Satz-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="ff5d0-152">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="ff5d0-153">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="ff5d0-153">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="ff5d0-154">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="ff5d0-154">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()
