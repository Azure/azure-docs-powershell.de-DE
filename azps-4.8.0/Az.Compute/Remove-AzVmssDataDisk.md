---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
ms.openlocfilehash: 908405de847526682d8526ef2e576e6a07893c3a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173307"
---
# <span data-ttu-id="17f1d-101">Remove-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="17f1d-101">Remove-AzVmssDataDisk</span></span>

## <span data-ttu-id="17f1d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="17f1d-102">SYNOPSIS</span></span>
<span data-ttu-id="17f1d-103">Entfernt einen Datenträger aus dem VMSS.</span><span class="sxs-lookup"><span data-stu-id="17f1d-103">Removes a data disk from the VMSS.</span></span>

## <span data-ttu-id="17f1d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="17f1d-104">SYNTAX</span></span>

### <span data-ttu-id="17f1d-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="17f1d-105">NameParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17f1d-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="17f1d-106">LunParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17f1d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17f1d-107">DESCRIPTION</span></span>
<span data-ttu-id="17f1d-108">Das Cmdlet **Remove-AzVmssDataDisk** entfernt einen Datenträger aus der Instanz des virtuellen Computer-Skalierungs Satzes (VMSS).</span><span class="sxs-lookup"><span data-stu-id="17f1d-108">The **Remove-AzVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="17f1d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="17f1d-109">EXAMPLES</span></span>

### <span data-ttu-id="17f1d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="17f1d-110">Example 1</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="17f1d-111">Dieser Befehl entfernt den Datenträger mit dem Namen "DataDisk1" aus dem VMSS-Objekt.</span><span class="sxs-lookup"><span data-stu-id="17f1d-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="17f1d-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="17f1d-112">Example 2</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="17f1d-113">Mit diesem Befehl wird der Daten Datenträger von LUN 0 aus dem VMSS-Objekt entfernt.</span><span class="sxs-lookup"><span data-stu-id="17f1d-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="17f1d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="17f1d-114">PARAMETERS</span></span>

### <span data-ttu-id="17f1d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17f1d-115">-DefaultProfile</span></span>
<span data-ttu-id="17f1d-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="17f1d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17f1d-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="17f1d-117">-Lun</span></span>
<span data-ttu-id="17f1d-118">Gibt die logische Einheitsnummer des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="17f1d-118">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="17f1d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="17f1d-119">-Name</span></span>
<span data-ttu-id="17f1d-120">Gibt den Namen des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="17f1d-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="17f1d-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="17f1d-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="17f1d-122">Geben Sie das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="17f1d-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="17f1d-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="17f1d-123">-Confirm</span></span>
<span data-ttu-id="17f1d-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="17f1d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17f1d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17f1d-125">-WhatIf</span></span>
<span data-ttu-id="17f1d-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="17f1d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17f1d-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="17f1d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17f1d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17f1d-128">CommonParameters</span></span>
<span data-ttu-id="17f1d-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17f1d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17f1d-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17f1d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17f1d-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="17f1d-131">INPUTS</span></span>

### <span data-ttu-id="17f1d-132">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="17f1d-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="17f1d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="17f1d-133">System.String</span></span>

### <span data-ttu-id="17f1d-134">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="17f1d-134">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="17f1d-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="17f1d-135">OUTPUTS</span></span>

### <span data-ttu-id="17f1d-136">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="17f1d-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="17f1d-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="17f1d-137">NOTES</span></span>

## <span data-ttu-id="17f1d-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="17f1d-138">RELATED LINKS</span></span>
