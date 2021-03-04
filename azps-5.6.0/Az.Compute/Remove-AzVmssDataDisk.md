---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
ms.openlocfilehash: abdef821862976a3bffb0b39bc48a3619e17d64f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943088"
---
# <span data-ttu-id="a5f91-101">Remove-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="a5f91-101">Remove-AzVmssDataDisk</span></span>

## <span data-ttu-id="a5f91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5f91-102">SYNOPSIS</span></span>
<span data-ttu-id="a5f91-103">Entfernt einen Datenträger aus dem VMSS.</span><span class="sxs-lookup"><span data-stu-id="a5f91-103">Removes a data disk from the VMSS.</span></span>

## <span data-ttu-id="a5f91-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5f91-104">SYNTAX</span></span>

### <span data-ttu-id="a5f91-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5f91-105">NameParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5f91-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5f91-106">LunParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5f91-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5f91-107">DESCRIPTION</span></span>
<span data-ttu-id="a5f91-108">Das **Cmdlet Remove-AzVmssDataDisk** entfernt einen Datenträger aus der VmSS-Instanz (Virtual Machine Scale Set).</span><span class="sxs-lookup"><span data-stu-id="a5f91-108">The **Remove-AzVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="a5f91-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a5f91-109">EXAMPLES</span></span>

### <span data-ttu-id="a5f91-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a5f91-110">Example 1</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="a5f91-111">Mit diesem Befehl wird der Datenträger mit dem Namen "DataDisk1" aus dem VMSS-Objekt entfernt.</span><span class="sxs-lookup"><span data-stu-id="a5f91-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="a5f91-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a5f91-112">Example 2</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="a5f91-113">Mit diesem Befehl wird der Datenträger von LUN 0 aus dem VMSS-Objekt entfernt.</span><span class="sxs-lookup"><span data-stu-id="a5f91-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="a5f91-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a5f91-114">PARAMETERS</span></span>

### <span data-ttu-id="a5f91-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5f91-115">-DefaultProfile</span></span>
<span data-ttu-id="a5f91-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a5f91-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5f91-117">-Lun</span><span class="sxs-lookup"><span data-stu-id="a5f91-117">-Lun</span></span>
<span data-ttu-id="a5f91-118">Gibt die logische Einheitennummer des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="a5f91-118">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: LunParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5f91-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a5f91-119">-Name</span></span>
<span data-ttu-id="a5f91-120">Gibt den Namen des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="a5f91-120">Specifies the name of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5f91-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a5f91-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a5f91-122">Geben Sie das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a5f91-122">Specify the VMSS object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5f91-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a5f91-123">-Confirm</span></span>
<span data-ttu-id="a5f91-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a5f91-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f91-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5f91-125">-WhatIf</span></span>
<span data-ttu-id="a5f91-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a5f91-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5f91-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a5f91-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f91-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5f91-128">CommonParameters</span></span>
<span data-ttu-id="a5f91-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5f91-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5f91-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5f91-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5f91-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a5f91-131">INPUTS</span></span>

### <span data-ttu-id="a5f91-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a5f91-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="a5f91-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a5f91-133">System.String</span></span>

### <span data-ttu-id="a5f91-134">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a5f91-134">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a5f91-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a5f91-135">OUTPUTS</span></span>

### <span data-ttu-id="a5f91-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a5f91-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="a5f91-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a5f91-137">NOTES</span></span>

## <span data-ttu-id="a5f91-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a5f91-138">RELATED LINKS</span></span>
