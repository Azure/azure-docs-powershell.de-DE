---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
ms.openlocfilehash: ac961b4e7032d793cecb46008fe62091dca052f0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290026"
---
# <span data-ttu-id="a1e8c-101">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a1e8c-101">Stop-AzVmss</span></span>

## <span data-ttu-id="a1e8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1e8c-102">SYNOPSIS</span></span>
<span data-ttu-id="a1e8c-103">Beendet den VMSS oder eine Reihe virtueller Computer innerhalb der VMSS.</span><span class="sxs-lookup"><span data-stu-id="a1e8c-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="a1e8c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1e8c-104">SYNTAX</span></span>

### <span data-ttu-id="a1e8c-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="a1e8c-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1e8c-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="a1e8c-106">FriendMethod</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-SkipShutdown] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a1e8c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a1e8c-107">DESCRIPTION</span></span>
<span data-ttu-id="a1e8c-108">Das **Cmdlet "Stop-AzVmss"** stoppt alle virtuellen Computer innerhalb des Virtual Machine Scale Set (VMSS) oder einer Reihe virtueller Computer.</span><span class="sxs-lookup"><span data-stu-id="a1e8c-108">The **Stop-AzVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="a1e8c-109">Sie können den Parameter *"InstanceId"* verwenden, um eine Reihe virtueller Computer auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="a1e8c-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="a1e8c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a1e8c-110">EXAMPLES</span></span>

### <span data-ttu-id="a1e8c-111">Beispiel 1: Beenden aller virtuellen Computer innerhalb der VMSS</span><span class="sxs-lookup"><span data-stu-id="a1e8c-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="a1e8c-112">Dieser Befehl stoppt alle virtuellen Computer, die der VMSS namens ContosoVMSS angehören.</span><span class="sxs-lookup"><span data-stu-id="a1e8c-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="a1e8c-113">Beispiel 2: Beenden einer bestimmten Gruppe virtueller Computer innerhalb der VMSS</span><span class="sxs-lookup"><span data-stu-id="a1e8c-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="a1e8c-114">Mit diesem Befehl wird eine bestimmte Gruppe virtueller Computer beendet, die durch das Zeichenfolgenarray der Instanz-ID angegeben werden, die zu der VMSS namens ContosoVMSS gehören.</span><span class="sxs-lookup"><span data-stu-id="a1e8c-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="a1e8c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1e8c-115">PARAMETERS</span></span>

### <span data-ttu-id="a1e8c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1e8c-116">-AsJob</span></span>
<span data-ttu-id="a1e8c-117">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="a1e8c-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a1e8c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1e8c-118">-DefaultProfile</span></span>
<span data-ttu-id="a1e8c-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a1e8c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1e8c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a1e8c-120">-Force</span></span>
<span data-ttu-id="a1e8c-121">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="a1e8c-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a1e8c-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="a1e8c-122">-InstanceId</span></span>
<span data-ttu-id="a1e8c-123">Gibt als Zeichenfolgenarray die ID oder IDs der Instanzen des virtuellen Computers an, die dieses Cmdlet beendet.</span><span class="sxs-lookup"><span data-stu-id="a1e8c-123">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="a1e8c-124">Beispiel: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="a1e8c-124">For instance: `-InstanceId "0", "3"`.</span></span>

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

### <span data-ttu-id="a1e8c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1e8c-125">-ResourceGroupName</span></span>
<span data-ttu-id="a1e8c-126">Gibt den Namen der Ressourcengruppe der VMSS an.</span><span class="sxs-lookup"><span data-stu-id="a1e8c-126">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="a1e8c-127">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="a1e8c-127">-SkipShutdown</span></span>
<span data-ttu-id="a1e8c-128">So fordern Sie das Herunterfahren einer nicht kulanzvollen VM an</span><span class="sxs-lookup"><span data-stu-id="a1e8c-128">To request non-graceful VM shutdown</span></span>

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

### <span data-ttu-id="a1e8c-129">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="a1e8c-129">-StayProvisioned</span></span>
<span data-ttu-id="a1e8c-130">Falls angegeben, wird der virtuelle Computer angehalten.</span><span class="sxs-lookup"><span data-stu-id="a1e8c-130">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="a1e8c-131">Ist dies nicht angegeben, wird der virtuelle Computer in den Zustand "stopped-deallocated" (beendeter Deallocated) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a1e8c-131">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="a1e8c-132">VMs im angehaltenen Zustand werden dem Benutzer weiterhin in Rechnung gestellt, nicht jedoch VMs im Zustand "Stopped-deallocated".</span><span class="sxs-lookup"><span data-stu-id="a1e8c-132">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>

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

### <span data-ttu-id="a1e8c-133">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a1e8c-133">-VMScaleSetName</span></span>
<span data-ttu-id="a1e8c-134">Gibt den Namen der VMSS an, für die dieses Cmdlet die virtuellen Computer beendet.</span><span class="sxs-lookup"><span data-stu-id="a1e8c-134">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

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

### <span data-ttu-id="a1e8c-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1e8c-135">-Confirm</span></span>
<span data-ttu-id="a1e8c-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a1e8c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1e8c-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a1e8c-137">-WhatIf</span></span>
<span data-ttu-id="a1e8c-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a1e8c-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1e8c-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a1e8c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1e8c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1e8c-140">CommonParameters</span></span>
<span data-ttu-id="a1e8c-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1e8c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1e8c-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1e8c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1e8c-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a1e8c-143">INPUTS</span></span>

### <span data-ttu-id="a1e8c-144">System.String</span><span class="sxs-lookup"><span data-stu-id="a1e8c-144">System.String</span></span>

### <span data-ttu-id="a1e8c-145">System.String[]</span><span class="sxs-lookup"><span data-stu-id="a1e8c-145">System.String[]</span></span>

## <span data-ttu-id="a1e8c-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a1e8c-146">OUTPUTS</span></span>

### <span data-ttu-id="a1e8c-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="a1e8c-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="a1e8c-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a1e8c-148">NOTES</span></span>

## <span data-ttu-id="a1e8c-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a1e8c-149">RELATED LINKS</span></span>

[<span data-ttu-id="a1e8c-150">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a1e8c-150">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="a1e8c-151">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a1e8c-151">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="a1e8c-152">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a1e8c-152">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="a1e8c-153">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a1e8c-153">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="a1e8c-154">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a1e8c-154">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="a1e8c-155">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a1e8c-155">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="a1e8c-156">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a1e8c-156">Update-AzVmss</span></span>](./Update-AzVmss.md)


