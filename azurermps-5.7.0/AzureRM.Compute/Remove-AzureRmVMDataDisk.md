---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
ms.openlocfilehash: 3c1edb8302ac0921a8f396230637b842d88eab77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662750"
---
# <span data-ttu-id="0bb2e-101">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="0bb2e-101">Remove-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="0bb2e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0bb2e-102">SYNOPSIS</span></span>
<span data-ttu-id="0bb2e-103">Entfernt einen Datenträger von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="0bb2e-103">Removes a data disk from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0bb2e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0bb2e-104">SYNTAX</span></span>

```
Remove-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0bb2e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0bb2e-105">DESCRIPTION</span></span>
<span data-ttu-id="0bb2e-106">Das Cmdlet **Remove-AzureRmVMDataDisk** entfernt einen Daten Datenträger von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="0bb2e-106">The **Remove-AzureRmVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="0bb2e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0bb2e-107">EXAMPLES</span></span>

### <span data-ttu-id="0bb2e-108">Beispiel 1: Entfernen eines Daten Datenträgers von einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="0bb2e-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzureRmVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="0bb2e-109">Der erste Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine07 mit dem Cmdlet **Get-AzureRmVM** ab.</span><span class="sxs-lookup"><span data-stu-id="0bb2e-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="0bb2e-110">Der Befehl speichert den virtuellen Computer in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="0bb2e-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="0bb2e-111">Der zweite Befehl entfernt den Datenträger mit dem Namen Disk3 aus dem virtuellen Computer, der in $VirtualMachine gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="0bb2e-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="0bb2e-112">Der endgültige Befehl aktualisiert den Zustand des virtuellen Computers, der in $VirtualMachine in ResourceGroup11 gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="0bb2e-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="0bb2e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0bb2e-113">PARAMETERS</span></span>

### <span data-ttu-id="0bb2e-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="0bb2e-114">-DataDiskNames</span></span>
<span data-ttu-id="0bb2e-115">Gibt die Namen von mindestens einem Datenträger an, die von diesem Cmdlet entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="0bb2e-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb2e-116">-VM</span><span class="sxs-lookup"><span data-stu-id="0bb2e-116">-VM</span></span>
<span data-ttu-id="0bb2e-117">Gibt das Objekt des lokalen virtuellen Computers an, aus dem ein Daten Datenträger entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0bb2e-117">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="0bb2e-118">Verwenden Sie das Get-AzureRmVM-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0bb2e-118">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="0bb2e-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0bb2e-119">-Confirm</span></span>
<span data-ttu-id="0bb2e-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0bb2e-120">Prompts you for confirmation before running the cmdlet.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb2e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bb2e-121">-WhatIf</span></span>
<span data-ttu-id="0bb2e-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0bb2e-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0bb2e-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0bb2e-123">The cmdlet is not run.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb2e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bb2e-124">CommonParameters</span></span>
<span data-ttu-id="0bb2e-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bb2e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bb2e-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bb2e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bb2e-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0bb2e-127">INPUTS</span></span>

### <span data-ttu-id="0bb2e-128">Keine</span><span class="sxs-lookup"><span data-stu-id="0bb2e-128">None</span></span>
<span data-ttu-id="0bb2e-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="0bb2e-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0bb2e-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0bb2e-130">OUTPUTS</span></span>

## <span data-ttu-id="0bb2e-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="0bb2e-131">NOTES</span></span>

## <span data-ttu-id="0bb2e-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0bb2e-132">RELATED LINKS</span></span>

[<span data-ttu-id="0bb2e-133">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="0bb2e-133">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="0bb2e-134">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0bb2e-134">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


