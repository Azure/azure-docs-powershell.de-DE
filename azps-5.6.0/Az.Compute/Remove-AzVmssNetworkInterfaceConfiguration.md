---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 3c9e19c30d89d73a52be4defd18166f88b700889
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936272"
---
# <span data-ttu-id="feeba-101">Remove-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="feeba-101">Remove-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="feeba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="feeba-102">SYNOPSIS</span></span>
<span data-ttu-id="feeba-103">Entfernt eine Netzwerkschnittstellenkonfiguration aus einem VMSS.</span><span class="sxs-lookup"><span data-stu-id="feeba-103">Removes a network interface configuration from a VMSS.</span></span>

## <span data-ttu-id="feeba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="feeba-104">SYNTAX</span></span>

### <span data-ttu-id="feeba-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="feeba-105">NameParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="feeba-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="feeba-106">IdParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="feeba-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="feeba-107">DESCRIPTION</span></span>
<span data-ttu-id="feeba-108">Das **Cmdlet Remove-AzVmssNetworkInterfaceConfiguration** entfernt eine Netzwerkschnittstellenkonfiguration aus einem VmSS (Virtual Machine Scale Set).</span><span class="sxs-lookup"><span data-stu-id="feeba-108">The **Remove-AzVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="feeba-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="feeba-109">EXAMPLES</span></span>

### <span data-ttu-id="feeba-110">Beispiel 1: Entfernen einer Schnittstellenkonfiguration</span><span class="sxs-lookup"><span data-stu-id="feeba-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="feeba-111">Der erste Befehl ruft einen VMSS mithilfe des cmdlets Get-AzVmss ab und speichert ihn dann in der $VMSS Variablen.</span><span class="sxs-lookup"><span data-stu-id="feeba-111">The first command gets a VMSS by using the Get-AzVmss cmdlet, and then stores it in the $VMSS variable.</span></span>
<span data-ttu-id="feeba-112">Mit dem zweiten Befehl wird die Netzwerkschnittstellenkonfiguration contosoVmssInterface02 aus dem Satz in $VMSS.</span><span class="sxs-lookup"><span data-stu-id="feeba-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="feeba-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="feeba-113">PARAMETERS</span></span>

### <span data-ttu-id="feeba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feeba-114">-DefaultProfile</span></span>
<span data-ttu-id="feeba-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="feeba-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="feeba-116">-ID</span><span class="sxs-lookup"><span data-stu-id="feeba-116">-Id</span></span>
<span data-ttu-id="feeba-117">Gibt die ID der Netzwerkschnittstellenkonfiguration an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="feeba-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="feeba-118">-Name</span><span class="sxs-lookup"><span data-stu-id="feeba-118">-Name</span></span>
<span data-ttu-id="feeba-119">Gibt den Namen der Netzwerkschnittstellenkonfiguration an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="feeba-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="feeba-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="feeba-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="feeba-121">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="feeba-121">Specifies the VMSS object.</span></span>

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

### <span data-ttu-id="feeba-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="feeba-122">-Confirm</span></span>
<span data-ttu-id="feeba-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="feeba-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="feeba-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="feeba-124">-WhatIf</span></span>
<span data-ttu-id="feeba-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="feeba-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="feeba-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="feeba-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="feeba-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feeba-127">CommonParameters</span></span>
<span data-ttu-id="feeba-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="feeba-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feeba-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="feeba-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feeba-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="feeba-130">INPUTS</span></span>

### <span data-ttu-id="feeba-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="feeba-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="feeba-132">System.String</span><span class="sxs-lookup"><span data-stu-id="feeba-132">System.String</span></span>

## <span data-ttu-id="feeba-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="feeba-133">OUTPUTS</span></span>

### <span data-ttu-id="feeba-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="feeba-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="feeba-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="feeba-135">NOTES</span></span>

## <span data-ttu-id="feeba-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="feeba-136">RELATED LINKS</span></span>

[<span data-ttu-id="feeba-137">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="feeba-137">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="feeba-138">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="feeba-138">Get-AzVmss</span></span>](./Get-AzVmss.md)


