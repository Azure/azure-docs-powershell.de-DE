---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: e4204068b12a21732cca1802dcc20a770d74d5e0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175245"
---
# <span data-ttu-id="c0f5b-101">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="c0f5b-101">Invoke-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="c0f5b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c0f5b-102">SYNOPSIS</span></span>
  <span data-ttu-id="c0f5b-103">Ruft eine Pipeline auf, um einen Testlauf zu starten.</span><span class="sxs-lookup"><span data-stu-id="c0f5b-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="c0f5b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0f5b-104">SYNTAX</span></span>

### <span data-ttu-id="c0f5b-105">ByFactoryNameByParameterFile (Standard)</span><span class="sxs-lookup"><span data-stu-id="c0f5b-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0f5b-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="c0f5b-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0f5b-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="c0f5b-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0f5b-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="c0f5b-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0f5b-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c0f5b-109">DESCRIPTION</span></span>
<span data-ttu-id="c0f5b-110">Der Befehl **Invoke-AzDataFactoryV2Pipeline** startet eine Ausführung für die angegebene Pipeline und gibt eine ID für diesen Testlauf zurück.</span><span class="sxs-lookup"><span data-stu-id="c0f5b-110">The **Invoke-AzDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="c0f5b-111">Diese GUID kann an **Get-AzDataFactoryV2PipelineRun** oder **Get-AzDataFactoryV2ActivityRun** übergeben werden, um weitere Details zu diesem Testlauf abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c0f5b-111">This GUID can be passed to **Get-AzDataFactoryV2PipelineRun** or **Get-AzDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="c0f5b-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c0f5b-112">EXAMPLES</span></span>

### <span data-ttu-id="c0f5b-113">Beispiel 1: Aufrufen einer Pipeline zum Starten einer Ausführung</span><span class="sxs-lookup"><span data-stu-id="c0f5b-113">Example 1: Invoke a pipeline to start a run</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="c0f5b-114">Mit diesem Befehl wird eine Run für "DPWikisample"-Pipeline in der Factory "WikiADF" gestartet.</span><span class="sxs-lookup"><span data-stu-id="c0f5b-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

### <span data-ttu-id="c0f5b-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c0f5b-115">Example 2</span></span>

