---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
ms.openlocfilehash: c44369915c38219491bd8dfdc1ca288487da27f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928336"
---
# <span data-ttu-id="fdebf-101">Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="fdebf-101">Remove-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="fdebf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdebf-102">SYNOPSIS</span></span>
<span data-ttu-id="fdebf-103">Entfernt einen Datenträger von einer virtuellen Computerskalensatz-VM</span><span class="sxs-lookup"><span data-stu-id="fdebf-103">Removes a data disk from a virtual machine scale set VM</span></span>

## <span data-ttu-id="fdebf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fdebf-104">SYNTAX</span></span>

```
Remove-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdebf-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fdebf-105">DESCRIPTION</span></span>
<span data-ttu-id="fdebf-106">Das **Cmdlet Remove-AzVmssVMDataDisk** entfernt einen Datenträger von einer VM-Skalierungssatz-VM</span><span class="sxs-lookup"><span data-stu-id="fdebf-106">The **Remove-AzVmssVMDataDisk** cmdlet removes a data disk from a VM scale set VM</span></span>

## <span data-ttu-id="fdebf-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fdebf-107">EXAMPLES</span></span>

### <span data-ttu-id="fdebf-108">Beispiel 1: Entfernen eines Datenträgers von einer VM-Skalierungssatz-VM</span><span class="sxs-lookup"><span data-stu-id="fdebf-108">Example 1: Remove a data disk from a VM scale set VM</span></span>
```powershell
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 
PS C:\> Remove-AzVmssVMDataDisk -VM $VirtualMachine -Lun 0
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="fdebf-109">Der erste Befehl getsan vorhandene Vmss VM, die durch den Ressourcengruppennamen, den Vmss-Namen und die Instanz-ID angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fdebf-109">The first command getsan existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="fdebf-110">Mit dem zweiten Befehl wird der Datenträger lun 0 aus der VM-Skalierungssatz-VM entfernt, die in $VmssVM Der letzte Befehl aktualisiert die Vmss-VM mit dem entfernten Datenträger.</span><span class="sxs-lookup"><span data-stu-id="fdebf-110">The second command removes the data disk lun 0 from the VM scale set VM stored in $VmssVM The final command updates the Vmss VM with removed data disk.</span></span>

## <span data-ttu-id="fdebf-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fdebf-111">PARAMETERS</span></span>

### <span data-ttu-id="fdebf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdebf-112">-DefaultProfile</span></span>
<span data-ttu-id="fdebf-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fdebf-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdebf-114">-Lun</span><span class="sxs-lookup"><span data-stu-id="fdebf-114">-Lun</span></span>
<span data-ttu-id="fdebf-115">Gibt die logische Einheitennummer des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="fdebf-115">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="fdebf-116">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="fdebf-116">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="fdebf-117">Der Skalierungssatz für virtuelle Computer setzt das VM-Profil.</span><span class="sxs-lookup"><span data-stu-id="fdebf-117">The virtual machine scale set VM profile.</span></span>

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

### <span data-ttu-id="fdebf-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdebf-118">CommonParameters</span></span>
<span data-ttu-id="fdebf-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdebf-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdebf-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fdebf-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdebf-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fdebf-121">INPUTS</span></span>

### <span data-ttu-id="fdebf-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="fdebf-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="fdebf-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fdebf-123">OUTPUTS</span></span>

### <span data-ttu-id="fdebf-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="fdebf-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="fdebf-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fdebf-125">NOTES</span></span>

## <span data-ttu-id="fdebf-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fdebf-126">RELATED LINKS</span></span>
