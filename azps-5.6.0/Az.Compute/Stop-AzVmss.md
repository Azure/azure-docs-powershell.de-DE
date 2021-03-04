---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: https://docs.microsoft.com/powershell/module/az.compute/stop-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
ms.openlocfilehash: 152be66a2e1582d9f8377e09e250d3cf044c64db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948008"
---
# <span data-ttu-id="27610-101">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="27610-101">Stop-AzVmss</span></span>

## <span data-ttu-id="27610-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27610-102">SYNOPSIS</span></span>
<span data-ttu-id="27610-103">Beendet den VMSS oder eine Reihe virtueller Computer innerhalb des VMSS.</span><span class="sxs-lookup"><span data-stu-id="27610-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="27610-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27610-104">SYNTAX</span></span>

### <span data-ttu-id="27610-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="27610-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27610-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="27610-106">FriendMethod</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-SkipShutdown] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="27610-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27610-107">DESCRIPTION</span></span>
<span data-ttu-id="27610-108">Das **Cmdlet Stopp-AzVmss** stoppt alle virtuellen Computer im VmSS (Virtual Machine Scale Set) oder einer Reihe virtueller Computer.</span><span class="sxs-lookup"><span data-stu-id="27610-108">The **Stop-AzVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="27610-109">Sie können den *Parameter InstanzId* verwenden, um eine Gruppe virtueller Computer auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="27610-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="27610-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="27610-110">EXAMPLES</span></span>

### <span data-ttu-id="27610-111">Beispiel 1: Beenden aller virtuellen Computer im VMSS</span><span class="sxs-lookup"><span data-stu-id="27610-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="27610-112">Mit diesem Befehl werden alle virtuellen Computer beendet, die zum VMSS mit dem Namen ContosoVMSS gehören.</span><span class="sxs-lookup"><span data-stu-id="27610-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="27610-113">Beispiel 2: Beenden einer bestimmten Gruppe virtueller Computer innerhalb des VMSS</span><span class="sxs-lookup"><span data-stu-id="27610-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="27610-114">Mit diesem Befehl wird eine bestimmte Gruppe virtueller Computer beendet, die vom Array der Instanz-ID-Zeichenfolge angegeben werden, die zum VMSS mit dem Namen ContosoVMSS gehören.</span><span class="sxs-lookup"><span data-stu-id="27610-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="27610-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="27610-115">PARAMETERS</span></span>

### <span data-ttu-id="27610-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27610-116">-AsJob</span></span>
<span data-ttu-id="27610-117">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="27610-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="27610-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27610-118">-DefaultProfile</span></span>
<span data-ttu-id="27610-119">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="27610-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27610-120">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="27610-120">-Force</span></span>
<span data-ttu-id="27610-121">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="27610-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="27610-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="27610-122">-InstanceId</span></span>
<span data-ttu-id="27610-123">Gibt als Zeichenfolgenarray die ID oder IDs der Instanzen des virtuellen Computers an, die dieses Cmdlet beendet.</span><span class="sxs-lookup"><span data-stu-id="27610-123">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="27610-124">Beispiel: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="27610-124">For instance: `-InstanceId "0", "3"`.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27610-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27610-125">-ResourceGroupName</span></span>
<span data-ttu-id="27610-126">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="27610-126">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="27610-127">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="27610-127">-SkipShutdown</span></span>
<span data-ttu-id="27610-128">So fordern Sie ein nicht anmutiges Herunterfahren von virtuellen Computer an</span><span class="sxs-lookup"><span data-stu-id="27610-128">To request non-graceful VM shutdown</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27610-129">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="27610-129">-StayProvisioned</span></span>
<span data-ttu-id="27610-130">Wenn angegeben, wird der virtuelle Computer in den Status "Beendet" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="27610-130">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="27610-131">Wenn nicht angegeben, wird der virtuelle Computer in den Zustand "Stopped-deallocated" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="27610-131">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="27610-132">Dem Benutzer werden weiterhin VMs im Angehalten-Zustand in Rechnung gestellt, nicht jedoch VMs im status "Stopped-deallocated".</span><span class="sxs-lookup"><span data-stu-id="27610-132">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27610-133">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="27610-133">-VMScaleSetName</span></span>
<span data-ttu-id="27610-134">Gibt den Namen des VMSS an, für den dieses Cmdlet die virtuellen Computer beendet.</span><span class="sxs-lookup"><span data-stu-id="27610-134">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27610-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="27610-135">-Confirm</span></span>
<span data-ttu-id="27610-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="27610-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27610-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27610-137">-WhatIf</span></span>
<span data-ttu-id="27610-138">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="27610-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27610-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="27610-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27610-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27610-140">CommonParameters</span></span>
<span data-ttu-id="27610-141">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27610-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27610-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27610-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27610-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="27610-143">INPUTS</span></span>

### <span data-ttu-id="27610-144">System.String</span><span class="sxs-lookup"><span data-stu-id="27610-144">System.String</span></span>

### <span data-ttu-id="27610-145">System.String[]</span><span class="sxs-lookup"><span data-stu-id="27610-145">System.String[]</span></span>

## <span data-ttu-id="27610-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="27610-146">OUTPUTS</span></span>

### <span data-ttu-id="27610-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="27610-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="27610-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="27610-148">NOTES</span></span>

## <span data-ttu-id="27610-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="27610-149">RELATED LINKS</span></span>

[<span data-ttu-id="27610-150">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="27610-150">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="27610-151">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="27610-151">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="27610-152">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="27610-152">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="27610-153">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="27610-153">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="27610-154">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="27610-154">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="27610-155">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="27610-155">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="27610-156">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="27610-156">Update-AzVmss</span></span>](./Update-AzVmss.md)


