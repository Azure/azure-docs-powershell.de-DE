---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/invoke-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: 91eb23f3af613cf349219f82d133d08dd6e65b5c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930123"
---
# <span data-ttu-id="0f291-101">Invoke-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="0f291-101">Invoke-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="0f291-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f291-102">SYNOPSIS</span></span>
 <span data-ttu-id="0f291-103">Ruft eine andere Instanz einer Triggerauslösung auf.</span><span class="sxs-lookup"><span data-stu-id="0f291-103">Invokes another instance of a trigger run.</span></span>

## <span data-ttu-id="0f291-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f291-104">SYNTAX</span></span>

### <span data-ttu-id="0f291-105">ByFactoryNameByParameterFile (Standard)</span><span class="sxs-lookup"><span data-stu-id="0f291-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f291-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0f291-106">ByInputObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f291-107">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="0f291-107">ByFactoryName</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f291-108">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0f291-108">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0f291-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0f291-109">DESCRIPTION</span></span>
<span data-ttu-id="0f291-110">Der **Befehl Invoke-AzDataFactoryV2TriggerRun startet** eine andere Instanz eines Triggers, der mit einer neuen Trigger-Run-ID ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0f291-110">The **Invoke-AzDataFactoryV2TriggerRun** command starts another instance of a trigger run with a new trigger run id.</span></span>

## <span data-ttu-id="0f291-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0f291-111">EXAMPLES</span></span>

### <span data-ttu-id="0f291-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0f291-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```
<span data-ttu-id="0f291-113">Startet eine andere Instanz eines Triggers, die mit einer neuen Trigger-Ausführungs-ID ausgeführt wird, und bleibt dabei das gleiche FensterStartTime und windowEndTime wie der ursprüngliche Trigger.</span><span class="sxs-lookup"><span data-stu-id="0f291-113">Starts another instance of a trigger run with a new trigger run id, keeping the same windowStartTime and windowEndTime as the original trigger run.</span></span>

## <span data-ttu-id="0f291-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0f291-114">PARAMETERS</span></span>

### <span data-ttu-id="0f291-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="0f291-115">-DataFactory</span></span>
<span data-ttu-id="0f291-116">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0f291-116">The data factory object.</span></span>

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

### <span data-ttu-id="0f291-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0f291-117">-DataFactoryName</span></span>
<span data-ttu-id="0f291-118">Der Name der Datenfabrik.</span><span class="sxs-lookup"><span data-stu-id="0f291-118">The data factory name.</span></span>

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

### <span data-ttu-id="0f291-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f291-119">-DefaultProfile</span></span>
<span data-ttu-id="0f291-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0f291-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f291-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f291-121">-InputObject</span></span>
<span data-ttu-id="0f291-122">Die Informationen zum Trigger werden ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0f291-122">The information about the trigger run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f291-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f291-123">-PassThru</span></span>
<span data-ttu-id="0f291-124">Wenn das Cmdlet "write true" angegeben ist, ist der Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="0f291-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="0f291-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f291-125">-ResourceGroupName</span></span>
<span data-ttu-id="0f291-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0f291-126">The resource group name.</span></span>

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

### <span data-ttu-id="0f291-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="0f291-127">-TriggerName</span></span>
<span data-ttu-id="0f291-128">Der Triggername.</span><span class="sxs-lookup"><span data-stu-id="0f291-128">The trigger name.</span></span>

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

### <span data-ttu-id="0f291-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="0f291-129">-TriggerRunId</span></span>
<span data-ttu-id="0f291-130">Die Ausführungs-ID des Triggers.</span><span class="sxs-lookup"><span data-stu-id="0f291-130">The Run ID of the trigger.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f291-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0f291-131">-Confirm</span></span>
<span data-ttu-id="0f291-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0f291-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f291-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f291-133">-WhatIf</span></span>
<span data-ttu-id="0f291-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0f291-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f291-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0f291-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f291-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f291-136">CommonParameters</span></span>
<span data-ttu-id="0f291-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f291-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f291-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f291-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f291-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0f291-139">INPUTS</span></span>

### <span data-ttu-id="0f291-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="0f291-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="0f291-141">System.String</span><span class="sxs-lookup"><span data-stu-id="0f291-141">System.String</span></span>

### <span data-ttu-id="0f291-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0f291-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="0f291-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0f291-143">OUTPUTS</span></span>

### <span data-ttu-id="0f291-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="0f291-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="0f291-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0f291-145">NOTES</span></span>

## <span data-ttu-id="0f291-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0f291-146">RELATED LINKS</span></span>
