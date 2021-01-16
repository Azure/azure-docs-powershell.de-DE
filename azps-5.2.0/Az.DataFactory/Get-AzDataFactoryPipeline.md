---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
ms.openlocfilehash: 46f32dd48c433e34209b4a661b8c5b770a40db8f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307488"
---
# <span data-ttu-id="028af-101">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="028af-101">Get-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="028af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="028af-102">SYNOPSIS</span></span>
<span data-ttu-id="028af-103">Ruft Informationen zu Pipelines in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="028af-103">Gets information about pipelines in Azure Data Factory.</span></span>

## <span data-ttu-id="028af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="028af-104">SYNTAX</span></span>

### <span data-ttu-id="028af-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="028af-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="028af-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="028af-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="028af-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="028af-107">DESCRIPTION</span></span>
<span data-ttu-id="028af-108">Das **Cmdlet "Get-AzDataFactoryPipeline"** ruft Informationen zu Pipelines in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="028af-108">The **Get-AzDataFactoryPipeline** cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="028af-109">Wenn Sie den Namen einer Pipeline angeben, ruft dieses Cmdlet Informationen zu dieser Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="028af-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="028af-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Pipelines in der Daten factory ab.</span><span class="sxs-lookup"><span data-stu-id="028af-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="028af-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="028af-111">EXAMPLES</span></span>

### <span data-ttu-id="028af-112">Beispiel 1: Informationen zu allen Pipelines</span><span class="sxs-lookup"><span data-stu-id="028af-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

<span data-ttu-id="028af-113">Dieser Befehl ruft Informationen zu allen Pipelines in der Daten factory namens WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="028af-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="028af-114">Sie können einen der folgenden Beispielbefehle verwenden.</span><span class="sxs-lookup"><span data-stu-id="028af-114">You can either one of the following example commands.</span></span>
<span data-ttu-id="028af-115">Im zweiten Parameter wird ein **DataFactory-Objekt** als Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="028af-115">The second one uses a **DataFactory** object as a parameter.</span></span>

### <span data-ttu-id="028af-116">Beispiel 2: Informationen zu einer bestimmten Pipeline</span><span class="sxs-lookup"><span data-stu-id="028af-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="028af-117">Dieser Befehl ruft Informationen über die Pipeline mit dem Namen DPWikisample in der Daten factory namens WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="028af-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="028af-118">Der Befehl übergibt diese Informationen mithilfe des Pipelineoperators Format-List an das Format-List Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="028af-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="028af-119">Mit diesem Cmdlet werden die Ergebnisse formatiert.</span><span class="sxs-lookup"><span data-stu-id="028af-119">That cmdlet formats the results.</span></span>
<span data-ttu-id="028af-120">Weitere Informationen erhalten Sie, wenn Sie " `Get-Help Format-List` eingeben" aus.</span><span class="sxs-lookup"><span data-stu-id="028af-120">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="028af-121">Beispiel 3: Erhalten der Eigenschaften für eine bestimmte Pipeline</span><span class="sxs-lookup"><span data-stu-id="028af-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

<span data-ttu-id="028af-122">Dieser Befehl ruft Informationen für die Pipeline mit dem Namen DPWikisample in der Daten factory namens WikiADF ab und verwendet dann die standardmäßige Punkt-Notation, um die mit dieser Pipeline verknüpfte Eigenschaft **"Properties"** (Eigenschaften) anzeigen.</span><span class="sxs-lookup"><span data-stu-id="028af-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Properties** property associated with that pipeline.</span></span>

### <span data-ttu-id="028af-123">Beispiel 4: Erhalten der Aktivitäten für eine bestimmte Pipeline</span><span class="sxs-lookup"><span data-stu-id="028af-123">Example 4: Get the activities for a specific pipeline</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.Activities
Transformation    : Microsoft.DataFactories.HDInsightActivityProperties
Description       : 
Inputs            : {DAWikipediaClickEvents}
LinkedServiceName : HDILinkedService
Name              : WikiHiveActivity
Outputs           : {DACuratedWikiData}
Policy            : Microsoft.DataFactories.ActivityPolicy

