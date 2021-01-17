---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2dataflowdebugsessioncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
ms.openlocfilehash: 4009835b2efe8346ff873bde59870954c73ab5d7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470574"
---
# <span data-ttu-id="5df9a-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="5df9a-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>

## <span data-ttu-id="5df9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5df9a-102">SYNOPSIS</span></span>
<span data-ttu-id="5df9a-103">Rufen Sie die Debugaktion in der Datenflussdebuggersitzung auf.</span><span class="sxs-lookup"><span data-stu-id="5df9a-103">Invoke debug action in data flow debug session.</span></span>

## <span data-ttu-id="5df9a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5df9a-104">SYNTAX</span></span>

### <span data-ttu-id="5df9a-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="5df9a-105">ByFactoryName (Default)</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5df9a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5df9a-106">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5df9a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5df9a-107">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5df9a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5df9a-108">DESCRIPTION</span></span>
<span data-ttu-id="5df9a-109">Mit diesem Befehl werden Datenvorschau/Stats-Vorschau/Ausdrucksvorschau für einen anderen Datenflussstrom in der Debugsitzung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5df9a-109">This command executes data preview/stats preview/expression preview for different stream of data flow in debug session.</span></span>
<span data-ttu-id="5df9a-110">Die Befehlssequenz von PowerShell für den Workflow für den Datenflussdebugger sollte wie im Folgenden angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="5df9a-110">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="5df9a-111">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="5df9a-111">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="5df9a-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="5df9a-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="5df9a-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (wiederholen Sie diesen Schritt für verschiedene Befehle/Ziele, oder wiederholen Sie die Schritte 2 bis 3, um die Paketdatei zu ändern.)</span><span class="sxs-lookup"><span data-stu-id="5df9a-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="5df9a-114">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="5df9a-114">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="5df9a-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5df9a-115">EXAMPLES</span></span>

### <span data-ttu-id="5df9a-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5df9a-116">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> $result = Invoke-AzDataFactoryV2DataFlowDebugSessionCommand -ResourceGroupName adf -DataFactoryName WiKiADF -Command executePreviewQuery -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d -StreamName source1 -RowLimits 100 -AsJob
PS C:\WINDOWS\system32> $result

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
3      Long Running... AzureLongRun... Running       True            localhost            Invoke-AzDataFactoryV2...


(After 2 minutes)

PS C:\WINDOWS\system32> $result

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
3      Long Running... AzureLongRun... Completed     True            localhost            Invoke-AzDataFactoryV2...

PS C:\WINDOWS\system32> $output = ConvertFrom-Json($result.Output.Data)
PS C:\WINDOWS\system32> $output.output

    {
      "schema": "output(ResourceAgencyNum as string, PublicName as string)" ,
      "data": [["4445679354", "Syrian Refugee Information", 1], ["44456793", "Syrian Refugee Information", 1]]
    }


