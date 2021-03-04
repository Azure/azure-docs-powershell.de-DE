---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/stop-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: 1e3310b99173c0a7fa83dcada286833747457213
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925051"
---
# <span data-ttu-id="47d7f-101">Stop-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="47d7f-101">Stop-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="47d7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47d7f-102">SYNOPSIS</span></span>
<span data-ttu-id="47d7f-103">Beendet die Ausführung eines Triggers in einer Daten factory.</span><span class="sxs-lookup"><span data-stu-id="47d7f-103">Stops a trigger run in a data factory.</span></span>

## <span data-ttu-id="47d7f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47d7f-104">SYNTAX</span></span>

### <span data-ttu-id="47d7f-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="47d7f-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47d7f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="47d7f-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47d7f-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="47d7f-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="47d7f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47d7f-108">DESCRIPTION</span></span>
<span data-ttu-id="47d7f-109">Das **Cmdlet Stop-AzDataFactoryV2TriggerRun** beendet die Ausführung eines Triggers in einer Datenfactory, die mit dem Triggernamen und der Triggerlauf-ID angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="47d7f-109">The **Stop-AzDataFactoryV2TriggerRun** cmdlet stops a trigger run in a data factory specified with the trigger name and trigger run ID.</span></span>
<span data-ttu-id="47d7f-110">Wird derzeit nur für TumblingWindowTriggers im WaitingOnDependency State unterstützt.</span><span class="sxs-lookup"><span data-stu-id="47d7f-110">Currently only supported for TumblingWindowTriggers in WaitingOnDependency State.</span></span>

## <span data-ttu-id="47d7f-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="47d7f-111">EXAMPLES</span></span>

### <span data-ttu-id="47d7f-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="47d7f-112">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```

<span data-ttu-id="47d7f-113">Mit diesem Befehl wird die Ausführung des Triggers mit der ID '0858600246800588497807248799CU16' im Factory-WikiADF beendet.</span><span class="sxs-lookup"><span data-stu-id="47d7f-113">This command stops the trigger run with id '08586002468005888497807248799CU16' in the factory WikiADF.</span></span>

## <span data-ttu-id="47d7f-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="47d7f-114">PARAMETERS</span></span>

### <span data-ttu-id="47d7f-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="47d7f-115">-DataFactory</span></span>
<span data-ttu-id="47d7f-116">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="47d7f-116">The data factory object.</span></span>

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

### <span data-ttu-id="47d7f-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="47d7f-117">-DataFactoryName</span></span>
<span data-ttu-id="47d7f-118">Der Name der Datenfabrik.</span><span class="sxs-lookup"><span data-stu-id="47d7f-118">The data factory name.</span></span>

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

### <span data-ttu-id="47d7f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47d7f-119">-DefaultProfile</span></span>
<span data-ttu-id="47d7f-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47d7f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47d7f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47d7f-121">-InputObject</span></span>
<span data-ttu-id="47d7f-122">Die Informationen zum Trigger werden ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="47d7f-122">The information about the trigger run.</span></span>

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

### <span data-ttu-id="47d7f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47d7f-123">-PassThru</span></span>
<span data-ttu-id="47d7f-124">Wenn das Cmdlet "write true" angegeben ist, ist der Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="47d7f-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="47d7f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47d7f-125">-ResourceGroupName</span></span>
<span data-ttu-id="47d7f-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="47d7f-126">The resource group name.</span></span>

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

### <span data-ttu-id="47d7f-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="47d7f-127">-TriggerName</span></span>
<span data-ttu-id="47d7f-128">Der Triggername.</span><span class="sxs-lookup"><span data-stu-id="47d7f-128">The trigger name.</span></span>

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

### <span data-ttu-id="47d7f-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="47d7f-129">-TriggerRunId</span></span>
<span data-ttu-id="47d7f-130">Die Ausführungs-ID des Triggers.</span><span class="sxs-lookup"><span data-stu-id="47d7f-130">The Run ID of the trigger.</span></span>

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

### <span data-ttu-id="47d7f-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="47d7f-131">-Confirm</span></span>
<span data-ttu-id="47d7f-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="47d7f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47d7f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47d7f-133">-WhatIf</span></span>
<span data-ttu-id="47d7f-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="47d7f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47d7f-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="47d7f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47d7f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47d7f-136">CommonParameters</span></span>
<span data-ttu-id="47d7f-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47d7f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47d7f-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47d7f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47d7f-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="47d7f-139">INPUTS</span></span>

### <span data-ttu-id="47d7f-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="47d7f-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="47d7f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="47d7f-141">System.String</span></span>

### <span data-ttu-id="47d7f-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="47d7f-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="47d7f-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="47d7f-143">OUTPUTS</span></span>

### <span data-ttu-id="47d7f-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="47d7f-144">System.Boolean</span></span>

## <span data-ttu-id="47d7f-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="47d7f-145">NOTES</span></span>

## <span data-ttu-id="47d7f-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="47d7f-146">RELATED LINKS</span></span>