Transformation    : Microsoft.DataFactories.CopyActivityProperties
Description       : 
Inputs            : {DACuratedWikiData}
LinkedServiceName : HDILinkedService
Name              : BlobToSqlCopyActivity
Outputs           : {DAWikiAggregatedData}
Policy            : Microsoft.DataFactories.ActivityPolicy
```

<span data-ttu-id="028af-124">Dieser Befehl ruft Informationen für die Pipeline mit dem Namen DPWikisample in der Daten factory mit dem Namen WikiADF ab und verwendet dann die standardmäßige Punkt-Notation, um die dieser Pipeline zugeordnete Eigenschaft **"Activities"** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="028af-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>

### <span data-ttu-id="028af-125">Beispiel 5: Erhalten der Laufzeitinformationen für eine bestimmte Pipeline</span><span class="sxs-lookup"><span data-stu-id="028af-125">Example 5: Get the runtime information for a specific pipeline</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

<span data-ttu-id="028af-126">Dieser Befehl ruft Informationen für die Pipeline mit dem Namen DPWikisample in der Daten factory mit dem Namen WikiADF ab und verwendet dann die standardmäßige Punkt-Notation, um die der Pipeline zugeordnete **RuntimeInfo-Eigenschaft** zu sehen.</span><span class="sxs-lookup"><span data-stu-id="028af-126">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **RuntimeInfo** property associated with that pipeline.</span></span>

### <span data-ttu-id="028af-127">Beispiel 6: Informationen zu Eingaben für die erste Aktivität</span><span class="sxs-lookup"><span data-stu-id="028af-127">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

<span data-ttu-id="028af-128">Dieser Befehl ruft Informationen für die Pipeline mit dem Namen DPWikisample in der Daten factory mit dem Namen WikiADF ab und verwendet dann die standardmäßige Punkt-Notation, um die dieser Pipeline zugeordnete Eigenschaft **"Activities"** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="028af-128">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>
<span data-ttu-id="028af-129">Der Befehl zeigt **mithilfe** von **"Format-List"** die Eingabeeigenschaft des ersten Elements des **Arrays** "Aktivitäten" an.</span><span class="sxs-lookup"><span data-stu-id="028af-129">The command displays the **Inputs** property of the first element of the **Activities** array by using **Format-List**.</span></span>

## <span data-ttu-id="028af-130">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="028af-130">PARAMETERS</span></span>

### <span data-ttu-id="028af-131">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="028af-131">-DataFactory</span></span>
<span data-ttu-id="028af-132">Gibt ein **"PSDataFactory"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="028af-132">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="028af-133">Dieses Cmdlet ruft Pipelines ab, die zu der von diesem Parameter angegebenen Daten factory gehören.</span><span class="sxs-lookup"><span data-stu-id="028af-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="028af-134">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="028af-134">-DataFactoryName</span></span>
<span data-ttu-id="028af-135">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="028af-135">Specifies the name of a data factory.</span></span>
<span data-ttu-id="028af-136">Dieses Cmdlet ruft Pipelines ab, die zu der von diesem Parameter angegebenen Daten factory gehören.</span><span class="sxs-lookup"><span data-stu-id="028af-136">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="028af-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="028af-137">-DefaultProfile</span></span>
<span data-ttu-id="028af-138">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="028af-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="028af-139">-Name</span><span class="sxs-lookup"><span data-stu-id="028af-139">-Name</span></span>
<span data-ttu-id="028af-140">Gibt den Namen der Pipeline an, über die Informationen angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="028af-140">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="028af-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="028af-141">-ResourceGroupName</span></span>
<span data-ttu-id="028af-142">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="028af-142">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="028af-143">Dieses Cmdlet ruft Pipelines ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="028af-143">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="028af-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="028af-144">CommonParameters</span></span>
<span data-ttu-id="028af-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="028af-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="028af-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="028af-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="028af-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="028af-147">INPUTS</span></span>

### <span data-ttu-id="028af-148">System.String</span><span class="sxs-lookup"><span data-stu-id="028af-148">System.String</span></span>

### <span data-ttu-id="028af-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="028af-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="028af-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="028af-150">OUTPUTS</span></span>

### <span data-ttu-id="028af-151">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="028af-151">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="028af-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="028af-152">NOTES</span></span>
* <span data-ttu-id="028af-153">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="028af-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="028af-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="028af-154">RELATED LINKS</span></span>

[<span data-ttu-id="028af-155">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="028af-155">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="028af-156">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="028af-156">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="028af-157">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="028af-157">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="028af-158">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="028af-158">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="028af-159">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="028af-159">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


