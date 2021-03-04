---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDataDisk.md
ms.openlocfilehash: 72ccf9994b303e9e191594f32bb2aa23f0abd9ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934259"
---
# <span data-ttu-id="29eb4-101">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="29eb4-101">Remove-AzVMDataDisk</span></span>

## <span data-ttu-id="29eb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29eb4-102">SYNOPSIS</span></span>
<span data-ttu-id="29eb4-103">Entfernt einen Datenträger von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="29eb4-103">Removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="29eb4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29eb4-104">SYNTAX</span></span>

```
Remove-AzVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29eb4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29eb4-105">DESCRIPTION</span></span>
<span data-ttu-id="29eb4-106">Das **Cmdlet Remove-AzVMDataDisk** entfernt einen Datenträger von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="29eb4-106">The **Remove-AzVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="29eb4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="29eb4-107">EXAMPLES</span></span>

### <span data-ttu-id="29eb4-108">Beispiel 1: Entfernen eines Datenträgers von einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="29eb4-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="29eb4-109">Der erste Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine07 mithilfe des **Get-AzVM-Cmdlets** ab.</span><span class="sxs-lookup"><span data-stu-id="29eb4-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="29eb4-110">Der Befehl speichert den virtuellen Computer in der $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="29eb4-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="29eb4-111">Mit dem zweiten Befehl wird der Datenträger mit dem Namen "Disk3" von dem virtuellen Computer entfernt, der auf der $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="29eb4-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="29eb4-112">Der letzte Befehl aktualisiert den Zustand des virtuellen Computers, der in $VirtualMachine In ResourceGroup11 gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="29eb4-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="29eb4-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="29eb4-113">PARAMETERS</span></span>

### <span data-ttu-id="29eb4-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="29eb4-114">-DataDiskNames</span></span>
<span data-ttu-id="29eb4-115">Gibt die Namen einer oder mehrere Datenträger an, die von diesem Cmdlet entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="29eb4-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29eb4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29eb4-116">-DefaultProfile</span></span>
<span data-ttu-id="29eb4-117">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="29eb4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29eb4-118">-VM</span><span class="sxs-lookup"><span data-stu-id="29eb4-118">-VM</span></span>
<span data-ttu-id="29eb4-119">Gibt das Objekt des lokalen virtuellen Computers an, von dem ein Datenträger entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="29eb4-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="29eb4-120">Zum Abrufen eines Virtuellen Computerobjekts verwenden Sie das Get-AzVM Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29eb4-120">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="29eb4-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="29eb4-121">-Confirm</span></span>
<span data-ttu-id="29eb4-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="29eb4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29eb4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29eb4-123">-WhatIf</span></span>
<span data-ttu-id="29eb4-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="29eb4-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29eb4-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="29eb4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29eb4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29eb4-126">CommonParameters</span></span>
<span data-ttu-id="29eb4-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29eb4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29eb4-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29eb4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29eb4-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="29eb4-129">INPUTS</span></span>

### <span data-ttu-id="29eb4-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="29eb4-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="29eb4-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="29eb4-131">OUTPUTS</span></span>

### <span data-ttu-id="29eb4-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="29eb4-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="29eb4-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="29eb4-133">NOTES</span></span>

## <span data-ttu-id="29eb4-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="29eb4-134">RELATED LINKS</span></span>

[<span data-ttu-id="29eb4-135">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="29eb4-135">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="29eb4-136">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="29eb4-136">Get-AzVM</span></span>](./Get-AzVM.md)


