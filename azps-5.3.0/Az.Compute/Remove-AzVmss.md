---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmss.md
ms.openlocfilehash: e02ddb83e40495fbcf729428a737f27e6665d765
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472995"
---
# <span data-ttu-id="0df05-101">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0df05-101">Remove-AzVmss</span></span>

## <span data-ttu-id="0df05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0df05-102">SYNOPSIS</span></span>
<span data-ttu-id="0df05-103">Entfernt den VMSS oder einen virtuellen Computer innerhalb der VMSS.</span><span class="sxs-lookup"><span data-stu-id="0df05-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

## <span data-ttu-id="0df05-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0df05-104">SYNTAX</span></span>

```
Remove-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0df05-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0df05-105">DESCRIPTION</span></span>
<span data-ttu-id="0df05-106">Das **Cmdlet "Remove-AzVmss"** entfernt den Virtual Machine Scale Set (VMSS) aus Azure.</span><span class="sxs-lookup"><span data-stu-id="0df05-106">The **Remove-AzVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="0df05-107">Dieses Cmdlet kann auch verwendet werden, um einen bestimmten virtuellen Computer innerhalb der VMSS zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="0df05-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="0df05-108">Sie können den Parameter *"InstanceId"* verwenden, um einen bestimmten virtuellen Computer innerhalb der VMSS zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="0df05-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="0df05-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0df05-109">EXAMPLES</span></span>

### <span data-ttu-id="0df05-110">Beispiel 1: Entfernen eines VMSS</span><span class="sxs-lookup"><span data-stu-id="0df05-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="0df05-111">Dieser Befehl entfernt die VMSS namens VMScaleSet001, die zur Ressourcengruppe "Group001" gehört.</span><span class="sxs-lookup"><span data-stu-id="0df05-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="0df05-112">Beispiel 2: Entfernen eines virtuellen Computers aus einem VMSS</span><span class="sxs-lookup"><span data-stu-id="0df05-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="0df05-113">Dieser Befehl entfernt den virtuellen Computer mit der Instanz-ID 3 aus der VMSS namens VMScaleSet002, die zur Ressourcengruppe "Group002" gehört.</span><span class="sxs-lookup"><span data-stu-id="0df05-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="0df05-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0df05-114">PARAMETERS</span></span>

### <span data-ttu-id="0df05-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0df05-115">-AsJob</span></span>
<span data-ttu-id="0df05-116">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="0df05-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="0df05-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0df05-117">-DefaultProfile</span></span>
<span data-ttu-id="0df05-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0df05-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0df05-119">-Force</span><span class="sxs-lookup"><span data-stu-id="0df05-119">-Force</span></span>
<span data-ttu-id="0df05-120">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="0df05-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0df05-121">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="0df05-121">-InstanceId</span></span>
<span data-ttu-id="0df05-122">Gibt als Zeichenfolgenarray die ID der Instanzen an, die gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="0df05-122">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="0df05-123">Zum Beispiel: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="0df05-123">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="0df05-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0df05-124">-ResourceGroupName</span></span>
<span data-ttu-id="0df05-125">Gibt den Namen der Ressourcengruppe an, zu der die VMSS gehört.</span><span class="sxs-lookup"><span data-stu-id="0df05-125">Specifies the name of the resource group that the VMSS belongs to.</span></span>

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

### <span data-ttu-id="0df05-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="0df05-126">-VMScaleSetName</span></span>
<span data-ttu-id="0df05-127">Arten des Namens der VMSS, die von diesem Cmdlet entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="0df05-127">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="0df05-128">Wenn Sie den Parameter *"InstanceId"* angeben, entfernt das Cmdlet den angegebenen virtuellen Computer aus dem VMSS, der von diesem Parameter benannt wird.</span><span class="sxs-lookup"><span data-stu-id="0df05-128">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

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

### <span data-ttu-id="0df05-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0df05-129">-Confirm</span></span>
<span data-ttu-id="0df05-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0df05-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0df05-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0df05-131">-WhatIf</span></span>
<span data-ttu-id="0df05-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0df05-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0df05-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0df05-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0df05-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0df05-134">CommonParameters</span></span>
<span data-ttu-id="0df05-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0df05-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0df05-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0df05-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0df05-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0df05-137">INPUTS</span></span>

### <span data-ttu-id="0df05-138">System.String</span><span class="sxs-lookup"><span data-stu-id="0df05-138">System.String</span></span>

### <span data-ttu-id="0df05-139">System.String[]</span><span class="sxs-lookup"><span data-stu-id="0df05-139">System.String[]</span></span>

## <span data-ttu-id="0df05-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0df05-140">OUTPUTS</span></span>

### <span data-ttu-id="0df05-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="0df05-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="0df05-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0df05-142">NOTES</span></span>

## <span data-ttu-id="0df05-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0df05-143">RELATED LINKS</span></span>

[<span data-ttu-id="0df05-144">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0df05-144">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="0df05-145">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0df05-145">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="0df05-146">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0df05-146">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="0df05-147">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0df05-147">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="0df05-148">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0df05-148">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="0df05-149">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0df05-149">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="0df05-150">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0df05-150">Update-AzVmss</span></span>](./Update-AzVmss.md)


