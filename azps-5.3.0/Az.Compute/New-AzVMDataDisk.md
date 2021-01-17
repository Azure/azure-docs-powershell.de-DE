---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
ms.openlocfilehash: 4eefa5a0a22b3db0e7ab10085729e1040dbd4e71
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473061"
---
# <span data-ttu-id="b7154-101">New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="b7154-101">New-AzVMDataDisk</span></span>

## <span data-ttu-id="b7154-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7154-102">SYNOPSIS</span></span>
<span data-ttu-id="b7154-103">Erstellt ein lokales Datendatenträgerobjekt für einen virtuellen Computer oder eine Vmss VM.</span><span class="sxs-lookup"><span data-stu-id="b7154-103">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="b7154-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b7154-104">SYNTAX</span></span>

### <span data-ttu-id="b7154-105">NormalDiskParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b7154-105">NormalDiskParameterSetName (Default)</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-VhdUri <String>] [-SourceImageUri <String>] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7154-106">ManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b7154-106">ManagedDiskParameterSetName</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7154-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b7154-107">DESCRIPTION</span></span>
<span data-ttu-id="b7154-108">Das **Cmdlet "New-AzVMDataDisk"** erstellt ein lokales Datenspeicherobjekt für einen virtuellen Computer oder eine Vmss VM.</span><span class="sxs-lookup"><span data-stu-id="b7154-108">The **New-AzVMDataDisk** cmdlet creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="b7154-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b7154-109">EXAMPLES</span></span>

### <span data-ttu-id="b7154-110">Beispiel 1: Hinzufügen eines verwalteten Datenspeichers zu einer Vmss VM.</span><span class="sxs-lookup"><span data-stu-id="b7154-110">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="b7154-111">Der erste Befehl ruft einen vorhandenen verwalteten Datenträger ab.</span><span class="sxs-lookup"><span data-stu-id="b7154-111">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="b7154-112">Der nächste Befehl erstellt ein Datenträgerobjekt mit dem verwalteten Datenträger.</span><span class="sxs-lookup"><span data-stu-id="b7154-112">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="b7154-113">Der nächste Befehl ruft eine vorhandene Vmss VM ab, die durch den Namen der Ressourcengruppe, den Namen der vmss und die Instanz-ID angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b7154-113">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="b7154-114">Der letzte Befehl aktualisiert die Vmss VM, indem ein neuer Datenträger hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="b7154-114">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="b7154-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b7154-115">Example 2</span></span>

<span data-ttu-id="b7154-116">Erstellt ein lokales Datendatenträgerobjekt für einen virtuellen Computer oder eine Vmss VM.</span><span class="sxs-lookup"><span data-stu-id="b7154-116">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span> <span data-ttu-id="b7154-117">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="b7154-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzVMDataDisk -Caching None -CreateOption Attach -DiskSizeInGB 1 -Lun 2 -Name 'AgentPool01'
```

## <span data-ttu-id="b7154-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7154-118">PARAMETERS</span></span>

### <span data-ttu-id="b7154-119">-Zwischenspeichern</span><span class="sxs-lookup"><span data-stu-id="b7154-119">-Caching</span></span>
<span data-ttu-id="b7154-120">Zwischenspeicherung des Virtuellen Computerdatenträgers.</span><span class="sxs-lookup"><span data-stu-id="b7154-120">The virtual machine data disk's caching.</span></span>

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

### <span data-ttu-id="b7154-121">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="b7154-121">-CreateOption</span></span>
<span data-ttu-id="b7154-122">Die Erstellungsoption des Virtuellen Computerdatenträgers.</span><span class="sxs-lookup"><span data-stu-id="b7154-122">The virtual machine data disk's create option.</span></span>

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

### <span data-ttu-id="b7154-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7154-123">-DefaultProfile</span></span>
<span data-ttu-id="b7154-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b7154-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7154-125">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="b7154-125">-DiskEncryptionSetId</span></span>
<span data-ttu-id="b7154-126">Id des verwalteten Verschlüsselungssatzs des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="b7154-126">The virtual machine managed disk encryption set's Id.</span></span>

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

### <span data-ttu-id="b7154-127">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="b7154-127">-DiskSizeInGB</span></span>
<span data-ttu-id="b7154-128">Die Größe des Datenträgers des virtuellen Computers in GB.</span><span class="sxs-lookup"><span data-stu-id="b7154-128">The virtual machine data disk's size in GB.</span></span>

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

### <span data-ttu-id="b7154-129">-Lun</span><span class="sxs-lookup"><span data-stu-id="b7154-129">-Lun</span></span>
<span data-ttu-id="b7154-130">Der Lun des Virtuellen Computerdatenträgers.</span><span class="sxs-lookup"><span data-stu-id="b7154-130">The virtual machine data disk's Lun.</span></span>

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

### <span data-ttu-id="b7154-131">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="b7154-131">-ManagedDiskId</span></span>
<span data-ttu-id="b7154-132">Die ID des virtuellen Computers, auf dem der Datenträger verwaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="b7154-132">The virtual machine managed disk's Id.</span></span>

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

### <span data-ttu-id="b7154-133">-Name</span><span class="sxs-lookup"><span data-stu-id="b7154-133">-Name</span></span>
<span data-ttu-id="b7154-134">Der Name des Virtuellen Computerdatenträgers.</span><span class="sxs-lookup"><span data-stu-id="b7154-134">The virtual machine data disk's name.</span></span>

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

### <span data-ttu-id="b7154-135">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="b7154-135">-SourceImageUri</span></span>
<span data-ttu-id="b7154-136">Der Quellbild-URI des Betriebssystemdatenträgers des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="b7154-136">The virtual machine OS disk's source image Uri.</span></span>

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

### <span data-ttu-id="b7154-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="b7154-137">-StorageAccountType</span></span>
<span data-ttu-id="b7154-138">Der Kontotyp des verwalteten virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="b7154-138">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="b7154-139">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="b7154-139">-VhdUri</span></span>
<span data-ttu-id="b7154-140">Der Vhd-URI des virtuellen Computerdatenträgers.</span><span class="sxs-lookup"><span data-stu-id="b7154-140">The virtual machine data disk's Vhd Uri.</span></span>

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

### <span data-ttu-id="b7154-141">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="b7154-141">-WriteAccelerator</span></span>
<span data-ttu-id="b7154-142">Gibt an, ob WriteAccelerator auf einem verwalteten Datenträger aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b7154-142">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="b7154-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7154-143">CommonParameters</span></span>
<span data-ttu-id="b7154-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7154-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7154-145">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7154-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7154-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b7154-146">INPUTS</span></span>

### <span data-ttu-id="b7154-147">System.Int32</span><span class="sxs-lookup"><span data-stu-id="b7154-147">System.Int32</span></span>

### <span data-ttu-id="b7154-148">System.String</span><span class="sxs-lookup"><span data-stu-id="b7154-148">System.String</span></span>

### <span data-ttu-id="b7154-149">Microsoft.Azure.Management.Compute.Models.CachingTypes</span><span class="sxs-lookup"><span data-stu-id="b7154-149">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="b7154-150">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b7154-150">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b7154-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b7154-151">OUTPUTS</span></span>

### <span data-ttu-id="b7154-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk</span><span class="sxs-lookup"><span data-stu-id="b7154-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk</span></span>

## <span data-ttu-id="b7154-153">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b7154-153">NOTES</span></span>

## <span data-ttu-id="b7154-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b7154-154">RELATED LINKS</span></span>
