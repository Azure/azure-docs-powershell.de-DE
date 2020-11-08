---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
ms.openlocfilehash: 46f32dd48c433e34209b4a661b8c5b770a40db8f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008559"
---
# <span data-ttu-id="75d80-101">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="75d80-101">Get-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="75d80-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="75d80-102">SYNOPSIS</span></span>
<span data-ttu-id="75d80-103">Ruft Informationen zu Pipelines in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="75d80-103">Gets information about pipelines in Azure Data Factory.</span></span>

## <span data-ttu-id="75d80-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="75d80-104">SYNTAX</span></span>

### <span data-ttu-id="75d80-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="75d80-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75d80-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="75d80-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75d80-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75d80-107">DESCRIPTION</span></span>
<span data-ttu-id="75d80-108">Das Cmdlet " **Get-AzDataFactoryPipeline** " Ruft Informationen zu Pipelines in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="75d80-108">The **Get-AzDataFactoryPipeline** cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="75d80-109">Wenn Sie den Namen einer Pipeline angeben, ruft dieses Cmdlet Informationen zu dieser Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="75d80-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="75d80-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Pipelines in der Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="75d80-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="75d80-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75d80-111">EXAMPLES</span></span>

### <span data-ttu-id="75d80-112">Beispiel 1: Abrufen von Informationen zu allen Pipelines</span><span class="sxs-lookup"><span data-stu-id="75d80-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

<span data-ttu-id="75d80-113">Dieser Befehl ruft Informationen zu allen Pipelines in der Data Factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="75d80-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="75d80-114">Sie können entweder einen der folgenden Beispielbefehle ausführen.</span><span class="sxs-lookup"><span data-stu-id="75d80-114">You can either one of the following example commands.</span></span>
<span data-ttu-id="75d80-115">Bei der zweiten wird ein **DataFactory** -Objekt als Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="75d80-115">The second one uses a **DataFactory** object as a parameter.</span></span>

### <span data-ttu-id="75d80-116">Beispiel 2: Abrufen von Informationen zu einer bestimmten Pipeline</span><span class="sxs-lookup"><span data-stu-id="75d80-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="75d80-117">Dieser Befehl ruft Informationen zur Pipeline mit dem Namen DPWikisample in der Data Factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="75d80-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="75d80-118">Der Befehl übergibt diese Informationen mithilfe des Pipelineoperators an das Format-List-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75d80-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="75d80-119">Dieses Cmdlet formatiert die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="75d80-119">That cmdlet formats the results.</span></span>
<span data-ttu-id="75d80-120">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="75d80-120">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="75d80-121">Beispiel 3: Abrufen der Eigenschaften für eine bestimmte Pipeline</span><span class="sxs-lookup"><span data-stu-id="75d80-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

<span data-ttu-id="75d80-122">Dieser Befehl ruft Informationen für die Pipeline mit dem Namen DPWikisample in der Data Factory mit dem Namen WikiADF ab und verwendet dann die standardmäßige Punktnotation, um die **Eigenschaften** Eigenschaft anzuzeigen, die dieser Pipeline zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="75d80-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Properties** property associated with that pipeline.</span></span>

### <span data-ttu-id="75d80-123">Beispiel 4: Abrufen der Aktivitäten für eine bestimmte Pipeline</span><span class="sxs-lookup"><span data-stu-id="75d80-123">Example 4: Get the activities for a specific pipeline</span></span>
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

<span data-ttu-id="75d80-124">Dieser Befehl ruft Informationen für die Pipeline mit dem Namen DPWikisample in der Data Factory mit dem Namen WikiADF ab und verwendet dann die standardmäßige Punktnotation, um die **Aktivitäten** -Eigenschaft anzuzeigen, die dieser Pipeline zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="75d80-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>

