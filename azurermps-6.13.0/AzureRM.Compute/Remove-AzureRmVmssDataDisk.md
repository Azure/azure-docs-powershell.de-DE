---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
ms.openlocfilehash: 1e0c04bd7283bc2a741b5e2a7130e83b35d00133
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502190"
---
# <span data-ttu-id="9c8f0-101">Remove-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="9c8f0-101">Remove-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="9c8f0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9c8f0-102">SYNOPSIS</span></span>
<span data-ttu-id="9c8f0-103">Entfernt einen Datenträger aus dem VMSS.</span><span class="sxs-lookup"><span data-stu-id="9c8f0-103">Removes a data disk from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c8f0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c8f0-104">SYNTAX</span></span>

### <span data-ttu-id="9c8f0-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c8f0-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c8f0-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c8f0-106">LunParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c8f0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c8f0-107">DESCRIPTION</span></span>
<span data-ttu-id="9c8f0-108">Das Cmdlet **Remove-AzureRmVmssDataDisk** entfernt einen Datenträger aus der Instanz des virtuellen Computer-Skalierungs Satzes (VMSS).</span><span class="sxs-lookup"><span data-stu-id="9c8f0-108">The **Remove-AzureRmVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="9c8f0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9c8f0-109">EXAMPLES</span></span>

### <span data-ttu-id="9c8f0-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9c8f0-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="9c8f0-111">Dieser Befehl entfernt den Datenträger mit dem Namen "DataDisk1" aus dem VMSS-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9c8f0-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="9c8f0-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9c8f0-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="9c8f0-113">Mit diesem Befehl wird der Daten Datenträger von LUN 0 aus dem VMSS-Objekt entfernt.</span><span class="sxs-lookup"><span data-stu-id="9c8f0-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="9c8f0-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c8f0-114">PARAMETERS</span></span>

### <span data-ttu-id="9c8f0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c8f0-115">-DefaultProfile</span></span>
<span data-ttu-id="9c8f0-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9c8f0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c8f0-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="9c8f0-117">-Lun</span></span>
<span data-ttu-id="9c8f0-118">Gibt die logische Einheitsnummer des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="9c8f0-118">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="9c8f0-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9c8f0-119">-Name</span></span>
<span data-ttu-id="9c8f0-120">Gibt den Namen des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="9c8f0-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="9c8f0-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9c8f0-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="9c8f0-122">Geben Sie das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="9c8f0-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="9c8f0-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9c8f0-123">-Confirm</span></span>
<span data-ttu-id="9c8f0-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9c8f0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c8f0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c8f0-125">-WhatIf</span></span>
<span data-ttu-id="9c8f0-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9c8f0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c8f0-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9c8f0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c8f0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c8f0-128">CommonParameters</span></span>
<span data-ttu-id="9c8f0-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c8f0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c8f0-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c8f0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c8f0-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9c8f0-131">INPUTS</span></span>

### <span data-ttu-id="9c8f0-132">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9c8f0-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="9c8f0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9c8f0-133">System.String</span></span>

### <span data-ttu-id="9c8f0-134">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9c8f0-134">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="9c8f0-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9c8f0-135">OUTPUTS</span></span>

### <span data-ttu-id="9c8f0-136">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9c8f0-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="9c8f0-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="9c8f0-137">NOTES</span></span>

## <span data-ttu-id="9c8f0-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9c8f0-138">RELATED LINKS</span></span>
