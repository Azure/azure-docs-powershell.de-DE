---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 41605bbdd37ae29f420581f9ad916a1cc87150be
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290873"
---
# <span data-ttu-id="50719-101">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="50719-101">Start-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="50719-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50719-102">SYNOPSIS</span></span>
<span data-ttu-id="50719-103">Stellt eine KONFIGURATION des DSC-Knotens in der Automatisierung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="50719-103">Deploys a DSC Node configuration in Automation.</span></span>

## <span data-ttu-id="50719-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="50719-104">SYNTAX</span></span>

### <span data-ttu-id="50719-105">ByAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="50719-105">ByAll (Default)</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 [-Schedule <Schedule>] [-Force] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50719-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="50719-106">ByInputObject</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 -InputObject <NodeConfigurationDeployment> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50719-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50719-107">DESCRIPTION</span></span>
<span data-ttu-id="50719-108">Das **Cmdlet "Start-AzAutomationDscNodeConfigurationDeployment"** stellt eine Knotenkonfiguration (Desired State Configuration, DSC) in der Azure Automation bereit.</span><span class="sxs-lookup"><span data-stu-id="50719-108">The **Start-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="50719-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="50719-109">EXAMPLES</span></span>

### <span data-ttu-id="50719-110">Beispiel 1: Bereitstellen einer Azure DSC-Knotenkonfiguration in der Automatisierung</span><span class="sxs-lookup"><span data-stu-id="50719-110">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
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

<span data-ttu-id="50719-111">Mit dem oben angegebenen Befehl wird die Konfiguration des DSC-Knotens namens "Config01.Node1" für das angegebene zweidimensionale Array von Knotennamen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="50719-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="50719-112">Die Bereitstellung erfolgt in mehrstufiger Form.</span><span class="sxs-lookup"><span data-stu-id="50719-112">The deployment happens in a staged manner.</span></span>

### <span data-ttu-id="50719-113">Beispiel 2: Planen einer Azure DSC-Knoten-Konfigurationsbereitstellung in der Automatisierung</span><span class="sxs-lookup"><span data-stu-id="50719-113">Example 2: Schedule an Azure DSC node configuration deployment in Automation</span></span>
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

<span data-ttu-id="50719-114">Der oben aufgeführte Befehl plant eine Bereitstellung einer DSC-Knotenkonfiguration namens "Config01.Node1" für das angegebene zweidimensionale Array mit Knotennamen.</span><span class="sxs-lookup"><span data-stu-id="50719-114">The above command schedules a deployment of a DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="50719-115">Die Bereitstellung erfolgt auf mehrstufige Art und Weise und wird basierend auf dem Zeitplan ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="50719-115">The deployment happens in a staged manner and will be executed based on the schedule.</span></span>

## <span data-ttu-id="50719-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50719-116">PARAMETERS</span></span>

### <span data-ttu-id="50719-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="50719-117">-AutomationAccountName</span></span>
<span data-ttu-id="50719-118">Gibt den Namen des Automatisierungskontos an, das die VON diesem Cmdlet kompilierte DSC-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="50719-118">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="50719-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50719-119">-DefaultProfile</span></span>
<span data-ttu-id="50719-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="50719-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50719-121">-Force</span><span class="sxs-lookup"><span data-stu-id="50719-121">-Force</span></span>
<span data-ttu-id="50719-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="50719-122">ps_force</span></span>

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

### <span data-ttu-id="50719-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50719-123">-InputObject</span></span>
<span data-ttu-id="50719-124">Eingabeobjekt für die Pipierung</span><span class="sxs-lookup"><span data-stu-id="50719-124">Input object for Piping</span></span>

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

### <span data-ttu-id="50719-125">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="50719-125">-NodeConfigurationName</span></span>
<span data-ttu-id="50719-126">Gibt den Namen der DSC-Knotenkonfiguration an, die von diesem Cmdlet bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="50719-126">Specifies the name of the DSC node configuration that this cmdlet deploys.</span></span>

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

### <span data-ttu-id="50719-127">-NodeName</span><span class="sxs-lookup"><span data-stu-id="50719-127">-NodeName</span></span>
<span data-ttu-id="50719-128">Gibt die Namen der Knoten an, für die die Knotenkonfiguration bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="50719-128">Specifies the names of the nodes to which the Node Configuration would be deployed to.</span></span>

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

### <span data-ttu-id="50719-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50719-129">-ResourceGroupName</span></span>
<span data-ttu-id="50719-130">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet eine Konfiguration kompiliert.</span><span class="sxs-lookup"><span data-stu-id="50719-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="50719-131">-Schedule</span><span class="sxs-lookup"><span data-stu-id="50719-131">-Schedule</span></span>
<span data-ttu-id="50719-132">Automatisierungszeitplanobjekt zum Planen des Bereitstellungsauftrags.</span><span class="sxs-lookup"><span data-stu-id="50719-132">Automation Schedule object to schedule the deployment job.</span></span>

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

### <span data-ttu-id="50719-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50719-133">-Confirm</span></span>
<span data-ttu-id="50719-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="50719-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50719-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="50719-135">-WhatIf</span></span>
<span data-ttu-id="50719-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="50719-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50719-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="50719-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50719-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50719-138">CommonParameters</span></span>
<span data-ttu-id="50719-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50719-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50719-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50719-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50719-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="50719-141">INPUTS</span></span>

### <span data-ttu-id="50719-142">System.String</span><span class="sxs-lookup"><span data-stu-id="50719-142">System.String</span></span>

### <span data-ttu-id="50719-143">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="50719-143">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="50719-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="50719-144">OUTPUTS</span></span>

### <span data-ttu-id="50719-145">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="50719-145">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="50719-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="50719-146">NOTES</span></span>

## <span data-ttu-id="50719-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="50719-147">RELATED LINKS</span></span>

[<span data-ttu-id="50719-148">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="50719-148">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="50719-149">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="50719-149">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="50719-150">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="50719-150">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="50719-151">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="50719-151">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="50719-152">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="50719-152">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)

[<span data-ttu-id="50719-153">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="50719-153">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)