<span data-ttu-id="c0f5b-116">Ruft eine Pipeline auf, um einen Testlauf zu starten.</span><span class="sxs-lookup"><span data-stu-id="c0f5b-116">Invokes a pipeline to start a run for it.</span></span> <span data-ttu-id="c0f5b-117">automatisch</span><span class="sxs-lookup"><span data-stu-id="c0f5b-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Invoke-AzDataFactoryV2Pipeline -DataFactoryName 'WikiADF' -Parameter <Hashtable> -PipelineName 'DPWikisample' -ResourceGroupName 'ADF'
```

## <span data-ttu-id="c0f5b-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0f5b-118">PARAMETERS</span></span>

### <span data-ttu-id="c0f5b-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="c0f5b-119">-DataFactoryName</span></span>
<span data-ttu-id="c0f5b-120">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="c0f5b-120">The data factory name.</span></span>

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

### <span data-ttu-id="c0f5b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0f5b-121">-DefaultProfile</span></span>
<span data-ttu-id="c0f5b-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c0f5b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0f5b-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c0f5b-123">-InputObject</span></span>
<span data-ttu-id="c0f5b-124">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c0f5b-124">The data factory object.</span></span>

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

### <span data-ttu-id="c0f5b-125">-Isrecovery</span><span class="sxs-lookup"><span data-stu-id="c0f5b-125">-IsRecovery</span></span>
<span data-ttu-id="c0f5b-126">Flag für den Wiederherstellungsmodus.</span><span class="sxs-lookup"><span data-stu-id="c0f5b-126">Recovery mode flag.</span></span> <span data-ttu-id="c0f5b-127">Wenn der Wiederherstellungsmodus auf "true" festgelegt ist, wird die angegebene referenzierte Pipeline ausgeführt und der neue Run unter derselben Gruppen-Nr gruppiert.</span><span class="sxs-lookup"><span data-stu-id="c0f5b-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

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

### <span data-ttu-id="c0f5b-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="c0f5b-128">-Parameter</span></span>
<span data-ttu-id="c0f5b-129">Parameter für Pipelineausführung.</span><span class="sxs-lookup"><span data-stu-id="c0f5b-129">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="c0f5b-130">-Parameterdatei</span><span class="sxs-lookup"><span data-stu-id="c0f5b-130">-ParameterFile</span></span>
<span data-ttu-id="c0f5b-131">Der Name der Datei mit Parametern für die Pipelineausführung.</span><span class="sxs-lookup"><span data-stu-id="c0f5b-131">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="c0f5b-132">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="c0f5b-132">-PipelineName</span></span>
<span data-ttu-id="c0f5b-133">Der Name der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c0f5b-133">The pipeline name.</span></span>

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

### <span data-ttu-id="c0f5b-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="c0f5b-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="c0f5b-135">Die Pipeline Lauf-ID für die erneute Ausführung.</span><span class="sxs-lookup"><span data-stu-id="c0f5b-135">The pipeline run ID for rerun.</span></span> <span data-ttu-id="c0f5b-136">Wenn die Run-ID angegeben ist, werden die Parameter des angegebenen Laufs zum Erstellen eines neuen Laufs verwendet.</span><span class="sxs-lookup"><span data-stu-id="c0f5b-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

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

### <span data-ttu-id="c0f5b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0f5b-137">-ResourceGroupName</span></span>
<span data-ttu-id="c0f5b-138">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c0f5b-138">The resource group name.</span></span>

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

### <span data-ttu-id="c0f5b-139">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="c0f5b-139">-StartActivityName</span></span>
<span data-ttu-id="c0f5b-140">Im Wiederherstellungsmodus wird die erneute Ausführung von dieser Aktivität gestartet.</span><span class="sxs-lookup"><span data-stu-id="c0f5b-140">In recovery mode, the rerun will start from this activity.</span></span> <span data-ttu-id="c0f5b-141">Wenn nicht angegeben, werden alle Aktivitäten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0f5b-141">If not specified, all activities will run.</span></span>

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

### <span data-ttu-id="c0f5b-142">-StartFromFailure</span><span class="sxs-lookup"><span data-stu-id="c0f5b-142">-StartFromFailure</span></span>
<span data-ttu-id="c0f5b-143">Flag "erneute Ausführung von fehlgeschlagenen Aktivitäten starten"</span><span class="sxs-lookup"><span data-stu-id="c0f5b-143">Start rerun from failed activities flag.</span></span> <span data-ttu-id="c0f5b-144">Wenn angegeben, wird im Wiederherstellungsmodus die erneute Ausführung von fehlgeschlagenen Aktivitäten gestartet.</span><span class="sxs-lookup"><span data-stu-id="c0f5b-144">In recovery mode, if specified, the rerun will start from failed activities.</span></span>

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

### <span data-ttu-id="c0f5b-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c0f5b-145">-Confirm</span></span>
<span data-ttu-id="c0f5b-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c0f5b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0f5b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0f5b-147">-WhatIf</span></span>
<span data-ttu-id="c0f5b-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c0f5b-148">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="c0f5b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0f5b-149">CommonParameters</span></span>
<span data-ttu-id="c0f5b-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0f5b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0f5b-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0f5b-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0f5b-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c0f5b-152">INPUTS</span></span>

### <span data-ttu-id="c0f5b-153">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="c0f5b-153">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="c0f5b-154">System. String</span><span class="sxs-lookup"><span data-stu-id="c0f5b-154">System.String</span></span>

### <span data-ttu-id="c0f5b-155">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c0f5b-155">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c0f5b-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c0f5b-156">OUTPUTS</span></span>

### <span data-ttu-id="c0f5b-157">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="c0f5b-157">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="c0f5b-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="c0f5b-158">NOTES</span></span>

## <span data-ttu-id="c0f5b-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c0f5b-159">RELATED LINKS</span></span>

[<span data-ttu-id="c0f5b-160">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="c0f5b-160">Get-AzDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="c0f5b-161">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="c0f5b-161">Get-AzDataFactoryV2ActivityRun</span></span>]()

