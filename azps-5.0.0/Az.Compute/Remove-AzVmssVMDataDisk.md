---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
ms.openlocfilehash: 534b565e7fc77b1c8764b372675a7d8c4674b571
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175816"
---
# <span data-ttu-id="7a36b-101">Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7a36b-101">Remove-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="7a36b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7a36b-102">SYNOPSIS</span></span>
<span data-ttu-id="7a36b-103">Entfernt einen Datenträger aus einem virtuellen Computer mit Skalierungs Satz</span><span class="sxs-lookup"><span data-stu-id="7a36b-103">Removes a data disk from a virtual machine scale set VM</span></span>

## <span data-ttu-id="7a36b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a36b-104">SYNTAX</span></span>

```
Remove-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a36b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7a36b-105">DESCRIPTION</span></span>
<span data-ttu-id="7a36b-106">Das Cmdlet " **Remove-AzVmssVMDataDisk** " entfernt einen Datenträger aus einem VM-Skalierungs Satz VM</span><span class="sxs-lookup"><span data-stu-id="7a36b-106">The **Remove-AzVmssVMDataDisk** cmdlet removes a data disk from a VM scale set VM</span></span>

## <span data-ttu-id="7a36b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7a36b-107">EXAMPLES</span></span>

### <span data-ttu-id="7a36b-108">Beispiel 1: Entfernen eines Daten Datenträgers aus einem VM-Skalierungs Satz</span><span class="sxs-lookup"><span data-stu-id="7a36b-108">Example 1: Remove a data disk from a VM scale set VM</span></span>
```powershell
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 
PS C:\> Remove-AzVmssVMDataDisk -VM $VirtualMachine -Lun 0
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="7a36b-109">Der erste Befehl getsan vorhandene VMSS-VM, die durch den Ressourcengruppennamen, den VMSS-Namen und die Instanz-ID angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7a36b-109">The first command getsan existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="7a36b-110">Mit dem zweiten Befehl wird die Datenträger-LUN 0 aus dem VM-Skalierungs Satz VM entfernt, der in $VmssVM der endgültige Befehl die VMSS VM mit dem entfernten Datenträger aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7a36b-110">The second command removes the data disk lun 0 from the VM scale set VM stored in $VmssVM The final command updates the Vmss VM with removed data disk.</span></span>

## <span data-ttu-id="7a36b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a36b-111">PARAMETERS</span></span>

### <span data-ttu-id="7a36b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a36b-112">-DefaultProfile</span></span>
<span data-ttu-id="7a36b-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7a36b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a36b-114">-LUN</span><span class="sxs-lookup"><span data-stu-id="7a36b-114">-Lun</span></span>
<span data-ttu-id="7a36b-115">Gibt die logische Einheitsnummer des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="7a36b-115">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a36b-116">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="7a36b-116">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="7a36b-117">Der Skalierungs Satz des virtuellen Computers für VM-Profil.</span><span class="sxs-lookup"><span data-stu-id="7a36b-117">The virtual machine scale set VM profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a36b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a36b-118">CommonParameters</span></span>
<span data-ttu-id="7a36b-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a36b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a36b-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a36b-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a36b-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7a36b-121">INPUTS</span></span>

### <span data-ttu-id="7a36b-122">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="7a36b-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="7a36b-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7a36b-123">OUTPUTS</span></span>

### <span data-ttu-id="7a36b-124">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="7a36b-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="7a36b-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="7a36b-125">NOTES</span></span>

## <span data-ttu-id="7a36b-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7a36b-126">RELATED LINKS</span></span>
