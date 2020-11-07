---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 45095fefa0d4866a40b59c61ca02a98c118cf37a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664280"
---
# <span data-ttu-id="9c4f2-101">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="9c4f2-101">Invoke-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="9c4f2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9c4f2-102">SYNOPSIS</span></span>
  <span data-ttu-id="9c4f2-103">Ruft eine Pipeline auf, um einen Testlauf zu starten.</span><span class="sxs-lookup"><span data-stu-id="9c4f2-103">Invokes a pipeline to start a run for it.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c4f2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c4f2-104">SYNTAX</span></span>

### <span data-ttu-id="9c4f2-105">ByFactoryNameByParameterFile (Standard)</span><span class="sxs-lookup"><span data-stu-id="9c4f2-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="9c4f2-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="9c4f2-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="9c4f2-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="9c4f2-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="9c4f2-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="9c4f2-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="9c4f2-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c4f2-109">DESCRIPTION</span></span>
<span data-ttu-id="9c4f2-110">Der Befehl **Invoke-AzureRmDataFactoryV2Pipeline** startet eine Ausführung für die angegebene Pipeline und gibt eine ID für diesen Testlauf zurück.</span><span class="sxs-lookup"><span data-stu-id="9c4f2-110">The **Invoke-AzureRmDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="9c4f2-111">Diese GUID kann an **Get-AzureRmDataFactoryV2PipelineRun** oder **Get-AzureRmDataFactoryV2ActivityRun** übergeben werden, um weitere Details zu diesem Testlauf abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9c4f2-111">This GUID can be passed to **Get-AzureRmDataFactoryV2PipelineRun** or **Get-AzureRmDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="9c4f2-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9c4f2-112">EXAMPLES</span></span>

### <span data-ttu-id="9c4f2-113">Beispiel 1: Aufrufen einer Pipeline zum Starten einer Ausführung</span><span class="sxs-lookup"><span data-stu-id="9c4f2-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="9c4f2-114">Mit diesem Befehl wird eine Run für "DPWikisample"-Pipeline in der Factory "WikiADF" gestartet.</span><span class="sxs-lookup"><span data-stu-id="9c4f2-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="9c4f2-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c4f2-115">PARAMETERS</span></span>

### <span data-ttu-id="9c4f2-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9c4f2-116">-Confirm</span></span>
<span data-ttu-id="9c4f2-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9c4f2-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c4f2-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="9c4f2-118">-DataFactoryName</span></span>
<span data-ttu-id="9c4f2-119">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="9c4f2-119">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c4f2-120">-Parameterdatei</span><span class="sxs-lookup"><span data-stu-id="9c4f2-120">-ParameterFile</span></span>
<span data-ttu-id="9c4f2-121">Der Name der Datei mit Parametern für die Pipelineausführung.</span><span class="sxs-lookup"><span data-stu-id="9c4f2-121">The name of the file with parameters for pipeline run.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByPipelineObjectByParameterFile
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c4f2-122">-Parameter</span><span class="sxs-lookup"><span data-stu-id="9c4f2-122">-Parameter</span></span>
<span data-ttu-id="9c4f2-123">Parameter für Pipelineausführung.</span><span class="sxs-lookup"><span data-stu-id="9c4f2-123">Parameters for pipeline run.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByPipelineObjectByParameterObject, ByFactoryNameByParameterObject
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c4f2-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9c4f2-124">-InputObject</span></span>
<span data-ttu-id="9c4f2-125">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9c4f2-125">The data factory object.</span></span>

```yaml
Type: PSPipeline
Parameter Sets: ByPipelineObjectByParameterFile, ByPipelineObjectByParameterObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c4f2-126">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="9c4f2-126">-PipelineName</span></span>
<span data-ttu-id="9c4f2-127">Der Name der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="9c4f2-127">The pipeline name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c4f2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c4f2-128">-ResourceGroupName</span></span>
<span data-ttu-id="9c4f2-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9c4f2-129">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c4f2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c4f2-130">-WhatIf</span></span>
<span data-ttu-id="9c4f2-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9c4f2-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="9c4f2-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9c4f2-132">INPUTS</span></span>

### <span data-ttu-id="9c4f2-133">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="9c4f2-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="9c4f2-134">System. String System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9c4f2-134">System.String System.Collections.Hashtable</span></span>


## <span data-ttu-id="9c4f2-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9c4f2-135">OUTPUTS</span></span>

### <span data-ttu-id="9c4f2-136">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="9c4f2-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>


## <span data-ttu-id="9c4f2-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="9c4f2-137">NOTES</span></span>

## <span data-ttu-id="9c4f2-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9c4f2-138">RELATED LINKS</span></span>
[<span data-ttu-id="9c4f2-139">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="9c4f2-139">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="9c4f2-140">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="9c4f2-140">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

