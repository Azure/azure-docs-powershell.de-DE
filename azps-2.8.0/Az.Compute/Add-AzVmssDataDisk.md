---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
ms.openlocfilehash: 032c38c3fcc3b09286b795fd3e0efba85e076807
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652215"
---
# <span data-ttu-id="0b91b-101">Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="0b91b-101">Add-AzVmssDataDisk</span></span>

## <span data-ttu-id="0b91b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0b91b-102">SYNOPSIS</span></span>
<span data-ttu-id="0b91b-103">Fügt einen Datenträger zum VMSS hinzu.</span><span class="sxs-lookup"><span data-stu-id="0b91b-103">Adds a data disk to the VMSS.</span></span>

## <span data-ttu-id="0b91b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b91b-104">SYNTAX</span></span>

```
Add-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <String>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b91b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b91b-105">DESCRIPTION</span></span>
<span data-ttu-id="0b91b-106">Mit dem Cmdlet **Add-AzVmssDataDisk** wird der VMSS-Instanz (Virtual Machine Scale Sets) ein Daten Datenträger hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0b91b-106">The **Add-AzVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="0b91b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b91b-107">EXAMPLES</span></span>

### <span data-ttu-id="0b91b-108">Beispiel 1: Hinzufügen eines Daten Datenträgers</span><span class="sxs-lookup"><span data-stu-id="0b91b-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="0b91b-109">Dieser Befehl fügt dem VMSS-Objekt einen leeren Datenträger hinzu.</span><span class="sxs-lookup"><span data-stu-id="0b91b-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="0b91b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b91b-110">PARAMETERS</span></span>

### <span data-ttu-id="0b91b-111">-Caching</span><span class="sxs-lookup"><span data-stu-id="0b91b-111">-Caching</span></span>
<span data-ttu-id="0b91b-112">Gibt den zwischen Speichertyp des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="0b91b-112">Specifies the caching type of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b91b-113">-Createoption</span><span class="sxs-lookup"><span data-stu-id="0b91b-113">-CreateOption</span></span>
<span data-ttu-id="0b91b-114">Gibt die CREATE-Option des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="0b91b-114">Specifies the create option of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b91b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b91b-115">-DefaultProfile</span></span>
<span data-ttu-id="0b91b-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0b91b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b91b-117">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="0b91b-117">-DiskSizeGB</span></span>
<span data-ttu-id="0b91b-118">Gibt die Größe des Datenträgers in GB an.</span><span class="sxs-lookup"><span data-stu-id="0b91b-118">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b91b-119">-LUN</span><span class="sxs-lookup"><span data-stu-id="0b91b-119">-Lun</span></span>
<span data-ttu-id="0b91b-120">Gibt die logische Einheitsnummer des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="0b91b-120">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b91b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0b91b-121">-Name</span></span>
<span data-ttu-id="0b91b-122">Gibt den Namen des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="0b91b-122">Specifies the name of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b91b-123">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="0b91b-123">-StorageAccountType</span></span>
<span data-ttu-id="0b91b-124">Gibt den Speicher Kontotyp des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="0b91b-124">Specifies the storage account type of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b91b-125">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0b91b-125">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="0b91b-126">Geben Sie das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="0b91b-126">Specify the VMSS object.</span></span>
<span data-ttu-id="0b91b-127">Sie können das Cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0b91b-127">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="0b91b-128">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="0b91b-128">-WriteAccelerator</span></span>
<span data-ttu-id="0b91b-129">Gibt an, ob WriteAccelerator auf dem Datenträger aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0b91b-129">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b91b-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0b91b-130">-Confirm</span></span>
<span data-ttu-id="0b91b-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0b91b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b91b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b91b-132">-WhatIf</span></span>
<span data-ttu-id="0b91b-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b91b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b91b-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b91b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b91b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b91b-135">CommonParameters</span></span>
<span data-ttu-id="0b91b-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b91b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b91b-137">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b91b-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b91b-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0b91b-138">INPUTS</span></span>

### <span data-ttu-id="0b91b-139">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0b91b-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="0b91b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0b91b-140">System.String</span></span>

### <span data-ttu-id="0b91b-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="0b91b-141">System.Int32</span></span>

### <span data-ttu-id="0b91b-142">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. CachingTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="0b91b-142">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="0b91b-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0b91b-143">OUTPUTS</span></span>

### <span data-ttu-id="0b91b-144">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0b91b-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="0b91b-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="0b91b-145">NOTES</span></span>

## <span data-ttu-id="0b91b-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0b91b-146">RELATED LINKS</span></span>
