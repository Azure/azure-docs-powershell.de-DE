---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMNetworkInterface.md
ms.openlocfilehash: 11d2f8226e2cabba5fb431054a0e6c822e33af6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483141"
---
# <span data-ttu-id="4dd79-101">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4dd79-101">Add-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="4dd79-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4dd79-102">SYNOPSIS</span></span>
<span data-ttu-id="4dd79-103">Fügt eine Netzwerkschnittstelle zu einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="4dd79-103">Adds a network interface to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4dd79-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4dd79-104">SYNTAX</span></span>

### <span data-ttu-id="4dd79-105">GetNicFromNicId (Standard)</span><span class="sxs-lookup"><span data-stu-id="4dd79-105">GetNicFromNicId (Default)</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary] [<CommonParameters>]
```

### <span data-ttu-id="4dd79-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="4dd79-106">GetNicFromNicObject</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]>
 [<CommonParameters>]
```

## <span data-ttu-id="4dd79-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4dd79-107">DESCRIPTION</span></span>
<span data-ttu-id="4dd79-108">Mit dem Cmdlet **Add-AzureRmVMNetworkInterface** wird eine Netzwerkschnittstelle zu einem virtuellen Computer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4dd79-108">The **Add-AzureRmVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="4dd79-109">Sie können eine Schnittstelle hinzufügen, wenn Sie einen virtuellen Computer erstellen oder einem vorhandenen virtuellen Computer einen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4dd79-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="4dd79-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4dd79-110">EXAMPLES</span></span>

### <span data-ttu-id="4dd79-111">Beispiel 1: Hinzufügen einer Netzwerkschnittstelle zu einem neuen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="4dd79-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" 
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="4dd79-112">Der erste Befehl erstellt ein Objekt eines virtuellen Computers und speichert es dann in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4dd79-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="4dd79-113">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="4dd79-113">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="4dd79-114">Der zweite Befehl fügt dem virtuellen Computer, der in $VirtualMachine gespeichert ist, eine Netzwerkschnittstelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="4dd79-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="4dd79-115">Beispiel 2: Hinzufügen einer Netzwerkschnittstelle zu einem vorhandenen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="4dd79-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="4dd79-116">Der erste Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine07 mit dem Cmdlet **Get-AzureRmVM** ab.</span><span class="sxs-lookup"><span data-stu-id="4dd79-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="4dd79-117">Der Befehl speichert den virtuellen Computer in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4dd79-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="4dd79-118">Der zweite Befehl fügt dem virtuellen Computer, der in $VirtualMachine gespeichert ist, eine Netzwerkschnittstelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="4dd79-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="4dd79-119">Der endgültige Befehl aktualisiert den Zustand des virtuellen Computers, der in $VirtualMachine in ResourceGroup11 gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="4dd79-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="4dd79-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="4dd79-120">PARAMETERS</span></span>

### <span data-ttu-id="4dd79-121">-ID</span><span class="sxs-lookup"><span data-stu-id="4dd79-121">-Id</span></span>
<span data-ttu-id="4dd79-122">Gibt die ID einer Netzwerkschnittstelle an, die einem virtuellen Computer hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4dd79-122">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="4dd79-123">Sie können das Cmdlet [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) verwenden, um eine Netzwerkschnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4dd79-123">You can use the [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) cmdlet to obtain a network interface.</span></span>

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

### <span data-ttu-id="4dd79-124">-Network Interface</span><span class="sxs-lookup"><span data-stu-id="4dd79-124">-NetworkInterface</span></span>
<span data-ttu-id="4dd79-125">Gibt die Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="4dd79-125">Specifies the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]
Parameter Sets: GetNicFromNicObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4dd79-126">– Primär</span><span class="sxs-lookup"><span data-stu-id="4dd79-126">-Primary</span></span>
<span data-ttu-id="4dd79-127">Gibt an, dass dieses Cmdlet die Netzwerkschnittstelle als primäre Schnittstelle hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="4dd79-127">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

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

### <span data-ttu-id="4dd79-128">-VM</span><span class="sxs-lookup"><span data-stu-id="4dd79-128">-VM</span></span>
<span data-ttu-id="4dd79-129">Gibt ein lokales virtuelles Computerobjekt an, dem eine Netzwerkschnittstelle hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4dd79-129">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="4dd79-130">Verwenden Sie zum Erstellen eines virtuellen Computers das Cmdlet **New-AzureRmVMConfig** .</span><span class="sxs-lookup"><span data-stu-id="4dd79-130">To create a virtual machine, use the **New-AzureRmVMConfig** cmdlet.</span></span>
<span data-ttu-id="4dd79-131">Verwenden Sie zum Abrufen eines vorhandenen virtuellen Computers das Cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="4dd79-131">To obtain an existing virtual machine, use the **Get-AzureRmVM** cmdlet.</span></span>

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

### <span data-ttu-id="4dd79-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dd79-132">CommonParameters</span></span>
<span data-ttu-id="4dd79-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dd79-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dd79-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dd79-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dd79-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4dd79-135">INPUTS</span></span>

### <span data-ttu-id="4dd79-136">Keine</span><span class="sxs-lookup"><span data-stu-id="4dd79-136">None</span></span>
<span data-ttu-id="4dd79-137">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="4dd79-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4dd79-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4dd79-138">OUTPUTS</span></span>

## <span data-ttu-id="4dd79-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="4dd79-139">NOTES</span></span>

## <span data-ttu-id="4dd79-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4dd79-140">RELATED LINKS</span></span>

[<span data-ttu-id="4dd79-141">Neu – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="4dd79-141">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="4dd79-142">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4dd79-142">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="4dd79-143">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4dd79-143">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)
