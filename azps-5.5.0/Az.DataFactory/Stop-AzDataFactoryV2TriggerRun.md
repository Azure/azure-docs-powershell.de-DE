---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: e2800614e414a041073ae5396fb4b0e1e5833b59
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162049"
---
# <span data-ttu-id="0187c-101">Stop-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="0187c-101">Stop-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="0187c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0187c-102">SYNOPSIS</span></span>
<span data-ttu-id="0187c-103">Beendet die Ausführung eines Triggers in einer Daten factory.</span><span class="sxs-lookup"><span data-stu-id="0187c-103">Stops a trigger run in a data factory.</span></span>

## <span data-ttu-id="0187c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0187c-104">SYNTAX</span></span>

### <span data-ttu-id="0187c-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="0187c-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0187c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0187c-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0187c-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0187c-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0187c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0187c-108">DESCRIPTION</span></span>
<span data-ttu-id="0187c-109">Das **Cmdlet "Stop-AzDataFactoryV2TriggerRun"** beendet die Ausführung eines Triggers in einer Datenfactory, die mit dem Triggernamen und der Auslöser-Ausführungs-ID angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0187c-109">The **Stop-AzDataFactoryV2TriggerRun** cmdlet stops a trigger run in a data factory specified with the trigger name and trigger run ID.</span></span>
<span data-ttu-id="0187c-110">Derzeit nur für TumblingWindowTriggers im Status "WaitingOnDependency" unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0187c-110">Currently only supported for TumblingWindowTriggers in WaitingOnDependency State.</span></span>

## <span data-ttu-id="0187c-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0187c-111">EXAMPLES</span></span>

### <span data-ttu-id="0187c-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0187c-112">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```

<span data-ttu-id="0187c-113">Dieser Befehl beendet die Ausführung des Triggers mit der ID '08586002468005888497807248799CU16' in der WikiADF-Factory.</span><span class="sxs-lookup"><span data-stu-id="0187c-113">This command stops the trigger run with id '08586002468005888497807248799CU16' in the factory WikiADF.</span></span>

## <span data-ttu-id="0187c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0187c-114">PARAMETERS</span></span>

### <span data-ttu-id="0187c-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="0187c-115">-DataFactory</span></span>
<span data-ttu-id="0187c-116">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0187c-116">The data factory object.</span></span>

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

### <span data-ttu-id="0187c-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0187c-117">-DataFactoryName</span></span>
<span data-ttu-id="0187c-118">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="0187c-118">The data factory name.</span></span>

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

### <span data-ttu-id="0187c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0187c-119">-DefaultProfile</span></span>
<span data-ttu-id="0187c-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0187c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0187c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0187c-121">-InputObject</span></span>
<span data-ttu-id="0187c-122">Die Informationen zum Trigger werden ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0187c-122">The information about the trigger run.</span></span>

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

### <span data-ttu-id="0187c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0187c-123">-PassThru</span></span>
<span data-ttu-id="0187c-124">Wenn angegeben, wird für den Fall, dass der Vorgang erfolgreich ausgeführt wird, das Cmdlet "true" geschrieben.</span><span class="sxs-lookup"><span data-stu-id="0187c-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="0187c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0187c-125">-ResourceGroupName</span></span>
<span data-ttu-id="0187c-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0187c-126">The resource group name.</span></span>

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

### <span data-ttu-id="0187c-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="0187c-127">-TriggerName</span></span>
<span data-ttu-id="0187c-128">Der Auslösername.</span><span class="sxs-lookup"><span data-stu-id="0187c-128">The trigger name.</span></span>

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

### <span data-ttu-id="0187c-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="0187c-129">-TriggerRunId</span></span>
<span data-ttu-id="0187c-130">Die Ausführungs-ID des Triggers.</span><span class="sxs-lookup"><span data-stu-id="0187c-130">The Run ID of the trigger.</span></span>

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

### <span data-ttu-id="0187c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0187c-131">-Confirm</span></span>
<span data-ttu-id="0187c-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0187c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0187c-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0187c-133">-WhatIf</span></span>
<span data-ttu-id="0187c-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0187c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0187c-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0187c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0187c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0187c-136">CommonParameters</span></span>
<span data-ttu-id="0187c-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0187c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0187c-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0187c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0187c-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0187c-139">INPUTS</span></span>

### <span data-ttu-id="0187c-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="0187c-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="0187c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="0187c-141">System.String</span></span>

### <span data-ttu-id="0187c-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0187c-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="0187c-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0187c-143">OUTPUTS</span></span>

### <span data-ttu-id="0187c-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0187c-144">System.Boolean</span></span>

## <span data-ttu-id="0187c-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0187c-145">NOTES</span></span>

## <span data-ttu-id="0187c-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0187c-146">RELATED LINKS</span></span>
