---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/stop-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 096ee403a0ee12c80462a1fb87db4378e3d86f01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942856"
---
# <span data-ttu-id="2eef0-101">Stop-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="2eef0-101">Stop-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="2eef0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2eef0-102">SYNOPSIS</span></span>
<span data-ttu-id="2eef0-103">Beendet die Ausführung einer Pipeline in einer Daten factory.</span><span class="sxs-lookup"><span data-stu-id="2eef0-103">Stops a pipeline run in a data factory.</span></span>

## <span data-ttu-id="2eef0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2eef0-104">SYNTAX</span></span>

### <span data-ttu-id="2eef0-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="2eef0-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2eef0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2eef0-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2eef0-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="2eef0-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2eef0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2eef0-108">DESCRIPTION</span></span>
<span data-ttu-id="2eef0-109">Das **Cmdlet Stop-AzDataFactoryV2PipelineRun** beendet einen Pipelinelauf in einer Datenfactory, die mit der Pipelinelauf-ID angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="2eef0-109">The **Stop-AzDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pipeline run ID.</span></span>

## <span data-ttu-id="2eef0-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2eef0-110">EXAMPLES</span></span>

### <span data-ttu-id="2eef0-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2eef0-111">Example 1</span></span>
```
PS C:\> Stop-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="2eef0-112">Mit diesem Befehl wird die Pipeline mit der ID b9730a13-aa12-4926-a8b3-8e3a974ab0bd in der WikiADF-Factory beendet.</span><span class="sxs-lookup"><span data-stu-id="2eef0-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="2eef0-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2eef0-113">PARAMETERS</span></span>

### <span data-ttu-id="2eef0-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="2eef0-114">-DataFactory</span></span>
<span data-ttu-id="2eef0-115">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2eef0-115">The data factory object.</span></span>

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

### <span data-ttu-id="2eef0-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2eef0-116">-DataFactoryName</span></span>
<span data-ttu-id="2eef0-117">Der Name der Datenfabrik.</span><span class="sxs-lookup"><span data-stu-id="2eef0-117">The data factory name.</span></span>

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

### <span data-ttu-id="2eef0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eef0-118">-DefaultProfile</span></span>
<span data-ttu-id="2eef0-119">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2eef0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2eef0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2eef0-120">-InputObject</span></span>
<span data-ttu-id="2eef0-121">Die Ausführungs-ID der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="2eef0-121">The Run ID of the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2eef0-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2eef0-122">-PassThru</span></span>
<span data-ttu-id="2eef0-123">Wenn das Cmdlet "write true" angegeben ist, ist der Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="2eef0-123">If specified the cmdlet write true in case operation succeeds.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eef0-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="2eef0-124">-PipelineRunId</span></span>
<span data-ttu-id="2eef0-125">Die Ausführungs-ID der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="2eef0-125">The Run ID of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2eef0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eef0-126">-ResourceGroupName</span></span>
<span data-ttu-id="2eef0-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2eef0-127">The resource group name.</span></span>

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

### <span data-ttu-id="2eef0-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2eef0-128">-Confirm</span></span>
<span data-ttu-id="2eef0-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2eef0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2eef0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2eef0-130">-WhatIf</span></span>
<span data-ttu-id="2eef0-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2eef0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2eef0-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2eef0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2eef0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eef0-133">CommonParameters</span></span>
<span data-ttu-id="2eef0-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eef0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eef0-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2eef0-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eef0-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2eef0-136">INPUTS</span></span>

### <span data-ttu-id="2eef0-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="2eef0-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

### <span data-ttu-id="2eef0-138">System.String</span><span class="sxs-lookup"><span data-stu-id="2eef0-138">System.String</span></span>

### <span data-ttu-id="2eef0-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="2eef0-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="2eef0-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2eef0-140">OUTPUTS</span></span>

### <span data-ttu-id="2eef0-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2eef0-141">System.Boolean</span></span>

## <span data-ttu-id="2eef0-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2eef0-142">NOTES</span></span>

## <span data-ttu-id="2eef0-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2eef0-143">RELATED LINKS</span></span>
