---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: 358b24c403c4b08b221f97ad99271112ee0852be
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472983"
---
# <span data-ttu-id="eec43-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="eec43-101">Restart-AzVM</span></span>

## <span data-ttu-id="eec43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eec43-102">SYNOPSIS</span></span>
<span data-ttu-id="eec43-103">Startet einen virtuellen Azure-Computer neu.</span><span class="sxs-lookup"><span data-stu-id="eec43-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="eec43-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eec43-104">SYNTAX</span></span>

### <span data-ttu-id="eec43-105">RestartResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="eec43-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eec43-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="eec43-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eec43-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="eec43-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eec43-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="eec43-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-PerformMaintenance] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eec43-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eec43-109">DESCRIPTION</span></span>
<span data-ttu-id="eec43-110">Das **Cmdlet "Restart-AzVM"** startet einen virtuellen Azure-Computer neu.</span><span class="sxs-lookup"><span data-stu-id="eec43-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="eec43-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eec43-111">EXAMPLES</span></span>

### <span data-ttu-id="eec43-112">Beispiel 1: Neustarten eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="eec43-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="eec43-113">Dieser Befehl startet den virtuellen Computer mit dem Namen "VirtualMachine07" in ResourceGroup11 neu.</span><span class="sxs-lookup"><span data-stu-id="eec43-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="eec43-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eec43-114">PARAMETERS</span></span>

### <span data-ttu-id="eec43-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eec43-115">-AsJob</span></span>
<span data-ttu-id="eec43-116">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="eec43-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="eec43-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eec43-117">-DefaultProfile</span></span>
<span data-ttu-id="eec43-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eec43-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eec43-119">-ID</span><span class="sxs-lookup"><span data-stu-id="eec43-119">-Id</span></span>
<span data-ttu-id="eec43-120">Die ID des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="eec43-120">The ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eec43-121">-Name</span><span class="sxs-lookup"><span data-stu-id="eec43-121">-Name</span></span>
<span data-ttu-id="eec43-122">Der Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="eec43-122">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eec43-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="eec43-123">-NoWait</span></span>
<span data-ttu-id="eec43-124">Der Vorgang wird gestartet und unmittelbar vor Abschluss des Vorgangs beendet.</span><span class="sxs-lookup"><span data-stu-id="eec43-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="eec43-125">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="eec43-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="eec43-126">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="eec43-126">-PerformMaintenance</span></span>
<span data-ttu-id="eec43-127">Zum Ausführen der Wartung eines virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="eec43-127">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eec43-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eec43-128">-ResourceGroupName</span></span>
<span data-ttu-id="eec43-129">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="eec43-129">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eec43-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eec43-130">-Confirm</span></span>
<span data-ttu-id="eec43-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eec43-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eec43-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="eec43-132">-WhatIf</span></span>
<span data-ttu-id="eec43-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eec43-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eec43-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eec43-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eec43-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eec43-135">CommonParameters</span></span>
<span data-ttu-id="eec43-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eec43-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eec43-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eec43-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eec43-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eec43-138">INPUTS</span></span>

### <span data-ttu-id="eec43-139">System.String</span><span class="sxs-lookup"><span data-stu-id="eec43-139">System.String</span></span>

### <span data-ttu-id="eec43-140">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="eec43-140">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="eec43-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eec43-141">OUTPUTS</span></span>

### <span data-ttu-id="eec43-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="eec43-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="eec43-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="eec43-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="eec43-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="eec43-144">NOTES</span></span>

## <span data-ttu-id="eec43-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="eec43-145">RELATED LINKS</span></span>

[<span data-ttu-id="eec43-146">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="eec43-146">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="eec43-147">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="eec43-147">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="eec43-148">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="eec43-148">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="eec43-149">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="eec43-149">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="eec43-150">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="eec43-150">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="eec43-151">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="eec43-151">Update-AzVM</span></span>](./Update-AzVM.md)