### <span data-ttu-id="75d80-125">Beispiel 5: Abrufen der Laufzeitinformationen für eine bestimmte Pipeline</span><span class="sxs-lookup"><span data-stu-id="75d80-125">Example 5: Get the runtime information for a specific pipeline</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

<span data-ttu-id="75d80-126">Dieser Befehl ruft Informationen für die Pipeline mit dem Namen DPWikisample in der Data Factory mit dem Namen WikiADF ab und verwendet dann die standardmäßige Punktnotation, um die **RuntimeInfo** -Eigenschaft anzuzeigen, die dieser Pipeline zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="75d80-126">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **RuntimeInfo** property associated with that pipeline.</span></span>

### <span data-ttu-id="75d80-127">Beispiel 6: Abrufen von Informationen zu Eingaben für die erste Aktivität</span><span class="sxs-lookup"><span data-stu-id="75d80-127">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

<span data-ttu-id="75d80-128">Dieser Befehl ruft Informationen für die Pipeline mit dem Namen DPWikisample in der Data Factory mit dem Namen WikiADF ab und verwendet dann die standardmäßige Punktnotation, um die **Aktivitäten** -Eigenschaft anzuzeigen, die dieser Pipeline zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="75d80-128">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>
<span data-ttu-id="75d80-129">Der Befehl zeigt die **Inputs** -Eigenschaft des ersten Elements des **Activities** -Arrays mithilfe von **Format-List** an.</span><span class="sxs-lookup"><span data-stu-id="75d80-129">The command displays the **Inputs** property of the first element of the **Activities** array by using **Format-List**.</span></span>

## <span data-ttu-id="75d80-130">Parameter</span><span class="sxs-lookup"><span data-stu-id="75d80-130">PARAMETERS</span></span>

### <span data-ttu-id="75d80-131">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="75d80-131">-DataFactory</span></span>
<span data-ttu-id="75d80-132">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="75d80-132">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="75d80-133">Dieses Cmdlet ruft Pipelines ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="75d80-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="75d80-134">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="75d80-134">-DataFactoryName</span></span>
<span data-ttu-id="75d80-135">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="75d80-135">Specifies the name of a data factory.</span></span>
<span data-ttu-id="75d80-136">Dieses Cmdlet ruft Pipelines ab, die zu der Data Factory gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="75d80-136">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="75d80-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75d80-137">-DefaultProfile</span></span>
<span data-ttu-id="75d80-138">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="75d80-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75d80-139">-Name</span><span class="sxs-lookup"><span data-stu-id="75d80-139">-Name</span></span>
<span data-ttu-id="75d80-140">Gibt den Namen der Pipeline an, über die Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="75d80-140">Specifies the name of the pipeline about which to get information.</span></span>

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

### <span data-ttu-id="75d80-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75d80-141">-ResourceGroupName</span></span>
<span data-ttu-id="75d80-142">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="75d80-142">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="75d80-143">Dieses Cmdlet ruft Pipelines ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="75d80-143">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="75d80-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75d80-144">CommonParameters</span></span>
<span data-ttu-id="75d80-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75d80-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75d80-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75d80-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75d80-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="75d80-147">INPUTS</span></span>

### <span data-ttu-id="75d80-148">System. String</span><span class="sxs-lookup"><span data-stu-id="75d80-148">System.String</span></span>

### <span data-ttu-id="75d80-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="75d80-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="75d80-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="75d80-150">OUTPUTS</span></span>

### <span data-ttu-id="75d80-151">Microsoft. Azure. Commands. datafactoring. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="75d80-151">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="75d80-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="75d80-152">NOTES</span></span>
* <span data-ttu-id="75d80-153">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="75d80-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="75d80-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="75d80-154">RELATED LINKS</span></span>

[<span data-ttu-id="75d80-155">Neu – AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="75d80-155">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="75d80-156">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="75d80-156">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="75d80-157">Lebenslauf-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="75d80-157">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="75d80-158">Satz-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="75d80-158">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="75d80-159">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="75d80-159">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


