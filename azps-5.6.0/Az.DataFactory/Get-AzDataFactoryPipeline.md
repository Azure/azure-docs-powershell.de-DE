---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
ms.openlocfilehash: 5db024152a01fdab8233e388da5ae176849f4b7d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930320"
---
# <span data-ttu-id="fe131-101">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="fe131-101">Get-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="fe131-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe131-102">SYNOPSIS</span></span>
<span data-ttu-id="fe131-103">Ruft Informationen zu Pipelines in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="fe131-103">Gets information about pipelines in Azure Data Factory.</span></span>

## <span data-ttu-id="fe131-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe131-104">SYNTAX</span></span>

### <span data-ttu-id="fe131-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="fe131-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe131-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fe131-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe131-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fe131-107">DESCRIPTION</span></span>
<span data-ttu-id="fe131-108">Das **Get-AzDataFactoryPipeline-Cmdlet** ruft Informationen zu Pipelines in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="fe131-108">The **Get-AzDataFactoryPipeline** cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="fe131-109">Wenn Sie den Namen einer Pipeline angeben, ruft dieses Cmdlet Informationen zu dieser Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="fe131-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="fe131-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Pipelines in der Daten factory ab.</span><span class="sxs-lookup"><span data-stu-id="fe131-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="fe131-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fe131-111">EXAMPLES</span></span>

### <span data-ttu-id="fe131-112">Beispiel 1: Informationen zu allen Pipelines erhalten</span><span class="sxs-lookup"><span data-stu-id="fe131-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

<span data-ttu-id="fe131-113">Dieser Befehl ruft Informationen zu allen Pipelines in der Daten factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="fe131-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="fe131-114">Sie können einen der folgenden Beispielbefehle verwenden.</span><span class="sxs-lookup"><span data-stu-id="fe131-114">You can either one of the following example commands.</span></span>
<span data-ttu-id="fe131-115">Im zweiten wird ein **DataFactory-Objekt** als Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="fe131-115">The second one uses a **DataFactory** object as a parameter.</span></span>

