---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 3e5ec84dd3560c07fbf68c6f566b4691c1f6e512
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98300667"
---
# <span data-ttu-id="274e9-101">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="274e9-101">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="274e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="274e9-102">SYNOPSIS</span></span>
<span data-ttu-id="274e9-103">Beendet eine DSC-Knoten-Konfigurationsbereitstellung in der Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="274e9-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="274e9-104">Der aktuelle Bereitstellungsauftrag wird nur beendet, die zugewiesenen Knotenkonfigurationen werden jedoch nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="274e9-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

## <span data-ttu-id="274e9-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="274e9-105">SYNTAX</span></span>

### <span data-ttu-id="274e9-106">ByJobId (Standard)</span><span class="sxs-lookup"><span data-stu-id="274e9-106">ByJobId (Default)</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="274e9-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="274e9-107">ByInputObject</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="274e9-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="274e9-108">DESCRIPTION</span></span>
<span data-ttu-id="274e9-109">Das **Cmdlet "Stop-AzAutomationDscNodeConfigurationDeployment"** beendet die Bereitstellung einer Konfiguration des Knotens "Desired State Configuration (DSC)" in der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="274e9-109">The **Stop-AzAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="274e9-110">Damit wird die Zuweisung der Knotenkonfiguration zu Knotengruppen beendet, sofern noch Knoten zugewiesen werden müssen, die Zuweisung bereits zugewiesener Knoten wird jedoch nicht beendet.</span><span class="sxs-lookup"><span data-stu-id="274e9-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="274e9-111">Wenn Sie die Registrierung eines geplanten Auftrags aufheben möchten, verwenden Sie das ["Registrierung aufheben"-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) zusammen mit "JobScheduleId", um die Zuzuweisen eines vorhandenen geplanten Auftrags auf aufheben.</span><span class="sxs-lookup"><span data-stu-id="274e9-111">To unregister a scheduled job, please use the [Unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="274e9-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="274e9-112">EXAMPLES</span></span>

### <span data-ttu-id="274e9-113">Beispiel 1: Bereitstellen einer Azure DSC-Knotenkonfiguration in der Automatisierung</span><span class="sxs-lookup"><span data-stu-id="274e9-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="274e9-114">Der oben aufgeführte Befehl beendet den Bereitstellungsauftrag der DSC-Knotenkonfiguration mit der übergebenen jobId.</span><span class="sxs-lookup"><span data-stu-id="274e9-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="274e9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="274e9-115">PARAMETERS</span></span>

### <span data-ttu-id="274e9-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="274e9-116">-AutomationAccountName</span></span>
<span data-ttu-id="274e9-117">Gibt den Namen des Automatisierungskontos an, das die VON diesem Cmdlet kompilierte DSC-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="274e9-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles</span></span>

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

### <span data-ttu-id="274e9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="274e9-118">-DefaultProfile</span></span>
<span data-ttu-id="274e9-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="274e9-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="274e9-120">-Force</span><span class="sxs-lookup"><span data-stu-id="274e9-120">-Force</span></span>
<span data-ttu-id="274e9-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="274e9-121">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByJobId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="274e9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="274e9-122">-InputObject</span></span>
<span data-ttu-id="274e9-123">Eingabeobjekt für die Pipierung</span><span class="sxs-lookup"><span data-stu-id="274e9-123">Input object for Piping</span></span>

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

### <span data-ttu-id="274e9-124">-JobId</span><span class="sxs-lookup"><span data-stu-id="274e9-124">-JobId</span></span>
<span data-ttu-id="274e9-125">Gibt die Auftrags-ID eines vorhandenen Bereitstellungsauftrags an.</span><span class="sxs-lookup"><span data-stu-id="274e9-125">Specifies the Job id of an existing deployment job.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="274e9-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="274e9-126">-PassThru</span></span>
<span data-ttu-id="274e9-127">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="274e9-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="274e9-128">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="274e9-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="274e9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="274e9-129">-ResourceGroupName</span></span>
<span data-ttu-id="274e9-130">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet eine Konfiguration kompiliert.</span><span class="sxs-lookup"><span data-stu-id="274e9-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="274e9-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="274e9-131">-Confirm</span></span>
<span data-ttu-id="274e9-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="274e9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="274e9-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="274e9-133">-WhatIf</span></span>
<span data-ttu-id="274e9-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="274e9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="274e9-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="274e9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="274e9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="274e9-136">CommonParameters</span></span>
<span data-ttu-id="274e9-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="274e9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="274e9-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="274e9-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="274e9-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="274e9-139">INPUTS</span></span>

### <span data-ttu-id="274e9-140">System.Guid</span><span class="sxs-lookup"><span data-stu-id="274e9-140">System.Guid</span></span>

### <span data-ttu-id="274e9-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="274e9-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

### <span data-ttu-id="274e9-142">System.String</span><span class="sxs-lookup"><span data-stu-id="274e9-142">System.String</span></span>

## <span data-ttu-id="274e9-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="274e9-143">OUTPUTS</span></span>

### <span data-ttu-id="274e9-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="274e9-144">System.Boolean</span></span>

## <span data-ttu-id="274e9-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="274e9-145">NOTES</span></span>

## <span data-ttu-id="274e9-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="274e9-146">RELATED LINKS</span></span>

[<span data-ttu-id="274e9-147">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="274e9-147">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="274e9-148">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="274e9-148">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="274e9-149">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="274e9-149">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="274e9-150">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="274e9-150">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="274e9-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="274e9-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
