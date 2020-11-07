---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdatadisk
schema: 2.0.0
ms.openlocfilehash: ea8b069be4b153e6e4ca295a917e1c3e81629094
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849755"
---
# <span data-ttu-id="7de59-101">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7de59-101">Remove-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="7de59-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7de59-102">SYNOPSIS</span></span>
<span data-ttu-id="7de59-103">Entfernt einen Datenträger von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="7de59-103">Removes a data disk from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7de59-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7de59-104">SYNTAX</span></span>

```
Remove-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7de59-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7de59-105">DESCRIPTION</span></span>
<span data-ttu-id="7de59-106">Das Cmdlet **Remove-AzureRmVMDataDisk** entfernt einen Daten Datenträger von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="7de59-106">The **Remove-AzureRmVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="7de59-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7de59-107">EXAMPLES</span></span>

### <span data-ttu-id="7de59-108">Beispiel 1: Entfernen eines Daten Datenträgers von einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="7de59-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzureRmVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="7de59-109">Der erste Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine07 mit dem Cmdlet **Get-AzureRmVM** ab.</span><span class="sxs-lookup"><span data-stu-id="7de59-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="7de59-110">Der Befehl speichert den virtuellen Computer in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="7de59-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="7de59-111">Der zweite Befehl entfernt den Datenträger mit dem Namen Disk3 aus dem virtuellen Computer, der in $VirtualMachine gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="7de59-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="7de59-112">Der endgültige Befehl aktualisiert den Zustand des virtuellen Computers, der in $VirtualMachine in ResourceGroup11 gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="7de59-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="7de59-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7de59-113">PARAMETERS</span></span>

### <span data-ttu-id="7de59-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="7de59-114">-DataDiskNames</span></span>
<span data-ttu-id="7de59-115">Gibt die Namen von mindestens einem Datenträger an, die von diesem Cmdlet entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="7de59-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7de59-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7de59-116">-DefaultProfile</span></span>
<span data-ttu-id="7de59-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7de59-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7de59-118">-VM</span><span class="sxs-lookup"><span data-stu-id="7de59-118">-VM</span></span>
<span data-ttu-id="7de59-119">Gibt das Objekt des lokalen virtuellen Computers an, aus dem ein Daten Datenträger entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7de59-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="7de59-120">Verwenden Sie das Get-AzureRmVM-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7de59-120">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="7de59-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7de59-121">-Confirm</span></span>
<span data-ttu-id="7de59-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7de59-122">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="7de59-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7de59-123">-WhatIf</span></span>
<span data-ttu-id="7de59-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7de59-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7de59-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7de59-125">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="7de59-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7de59-126">CommonParameters</span></span>
<span data-ttu-id="7de59-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7de59-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7de59-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7de59-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7de59-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7de59-129">INPUTS</span></span>

### <span data-ttu-id="7de59-130">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7de59-130">PSVirtualMachine</span></span>
<span data-ttu-id="7de59-131">Der Parameter "VM" akzeptiert den Wert vom Typ "PSVirtualMachine" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="7de59-131">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="7de59-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7de59-132">OUTPUTS</span></span>

### <span data-ttu-id="7de59-133">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7de59-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="7de59-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="7de59-134">NOTES</span></span>

## <span data-ttu-id="7de59-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7de59-135">RELATED LINKS</span></span>

[<span data-ttu-id="7de59-136">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7de59-136">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="7de59-137">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7de59-137">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


