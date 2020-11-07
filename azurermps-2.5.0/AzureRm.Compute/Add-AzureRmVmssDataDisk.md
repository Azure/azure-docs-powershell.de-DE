---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssdatadisk
schema: 2.0.0
ms.openlocfilehash: c91b9dc68bcc0cdecda9ced83a9b3c64452d6413
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848940"
---
# <span data-ttu-id="69159-101">Add-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="69159-101">Add-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="69159-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="69159-102">SYNOPSIS</span></span>
<span data-ttu-id="69159-103">Fügt einen Datenträger zum VMSS hinzu.</span><span class="sxs-lookup"><span data-stu-id="69159-103">Adds a data disk to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69159-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="69159-104">SYNTAX</span></span>

```
Add-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Lun] <Int32>] [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <DiskCreateOptionTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <StorageAccountTypes>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69159-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="69159-105">DESCRIPTION</span></span>
<span data-ttu-id="69159-106">Mit dem Cmdlet **Add-AzureRmVmssDataDisk** wird der VMSS-Instanz (Virtual Machine Scale Sets) ein Daten Datenträger hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="69159-106">The **Add-AzureRmVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="69159-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="69159-107">EXAMPLES</span></span>

### <span data-ttu-id="69159-108">Beispiel 1: Hinzufügen eines Daten Datenträgers</span><span class="sxs-lookup"><span data-stu-id="69159-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="69159-109">Dieser Befehl fügt dem VMSS-Objekt einen leeren Datenträger hinzu.</span><span class="sxs-lookup"><span data-stu-id="69159-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="69159-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="69159-110">PARAMETERS</span></span>

### <span data-ttu-id="69159-111">-Caching</span><span class="sxs-lookup"><span data-stu-id="69159-111">-Caching</span></span>
<span data-ttu-id="69159-112">Gibt den zwischen Speichertyp des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="69159-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="69159-113">-Createoption</span><span class="sxs-lookup"><span data-stu-id="69159-113">-CreateOption</span></span>
<span data-ttu-id="69159-114">Gibt die CREATE-Option des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="69159-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="69159-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69159-115">-DefaultProfile</span></span>
<span data-ttu-id="69159-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="69159-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69159-117">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="69159-117">-DiskSizeGB</span></span>
<span data-ttu-id="69159-118">Gibt die Größe des Datenträgers in GB an.</span><span class="sxs-lookup"><span data-stu-id="69159-118">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="69159-119">-LUN</span><span class="sxs-lookup"><span data-stu-id="69159-119">-Lun</span></span>
<span data-ttu-id="69159-120">Gibt die logische Einheitsnummer des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="69159-120">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="69159-121">-Name</span><span class="sxs-lookup"><span data-stu-id="69159-121">-Name</span></span>
<span data-ttu-id="69159-122">Gibt den Namen des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="69159-122">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="69159-123">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="69159-123">-StorageAccountType</span></span>
<span data-ttu-id="69159-124">Gibt den Speicher Kontotyp des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="69159-124">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="69159-125">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="69159-125">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="69159-126">Geben Sie das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="69159-126">Specify the VMSS object.</span></span>
<span data-ttu-id="69159-127">Sie können das Cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="69159-127">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69159-128">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="69159-128">-WriteAccelerator</span></span>
<span data-ttu-id="69159-129">Gibt an, ob WriteAccelerator auf dem Datenträger aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="69159-129">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69159-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="69159-130">-Confirm</span></span>
<span data-ttu-id="69159-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="69159-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69159-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69159-132">-WhatIf</span></span>
<span data-ttu-id="69159-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="69159-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69159-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="69159-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69159-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69159-135">CommonParameters</span></span>
<span data-ttu-id="69159-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69159-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69159-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69159-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69159-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="69159-138">INPUTS</span></span>

### <span data-ttu-id="69159-139">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="69159-139">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="69159-140">System. String System. Int32-System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. Azure. Management. Compute. Models. DiskCreateOptionTypes, Microsoft. Azure. Management. COMPUTE, Version = 14.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]] System. Nullable `1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable` 1 [[Microsoft. Azure. Management. Compute. Models. StorageAccountTypes, Microsoft. Azure. Management. COMPUTE, Version = 14.0.0.0, Kultur = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="69159-140">System.String System.Int32 System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="69159-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="69159-141">OUTPUTS</span></span>

### <span data-ttu-id="69159-142">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="69159-142">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="69159-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="69159-143">NOTES</span></span>

## <span data-ttu-id="69159-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="69159-144">RELATED LINKS</span></span>

