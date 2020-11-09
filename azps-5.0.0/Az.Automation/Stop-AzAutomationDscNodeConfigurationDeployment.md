---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 3e5ec84dd3560c07fbf68c6f566b4691c1f6e512
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300801"
---
# <span data-ttu-id="a7214-101">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="a7214-101">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="a7214-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a7214-102">SYNOPSIS</span></span>
<span data-ttu-id="a7214-103">Beendet die Bereitstellung einer DSC-Knoten Konfiguration in der Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="a7214-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="a7214-104">Der aktuelle Bereitstellungsauftrag wird nur beendet, aber die Zuweisung bereits zugewiesener Knoten Konfigurationen wird nicht aufheben.</span><span class="sxs-lookup"><span data-stu-id="a7214-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

## <span data-ttu-id="a7214-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7214-105">SYNTAX</span></span>

### <span data-ttu-id="a7214-106">ByJobId (Standard)</span><span class="sxs-lookup"><span data-stu-id="a7214-106">ByJobId (Default)</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7214-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a7214-107">ByInputObject</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7214-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a7214-108">DESCRIPTION</span></span>
<span data-ttu-id="a7214-109">Das Cmdlet " **Stop-AzAutomationDscNodeConfigurationDeployment** " beendet die Bereitstellung einer Statuskonfiguration (DSC)-Knoten Konfiguration in Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="a7214-109">The **Stop-AzAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="a7214-110">Die Zuweisung der Knoten Konfiguration an Knotengruppen wird beendet, wenn eine solche zugewiesen werden soll, aber nicht die Zuweisung bereits zugewiesener Knoten aufheben.</span><span class="sxs-lookup"><span data-stu-id="a7214-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="a7214-111">Wenn Sie die Registrierung eines geplanten Auftrags aufheben möchten, verwenden Sie die [Unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) mit dem JobScheduleId, um die Zuweisung eines vorhandenen geplanten Auftrags aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="a7214-111">To unregister a scheduled job, please use the [Unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="a7214-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a7214-112">EXAMPLES</span></span>

### <span data-ttu-id="a7214-113">Beispiel 1: Bereitstelleneiner Azure DSC-Knoten Konfiguration in der Automatisierung</span><span class="sxs-lookup"><span data-stu-id="a7214-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="a7214-114">Der obige Befehl beendet den Bereitstellungsauftrag für die DSC-Knoten Konfiguration mit dem übergebenen JobID.</span><span class="sxs-lookup"><span data-stu-id="a7214-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="a7214-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7214-115">PARAMETERS</span></span>

### <span data-ttu-id="a7214-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a7214-116">-AutomationAccountName</span></span>
<span data-ttu-id="a7214-117">Gibt den Namen des Automatisierungs Kontos an, das die von diesem Cmdlet kompilierte DSC-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="a7214-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles</span></span>

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

### <span data-ttu-id="a7214-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7214-118">-DefaultProfile</span></span>
<span data-ttu-id="a7214-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a7214-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7214-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a7214-120">-Force</span></span>
<span data-ttu-id="a7214-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="a7214-121">ps_force</span></span>

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

### <span data-ttu-id="a7214-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a7214-122">-InputObject</span></span>
<span data-ttu-id="a7214-123">Eingabeobjekt für die Rohrverlegung</span><span class="sxs-lookup"><span data-stu-id="a7214-123">Input object for Piping</span></span>

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

### <span data-ttu-id="a7214-124">-JobId</span><span class="sxs-lookup"><span data-stu-id="a7214-124">-JobId</span></span>
<span data-ttu-id="a7214-125">Gibt die Auftrags-ID eines vorhandenen Bereitstellungsauftrags an.</span><span class="sxs-lookup"><span data-stu-id="a7214-125">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="a7214-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7214-126">-PassThru</span></span>
<span data-ttu-id="a7214-127">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="a7214-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a7214-128">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="a7214-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a7214-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7214-129">-ResourceGroupName</span></span>
<span data-ttu-id="a7214-130">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet eine Konfiguration kompiliert.</span><span class="sxs-lookup"><span data-stu-id="a7214-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="a7214-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a7214-131">-Confirm</span></span>
<span data-ttu-id="a7214-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a7214-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7214-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7214-133">-WhatIf</span></span>
<span data-ttu-id="a7214-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a7214-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7214-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a7214-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7214-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7214-136">CommonParameters</span></span>
<span data-ttu-id="a7214-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7214-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7214-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7214-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7214-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a7214-139">INPUTS</span></span>

### <span data-ttu-id="a7214-140">System. GUID</span><span class="sxs-lookup"><span data-stu-id="a7214-140">System.Guid</span></span>

### <span data-ttu-id="a7214-141">Microsoft. Azure. Commands. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="a7214-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

### <span data-ttu-id="a7214-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a7214-142">System.String</span></span>

## <span data-ttu-id="a7214-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a7214-143">OUTPUTS</span></span>

### <span data-ttu-id="a7214-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a7214-144">System.Boolean</span></span>

## <span data-ttu-id="a7214-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="a7214-145">NOTES</span></span>

## <span data-ttu-id="a7214-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a7214-146">RELATED LINKS</span></span>

[<span data-ttu-id="a7214-147">Anfang-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="a7214-147">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="a7214-148">Importieren-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7214-148">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="a7214-149">Anfang-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="a7214-149">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="a7214-150">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="a7214-150">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="a7214-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="a7214-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