### <span data-ttu-id="fe131-116">Beispiel 2: Informationen zu einer bestimmten Pipeline erhalten</span><span class="sxs-lookup"><span data-stu-id="fe131-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="fe131-117">Dieser Befehl ruft Informationen zur Pipeline mit dem Namen DPWikisample in der Daten factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="fe131-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="fe131-118">Der Befehl übergibt diese Informationen mithilfe des Pipelineoperators an Format-List-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe131-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fe131-119">Dieses Cmdlet formatiert die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="fe131-119">That cmdlet formats the results.</span></span>
<span data-ttu-id="fe131-120">Weitere Informationen finden Sie unter `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="fe131-120">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="fe131-121">Beispiel 3: Erhalten der Eigenschaften für eine bestimmte Pipeline</span><span class="sxs-lookup"><span data-stu-id="fe131-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

<span data-ttu-id="fe131-122">Dieser Befehl ruft Informationen für die Pipeline mit dem Namen DPWikisample in der Daten factory  mit dem Namen WikiADF ab und verwendet dann die Standardpunkt-Notation, um die Eigenschafteneigenschaft zu sehen, die dieser Pipeline zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fe131-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Properties** property associated with that pipeline.</span></span>

### <span data-ttu-id="fe131-123">Beispiel 4: Erhalten der Aktivitäten für eine bestimmte Pipeline</span><span class="sxs-lookup"><span data-stu-id="fe131-123">Example 4: Get the activities for a specific pipeline</span></span>
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

<span data-ttu-id="fe131-124">Dieser Befehl ruft Informationen für die Pipeline mit dem Namen DPWikisample in der Daten factory mit dem Namen WikiADF ab und verwendet dann die Standardpunkt-Notation, um die der Pipeline zugeordnete **Activities-Eigenschaft** anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="fe131-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>

### <span data-ttu-id="fe131-125">Beispiel 5: Erhalten der Laufzeitinformationen für eine bestimmte Pipeline</span><span class="sxs-lookup"><span data-stu-id="fe131-125">Example 5: Get the runtime information for a specific pipeline</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

<span data-ttu-id="fe131-126">Dieser Befehl ruft Informationen für die Pipeline mit dem Namen DPWikisample in der Daten factory mit dem Namen WikiADF ab und verwendet dann die Standardpunkt-Notation, um die **RuntimeInfo-Eigenschaft** zu sehen, die dieser Pipeline zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fe131-126">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **RuntimeInfo** property associated with that pipeline.</span></span>

### <span data-ttu-id="fe131-127">Beispiel 6: Informationen zu Eingaben für die erste Aktivität</span><span class="sxs-lookup"><span data-stu-id="fe131-127">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

<span data-ttu-id="fe131-128">Dieser Befehl ruft Informationen für die Pipeline mit dem Namen DPWikisample in der Daten factory mit dem Namen WikiADF ab und verwendet dann die Standardpunkt-Notation, um die der Pipeline zugeordnete **Activities-Eigenschaft** anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="fe131-128">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>
<span data-ttu-id="fe131-129">Der Befehl zeigt die **Eingabeeigenschaft** des ersten Elements des **Array Aktivitäten** mithilfe von **Format-List an.**</span><span class="sxs-lookup"><span data-stu-id="fe131-129">The command displays the **Inputs** property of the first element of the **Activities** array by using **Format-List**.</span></span>

## <span data-ttu-id="fe131-130">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fe131-130">PARAMETERS</span></span>

### <span data-ttu-id="fe131-131">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="fe131-131">-DataFactory</span></span>
<span data-ttu-id="fe131-132">Gibt ein **PSDataFactory-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="fe131-132">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="fe131-133">Dieses Cmdlet ruft Pipelines ab, die zur daten factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="fe131-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="fe131-134">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fe131-134">-DataFactoryName</span></span>
<span data-ttu-id="fe131-135">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="fe131-135">Specifies the name of a data factory.</span></span>
<span data-ttu-id="fe131-136">Dieses Cmdlet ruft Pipelines ab, die zur daten factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="fe131-136">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="fe131-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe131-137">-DefaultProfile</span></span>
<span data-ttu-id="fe131-138">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="fe131-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe131-139">-Name</span><span class="sxs-lookup"><span data-stu-id="fe131-139">-Name</span></span>
<span data-ttu-id="fe131-140">Gibt den Namen der Pipeline an, über die Informationen zu erhalten sind.</span><span class="sxs-lookup"><span data-stu-id="fe131-140">Specifies the name of the pipeline about which to get information.</span></span>

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

### <span data-ttu-id="fe131-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe131-141">-ResourceGroupName</span></span>
<span data-ttu-id="fe131-142">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="fe131-142">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="fe131-143">Dieses Cmdlet ruft Pipelines ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="fe131-143">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fe131-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe131-144">CommonParameters</span></span>
<span data-ttu-id="fe131-145">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe131-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe131-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe131-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe131-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fe131-147">INPUTS</span></span>

### <span data-ttu-id="fe131-148">System.String</span><span class="sxs-lookup"><span data-stu-id="fe131-148">System.String</span></span>

### <span data-ttu-id="fe131-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="fe131-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="fe131-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fe131-150">OUTPUTS</span></span>

### <span data-ttu-id="fe131-151">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="fe131-151">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="fe131-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fe131-152">NOTES</span></span>
* <span data-ttu-id="fe131-153">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factory</span><span class="sxs-lookup"><span data-stu-id="fe131-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="fe131-154">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fe131-154">RELATED LINKS</span></span>

[<span data-ttu-id="fe131-155">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="fe131-155">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="fe131-156">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="fe131-156">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="fe131-157">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="fe131-157">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="fe131-158">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="fe131-158">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="fe131-159">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="fe131-159">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


