---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
ms.openlocfilehash: ceca2477d66cb6ce19564899e67a3b66d6917cfe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98308016"
---
# <span data-ttu-id="8ef9c-101">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="8ef9c-101">Remove-AzVmssExtension</span></span>

## <span data-ttu-id="8ef9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ef9c-102">SYNOPSIS</span></span>
<span data-ttu-id="8ef9c-103">Entfernt eine Erweiterung aus der VMSS.</span><span class="sxs-lookup"><span data-stu-id="8ef9c-103">Removes an extension from the VMSS.</span></span>

## <span data-ttu-id="8ef9c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8ef9c-104">SYNTAX</span></span>

### <span data-ttu-id="8ef9c-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ef9c-105">NameParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ef9c-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ef9c-106">IdParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ef9c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8ef9c-107">DESCRIPTION</span></span>
<span data-ttu-id="8ef9c-108">Das **Cmdlet "Remove-AzVmssExtension"** entfernt eine Erweiterung aus dem Virtual Machine Scale Set (VMSS).</span><span class="sxs-lookup"><span data-stu-id="8ef9c-108">The **Remove-AzVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="8ef9c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8ef9c-109">EXAMPLES</span></span>

### <span data-ttu-id="8ef9c-110">Beispiel 1: Entfernen einer VMSS-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="8ef9c-110">Example 1: Remove a VMSS extension</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName
PS C:\> Update-AzVmss -ResourceGroupName $RGName -Name $vmssName -VirtualMachineScaleSet $vmss
```

<span data-ttu-id="8ef9c-111">Mit diesem Befehl wird die Erweiterung eines VMSS entfernt und der VMSS nach der Änderung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="8ef9c-111">This command removes the extension of a VMSS and update the VMSS after the modification.</span></span>

### <span data-ttu-id="8ef9c-112">Beispiel 2: Entfernen einer Instanz aus einem VMSS</span><span class="sxs-lookup"><span data-stu-id="8ef9c-112">Example 2: Remove an instance from within a VMSS</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -ResourceGroupName "Group002" -VirtualMachineScaleSet $vmss -Id $extensionId
```

<span data-ttu-id="8ef9c-113">Mit diesem Befehl wird die "specify extension id" aus der VMSS entfernt, die zur Ressourcengruppe "Group002" gehört.</span><span class="sxs-lookup"><span data-stu-id="8ef9c-113">This command removes specify extension id from the VMSS that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="8ef9c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ef9c-114">PARAMETERS</span></span>

### <span data-ttu-id="8ef9c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ef9c-115">-DefaultProfile</span></span>
<span data-ttu-id="8ef9c-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8ef9c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ef9c-117">-ID</span><span class="sxs-lookup"><span data-stu-id="8ef9c-117">-Id</span></span>
<span data-ttu-id="8ef9c-118">Gibt die ID der Erweiterung an, die dieses Cmdlet von der VMSS entfernt.</span><span class="sxs-lookup"><span data-stu-id="8ef9c-118">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ef9c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8ef9c-119">-Name</span></span>
<span data-ttu-id="8ef9c-120">Gibt den Namen der Erweiterung an, die dieses Cmdlet von der VMSS entfernt.</span><span class="sxs-lookup"><span data-stu-id="8ef9c-120">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ef9c-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8ef9c-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8ef9c-122">Gibt den VMSS an, von dem die Erweiterung entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8ef9c-122">Specifies the VMSS from which to remove the extension from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ef9c-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ef9c-123">-Confirm</span></span>
<span data-ttu-id="8ef9c-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8ef9c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ef9c-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8ef9c-125">-WhatIf</span></span>
<span data-ttu-id="8ef9c-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8ef9c-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ef9c-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8ef9c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ef9c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ef9c-128">CommonParameters</span></span>
<span data-ttu-id="8ef9c-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ef9c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ef9c-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ef9c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ef9c-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8ef9c-131">INPUTS</span></span>

### <span data-ttu-id="8ef9c-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8ef9c-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="8ef9c-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8ef9c-133">System.String</span></span>

## <span data-ttu-id="8ef9c-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8ef9c-134">OUTPUTS</span></span>

### <span data-ttu-id="8ef9c-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8ef9c-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="8ef9c-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8ef9c-136">NOTES</span></span>

## <span data-ttu-id="8ef9c-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8ef9c-137">RELATED LINKS</span></span>

[<span data-ttu-id="8ef9c-138">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="8ef9c-138">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)
