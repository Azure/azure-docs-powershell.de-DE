---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 41605bbdd37ae29f420581f9ad916a1cc87150be
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008118"
---
# <span data-ttu-id="9126d-101">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="9126d-101">Start-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="9126d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9126d-102">SYNOPSIS</span></span>
<span data-ttu-id="9126d-103">Stellt eine DSC-Knoten Konfiguration in der Automatisierung bereit.</span><span class="sxs-lookup"><span data-stu-id="9126d-103">Deploys a DSC Node configuration in Automation.</span></span>

## <span data-ttu-id="9126d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9126d-104">SYNTAX</span></span>

### <span data-ttu-id="9126d-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="9126d-105">ByAll (Default)</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 [-Schedule <Schedule>] [-Force] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9126d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9126d-106">ByInputObject</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 -InputObject <NodeConfigurationDeployment> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9126d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9126d-107">DESCRIPTION</span></span>
<span data-ttu-id="9126d-108">Das Cmdlet " **Start-AzAutomationDscNodeConfigurationDeployment** " stellt eine Konfiguration des gewünschten Zustands Konfiguration (DSC)-Knotens in Azure Automation bereit.</span><span class="sxs-lookup"><span data-stu-id="9126d-108">The **Start-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="9126d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9126d-109">EXAMPLES</span></span>

### <span data-ttu-id="9126d-110">Beispiel 1: Bereitstelleneiner Azure DSC-Knoten Konfiguration in der Automatisierung</span><span class="sxs-lookup"><span data-stu-id="9126d-110">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
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

<span data-ttu-id="9126d-111">Der obige Befehl stellt die Konfiguration des DSC-Knotens mit dem Namen "Config01. Node1" für das angegebene zweidimensionale Array von Knotennamen bereit.</span><span class="sxs-lookup"><span data-stu-id="9126d-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="9126d-112">Die Bereitstellung erfolgt in einer stufenweisen Weise.</span><span class="sxs-lookup"><span data-stu-id="9126d-112">The deployment happens in a staged manner.</span></span>

### <span data-ttu-id="9126d-113">Beispiel 2: Planen der Bereitstellung einer Azure DSC-Knoten Konfiguration in der Automatisierung</span><span class="sxs-lookup"><span data-stu-id="9126d-113">Example 2: Schedule an Azure DSC node configuration deployment in Automation</span></span>
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

<span data-ttu-id="9126d-114">Der obige Befehl plant eine Bereitstellung einer DSC-Knoten Konfiguration mit dem Namen "Config01. Node1" für das angegebene zweidimensionale Array von Knotennamen.</span><span class="sxs-lookup"><span data-stu-id="9126d-114">The above command schedules a deployment of a DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="9126d-115">Die Bereitstellung erfolgt in einer stufenweise und wird basierend auf dem Zeitplan ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9126d-115">The deployment happens in a staged manner and will be executed based on the schedule.</span></span>

## <span data-ttu-id="9126d-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="9126d-116">PARAMETERS</span></span>

### <span data-ttu-id="9126d-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9126d-117">-AutomationAccountName</span></span>
<span data-ttu-id="9126d-118">Gibt den Namen des Automatisierungs Kontos an, das die DSC-Konfiguration enthält, die von diesem Cmdlet kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="9126d-118">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="9126d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9126d-119">-DefaultProfile</span></span>
<span data-ttu-id="9126d-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9126d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9126d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9126d-121">-Force</span></span>
<span data-ttu-id="9126d-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="9126d-122">ps_force</span></span>

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

### <span data-ttu-id="9126d-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9126d-123">-InputObject</span></span>
<span data-ttu-id="9126d-124">Eingabeobjekt für die Rohrverlegung</span><span class="sxs-lookup"><span data-stu-id="9126d-124">Input object for Piping</span></span>

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

### <span data-ttu-id="9126d-125">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="9126d-125">-NodeConfigurationName</span></span>
<span data-ttu-id="9126d-126">Gibt den Namen der DSC-Knoten Konfiguration an, die von diesem Cmdlet bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="9126d-126">Specifies the name of the DSC node configuration that this cmdlet deploys.</span></span>

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

### <span data-ttu-id="9126d-127">-Nodename</span><span class="sxs-lookup"><span data-stu-id="9126d-127">-NodeName</span></span>
<span data-ttu-id="9126d-128">Gibt die Namen der Knoten an, für die die Knoten Konfiguration bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9126d-128">Specifies the names of the nodes to which the Node Configuration would be deployed to.</span></span>

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

### <span data-ttu-id="9126d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9126d-129">-ResourceGroupName</span></span>
<span data-ttu-id="9126d-130">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet eine Konfiguration kompiliert.</span><span class="sxs-lookup"><span data-stu-id="9126d-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="9126d-131">-Terminplan</span><span class="sxs-lookup"><span data-stu-id="9126d-131">-Schedule</span></span>
<span data-ttu-id="9126d-132">Automatisierungs Zeitplan-Objekt zum Planen des Bereitstellungsauftrags</span><span class="sxs-lookup"><span data-stu-id="9126d-132">Automation Schedule object to schedule the deployment job.</span></span>

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

### <span data-ttu-id="9126d-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9126d-133">-Confirm</span></span>
<span data-ttu-id="9126d-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9126d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9126d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9126d-135">-WhatIf</span></span>
<span data-ttu-id="9126d-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9126d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9126d-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9126d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9126d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9126d-138">CommonParameters</span></span>
<span data-ttu-id="9126d-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9126d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9126d-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9126d-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9126d-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9126d-141">INPUTS</span></span>

### <span data-ttu-id="9126d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9126d-142">System.String</span></span>

### <span data-ttu-id="9126d-143">Microsoft. Azure. Commands. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="9126d-143">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="9126d-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9126d-144">OUTPUTS</span></span>

### <span data-ttu-id="9126d-145">Microsoft. Azure. Commands. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="9126d-145">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="9126d-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="9126d-146">NOTES</span></span>

## <span data-ttu-id="9126d-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9126d-147">RELATED LINKS</span></span>

[<span data-ttu-id="9126d-148">Anfang-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="9126d-148">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="9126d-149">Importieren-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="9126d-149">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="9126d-150">Stopp-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="9126d-150">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="9126d-151">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="9126d-151">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="9126d-152">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="9126d-152">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)

[<span data-ttu-id="9126d-153">Neu – AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="9126d-153">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)
