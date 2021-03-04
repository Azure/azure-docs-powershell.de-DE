---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: eca73d71d213b31c0bbc339708cc744b3bf64d2a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924240"
---
# <span data-ttu-id="f9439-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="f9439-101">Restart-AzVM</span></span>

## <span data-ttu-id="f9439-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9439-102">SYNOPSIS</span></span>
<span data-ttu-id="f9439-103">Startet einen virtuellen Azure-Computer neu.</span><span class="sxs-lookup"><span data-stu-id="f9439-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="f9439-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9439-104">SYNTAX</span></span>

### <span data-ttu-id="f9439-105">RestartResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="f9439-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9439-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f9439-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9439-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f9439-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f9439-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f9439-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-PerformMaintenance] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9439-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9439-109">DESCRIPTION</span></span>
<span data-ttu-id="f9439-110">Das **Cmdlet Restart-AzVM** startet einen virtuellen Azure-Computer neu.</span><span class="sxs-lookup"><span data-stu-id="f9439-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="f9439-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f9439-111">EXAMPLES</span></span>

### <span data-ttu-id="f9439-112">Beispiel 1: Neustarten eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="f9439-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="f9439-113">Mit diesem Befehl wird der virtuelle Computer mit dem Namen VirtualMachine07 in ResourceGroup11 neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="f9439-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="f9439-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f9439-114">PARAMETERS</span></span>

### <span data-ttu-id="f9439-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9439-115">-AsJob</span></span>
<span data-ttu-id="f9439-116">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="f9439-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f9439-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9439-117">-DefaultProfile</span></span>
<span data-ttu-id="f9439-118">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f9439-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9439-119">-ID</span><span class="sxs-lookup"><span data-stu-id="f9439-119">-Id</span></span>
<span data-ttu-id="f9439-120">Die ID des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="f9439-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="f9439-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f9439-121">-Name</span></span>
<span data-ttu-id="f9439-122">Der Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="f9439-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="f9439-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f9439-123">-NoWait</span></span>
<span data-ttu-id="f9439-124">Startet den Vorgang und gibt sofort zurück, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="f9439-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="f9439-125">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="f9439-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="f9439-126">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="f9439-126">-PerformMaintenance</span></span>
<span data-ttu-id="f9439-127">So führen Sie die Wartung des virtuellen Computers durch.</span><span class="sxs-lookup"><span data-stu-id="f9439-127">To perform the maintenance of virtual machine.</span></span>

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

### <span data-ttu-id="f9439-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9439-128">-ResourceGroupName</span></span>
<span data-ttu-id="f9439-129">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="f9439-129">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f9439-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f9439-130">-Confirm</span></span>
<span data-ttu-id="f9439-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f9439-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9439-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9439-132">-WhatIf</span></span>
<span data-ttu-id="f9439-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9439-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9439-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f9439-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9439-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9439-135">CommonParameters</span></span>
<span data-ttu-id="f9439-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9439-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9439-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9439-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9439-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f9439-138">INPUTS</span></span>

### <span data-ttu-id="f9439-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f9439-139">System.String</span></span>

### <span data-ttu-id="f9439-140">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f9439-140">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f9439-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f9439-141">OUTPUTS</span></span>

### <span data-ttu-id="f9439-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="f9439-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="f9439-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f9439-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f9439-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f9439-144">NOTES</span></span>

## <span data-ttu-id="f9439-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f9439-145">RELATED LINKS</span></span>

[<span data-ttu-id="f9439-146">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="f9439-146">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="f9439-147">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="f9439-147">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="f9439-148">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="f9439-148">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="f9439-149">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="f9439-149">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="f9439-150">Stopp-AzVM</span><span class="sxs-lookup"><span data-stu-id="f9439-150">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="f9439-151">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="f9439-151">Update-AzVM</span></span>](./Update-AzVM.md)


