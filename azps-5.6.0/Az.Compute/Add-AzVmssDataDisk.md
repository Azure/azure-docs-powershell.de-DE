---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
ms.openlocfilehash: ec16e946907e7d2815997cbcfb9cbf1563805039
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930355"
---
# <span data-ttu-id="15e3c-101">Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="15e3c-101">Add-AzVmssDataDisk</span></span>

## <span data-ttu-id="15e3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15e3c-102">SYNOPSIS</span></span>
<span data-ttu-id="15e3c-103">Fügt dem VMSS einen Datenträger hinzu.</span><span class="sxs-lookup"><span data-stu-id="15e3c-103">Adds a data disk to the VMSS.</span></span>

## <span data-ttu-id="15e3c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15e3c-104">SYNTAX</span></span>

```
Add-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <String>] [-DiskSizeGB <Int32>]
 [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="15e3c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="15e3c-105">DESCRIPTION</span></span>
<span data-ttu-id="15e3c-106">Das **Add-AzVmssDataDisk-Cmdlet** fügt der VmSS-Instanz (Virtual Machine Scale Set) einen Datenträger hinzu.</span><span class="sxs-lookup"><span data-stu-id="15e3c-106">The **Add-AzVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="15e3c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="15e3c-107">EXAMPLES</span></span>

### <span data-ttu-id="15e3c-108">Beispiel 1: Hinzufügen eines Datenträgers</span><span class="sxs-lookup"><span data-stu-id="15e3c-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="15e3c-109">Mit diesem Befehl wird dem VMSS-Objekt ein leerer Datenträger hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="15e3c-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="15e3c-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="15e3c-110">PARAMETERS</span></span>

### <span data-ttu-id="15e3c-111">-Zwischenspeichern</span><span class="sxs-lookup"><span data-stu-id="15e3c-111">-Caching</span></span>
<span data-ttu-id="15e3c-112">Gibt den Zwischenspeichertyp des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="15e3c-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="15e3c-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="15e3c-113">-CreateOption</span></span>
<span data-ttu-id="15e3c-114">Gibt die Erstellungsoption des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="15e3c-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="15e3c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15e3c-115">-DefaultProfile</span></span>
<span data-ttu-id="15e3c-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="15e3c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15e3c-117">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="15e3c-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="15e3c-118">Gibt die Ressourcen-ID des vom Kunden verwalteten Datenträgerverschlüsselungssatzs an.</span><span class="sxs-lookup"><span data-stu-id="15e3c-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="15e3c-119">Dies kann nur für verwaltete Datenträger angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="15e3c-119">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="15e3c-120">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="15e3c-120">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="15e3c-121">Gibt die Read-Write IOPS für den verwalteten Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="15e3c-121">Specifies the Read-Write IOPS for the managed disk.</span></span> <span data-ttu-id="15e3c-122">Sollte nur verwendet werden, wenn StorageAccountType UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="15e3c-122">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="15e3c-123">Wenn nicht angegeben, wird ein Standardwert basierend auf diskSizeGB zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="15e3c-123">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e3c-124">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="15e3c-124">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="15e3c-125">Gibt die Bandbreite in MB pro Sekunde für den verwalteten Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="15e3c-125">Specifies the bandwidth in MB per second for the managed disk.</span></span> <span data-ttu-id="15e3c-126">Sollte nur verwendet werden, wenn StorageAccountType UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="15e3c-126">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="15e3c-127">Wenn nicht angegeben, wird ein Standardwert basierend auf diskSizeGB zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="15e3c-127">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e3c-128">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="15e3c-128">-DiskSizeGB</span></span>
<span data-ttu-id="15e3c-129">Gibt die Größe des Datenträgers in GB an.</span><span class="sxs-lookup"><span data-stu-id="15e3c-129">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="15e3c-130">-Lun</span><span class="sxs-lookup"><span data-stu-id="15e3c-130">-Lun</span></span>
<span data-ttu-id="15e3c-131">Gibt die logische Einheitennummer des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="15e3c-131">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="15e3c-132">-Name</span><span class="sxs-lookup"><span data-stu-id="15e3c-132">-Name</span></span>
<span data-ttu-id="15e3c-133">Gibt den Namen des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="15e3c-133">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="15e3c-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="15e3c-134">-StorageAccountType</span></span>
<span data-ttu-id="15e3c-135">Gibt den Speicherkontotyp des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="15e3c-135">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="15e3c-136">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="15e3c-136">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="15e3c-137">Geben Sie das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="15e3c-137">Specify the VMSS object.</span></span>
<span data-ttu-id="15e3c-138">Sie können das [Cmdlet New-AzVmssConfig](./New-AzVmssConfig.md) verwenden, um das -Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="15e3c-138">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="15e3c-139">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="15e3c-139">-WriteAccelerator</span></span>
<span data-ttu-id="15e3c-140">Gibt an, ob WriteAccelerator auf dem Datenträger aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="15e3c-140">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="15e3c-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="15e3c-141">-Confirm</span></span>
<span data-ttu-id="15e3c-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="15e3c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15e3c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15e3c-143">-WhatIf</span></span>
<span data-ttu-id="15e3c-144">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15e3c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15e3c-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="15e3c-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15e3c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15e3c-146">CommonParameters</span></span>
<span data-ttu-id="15e3c-147">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15e3c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15e3c-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15e3c-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15e3c-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="15e3c-149">INPUTS</span></span>

### <span data-ttu-id="15e3c-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="15e3c-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="15e3c-151">System.String</span><span class="sxs-lookup"><span data-stu-id="15e3c-151">System.String</span></span>

### <span data-ttu-id="15e3c-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="15e3c-152">System.Int32</span></span>

### <span data-ttu-id="15e3c-153">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="15e3c-153">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="15e3c-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="15e3c-154">OUTPUTS</span></span>

### <span data-ttu-id="15e3c-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="15e3c-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="15e3c-156">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="15e3c-156">NOTES</span></span>

## <span data-ttu-id="15e3c-157">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="15e3c-157">RELATED LINKS</span></span>
