---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 98b34b4926dc4edc15d30308b2d6bfee33336f0d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651663"
---
# <span data-ttu-id="fc8ab-101">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="fc8ab-101">Start-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="fc8ab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fc8ab-102">SYNOPSIS</span></span>
<span data-ttu-id="fc8ab-103">Startet eine Datenfluss-Debugsitzung in Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="fc8ab-103">Starts a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="fc8ab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc8ab-104">SYNTAX</span></span>

### <span data-ttu-id="fc8ab-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="fc8ab-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc8ab-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fc8ab-106">ByFactoryObject</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc8ab-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fc8ab-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc8ab-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fc8ab-108">DESCRIPTION</span></span>
<span data-ttu-id="fc8ab-109">Dieser lange ausgeführte Befehl startet eine Datenfluss-Debug-Sitzung für die bevorstehenden Debug-Befehle.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-109">This long running command starts a data flow debug session for the upcoming debug commands.</span></span> <span data-ttu-id="fc8ab-110">Dieser Befehl kann mit einer Integration Runtime-Definition angefügt werden, um die Größe/den Typ des Debug-Sitzungs Clusters zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-110">This command can attach with an integration runtime definition to configure the size/type of debug session cluster.</span></span>
<span data-ttu-id="fc8ab-111">Die PowerShell-Befehlssequenz für den Workflow zum Debuggen von Datenströmen sollte wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="fc8ab-111">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="fc8ab-112">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="fc8ab-112">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="fc8ab-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="fc8ab-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="fc8ab-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (wiederholen Sie diesen Schritt für verschiedene Befehle/Ziele, oder wiederholen Sie Schritt 2-3, um die Paketdatei zu ändern)</span><span class="sxs-lookup"><span data-stu-id="fc8ab-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="fc8ab-115">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="fc8ab-115">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="fc8ab-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fc8ab-116">EXAMPLES</span></span>

### <span data-ttu-id="fc8ab-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fc8ab-117">Example 1</span></span>
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

<span data-ttu-id="fc8ab-118">Startet eine Debugsitzung mit AsJob-Flag.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-118">Starts a debug session with AsJob flag.</span></span>

## <span data-ttu-id="fc8ab-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc8ab-119">PARAMETERS</span></span>

### <span data-ttu-id="fc8ab-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fc8ab-120">-AsJob</span></span>
<span data-ttu-id="fc8ab-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fc8ab-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fc8ab-122">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="fc8ab-122">-DataFactory</span></span>
<span data-ttu-id="fc8ab-123">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-123">The data factory object.</span></span>

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

### <span data-ttu-id="fc8ab-124">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="fc8ab-124">-DataFactoryName</span></span>
<span data-ttu-id="fc8ab-125">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-125">The data factory name.</span></span>

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

### <span data-ttu-id="fc8ab-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc8ab-126">-DefaultProfile</span></span>
<span data-ttu-id="fc8ab-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc8ab-128">-IntegrationRuntimeFile</span><span class="sxs-lookup"><span data-stu-id="fc8ab-128">-IntegrationRuntimeFile</span></span>
<span data-ttu-id="fc8ab-129">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-129">The JSON file path.</span></span>

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

### <span data-ttu-id="fc8ab-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc8ab-130">-ResourceGroupName</span></span>
<span data-ttu-id="fc8ab-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-131">The resource group name.</span></span>

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

### <span data-ttu-id="fc8ab-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="fc8ab-132">-ResourceId</span></span>
<span data-ttu-id="fc8ab-133">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-133">The Azure resource ID.</span></span>

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

### <span data-ttu-id="fc8ab-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fc8ab-134">-Confirm</span></span>
<span data-ttu-id="fc8ab-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc8ab-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc8ab-136">-WhatIf</span></span>
<span data-ttu-id="fc8ab-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc8ab-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc8ab-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc8ab-139">CommonParameters</span></span>
<span data-ttu-id="fc8ab-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc8ab-141">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc8ab-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc8ab-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fc8ab-142">INPUTS</span></span>

### <span data-ttu-id="fc8ab-143">System. String</span><span class="sxs-lookup"><span data-stu-id="fc8ab-143">System.String</span></span>

### <span data-ttu-id="fc8ab-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="fc8ab-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="fc8ab-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fc8ab-145">OUTPUTS</span></span>

### <span data-ttu-id="fc8ab-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="fc8ab-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span></span>

## <span data-ttu-id="fc8ab-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="fc8ab-147">NOTES</span></span>
<span data-ttu-id="fc8ab-148">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="fc8ab-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="fc8ab-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fc8ab-149">RELATED LINKS</span></span>

[<span data-ttu-id="fc8ab-150">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="fc8ab-150">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="fc8ab-151">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="fc8ab-151">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="fc8ab-152">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="fc8ab-152">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="fc8ab-153">Stopp-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="fc8ab-153">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)