---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
ms.openlocfilehash: 293bb0f314b82ed2318684996f9b18c79a3b81d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662239"
---
# <span data-ttu-id="8d436-101">Remove-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="8d436-101">Remove-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="8d436-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8d436-102">SYNOPSIS</span></span>
<span data-ttu-id="8d436-103">Entfernt einen Datenträger aus dem VMSS.</span><span class="sxs-lookup"><span data-stu-id="8d436-103">Removes a data disk from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d436-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d436-104">SYNTAX</span></span>

### <span data-ttu-id="8d436-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d436-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Name] <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d436-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d436-106">LunParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Lun] <Int32> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d436-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d436-107">DESCRIPTION</span></span>
<span data-ttu-id="8d436-108">Das Cmdlet **Remove-AzureRmVmssDataDisk** entfernt einen Datenträger aus der Instanz des virtuellen Computer-Skalierungs Satzes (VMSS).</span><span class="sxs-lookup"><span data-stu-id="8d436-108">The **Remove-AzureRmVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="8d436-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8d436-109">EXAMPLES</span></span>

### <span data-ttu-id="8d436-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8d436-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="8d436-111">Dieser Befehl entfernt den Datenträger mit dem Namen "DataDisk1" aus dem VMSS-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8d436-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="8d436-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8d436-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="8d436-113">Mit diesem Befehl wird der Daten Datenträger von LUN 0 aus dem VMSS-Objekt entfernt.</span><span class="sxs-lookup"><span data-stu-id="8d436-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="8d436-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d436-114">PARAMETERS</span></span>

### <span data-ttu-id="8d436-115">-LUN</span><span class="sxs-lookup"><span data-stu-id="8d436-115">-Lun</span></span>
<span data-ttu-id="8d436-116">Gibt die logische Einheitsnummer des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="8d436-116">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: LunParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d436-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8d436-117">-Name</span></span>
<span data-ttu-id="8d436-118">Gibt den Namen des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="8d436-118">Specifies the name of the disk.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d436-119">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8d436-119">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8d436-120">Geben Sie das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8d436-120">Specify the VMSS object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d436-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8d436-121">-Confirm</span></span>
<span data-ttu-id="8d436-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8d436-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d436-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d436-123">-WhatIf</span></span>
<span data-ttu-id="8d436-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8d436-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d436-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8d436-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d436-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d436-126">CommonParameters</span></span>
<span data-ttu-id="8d436-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d436-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d436-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d436-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d436-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8d436-129">INPUTS</span></span>

### <span data-ttu-id="8d436-130">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8d436-130">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="8d436-131">System. String System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="8d436-131">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="8d436-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8d436-132">OUTPUTS</span></span>

### <span data-ttu-id="8d436-133">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8d436-133">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="8d436-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="8d436-134">NOTES</span></span>

## <span data-ttu-id="8d436-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8d436-135">RELATED LINKS</span></span>

