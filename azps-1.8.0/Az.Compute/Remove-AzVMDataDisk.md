---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDataDisk.md
ms.openlocfilehash: eee21edf854756415c70f84f40ce79a948cd21e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820607"
---
# <span data-ttu-id="c4b6c-101">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="c4b6c-101">Remove-AzVMDataDisk</span></span>

## <span data-ttu-id="c4b6c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c4b6c-102">SYNOPSIS</span></span>
<span data-ttu-id="c4b6c-103">Entfernt einen Datenträger von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="c4b6c-103">Removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="c4b6c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4b6c-104">SYNTAX</span></span>

```
Remove-AzVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4b6c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4b6c-105">DESCRIPTION</span></span>
<span data-ttu-id="c4b6c-106">Das Cmdlet **Remove-AzVMDataDisk** entfernt einen Daten Datenträger von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="c4b6c-106">The **Remove-AzVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="c4b6c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4b6c-107">EXAMPLES</span></span>

### <span data-ttu-id="c4b6c-108">Beispiel 1: Entfernen eines Daten Datenträgers von einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="c4b6c-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="c4b6c-109">Der erste Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine07 mit dem Cmdlet **Get-AzVM** ab.</span><span class="sxs-lookup"><span data-stu-id="c4b6c-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="c4b6c-110">Der Befehl speichert den virtuellen Computer in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="c4b6c-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="c4b6c-111">Der zweite Befehl entfernt den Datenträger mit dem Namen Disk3 aus dem virtuellen Computer, der in $VirtualMachine gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="c4b6c-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="c4b6c-112">Der endgültige Befehl aktualisiert den Zustand des virtuellen Computers, der in $VirtualMachine in ResourceGroup11 gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="c4b6c-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="c4b6c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4b6c-113">PARAMETERS</span></span>

### <span data-ttu-id="c4b6c-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="c4b6c-114">-DataDiskNames</span></span>
<span data-ttu-id="c4b6c-115">Gibt die Namen von mindestens einem Datenträger an, die von diesem Cmdlet entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="c4b6c-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c4b6c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4b6c-116">-DefaultProfile</span></span>
<span data-ttu-id="c4b6c-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c4b6c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4b6c-118">-VM</span><span class="sxs-lookup"><span data-stu-id="c4b6c-118">-VM</span></span>
<span data-ttu-id="c4b6c-119">Gibt das Objekt des lokalen virtuellen Computers an, aus dem ein Daten Datenträger entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c4b6c-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="c4b6c-120">Verwenden Sie das Get-AzVM-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c4b6c-120">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="c4b6c-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c4b6c-121">-Confirm</span></span>
<span data-ttu-id="c4b6c-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c4b6c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4b6c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4b6c-123">-WhatIf</span></span>
<span data-ttu-id="c4b6c-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c4b6c-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4b6c-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4b6c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4b6c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4b6c-126">CommonParameters</span></span>
<span data-ttu-id="c4b6c-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4b6c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4b6c-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4b6c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4b6c-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c4b6c-129">INPUTS</span></span>

### <span data-ttu-id="c4b6c-130">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c4b6c-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="c4b6c-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c4b6c-131">OUTPUTS</span></span>

### <span data-ttu-id="c4b6c-132">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c4b6c-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="c4b6c-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="c4b6c-133">NOTES</span></span>

## <span data-ttu-id="c4b6c-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c4b6c-134">RELATED LINKS</span></span>

[<span data-ttu-id="c4b6c-135">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="c4b6c-135">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="c4b6c-136">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="c4b6c-136">Get-AzVM</span></span>](./Get-AzVM.md)


