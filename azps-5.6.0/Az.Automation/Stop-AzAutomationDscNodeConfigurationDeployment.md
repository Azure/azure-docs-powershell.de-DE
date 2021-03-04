---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/powershell/module/az.automation/stop-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 726423dfcfef07142002cd40b29b6e4d26f91137
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932072"
---
# <span data-ttu-id="d9c9c-101">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="d9c9c-101">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="d9c9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9c9c-102">SYNOPSIS</span></span>
<span data-ttu-id="d9c9c-103">Beendet eine DSC-Knotenkonfigurationsbereitstellung in der Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="d9c9c-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="d9c9c-104">Es wird nur der aktuelle Bereitstellungsauftrag beendet, aber die Zuweisen bereits zugewiesener Knotenkonfigurationen wird nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="d9c9c-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

## <span data-ttu-id="d9c9c-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9c9c-105">SYNTAX</span></span>

### <span data-ttu-id="d9c9c-106">ByJobId (Standard)</span><span class="sxs-lookup"><span data-stu-id="d9c9c-106">ByJobId (Default)</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9c9c-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d9c9c-107">ByInputObject</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9c9c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d9c9c-108">DESCRIPTION</span></span>
<span data-ttu-id="d9c9c-109">Das **Cmdlet Stop-AzAutomationDscNodeConfigurationDeployment** beendet die Bereitstellung einer Dsc-Knotenkonfiguration (Desired State Configuration) in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d9c9c-109">The **Stop-AzAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="d9c9c-110">Die Zuweisung der Knotenkonfiguration zu Knotengruppen wird beendet, sofern noch zuzuweisende Knoten vorhanden sind, aber die Zuweisung bereits zugewiesener Knoten wird nicht beendet.</span><span class="sxs-lookup"><span data-stu-id="d9c9c-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="d9c9c-111">Wenn Sie die Registrierung eines geplanten Auftrags aufheben möchten, verwenden Sie das [Unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) mit der JobScheduleId, um die Zuzuweisen eines vorhandenen geplanten Auftrags zu aufheben.</span><span class="sxs-lookup"><span data-stu-id="d9c9c-111">To unregister a scheduled job, please use the [Unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="d9c9c-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d9c9c-112">EXAMPLES</span></span>

### <span data-ttu-id="d9c9c-113">Beispiel 1: Bereitstellen einer Azure DSC-Knotenkonfiguration in der Automatisierung</span><span class="sxs-lookup"><span data-stu-id="d9c9c-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="d9c9c-114">Der oben beschriebene Befehl beendet den Bereitstellungsauftrag für die DSC-Knotenkonfiguration mit der übergebenen jobId.</span><span class="sxs-lookup"><span data-stu-id="d9c9c-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="d9c9c-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d9c9c-115">PARAMETERS</span></span>

### <span data-ttu-id="d9c9c-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d9c9c-116">-AutomationAccountName</span></span>
<span data-ttu-id="d9c9c-117">Gibt den Namen des Automatisierungskontos an, das die VON diesem Cmdlet kompilierte DSC-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="d9c9c-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles</span></span>

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

### <span data-ttu-id="d9c9c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9c9c-118">-DefaultProfile</span></span>
<span data-ttu-id="d9c9c-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d9c9c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9c9c-120">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="d9c9c-120">-Force</span></span>
<span data-ttu-id="d9c9c-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="d9c9c-121">ps_force</span></span>

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

### <span data-ttu-id="d9c9c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9c9c-122">-InputObject</span></span>
<span data-ttu-id="d9c9c-123">Eingabeobjekt für Piping</span><span class="sxs-lookup"><span data-stu-id="d9c9c-123">Input object for Piping</span></span>

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

### <span data-ttu-id="d9c9c-124">-JobId</span><span class="sxs-lookup"><span data-stu-id="d9c9c-124">-JobId</span></span>
<span data-ttu-id="d9c9c-125">Gibt die Auftrags-ID eines vorhandenen Bereitstellungsauftrags an.</span><span class="sxs-lookup"><span data-stu-id="d9c9c-125">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="d9c9c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9c9c-126">-PassThru</span></span>
<span data-ttu-id="d9c9c-127">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="d9c9c-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d9c9c-128">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="d9c9c-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d9c9c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9c9c-129">-ResourceGroupName</span></span>
<span data-ttu-id="d9c9c-130">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet eine Konfiguration kompiliert.</span><span class="sxs-lookup"><span data-stu-id="d9c9c-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="d9c9c-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d9c9c-131">-Confirm</span></span>
<span data-ttu-id="d9c9c-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d9c9c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9c9c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9c9c-133">-WhatIf</span></span>
<span data-ttu-id="d9c9c-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d9c9c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9c9c-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9c9c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9c9c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9c9c-136">CommonParameters</span></span>
<span data-ttu-id="d9c9c-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9c9c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9c9c-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9c9c-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9c9c-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d9c9c-139">INPUTS</span></span>

### <span data-ttu-id="d9c9c-140">System.Guid</span><span class="sxs-lookup"><span data-stu-id="d9c9c-140">System.Guid</span></span>

### <span data-ttu-id="d9c9c-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="d9c9c-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

### <span data-ttu-id="d9c9c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d9c9c-142">System.String</span></span>

## <span data-ttu-id="d9c9c-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d9c9c-143">OUTPUTS</span></span>

### <span data-ttu-id="d9c9c-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d9c9c-144">System.Boolean</span></span>

## <span data-ttu-id="d9c9c-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d9c9c-145">NOTES</span></span>

## <span data-ttu-id="d9c9c-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d9c9c-146">RELATED LINKS</span></span>

[<span data-ttu-id="d9c9c-147">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="d9c9c-147">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="d9c9c-148">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9c9c-148">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="d9c9c-149">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="d9c9c-149">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="d9c9c-150">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="d9c9c-150">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="d9c9c-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="d9c9c-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
