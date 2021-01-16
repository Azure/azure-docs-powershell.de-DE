---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: e4204068b12a21732cca1802dcc20a770d74d5e0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295925"
---
# <span data-ttu-id="3bc83-101">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="3bc83-101">Invoke-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="3bc83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bc83-102">SYNOPSIS</span></span>
  <span data-ttu-id="3bc83-103">Ruft eine Pipeline auf, um eine Ausführung dafür zu starten.</span><span class="sxs-lookup"><span data-stu-id="3bc83-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="3bc83-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3bc83-104">SYNTAX</span></span>

### <span data-ttu-id="3bc83-105">ByFactoryNameByParameterFile (Standard)</span><span class="sxs-lookup"><span data-stu-id="3bc83-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bc83-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="3bc83-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bc83-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="3bc83-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bc83-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="3bc83-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bc83-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3bc83-109">DESCRIPTION</span></span>
<span data-ttu-id="3bc83-110">Der **Befehl "Invoke-AzDataFactoryV2Pipeline"** startet eine Ausführung für die angegebene Pipeline und gibt eine ID für diese Ausführung zurück.</span><span class="sxs-lookup"><span data-stu-id="3bc83-110">The **Invoke-AzDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="3bc83-111">Diese GUID kann an **"Get-AzDataFactoryV2PipelineRun"** oder **"Get-AzDataFactoryV2ActivityRun"** übergeben werden, um weitere Details zu diesem Ausführen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3bc83-111">This GUID can be passed to **Get-AzDataFactoryV2PipelineRun** or **Get-AzDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="3bc83-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3bc83-112">EXAMPLES</span></span>

### <span data-ttu-id="3bc83-113">Beispiel 1: Aufrufen einer Pipeline zum Starten einer Ausführung</span><span class="sxs-lookup"><span data-stu-id="3bc83-113">Example 1: Invoke a pipeline to start a run</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="3bc83-114">Dieser Befehl startet eine Ausführung für die Pipeline "DPWikisample" in der "WikiADF"-Factory.</span><span class="sxs-lookup"><span data-stu-id="3bc83-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

### <span data-ttu-id="3bc83-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3bc83-115">Example 2</span></span>

<span data-ttu-id="3bc83-116">Ruft eine Pipeline auf, um eine Ausführung dafür zu starten.</span><span class="sxs-lookup"><span data-stu-id="3bc83-116">Invokes a pipeline to start a run for it.</span></span> <span data-ttu-id="3bc83-117">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="3bc83-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Invoke-AzDataFactoryV2Pipeline -DataFactoryName 'WikiADF' -Parameter <Hashtable> -PipelineName 'DPWikisample' -ResourceGroupName 'ADF'
```

## <span data-ttu-id="3bc83-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3bc83-118">PARAMETERS</span></span>

### <span data-ttu-id="3bc83-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3bc83-119">-DataFactoryName</span></span>
<span data-ttu-id="3bc83-120">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="3bc83-120">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc83-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bc83-121">-DefaultProfile</span></span>
<span data-ttu-id="3bc83-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3bc83-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3bc83-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3bc83-123">-InputObject</span></span>
<span data-ttu-id="3bc83-124">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3bc83-124">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline
Parameter Sets: ByPipelineObjectByParameterFile, ByPipelineObjectByParameterObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc83-125">-IsRecovery</span><span class="sxs-lookup"><span data-stu-id="3bc83-125">-IsRecovery</span></span>
<span data-ttu-id="3bc83-126">Kennzeichen für den Wiederherstellungsmodus.</span><span class="sxs-lookup"><span data-stu-id="3bc83-126">Recovery mode flag.</span></span> <span data-ttu-id="3bc83-127">Wenn der Wiederherstellungsmodus auf "true" festgelegt ist, werden die angegebene Pipeline, auf die verwiesen wird, und die neue Ausführung unter derselben groupId gruppieren.</span><span class="sxs-lookup"><span data-stu-id="3bc83-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc83-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="3bc83-128">-Parameter</span></span>
<span data-ttu-id="3bc83-129">Parameter für die Ausführung der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="3bc83-129">Parameters for pipeline run.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByPipelineObjectByParameterObject, ByFactoryNameByParameterObject
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc83-130">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="3bc83-130">-ParameterFile</span></span>
<span data-ttu-id="3bc83-131">Der Name der Datei mit Parametern für die Ausführung der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="3bc83-131">The name of the file with parameters for pipeline run.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByPipelineObjectByParameterFile
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc83-132">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="3bc83-132">-PipelineName</span></span>
<span data-ttu-id="3bc83-133">Der Pipelinename.</span><span class="sxs-lookup"><span data-stu-id="3bc83-133">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc83-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="3bc83-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="3bc83-135">Die Pipeline-Ausführungs-ID für die erneute Ausführung.</span><span class="sxs-lookup"><span data-stu-id="3bc83-135">The pipeline run ID for rerun.</span></span> <span data-ttu-id="3bc83-136">Wenn "Run ID" angegeben wird, werden die Parameter der angegebenen Ausführung verwendet, um eine neue Ausführung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3bc83-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc83-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bc83-137">-ResourceGroupName</span></span>
<span data-ttu-id="3bc83-138">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3bc83-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc83-139">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="3bc83-139">-StartActivityName</span></span>
<span data-ttu-id="3bc83-140">Im Wiederherstellungsmodus beginnt der erneute Ausführen mit dieser Aktivität.</span><span class="sxs-lookup"><span data-stu-id="3bc83-140">In recovery mode, the rerun will start from this activity.</span></span> <span data-ttu-id="3bc83-141">Wenn nicht angegeben, werden alle Aktivitäten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3bc83-141">If not specified, all activities will run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc83-142">-StartFromFailure</span><span class="sxs-lookup"><span data-stu-id="3bc83-142">-StartFromFailure</span></span>
<span data-ttu-id="3bc83-143">"Erneutes Ausführen von fehlgeschlagenen Aktivitäten starten" (Flag).</span><span class="sxs-lookup"><span data-stu-id="3bc83-143">Start rerun from failed activities flag.</span></span> <span data-ttu-id="3bc83-144">Im Wiederherstellungsmodus (sofern angegeben) beginnt der erneute Ausführen mit fehlgeschlagenen Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="3bc83-144">In recovery mode, if specified, the rerun will start from failed activities.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc83-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3bc83-145">-Confirm</span></span>
<span data-ttu-id="3bc83-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3bc83-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc83-147">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3bc83-147">-WhatIf</span></span>
<span data-ttu-id="3bc83-148">Zeigt, was geschieht, wenn das Cmdlet ausgeführt, aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3bc83-148">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc83-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bc83-149">CommonParameters</span></span>
<span data-ttu-id="3bc83-150">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bc83-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bc83-151">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3bc83-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bc83-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3bc83-152">INPUTS</span></span>

### <span data-ttu-id="3bc83-153">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="3bc83-153">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="3bc83-154">System.String</span><span class="sxs-lookup"><span data-stu-id="3bc83-154">System.String</span></span>

### <span data-ttu-id="3bc83-155">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3bc83-155">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3bc83-156">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3bc83-156">OUTPUTS</span></span>

### <span data-ttu-id="3bc83-157">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="3bc83-157">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="3bc83-158">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3bc83-158">NOTES</span></span>

## <span data-ttu-id="3bc83-159">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3bc83-159">RELATED LINKS</span></span>

[<span data-ttu-id="3bc83-160">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="3bc83-160">Get-AzDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="3bc83-161">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="3bc83-161">Get-AzDataFactoryV2ActivityRun</span></span>]()

