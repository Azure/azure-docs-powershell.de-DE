---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/start-azurermautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 21fe2cfb9a9022cad2ce9947b1e5919a6ebc268b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476262"
---
# <span data-ttu-id="3e9ff-101">Start-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="3e9ff-101">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="3e9ff-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3e9ff-102">SYNOPSIS</span></span>
<span data-ttu-id="3e9ff-103">Stellt eine DSC-Knoten Konfiguration in der Automatisierung bereit.</span><span class="sxs-lookup"><span data-stu-id="3e9ff-103">Deploys a DSC Node configuration in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e9ff-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e9ff-104">SYNTAX</span></span>

### <span data-ttu-id="3e9ff-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="3e9ff-105">ByAll (Default)</span></span>
```
Start-AzureRmAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String>
 [-NodeName] <String[][]> [-Schedule <Schedule>] [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e9ff-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3e9ff-106">ByInputObject</span></span>
```
Start-AzureRmAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String>
 [-NodeName] <String[][]> -InputObject <NodeConfigurationDeployment> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e9ff-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3e9ff-107">DESCRIPTION</span></span>
<span data-ttu-id="3e9ff-108">Das Cmdlet " **Start-AzureRmAutomationDscNodeConfigurationDeployment** " stellt eine Konfiguration des gewünschten Zustands Konfiguration (DSC)-Knotens in Azure Automation bereit.</span><span class="sxs-lookup"><span data-stu-id="3e9ff-108">The **Start-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet deployes a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="3e9ff-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3e9ff-109">EXAMPLES</span></span>

### <span data-ttu-id="3e9ff-110">Beispiel 1: Bereitstelleneiner Azure DSC-Knoten Konfiguration in der Automatisierung</span><span class="sxs-lookup"><span data-stu-id="3e9ff-110">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzureRmAutomationDscNodeConfigurationDeployment `
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

<span data-ttu-id="3e9ff-111">Der obige Befehl stellt die Konfiguration des DSC-Knotens mit dem Namen "Config01. Node1" für das angegebene zweidimensionale Array von Knotennamen bereit.</span><span class="sxs-lookup"><span data-stu-id="3e9ff-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="3e9ff-112">Die Bereitstellung erfolgt in einer stufenweisen Weise.</span><span class="sxs-lookup"><span data-stu-id="3e9ff-112">The deployment happens in a staged manner.</span></span>

### <span data-ttu-id="3e9ff-113">Beispiel 2: Planen der Bereitstellung einer Azure DSC-Knoten Konfiguration in der Automatisierung</span><span class="sxs-lookup"><span data-stu-id="3e9ff-113">Example 2: Schedule an Azure DSC node configuration deployment in Automation</span></span>
```
PS C:\> $sched = New-AzureRmAutomationSchedule -AutomationAccountName "Contoso01" `
            -ResourceGroupName "ResourceGroup01" `
            -Name "TestSchedule" `
            -StartTime "23:00" `
            -OneTime
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzureRmAutomationDscNodeConfigurationDeployment `
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

<span data-ttu-id="3e9ff-114">Der obige Befehl plant eine Bereitstellung einer DSC-Knoten Konfiguration mit dem Namen "Config01. Node1" für das angegebene zweidimensionale Array von Knotennamen.</span><span class="sxs-lookup"><span data-stu-id="3e9ff-114">The above command schedules a deployment of a DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="3e9ff-115">Die Bereitstellung erfolgt in einer stufenweise und wird basierend auf dem Zeitplan ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3e9ff-115">The deployment happens in a staged manner and will be executed based on the schedule.</span></span>

## <span data-ttu-id="3e9ff-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e9ff-116">PARAMETERS</span></span>

