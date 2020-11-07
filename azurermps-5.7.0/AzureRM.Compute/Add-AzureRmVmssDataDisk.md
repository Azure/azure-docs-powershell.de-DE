---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
ms.openlocfilehash: e2eca141678c5455df0e443c155693c3c1445e19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663077"
---
# <span data-ttu-id="18792-101">Add-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="18792-101">Add-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="18792-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="18792-102">SYNOPSIS</span></span>
<span data-ttu-id="18792-103">Fügt einen Datenträger zum VMSS hinzu.</span><span class="sxs-lookup"><span data-stu-id="18792-103">Adds a data disk to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18792-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="18792-104">SYNTAX</span></span>

```
Add-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-CreateOption <DiskCreateOptionTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <StorageAccountTypes>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18792-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18792-105">DESCRIPTION</span></span>
<span data-ttu-id="18792-106">Mit dem Cmdlet **Add-AzureRmVmssDataDisk** wird der VMSS-Instanz (Virtual Machine Scale Sets) ein Daten Datenträger hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="18792-106">The **Add-AzureRmVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="18792-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="18792-107">EXAMPLES</span></span>

### <span data-ttu-id="18792-108">Beispiel 1: Hinzufügen eines Daten Datenträgers</span><span class="sxs-lookup"><span data-stu-id="18792-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="18792-109">Dieser Befehl fügt dem VMSS-Objekt einen leeren Datenträger hinzu.</span><span class="sxs-lookup"><span data-stu-id="18792-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="18792-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="18792-110">PARAMETERS</span></span>

### <span data-ttu-id="18792-111">-Caching</span><span class="sxs-lookup"><span data-stu-id="18792-111">-Caching</span></span>
<span data-ttu-id="18792-112">Gibt den zwischen Speichertyp des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="18792-112">Specifies the caching type of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18792-113">-Createoption</span><span class="sxs-lookup"><span data-stu-id="18792-113">-CreateOption</span></span>
<span data-ttu-id="18792-114">Gibt die CREATE-Option des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="18792-114">Specifies the create option of the disk.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18792-115">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="18792-115">-DiskSizeGB</span></span>
<span data-ttu-id="18792-116">Gibt die Größe des Datenträgers in GB an.</span><span class="sxs-lookup"><span data-stu-id="18792-116">Specifies the size of the disk in GB.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18792-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="18792-117">-Lun</span></span>
<span data-ttu-id="18792-118">Gibt die logische Einheitsnummer des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="18792-118">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18792-119">-Name</span><span class="sxs-lookup"><span data-stu-id="18792-119">-Name</span></span>
<span data-ttu-id="18792-120">Gibt den Namen des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="18792-120">Specifies the name of the disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18792-121">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="18792-121">-StorageAccountType</span></span>
<span data-ttu-id="18792-122">Gibt den Speicher Kontotyp des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="18792-122">Specifies the storage account type of the disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18792-123">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="18792-123">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="18792-124">Geben Sie das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="18792-124">Specify the VMSS object.</span></span>
<span data-ttu-id="18792-125">Sie können das Cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="18792-125">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="18792-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="18792-126">-Confirm</span></span>
<span data-ttu-id="18792-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="18792-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18792-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18792-128">-WhatIf</span></span>
<span data-ttu-id="18792-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="18792-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18792-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="18792-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18792-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18792-131">CommonParameters</span></span>
<span data-ttu-id="18792-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18792-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18792-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18792-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18792-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="18792-134">INPUTS</span></span>

### <span data-ttu-id="18792-135">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="18792-135">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="18792-136">System. String System. Int32-System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. Azure. Management. Compute. Models. DiskCreateOptionTypes, Microsoft. Azure. Management. COMPUTE, Version = 14.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]] System. Nullable `1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable` 1 [[Microsoft. Azure. Management. Compute. Models. StorageAccountTypes, Microsoft. Azure. Management. COMPUTE, Version = 14.0.0.0, Kultur = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="18792-136">System.String System.Int32 System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="18792-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="18792-137">OUTPUTS</span></span>

### <span data-ttu-id="18792-138">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="18792-138">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="18792-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="18792-139">NOTES</span></span>

## <span data-ttu-id="18792-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="18792-140">RELATED LINKS</span></span>
