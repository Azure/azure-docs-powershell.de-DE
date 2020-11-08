---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
ms.openlocfilehash: 7f67b8b6ff287a98fc505cb63c3a6eda90f46ef7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996144"
---
# <span data-ttu-id="97de3-101">New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="97de3-101">New-AzVMDataDisk</span></span>

## <span data-ttu-id="97de3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="97de3-102">SYNOPSIS</span></span>
<span data-ttu-id="97de3-103">Erstellt ein lokales Daten Festplatten Objekt für einen virtuellen Computer oder einen VMSS-VM.</span><span class="sxs-lookup"><span data-stu-id="97de3-103">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="97de3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="97de3-104">SYNTAX</span></span>

### <span data-ttu-id="97de3-105">NormalDiskParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="97de3-105">NormalDiskParameterSetName (Default)</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-VhdUri <String>] [-SourceImageUri <String>] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97de3-106">ManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="97de3-106">ManagedDiskParameterSetName</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="97de3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97de3-107">DESCRIPTION</span></span>
<span data-ttu-id="97de3-108">Mit dem Cmdlet **New-AzVMDataDisk** wird ein lokales Daten Festplatten Objekt für einen virtuellen Computer oder einen VMSS-VM erstellt.</span><span class="sxs-lookup"><span data-stu-id="97de3-108">The **New-AzVMDataDisk** cmdlet creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="97de3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="97de3-109">EXAMPLES</span></span>

### <span data-ttu-id="97de3-110">Beispiel 1: Hinzufügen eines verwalteten Daten Datenträgers zu einer VMSS-VM</span><span class="sxs-lookup"><span data-stu-id="97de3-110">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="97de3-111">Der erste Befehl ruft einen vorhandenen verwalteten Datenträger ab.</span><span class="sxs-lookup"><span data-stu-id="97de3-111">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="97de3-112">Mit dem nächsten Befehl wird ein Datenträgerobjekt mit dem verwalteten Datenträger erstellt.</span><span class="sxs-lookup"><span data-stu-id="97de3-112">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="97de3-113">Der nächste Befehl ruft eine vorhandene VMSS-VM ab, die durch den Ressourcengruppennamen, den VMSS-Namen und die Instanz-ID angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="97de3-113">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="97de3-114">Der endgültige Befehl aktualisiert die VMSS-VM durch Hinzufügen eines neuen Daten Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="97de3-114">The final command updates the Vmss VM by adding a new data disk.</span></span>

## <span data-ttu-id="97de3-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="97de3-115">PARAMETERS</span></span>

### <span data-ttu-id="97de3-116">-Caching</span><span class="sxs-lookup"><span data-stu-id="97de3-116">-Caching</span></span>
<span data-ttu-id="97de3-117">Zwischenspeicherung des Daten Datenträgers der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="97de3-117">The virtual machine data disk's caching.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97de3-118">-Createoption</span><span class="sxs-lookup"><span data-stu-id="97de3-118">-CreateOption</span></span>
<span data-ttu-id="97de3-119">Die CREATE-Option des Virtual Machine-Daten Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="97de3-119">The virtual machine data disk's create option.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97de3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97de3-120">-DefaultProfile</span></span>
<span data-ttu-id="97de3-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="97de3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97de3-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="97de3-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="97de3-123">Die ID des vom virtuellen Computer verwalteten Datenträger Verschlüsselungs Satzes.</span><span class="sxs-lookup"><span data-stu-id="97de3-123">The virtual machine managed disk encryption set's Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97de3-124">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="97de3-124">-DiskSizeInGB</span></span>
<span data-ttu-id="97de3-125">Die Größe des Daten Datenträgers des virtuellen Computers in GB.</span><span class="sxs-lookup"><span data-stu-id="97de3-125">The virtual machine data disk's size in GB.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97de3-126">-LUN</span><span class="sxs-lookup"><span data-stu-id="97de3-126">-Lun</span></span>
<span data-ttu-id="97de3-127">Die LUN des Daten Datenträgers des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="97de3-127">The virtual machine data disk's Lun.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97de3-128">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="97de3-128">-ManagedDiskId</span></span>
<span data-ttu-id="97de3-129">Die ID des vom virtuellen Computer verwalteten Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="97de3-129">The virtual machine managed disk's Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97de3-130">-Name</span><span class="sxs-lookup"><span data-stu-id="97de3-130">-Name</span></span>
<span data-ttu-id="97de3-131">Der Name des Daten Datenträgers der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="97de3-131">The virtual machine data disk's name.</span></span>

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

### <span data-ttu-id="97de3-132">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="97de3-132">-SourceImageUri</span></span>
<span data-ttu-id="97de3-133">Der URI des Quellbilds des virtuellen Computers auf dem Betriebssystemdatenträger.</span><span class="sxs-lookup"><span data-stu-id="97de3-133">The virtual machine OS disk's source image Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalDiskParameterSetName
Aliases: SourceImage

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97de3-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="97de3-134">-StorageAccountType</span></span>
<span data-ttu-id="97de3-135">Der Kontotyp des verwalteten Datenträgers des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="97de3-135">The virtual machine managed disk's account type.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97de3-136">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="97de3-136">-VhdUri</span></span>
<span data-ttu-id="97de3-137">Der VHD-URI des Datenlaufwerks des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="97de3-137">The virtual machine data disk's Vhd Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97de3-138">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="97de3-138">-WriteAccelerator</span></span>
<span data-ttu-id="97de3-139">Gibt an, ob WriteAccelerator auf einem verwalteten Daten Datenträger aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="97de3-139">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97de3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97de3-140">CommonParameters</span></span>
<span data-ttu-id="97de3-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97de3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97de3-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97de3-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97de3-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="97de3-143">INPUTS</span></span>

### <span data-ttu-id="97de3-144">System. Int32</span><span class="sxs-lookup"><span data-stu-id="97de3-144">System.Int32</span></span>

### <span data-ttu-id="97de3-145">System. String</span><span class="sxs-lookup"><span data-stu-id="97de3-145">System.String</span></span>

### <span data-ttu-id="97de3-146">Microsoft. Azure. Management. Compute. Models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="97de3-146">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="97de3-147">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="97de3-147">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="97de3-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="97de3-148">OUTPUTS</span></span>

### <span data-ttu-id="97de3-149">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineDataDisk</span><span class="sxs-lookup"><span data-stu-id="97de3-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk</span></span>

## <span data-ttu-id="97de3-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="97de3-150">NOTES</span></span>

## <span data-ttu-id="97de3-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="97de3-151">RELATED LINKS</span></span>