### <span data-ttu-id="3e9ff-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3e9ff-117">-AutomationAccountName</span></span>
<span data-ttu-id="3e9ff-118">Gibt den Namen des Automatisierungs Kontos an, das die DSC-Konfiguration enthält, die von diesem Cmdlet kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="3e9ff-118">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="3e9ff-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e9ff-119">-DefaultProfile</span></span>
<span data-ttu-id="3e9ff-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3e9ff-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e9ff-121">-Force</span><span class="sxs-lookup"><span data-stu-id="3e9ff-121">-Force</span></span>
<span data-ttu-id="3e9ff-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="3e9ff-122">ps_force</span></span>

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

### <span data-ttu-id="3e9ff-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3e9ff-123">-InputObject</span></span>
<span data-ttu-id="3e9ff-124">Eingabeobjekt für die Rohrverlegung</span><span class="sxs-lookup"><span data-stu-id="3e9ff-124">Input object for Piping</span></span>

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

### <span data-ttu-id="3e9ff-125">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="3e9ff-125">-NodeConfigurationName</span></span>
<span data-ttu-id="3e9ff-126">Gibt den Namen der DSC-Knoten Konfiguration an, die von diesem Cmdlet bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3e9ff-126">Specifies the name of the DSC node configuration that this cmdlet deploys.</span></span>

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

### <span data-ttu-id="3e9ff-127">-Nodename</span><span class="sxs-lookup"><span data-stu-id="3e9ff-127">-NodeName</span></span>
<span data-ttu-id="3e9ff-128">Gibt die Namen der Knoten an, für die die Knoten Konfiguration bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3e9ff-128">Specifies the names of the nodes to which the Node Configuration would be deployed to.</span></span>

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

### <span data-ttu-id="3e9ff-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e9ff-129">-ResourceGroupName</span></span>
<span data-ttu-id="3e9ff-130">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet eine Konfiguration kompiliert.</span><span class="sxs-lookup"><span data-stu-id="3e9ff-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="3e9ff-131">-Terminplan</span><span class="sxs-lookup"><span data-stu-id="3e9ff-131">-Schedule</span></span>
<span data-ttu-id="3e9ff-132">Automatisierungs Zeitplan-Objekt zum Planen des Bereitstellungsauftrags</span><span class="sxs-lookup"><span data-stu-id="3e9ff-132">Automation Schedule object to schedule the deployment job.</span></span>

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

### <span data-ttu-id="3e9ff-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3e9ff-133">-Confirm</span></span>
<span data-ttu-id="3e9ff-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3e9ff-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e9ff-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e9ff-135">-WhatIf</span></span>
<span data-ttu-id="3e9ff-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3e9ff-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e9ff-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3e9ff-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e9ff-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e9ff-138">CommonParameters</span></span>
<span data-ttu-id="3e9ff-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e9ff-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e9ff-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e9ff-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e9ff-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3e9ff-141">INPUTS</span></span>

### <span data-ttu-id="3e9ff-142">System. String</span><span class="sxs-lookup"><span data-stu-id="3e9ff-142">System.String</span></span>

### <span data-ttu-id="3e9ff-143">Microsoft. Azure. Commands. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="3e9ff-143">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>
<span data-ttu-id="3e9ff-144">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3e9ff-144">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="3e9ff-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3e9ff-145">OUTPUTS</span></span>

### <span data-ttu-id="3e9ff-146">Microsoft. Azure. Commands. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="3e9ff-146">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="3e9ff-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="3e9ff-147">NOTES</span></span>

## <span data-ttu-id="3e9ff-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3e9ff-148">RELATED LINKS</span></span>

[<span data-ttu-id="3e9ff-149">Anfang-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="3e9ff-149">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="3e9ff-150">Importieren-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e9ff-150">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="3e9ff-151">Stopp-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="3e9ff-151">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="3e9ff-152">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="3e9ff-152">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="3e9ff-153">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="3e9ff-153">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)

[<span data-ttu-id="3e9ff-154">Neu – AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="3e9ff-154">New-AzureRmAutomationSchedule</span></span>](./New-AzureRmAutomationSchedule.md)
