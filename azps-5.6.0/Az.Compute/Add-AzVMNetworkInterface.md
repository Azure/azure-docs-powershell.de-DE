---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
ms.openlocfilehash: efe587cf01fa2adf16e4b6beaaa319312f3c9fa5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927400"
---
# <span data-ttu-id="05d2f-101">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="05d2f-101">Add-AzVMNetworkInterface</span></span>

## <span data-ttu-id="05d2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05d2f-102">SYNOPSIS</span></span>
<span data-ttu-id="05d2f-103">Fügt einem virtuellen Computer eine Netzwerkschnittstelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="05d2f-103">Adds a network interface to a virtual machine.</span></span>

## <span data-ttu-id="05d2f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="05d2f-104">SYNTAX</span></span>

### <span data-ttu-id="05d2f-105">GetNicFromNicId (Standard)</span><span class="sxs-lookup"><span data-stu-id="05d2f-105">GetNicFromNicId (Default)</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05d2f-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="05d2f-106">GetNicFromNicObject</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05d2f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="05d2f-107">DESCRIPTION</span></span>
<span data-ttu-id="05d2f-108">Das **Add-AzVMNetworkInterface-Cmdlet** fügt einem virtuellen Computer eine Netzwerkschnittstelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="05d2f-108">The **Add-AzVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="05d2f-109">Sie können eine Schnittstelle hinzufügen, wenn Sie einen virtuellen Computer erstellen oder einen zu einem vorhandenen virtuellen Computer hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="05d2f-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="05d2f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="05d2f-110">EXAMPLES</span></span>

### <span data-ttu-id="05d2f-111">Beispiel 1: Hinzufügen einer Netzwerkschnittstelle zu einem neuen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="05d2f-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="05d2f-112">Mit dem ersten Befehl wird ein Objekt eines virtuellen Computers erstellt und dann in der $VirtualMachine gespeichert.</span><span class="sxs-lookup"><span data-stu-id="05d2f-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="05d2f-113">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="05d2f-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="05d2f-114">Mit dem zweiten Befehl wird dem virtuellen Computer, der auf dem Computer gespeichert ist, eine Netzwerkschnittstelle $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="05d2f-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="05d2f-115">Beispiel 2: Hinzufügen einer Netzwerkschnittstelle zu einem vorhandenen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="05d2f-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="05d2f-116">Der erste Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine07 mithilfe des **Get-AzVM-Cmdlets** ab.</span><span class="sxs-lookup"><span data-stu-id="05d2f-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="05d2f-117">Der Befehl speichert den virtuellen Computer in der $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="05d2f-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="05d2f-118">Mit dem zweiten Befehl wird dem virtuellen Computer, der auf dem Computer gespeichert ist, eine Netzwerkschnittstelle $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="05d2f-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="05d2f-119">Der letzte Befehl aktualisiert den Zustand des virtuellen Computers, der in $VirtualMachine In ResourceGroup11 gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="05d2f-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="05d2f-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="05d2f-120">PARAMETERS</span></span>

### <span data-ttu-id="05d2f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05d2f-121">-DefaultProfile</span></span>
<span data-ttu-id="05d2f-122">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="05d2f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05d2f-123">-ID</span><span class="sxs-lookup"><span data-stu-id="05d2f-123">-Id</span></span>
<span data-ttu-id="05d2f-124">Gibt die ID einer Netzwerkschnittstelle an, die einem virtuellen Computer hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="05d2f-124">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="05d2f-125">Sie können das [Get-AzNetworkInterface-Cmdlet](/powershell/module/az.network/get-aznetworkinterface) verwenden, um eine Netzwerkschnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="05d2f-125">You can use the [Get-AzNetworkInterface](/powershell/module/az.network/get-aznetworkinterface) cmdlet to obtain a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: GetNicFromNicId
Aliases: NicId, NetworkInterfaceId

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05d2f-126">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="05d2f-126">-NetworkInterface</span></span>
<span data-ttu-id="05d2f-127">Gibt die Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="05d2f-127">Specifies the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]
Parameter Sets: GetNicFromNicObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05d2f-128">-Primär</span><span class="sxs-lookup"><span data-stu-id="05d2f-128">-Primary</span></span>
<span data-ttu-id="05d2f-129">Gibt an, dass dieses Cmdlet die Netzwerkschnittstelle als primäre Schnittstelle hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="05d2f-129">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetNicFromNicId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05d2f-130">-VM</span><span class="sxs-lookup"><span data-stu-id="05d2f-130">-VM</span></span>
<span data-ttu-id="05d2f-131">Gibt ein Objekt des lokalen virtuellen Computers an, dem eine Netzwerkschnittstelle hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="05d2f-131">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="05d2f-132">Verwenden Sie zum Erstellen eines virtuellen Computers **das Cmdlet New-AzVMConfig.**</span><span class="sxs-lookup"><span data-stu-id="05d2f-132">To create a virtual machine, use the **New-AzVMConfig** cmdlet.</span></span>
<span data-ttu-id="05d2f-133">Um einen vorhandenen virtuellen Computer zu erhalten, verwenden Sie **das Get-AzVM-Cmdlet.**</span><span class="sxs-lookup"><span data-stu-id="05d2f-133">To obtain an existing virtual machine, use the **Get-AzVM** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05d2f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05d2f-134">CommonParameters</span></span>
<span data-ttu-id="05d2f-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05d2f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05d2f-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05d2f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05d2f-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="05d2f-137">INPUTS</span></span>

### <span data-ttu-id="05d2f-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="05d2f-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="05d2f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="05d2f-139">System.String</span></span>

### <span data-ttu-id="05d2f-140">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="05d2f-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="05d2f-141">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="05d2f-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="05d2f-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="05d2f-142">OUTPUTS</span></span>

### <span data-ttu-id="05d2f-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="05d2f-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="05d2f-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="05d2f-144">NOTES</span></span>

## <span data-ttu-id="05d2f-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="05d2f-145">RELATED LINKS</span></span>

[<span data-ttu-id="05d2f-146">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="05d2f-146">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="05d2f-147">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="05d2f-147">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="05d2f-148">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="05d2f-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)
