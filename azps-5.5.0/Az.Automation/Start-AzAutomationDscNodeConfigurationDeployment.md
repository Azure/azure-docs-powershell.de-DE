---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 41605bbdd37ae29f420581f9ad916a1cc87150be
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168225"
---
# <span data-ttu-id="90ca0-101">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="90ca0-101">Start-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="90ca0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90ca0-102">SYNOPSIS</span></span>
<span data-ttu-id="90ca0-103">Stellt eine KONFIGURATION des DSC-Knotens in der Automatisierung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="90ca0-103">Deploys a DSC Node configuration in Automation.</span></span>

## <span data-ttu-id="90ca0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="90ca0-104">SYNTAX</span></span>

### <span data-ttu-id="90ca0-105">ByAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="90ca0-105">ByAll (Default)</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 [-Schedule <Schedule>] [-Force] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90ca0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="90ca0-106">ByInputObject</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 -InputObject <NodeConfigurationDeployment> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90ca0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="90ca0-107">DESCRIPTION</span></span>
<span data-ttu-id="90ca0-108">Das **Cmdlet "Start-AzAutomationDscNodeConfigurationDeployment"** stellt eine Knotenkonfiguration (Desired State Configuration, DSC) in der Azure Automation bereit.</span><span class="sxs-lookup"><span data-stu-id="90ca0-108">The **Start-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="90ca0-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="90ca0-109">EXAMPLES</span></span>

### <span data-ttu-id="90ca0-110">Beispiel 1: Bereitstellen einer Azure DSC-Knotenkonfiguration in der Automatisierung</span><span class="sxs-lookup"><span data-stu-id="90ca0-110">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzAutomationDscNodeConfigurationDeployment `
            -NodeConfigurationName "Config01.Node1" `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01" `
            -NodeName $nodes `

Starting a node configuration deployment.
Starting a node configuration deployment. It will override any existing node configurations assigned to the node.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Yes

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 35b14eb4-52b7-4a1d-ad62-8e9f84adc657
Job                   : Microsoft.Azure.Commands.Automation.Model.Job
JobStatus             : New
NodeStatus            :
NodeConfigurationName : Config01.Node1
JobSchedule           :
JobScheduleId         : 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="90ca0-111">Mit dem oben angegebenen Befehl wird die Konfiguration des DSC-Knotens namens "Config01.Node1" für das angegebene zweidimensionale Array von Knotennamen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="90ca0-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="90ca0-112">Die Bereitstellung erfolgt in mehrstufiger Form.</span><span class="sxs-lookup"><span data-stu-id="90ca0-112">The deployment happens in a staged manner.</span></span>

### <span data-ttu-id="90ca0-113">Beispiel 2: Planen einer Azure DSC-Knoten-Konfigurationsbereitstellung in der Automatisierung</span><span class="sxs-lookup"><span data-stu-id="90ca0-113">Example 2: Schedule an Azure DSC node configuration deployment in Automation</span></span>
```
PS C:\> $sched = New-AzAutomationSchedule -AutomationAccountName "Contoso01" `
            -ResourceGroupName "ResourceGroup01" `
            -Name "TestSchedule" `
            -StartTime "23:00" `
            -OneTime
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzAutomationDscNodeConfigurationDeployment `
            -NodeConfigurationName "Config01.Node1" `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01" `
            -NodeName $nodes `
            -Schedule $sched

Starting a node configuration deployment.
Starting a node configuration deployment. It will override any existing node configurations assigned to the node.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 00000000-0000-0000-0000-000000000000
Job                   :
JobStatus             :
NodeStatus            :
NodeConfigurationName : Config01.Node1
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
```

