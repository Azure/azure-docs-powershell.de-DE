---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
ms.openlocfilehash: 534b565e7fc77b1c8764b372675a7d8c4674b571
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98308003"
---
# <span data-ttu-id="4f47d-101">Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="4f47d-101">Remove-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="4f47d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f47d-102">SYNOPSIS</span></span>
<span data-ttu-id="4f47d-103">Entfernt einen Datendatenträger von einer virtuellen Computerskalensatz-VM.</span><span class="sxs-lookup"><span data-stu-id="4f47d-103">Removes a data disk from a virtual machine scale set VM</span></span>

## <span data-ttu-id="4f47d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f47d-104">SYNTAX</span></span>

```
Remove-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f47d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f47d-105">DESCRIPTION</span></span>
<span data-ttu-id="4f47d-106">Das **Cmdlet "Remove-AzVmssVMDataDisk"** entfernt einen Datenträger von einer VM-Skalierungssatz-VM.</span><span class="sxs-lookup"><span data-stu-id="4f47d-106">The **Remove-AzVmssVMDataDisk** cmdlet removes a data disk from a VM scale set VM</span></span>

## <span data-ttu-id="4f47d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4f47d-107">EXAMPLES</span></span>

### <span data-ttu-id="4f47d-108">Beispiel 1: Entfernen eines Datenträgers von einer VM-Skalierungssatz-VM</span><span class="sxs-lookup"><span data-stu-id="4f47d-108">Example 1: Remove a data disk from a VM scale set VM</span></span>
```powershell
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 
PS C:\> Remove-AzVmssVMDataDisk -VM $VirtualMachine -Lun 0
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="4f47d-109">Der erste Befehl getsan existing Vmss VM, der vom Ressourcengruppennamen, dem Namen der vmss und der Instanz-ID angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4f47d-109">The first command getsan existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="4f47d-110">Der zweite Befehl entfernt den Datenspeicher lun 0 aus der VM-Skalierungssatz-VM, die in $VmssVM Der letzte Befehl aktualisiert die Vmss VM mit dem entfernten Datenspeicher.</span><span class="sxs-lookup"><span data-stu-id="4f47d-110">The second command removes the data disk lun 0 from the VM scale set VM stored in $VmssVM The final command updates the Vmss VM with removed data disk.</span></span>

## <span data-ttu-id="4f47d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f47d-111">PARAMETERS</span></span>

### <span data-ttu-id="4f47d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f47d-112">-DefaultProfile</span></span>
<span data-ttu-id="4f47d-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4f47d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f47d-114">-Lun</span><span class="sxs-lookup"><span data-stu-id="4f47d-114">-Lun</span></span>
<span data-ttu-id="4f47d-115">Gibt die Nummer der logischen Einheit des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="4f47d-115">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="4f47d-116">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="4f47d-116">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="4f47d-117">Das Virtual Machine Scale Set VM-Profil.</span><span class="sxs-lookup"><span data-stu-id="4f47d-117">The virtual machine scale set VM profile.</span></span>

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

### <span data-ttu-id="4f47d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f47d-118">CommonParameters</span></span>
<span data-ttu-id="4f47d-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f47d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f47d-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f47d-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f47d-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4f47d-121">INPUTS</span></span>

### <span data-ttu-id="4f47d-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="4f47d-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="4f47d-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4f47d-123">OUTPUTS</span></span>

### <span data-ttu-id="4f47d-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="4f47d-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="4f47d-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4f47d-125">NOTES</span></span>

## <span data-ttu-id="4f47d-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4f47d-126">RELATED LINKS</span></span>
