---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
ms.openlocfilehash: 3c0a88d53ea1d2c6b77e08ab29a7def3ae9ee445
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003659"
---
# <span data-ttu-id="a4c64-101">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a4c64-101">Add-AzVMNetworkInterface</span></span>

## <span data-ttu-id="a4c64-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a4c64-102">SYNOPSIS</span></span>
<span data-ttu-id="a4c64-103">Fügt eine Netzwerkschnittstelle zu einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="a4c64-103">Adds a network interface to a virtual machine.</span></span>

## <span data-ttu-id="a4c64-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4c64-104">SYNTAX</span></span>

### <span data-ttu-id="a4c64-105">GetNicFromNicId (Standard)</span><span class="sxs-lookup"><span data-stu-id="a4c64-105">GetNicFromNicId (Default)</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4c64-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="a4c64-106">GetNicFromNicObject</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4c64-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a4c64-107">DESCRIPTION</span></span>
<span data-ttu-id="a4c64-108">Mit dem Cmdlet **Add-AzVMNetworkInterface** wird eine Netzwerkschnittstelle zu einem virtuellen Computer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a4c64-108">The **Add-AzVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="a4c64-109">Sie können eine Schnittstelle hinzufügen, wenn Sie einen virtuellen Computer erstellen oder einem vorhandenen virtuellen Computer einen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a4c64-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="a4c64-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a4c64-110">EXAMPLES</span></span>

### <span data-ttu-id="a4c64-111">Beispiel 1: Hinzufügen einer Netzwerkschnittstelle zu einem neuen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="a4c64-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="a4c64-112">Der erste Befehl erstellt ein Objekt eines virtuellen Computers und speichert es dann in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a4c64-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="a4c64-113">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="a4c64-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="a4c64-114">Der zweite Befehl fügt dem virtuellen Computer, der in $VirtualMachine gespeichert ist, eine Netzwerkschnittstelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="a4c64-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="a4c64-115">Beispiel 2: Hinzufügen einer Netzwerkschnittstelle zu einem vorhandenen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="a4c64-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="a4c64-116">Der erste Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine07 mit dem Cmdlet **Get-AzVM** ab.</span><span class="sxs-lookup"><span data-stu-id="a4c64-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="a4c64-117">Der Befehl speichert den virtuellen Computer in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a4c64-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="a4c64-118">Der zweite Befehl fügt dem virtuellen Computer, der in $VirtualMachine gespeichert ist, eine Netzwerkschnittstelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="a4c64-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="a4c64-119">Der endgültige Befehl aktualisiert den Zustand des virtuellen Computers, der in $VirtualMachine in ResourceGroup11 gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="a4c64-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="a4c64-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4c64-120">PARAMETERS</span></span>

### <span data-ttu-id="a4c64-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4c64-121">-DefaultProfile</span></span>
<span data-ttu-id="a4c64-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a4c64-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4c64-123">-ID</span><span class="sxs-lookup"><span data-stu-id="a4c64-123">-Id</span></span>
<span data-ttu-id="a4c64-124">Gibt die ID einer Netzwerkschnittstelle an, die einem virtuellen Computer hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a4c64-124">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="a4c64-125">Sie können das Cmdlet [Get-AzNetworkInterface](/powershell/module/az.network/get-aznetworkinterface) verwenden, um eine Netzwerkschnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a4c64-125">You can use the [Get-AzNetworkInterface](/powershell/module/az.network/get-aznetworkinterface) cmdlet to obtain a network interface.</span></span>

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

### <span data-ttu-id="a4c64-126">-Network Interface</span><span class="sxs-lookup"><span data-stu-id="a4c64-126">-NetworkInterface</span></span>
<span data-ttu-id="a4c64-127">Gibt die Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="a4c64-127">Specifies the network interface.</span></span>

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

### <span data-ttu-id="a4c64-128">– Primär</span><span class="sxs-lookup"><span data-stu-id="a4c64-128">-Primary</span></span>
<span data-ttu-id="a4c64-129">Gibt an, dass dieses Cmdlet die Netzwerkschnittstelle als primäre Schnittstelle hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="a4c64-129">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

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

### <span data-ttu-id="a4c64-130">-VM</span><span class="sxs-lookup"><span data-stu-id="a4c64-130">-VM</span></span>
<span data-ttu-id="a4c64-131">Gibt ein lokales virtuelles Computerobjekt an, dem eine Netzwerkschnittstelle hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a4c64-131">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="a4c64-132">Verwenden Sie zum Erstellen eines virtuellen Computers das Cmdlet **New-AzVMConfig** .</span><span class="sxs-lookup"><span data-stu-id="a4c64-132">To create a virtual machine, use the **New-AzVMConfig** cmdlet.</span></span>
<span data-ttu-id="a4c64-133">Verwenden Sie zum Abrufen eines vorhandenen virtuellen Computers das Cmdlet **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="a4c64-133">To obtain an existing virtual machine, use the **Get-AzVM** cmdlet.</span></span>

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

### <span data-ttu-id="a4c64-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4c64-134">CommonParameters</span></span>
<span data-ttu-id="a4c64-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4c64-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4c64-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4c64-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4c64-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a4c64-137">INPUTS</span></span>

### <span data-ttu-id="a4c64-138">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a4c64-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="a4c64-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a4c64-139">System.String</span></span>

### <span data-ttu-id="a4c64-140">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Management. Internal. Network. Common. INetworkInterfaceReference, Microsoft. Azure. PowerShell. Clients. Network, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="a4c64-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="a4c64-141">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="a4c64-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a4c64-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a4c64-142">OUTPUTS</span></span>

### <span data-ttu-id="a4c64-143">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a4c64-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="a4c64-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="a4c64-144">NOTES</span></span>

## <span data-ttu-id="a4c64-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a4c64-145">RELATED LINKS</span></span>

[<span data-ttu-id="a4c64-146">Neu – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="a4c64-146">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="a4c64-147">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="a4c64-147">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="a4c64-148">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a4c64-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)
