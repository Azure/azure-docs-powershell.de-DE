---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
ms.openlocfilehash: aaf1162cdeeb007a680a3e9de325cbd10fadef94
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844744"
---
# <span data-ttu-id="d89d6-101">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d89d6-101">Add-AzVMNetworkInterface</span></span>

## <span data-ttu-id="d89d6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d89d6-102">SYNOPSIS</span></span>
<span data-ttu-id="d89d6-103">Fügt eine Netzwerkschnittstelle zu einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="d89d6-103">Adds a network interface to a virtual machine.</span></span>

## <span data-ttu-id="d89d6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d89d6-104">SYNTAX</span></span>

### <span data-ttu-id="d89d6-105">GetNicFromNicId (Standard)</span><span class="sxs-lookup"><span data-stu-id="d89d6-105">GetNicFromNicId (Default)</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d89d6-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="d89d6-106">GetNicFromNicObject</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d89d6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d89d6-107">DESCRIPTION</span></span>
<span data-ttu-id="d89d6-108">Mit dem Cmdlet **Add-AzVMNetworkInterface** wird eine Netzwerkschnittstelle zu einem virtuellen Computer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d89d6-108">The **Add-AzVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="d89d6-109">Sie können eine Schnittstelle hinzufügen, wenn Sie einen virtuellen Computer erstellen oder einem vorhandenen virtuellen Computer einen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d89d6-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="d89d6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d89d6-110">EXAMPLES</span></span>

### <span data-ttu-id="d89d6-111">Beispiel 1: Hinzufügen einer Netzwerkschnittstelle zu einem neuen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="d89d6-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="d89d6-112">Der erste Befehl erstellt ein Objekt eines virtuellen Computers und speichert es dann in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="d89d6-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="d89d6-113">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="d89d6-113">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="d89d6-114">Der zweite Befehl fügt dem virtuellen Computer, der in $VirtualMachine gespeichert ist, eine Netzwerkschnittstelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="d89d6-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="d89d6-115">Beispiel 2: Hinzufügen einer Netzwerkschnittstelle zu einem vorhandenen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="d89d6-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="d89d6-116">Der erste Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine07 mit dem Cmdlet **Get-AzVM** ab.</span><span class="sxs-lookup"><span data-stu-id="d89d6-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="d89d6-117">Der Befehl speichert den virtuellen Computer in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="d89d6-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="d89d6-118">Der zweite Befehl fügt dem virtuellen Computer, der in $VirtualMachine gespeichert ist, eine Netzwerkschnittstelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="d89d6-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="d89d6-119">Der endgültige Befehl aktualisiert den Zustand des virtuellen Computers, der in $VirtualMachine in ResourceGroup11 gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="d89d6-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="d89d6-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="d89d6-120">PARAMETERS</span></span>

### <span data-ttu-id="d89d6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d89d6-121">-DefaultProfile</span></span>
<span data-ttu-id="d89d6-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d89d6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d89d6-123">-ID</span><span class="sxs-lookup"><span data-stu-id="d89d6-123">-Id</span></span>
<span data-ttu-id="d89d6-124">Gibt die ID einer Netzwerkschnittstelle an, die einem virtuellen Computer hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d89d6-124">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="d89d6-125">Sie können das Cmdlet [Get-AzNetworkInterface](/powershell/module/azurerm.network/get-aznetworkinterface) verwenden, um eine Netzwerkschnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d89d6-125">You can use the [Get-AzNetworkInterface](/powershell/module/azurerm.network/get-aznetworkinterface) cmdlet to obtain a network interface.</span></span>

```yaml
Type: String
Parameter Sets: GetNicFromNicId
Aliases: NicId, NetworkInterfaceId

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d89d6-126">-Network Interface</span><span class="sxs-lookup"><span data-stu-id="d89d6-126">-NetworkInterface</span></span>
<span data-ttu-id="d89d6-127">Gibt die Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="d89d6-127">Specifies the network interface.</span></span>

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

### <span data-ttu-id="d89d6-128">– Primär</span><span class="sxs-lookup"><span data-stu-id="d89d6-128">-Primary</span></span>
<span data-ttu-id="d89d6-129">Gibt an, dass dieses Cmdlet die Netzwerkschnittstelle als primäre Schnittstelle hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="d89d6-129">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetNicFromNicId
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d89d6-130">-VM</span><span class="sxs-lookup"><span data-stu-id="d89d6-130">-VM</span></span>
<span data-ttu-id="d89d6-131">Gibt ein lokales virtuelles Computerobjekt an, dem eine Netzwerkschnittstelle hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d89d6-131">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="d89d6-132">Verwenden Sie zum Erstellen eines virtuellen Computers das Cmdlet **New-AzVMConfig** .</span><span class="sxs-lookup"><span data-stu-id="d89d6-132">To create a virtual machine, use the **New-AzVMConfig** cmdlet.</span></span>
<span data-ttu-id="d89d6-133">Verwenden Sie zum Abrufen eines vorhandenen virtuellen Computers das Cmdlet **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="d89d6-133">To obtain an existing virtual machine, use the **Get-AzVM** cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d89d6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d89d6-134">CommonParameters</span></span>
<span data-ttu-id="d89d6-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d89d6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d89d6-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d89d6-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d89d6-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d89d6-137">INPUTS</span></span>

### <span data-ttu-id="d89d6-138">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Network. Models. PSNetworkInterface]</span><span class="sxs-lookup"><span data-stu-id="d89d6-138">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]</span></span>
<span data-ttu-id="d89d6-139">Der Parameter "Network Interface" akzeptiert den Wert vom Typ "System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Network. Models. PSNetworkInterface]" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="d89d6-139">Parameter 'NetworkInterface' accepts value of type 'System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]' from the pipeline</span></span>

### <span data-ttu-id="d89d6-140">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d89d6-140">PSVirtualMachine</span></span>
<span data-ttu-id="d89d6-141">Der Parameter "VM" akzeptiert den Wert vom Typ "PSVirtualMachine" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="d89d6-141">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="d89d6-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d89d6-142">OUTPUTS</span></span>

### <span data-ttu-id="d89d6-143">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d89d6-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="d89d6-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="d89d6-144">NOTES</span></span>

## <span data-ttu-id="d89d6-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d89d6-145">RELATED LINKS</span></span>

[<span data-ttu-id="d89d6-146">Neu – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="d89d6-146">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="d89d6-147">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="d89d6-147">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="d89d6-148">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d89d6-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)
