---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 27a7f0ee401f044cc693cecf103f2bed1e8ce946
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144372"
---
# <span data-ttu-id="456e1-101">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="456e1-101">Start-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="456e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="456e1-102">SYNOPSIS</span></span>
<span data-ttu-id="456e1-103">Startet eine Datenflussdebuggersitzung in Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="456e1-103">Starts a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="456e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="456e1-104">SYNTAX</span></span>

### <span data-ttu-id="456e1-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="456e1-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="456e1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="456e1-106">ByFactoryObject</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="456e1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="456e1-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="456e1-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="456e1-108">DESCRIPTION</span></span>
<span data-ttu-id="456e1-109">Mit diesem Befehl mit langer Ausführungs ausgeführt wird eine Datenflussdebuggersitzung für die anstehenden Debugbefehle gestartet.</span><span class="sxs-lookup"><span data-stu-id="456e1-109">This long running command starts a data flow debug session for the upcoming debug commands.</span></span> <span data-ttu-id="456e1-110">Dieser Befehl kann mit einer Integrationslaufzeitdefinition hinzugefügt werden, um die Größe/den Typ des Debugsitzungsclusters zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="456e1-110">This command can attach with an integration runtime definition to configure the size/type of debug session cluster.</span></span>
<span data-ttu-id="456e1-111">Die Befehlssequenz von PowerShell für den Workflow für den Datenflussdebugger sollte wie im Folgenden angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="456e1-111">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="456e1-112">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="456e1-112">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="456e1-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="456e1-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="456e1-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (wiederholen Sie diesen Schritt für verschiedene Befehle/Ziele, oder wiederholen Sie die Schritte 2 bis 3, um die Paketdatei zu ändern.)</span><span class="sxs-lookup"><span data-stu-id="456e1-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="456e1-115">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="456e1-115">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="456e1-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="456e1-116">EXAMPLES</span></span>

### <span data-ttu-id="456e1-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="456e1-117">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> $job = Start-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName jikma0601sea -AsJob
PS C:\WINDOWS\system32> $job 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Running       True            localhost            Start-AzDataFactoryV2D...

(After 5 minutes)

PS C:\WINDOWS\system32> $job

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Completed     True            localhost            Start-AzDataFactoryV2D...


PS C:\WINDOWS\system32> $job.Output

SessionId                            Status
---------                            ------
550effe4-93a3-485c-8525-eaf25259efbd Succeeded

```

<span data-ttu-id="456e1-118">Startet eine Debugsitzung mit dem Kennzeichen "AsJob".</span><span class="sxs-lookup"><span data-stu-id="456e1-118">Starts a debug session with AsJob flag.</span></span>

## <span data-ttu-id="456e1-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="456e1-119">PARAMETERS</span></span>

### <span data-ttu-id="456e1-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="456e1-120">-AsJob</span></span>
<span data-ttu-id="456e1-121">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="456e1-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="456e1-122">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="456e1-122">-DataFactory</span></span>
<span data-ttu-id="456e1-123">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="456e1-123">The data factory object.</span></span>

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

### <span data-ttu-id="456e1-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="456e1-124">-DataFactoryName</span></span>
<span data-ttu-id="456e1-125">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="456e1-125">The data factory name.</span></span>

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

### <span data-ttu-id="456e1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="456e1-126">-DefaultProfile</span></span>
<span data-ttu-id="456e1-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="456e1-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="456e1-128">-IntegrationRuntimeFile</span><span class="sxs-lookup"><span data-stu-id="456e1-128">-IntegrationRuntimeFile</span></span>
<span data-ttu-id="456e1-129">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="456e1-129">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="456e1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="456e1-130">-ResourceGroupName</span></span>
<span data-ttu-id="456e1-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="456e1-131">The resource group name.</span></span>

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

### <span data-ttu-id="456e1-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="456e1-132">-ResourceId</span></span>
<span data-ttu-id="456e1-133">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="456e1-133">The Azure resource ID.</span></span>

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

### <span data-ttu-id="456e1-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="456e1-134">-Confirm</span></span>
<span data-ttu-id="456e1-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="456e1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="456e1-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="456e1-136">-WhatIf</span></span>
<span data-ttu-id="456e1-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="456e1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="456e1-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="456e1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="456e1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="456e1-139">CommonParameters</span></span>
<span data-ttu-id="456e1-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="456e1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="456e1-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="456e1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="456e1-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="456e1-142">INPUTS</span></span>

### <span data-ttu-id="456e1-143">System.String</span><span class="sxs-lookup"><span data-stu-id="456e1-143">System.String</span></span>

### <span data-ttu-id="456e1-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="456e1-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="456e1-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="456e1-145">OUTPUTS</span></span>

### <span data-ttu-id="456e1-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="456e1-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span></span>

## <span data-ttu-id="456e1-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="456e1-147">NOTES</span></span>
<span data-ttu-id="456e1-148">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="456e1-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="456e1-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="456e1-149">RELATED LINKS</span></span>

[<span data-ttu-id="456e1-150">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="456e1-150">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="456e1-151">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="456e1-151">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="456e1-152">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="456e1-152">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="456e1-153">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="456e1-153">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)