```

<span data-ttu-id="5df9a-117">In diesem Beispiel wird der Befehl "Datenvorschau" für die Debugsitzung "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in der Daten factory "WiKiADF" aufgerufen. Konvertieren Sie dann die JSON-Ausgabe in eine lesbare Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="5df9a-117">This example invokes data preview command for debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WiKiADF" and then convert the JSON output into readable string.</span></span>

## <span data-ttu-id="5df9a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5df9a-118">PARAMETERS</span></span>

### <span data-ttu-id="5df9a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5df9a-119">-AsJob</span></span>
<span data-ttu-id="5df9a-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5df9a-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5df9a-121">-Columns</span><span class="sxs-lookup"><span data-stu-id="5df9a-121">-Columns</span></span>
<span data-ttu-id="5df9a-122">Die Spaltenliste für die Vorschau der Datenflussstatistiken.</span><span class="sxs-lookup"><span data-stu-id="5df9a-122">The columns list for data flow statistics preview.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5df9a-123">-Command</span><span class="sxs-lookup"><span data-stu-id="5df9a-123">-Command</span></span>
<span data-ttu-id="5df9a-124">Der Befehl zum Debuggen des Datenflusses.</span><span class="sxs-lookup"><span data-stu-id="5df9a-124">The data flow debug command.</span></span> <span data-ttu-id="5df9a-125">Optionalen sind executePreviewQuery, executeStatisticsQuery und executeExpressionQuery</span><span class="sxs-lookup"><span data-stu-id="5df9a-125">Optionals are executePreviewQuery, executeStatisticsQuery and executeExpressionQuery</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5df9a-126">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="5df9a-126">-DataFactory</span></span>
<span data-ttu-id="5df9a-127">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="5df9a-127">The data factory object.</span></span>

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

### <span data-ttu-id="5df9a-128">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5df9a-128">-DataFactoryName</span></span>
<span data-ttu-id="5df9a-129">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="5df9a-129">The data factory name.</span></span>

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

### <span data-ttu-id="5df9a-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5df9a-130">-DefaultProfile</span></span>
<span data-ttu-id="5df9a-131">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5df9a-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5df9a-132">-Expression</span><span class="sxs-lookup"><span data-stu-id="5df9a-132">-Expression</span></span>
<span data-ttu-id="5df9a-133">Der Ausdruck für die Vorschau des Datenflussausdrucks.</span><span class="sxs-lookup"><span data-stu-id="5df9a-133">The expression for data flow expression preview.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5df9a-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5df9a-134">-ResourceGroupName</span></span>
<span data-ttu-id="5df9a-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5df9a-135">The resource group name.</span></span>

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

### <span data-ttu-id="5df9a-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5df9a-136">-ResourceId</span></span>
<span data-ttu-id="5df9a-137">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="5df9a-137">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5df9a-138">-RowLimits</span><span class="sxs-lookup"><span data-stu-id="5df9a-138">-RowLimits</span></span>
<span data-ttu-id="5df9a-139">Das Zeilenlimit für die Datenflussdatenvorschau.</span><span class="sxs-lookup"><span data-stu-id="5df9a-139">The row limit for data flow data preview.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5df9a-140">-SessionId</span><span class="sxs-lookup"><span data-stu-id="5df9a-140">-SessionId</span></span>
<span data-ttu-id="5df9a-141">Die Sitzungs-ID des Datenflussdebuggers.</span><span class="sxs-lookup"><span data-stu-id="5df9a-141">The data flow debug session ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5df9a-142">-StreamName</span><span class="sxs-lookup"><span data-stu-id="5df9a-142">-StreamName</span></span>
<span data-ttu-id="5df9a-143">Der Datenstromname des Datenflusses zum Debuggen.</span><span class="sxs-lookup"><span data-stu-id="5df9a-143">The stream name of data flow for debugging.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5df9a-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5df9a-144">-Confirm</span></span>
<span data-ttu-id="5df9a-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5df9a-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5df9a-146">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5df9a-146">-WhatIf</span></span>
<span data-ttu-id="5df9a-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5df9a-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5df9a-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5df9a-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5df9a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5df9a-149">CommonParameters</span></span>
<span data-ttu-id="5df9a-150">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5df9a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5df9a-151">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5df9a-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5df9a-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5df9a-152">INPUTS</span></span>

### <span data-ttu-id="5df9a-153">System.String</span><span class="sxs-lookup"><span data-stu-id="5df9a-153">System.String</span></span>

### <span data-ttu-id="5df9a-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="5df9a-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="5df9a-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5df9a-155">OUTPUTS</span></span>

### <span data-ttu-id="5df9a-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span><span class="sxs-lookup"><span data-stu-id="5df9a-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span></span>

## <span data-ttu-id="5df9a-157">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5df9a-157">NOTES</span></span>
<span data-ttu-id="5df9a-158">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factoryKeywords: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="5df9a-158">Keywords: azure, azurerm, arm, resource, management, manager, data, factoriesKeywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5df9a-159">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5df9a-159">RELATED LINKS</span></span>

[<span data-ttu-id="5df9a-160">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="5df9a-160">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="5df9a-161">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="5df9a-161">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="5df9a-162">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="5df9a-162">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="5df9a-163">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="5df9a-163">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)