<span data-ttu-id="90ca0-114">Der oben aufgeführte Befehl plant eine Bereitstellung einer DSC-Knotenkonfiguration namens "Config01.Node1" für das angegebene zweidimensionale Array mit Knotennamen.</span><span class="sxs-lookup"><span data-stu-id="90ca0-114">The above command schedules a deployment of a DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="90ca0-115">Die Bereitstellung erfolgt mehrstufiger Art und Weise und wird basierend auf dem Zeitplan ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="90ca0-115">The deployment happens in a staged manner and will be executed based on the schedule.</span></span>

## <span data-ttu-id="90ca0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90ca0-116">PARAMETERS</span></span>

### <span data-ttu-id="90ca0-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="90ca0-117">-AutomationAccountName</span></span>
<span data-ttu-id="90ca0-118">Gibt den Namen des Automatisierungskontos an, das die VON diesem Cmdlet kompilierte DSC-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="90ca0-118">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90ca0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90ca0-119">-DefaultProfile</span></span>
<span data-ttu-id="90ca0-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="90ca0-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90ca0-121">-Force</span><span class="sxs-lookup"><span data-stu-id="90ca0-121">-Force</span></span>
<span data-ttu-id="90ca0-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="90ca0-122">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90ca0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90ca0-123">-InputObject</span></span>
<span data-ttu-id="90ca0-124">Eingabeobjekt für die Pipierung</span><span class="sxs-lookup"><span data-stu-id="90ca0-124">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90ca0-125">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="90ca0-125">-NodeConfigurationName</span></span>
<span data-ttu-id="90ca0-126">Gibt den Namen der DSC-Knotenkonfiguration an, die von diesem Cmdlet bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="90ca0-126">Specifies the name of the DSC node configuration that this cmdlet deploys.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90ca0-127">-NodeName</span><span class="sxs-lookup"><span data-stu-id="90ca0-127">-NodeName</span></span>
<span data-ttu-id="90ca0-128">Gibt die Namen der Knoten an, für die die Knotenkonfiguration bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="90ca0-128">Specifies the names of the nodes to which the Node Configuration would be deployed to.</span></span>

```yaml
Type: System.String[][]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90ca0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90ca0-129">-ResourceGroupName</span></span>
<span data-ttu-id="90ca0-130">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet eine Konfiguration kompiliert.</span><span class="sxs-lookup"><span data-stu-id="90ca0-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90ca0-131">-Schedule</span><span class="sxs-lookup"><span data-stu-id="90ca0-131">-Schedule</span></span>
<span data-ttu-id="90ca0-132">Automatisierungszeitplanobjekt zum Planen des Bereitstellungsauftrags.</span><span class="sxs-lookup"><span data-stu-id="90ca0-132">Automation Schedule object to schedule the deployment job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.Schedule
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90ca0-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90ca0-133">-Confirm</span></span>
<span data-ttu-id="90ca0-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="90ca0-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90ca0-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="90ca0-135">-WhatIf</span></span>
<span data-ttu-id="90ca0-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90ca0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90ca0-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="90ca0-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90ca0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90ca0-138">CommonParameters</span></span>
<span data-ttu-id="90ca0-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90ca0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90ca0-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90ca0-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90ca0-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="90ca0-141">INPUTS</span></span>

### <span data-ttu-id="90ca0-142">System.String</span><span class="sxs-lookup"><span data-stu-id="90ca0-142">System.String</span></span>

### <span data-ttu-id="90ca0-143">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="90ca0-143">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="90ca0-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="90ca0-144">OUTPUTS</span></span>

### <span data-ttu-id="90ca0-145">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="90ca0-145">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="90ca0-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="90ca0-146">NOTES</span></span>

## <span data-ttu-id="90ca0-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="90ca0-147">RELATED LINKS</span></span>

[<span data-ttu-id="90ca0-148">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="90ca0-148">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="90ca0-149">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="90ca0-149">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="90ca0-150">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="90ca0-150">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="90ca0-151">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="90ca0-151">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="90ca0-152">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="90ca0-152">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)

[<span data-ttu-id="90ca0-153">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="90ca0-153">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)
