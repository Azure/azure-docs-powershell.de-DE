---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 112403f4cb742c5df39538eb2d8d8fac629d3379
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850175"
---
# <span data-ttu-id="6c598-101">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6c598-101">Add-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="6c598-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6c598-102">SYNOPSIS</span></span>
<span data-ttu-id="6c598-103">Fügt eine Netzwerkschnittstelle zu einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="6c598-103">Adds a network interface to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c598-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c598-104">SYNTAX</span></span>

### <span data-ttu-id="6c598-105">GetNicFromNicId (Standard)</span><span class="sxs-lookup"><span data-stu-id="6c598-105">GetNicFromNicId (Default)</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c598-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="6c598-106">GetNicFromNicObject</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c598-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c598-107">DESCRIPTION</span></span>
<span data-ttu-id="6c598-108">Mit dem Cmdlet **Add-AzureRmVMNetworkInterface** wird eine Netzwerkschnittstelle zu einem virtuellen Computer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6c598-108">The **Add-AzureRmVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="6c598-109">Sie können eine Schnittstelle hinzufügen, wenn Sie einen virtuellen Computer erstellen oder einem vorhandenen virtuellen Computer einen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6c598-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="6c598-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6c598-110">EXAMPLES</span></span>

### <span data-ttu-id="6c598-111">Beispiel 1: Hinzufügen einer Netzwerkschnittstelle zu einem neuen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="6c598-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="6c598-112">Der erste Befehl erstellt ein Objekt eines virtuellen Computers und speichert es dann in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="6c598-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="6c598-113">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="6c598-113">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="6c598-114">Der zweite Befehl fügt dem virtuellen Computer, der in $VirtualMachine gespeichert ist, eine Netzwerkschnittstelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="6c598-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="6c598-115">Beispiel 2: Hinzufügen einer Netzwerkschnittstelle zu einem vorhandenen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="6c598-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="6c598-116">Der erste Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine07 mit dem Cmdlet **Get-AzureRmVM** ab.</span><span class="sxs-lookup"><span data-stu-id="6c598-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="6c598-117">Der Befehl speichert den virtuellen Computer in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="6c598-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="6c598-118">Der zweite Befehl fügt dem virtuellen Computer, der in $VirtualMachine gespeichert ist, eine Netzwerkschnittstelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="6c598-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="6c598-119">Der endgültige Befehl aktualisiert den Zustand des virtuellen Computers, der in $VirtualMachine in ResourceGroup11 gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="6c598-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="6c598-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c598-120">PARAMETERS</span></span>

### <span data-ttu-id="6c598-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c598-121">-DefaultProfile</span></span>
<span data-ttu-id="6c598-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6c598-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c598-123">-ID</span><span class="sxs-lookup"><span data-stu-id="6c598-123">-Id</span></span>
<span data-ttu-id="6c598-124">Gibt die ID einer Netzwerkschnittstelle an, die einem virtuellen Computer hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6c598-124">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="6c598-125">Sie können das Cmdlet [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) verwenden, um eine Netzwerkschnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6c598-125">You can use the [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) cmdlet to obtain a network interface.</span></span>

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

### <span data-ttu-id="6c598-126">-Network Interface</span><span class="sxs-lookup"><span data-stu-id="6c598-126">-NetworkInterface</span></span>
<span data-ttu-id="6c598-127">Gibt die Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="6c598-127">Specifies the network interface.</span></span>

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

### <span data-ttu-id="6c598-128">– Primär</span><span class="sxs-lookup"><span data-stu-id="6c598-128">-Primary</span></span>
<span data-ttu-id="6c598-129">Gibt an, dass dieses Cmdlet die Netzwerkschnittstelle als primäre Schnittstelle hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="6c598-129">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

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

### <span data-ttu-id="6c598-130">-VM</span><span class="sxs-lookup"><span data-stu-id="6c598-130">-VM</span></span>
<span data-ttu-id="6c598-131">Gibt ein lokales virtuelles Computerobjekt an, dem eine Netzwerkschnittstelle hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6c598-131">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="6c598-132">Verwenden Sie zum Erstellen eines virtuellen Computers das Cmdlet **New-AzureRmVMConfig** .</span><span class="sxs-lookup"><span data-stu-id="6c598-132">To create a virtual machine, use the **New-AzureRmVMConfig** cmdlet.</span></span>
<span data-ttu-id="6c598-133">Verwenden Sie zum Abrufen eines vorhandenen virtuellen Computers das Cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="6c598-133">To obtain an existing virtual machine, use the **Get-AzureRmVM** cmdlet.</span></span>

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

### <span data-ttu-id="6c598-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c598-134">CommonParameters</span></span>
<span data-ttu-id="6c598-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c598-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c598-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c598-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c598-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6c598-137">INPUTS</span></span>

### <span data-ttu-id="6c598-138">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Network. Models. PSNetworkInterface]</span><span class="sxs-lookup"><span data-stu-id="6c598-138">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]</span></span>
<span data-ttu-id="6c598-139">Der Parameter "Network Interface" akzeptiert den Wert vom Typ "System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Network. Models. PSNetworkInterface]" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="6c598-139">Parameter 'NetworkInterface' accepts value of type 'System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]' from the pipeline</span></span>

### <span data-ttu-id="6c598-140">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6c598-140">PSVirtualMachine</span></span>
<span data-ttu-id="6c598-141">Der Parameter "VM" akzeptiert den Wert vom Typ "PSVirtualMachine" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="6c598-141">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="6c598-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6c598-142">OUTPUTS</span></span>

### <span data-ttu-id="6c598-143">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6c598-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="6c598-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="6c598-144">NOTES</span></span>

## <span data-ttu-id="6c598-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6c598-145">RELATED LINKS</span></span>

[<span data-ttu-id="6c598-146">Neu – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="6c598-146">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="6c598-147">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6c598-147">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="6c598-148">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6c598-148">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)
