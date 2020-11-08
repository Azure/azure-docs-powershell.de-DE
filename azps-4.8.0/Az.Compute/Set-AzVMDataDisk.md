---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDataDisk.md
ms.openlocfilehash: d9c30c1a64888484eaa533056bf710c59e381031
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008601"
---
# <span data-ttu-id="c8b77-101">Set-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="c8b77-101">Set-AzVMDataDisk</span></span>

## <span data-ttu-id="c8b77-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c8b77-102">SYNOPSIS</span></span>
<span data-ttu-id="c8b77-103">Ändert die Eigenschaften eines Daten Datenträgers einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="c8b77-103">Modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="c8b77-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8b77-104">SYNTAX</span></span>

### <span data-ttu-id="c8b77-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="c8b77-105">ChangeWithName</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8b77-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="c8b77-106">ChangeWithLun</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>]
 [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8b77-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8b77-107">DESCRIPTION</span></span>
<span data-ttu-id="c8b77-108">Das Cmdlet " **Satz-AzVMDataDisk** " ändert die Eigenschaften eines Datenträgers einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="c8b77-108">The **Set-AzVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="c8b77-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c8b77-109">EXAMPLES</span></span>

### <span data-ttu-id="c8b77-110">Beispiel 1: Ändern des Cachemodus eines Datenlaufwerks</span><span class="sxs-lookup"><span data-stu-id="c8b77-110">Example 1: Modify the caching mode of a data disk</span></span>
```powershell
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzVM
```

<span data-ttu-id="c8b77-111">Der erste Befehl ruft den virtuellen Computer mit dem Namen ContosoVM07 mithilfe von **Get-AzVM**.</span><span class="sxs-lookup"><span data-stu-id="c8b77-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="c8b77-112">Der Befehl speichert Sie in der $VM-Variablen.</span><span class="sxs-lookup"><span data-stu-id="c8b77-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="c8b77-113">Der zweite Befehl ändert den Zwischenspeicherungsmodus für den Datenträger mit dem Namen DataDisk01 auf dem virtuellen Computer in $VM.</span><span class="sxs-lookup"><span data-stu-id="c8b77-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="c8b77-114">Der Befehl übergibt das Ergebnis an das Update-AzVM-Cmdlet, das Ihre Änderungen implementiert.</span><span class="sxs-lookup"><span data-stu-id="c8b77-114">The command passes the result to the Update-AzVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="c8b77-115">Eine Änderung des Einzahlungs Modus bewirkt, dass der virtuelle Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="c8b77-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

### <span data-ttu-id="c8b77-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c8b77-116">Example 2</span></span>

<span data-ttu-id="c8b77-117">Ändert die Eigenschaften eines Daten Datenträgers einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="c8b77-117">Modifies properties of a virtual machine data disk.</span></span> <span data-ttu-id="c8b77-118">automatisch</span><span class="sxs-lookup"><span data-stu-id="c8b77-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzVMDataDisk -Caching None -Lun 1 -VM <PSVirtualMachine>
```

## <span data-ttu-id="c8b77-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8b77-119">PARAMETERS</span></span>

### <span data-ttu-id="c8b77-120">-Caching</span><span class="sxs-lookup"><span data-stu-id="c8b77-120">-Caching</span></span>
<span data-ttu-id="c8b77-121">Gibt den Zwischenspeichermodus des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="c8b77-121">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="c8b77-122">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c8b77-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c8b77-123">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="c8b77-123">ReadOnly</span></span>
- <span data-ttu-id="c8b77-124">ReadWrite der Standardwert ist ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="c8b77-124">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="c8b77-125">Wenn Sie diesen Wert ändern, wird der virtuelle Computer neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="c8b77-125">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="c8b77-126">Diese Einstellung wirkt sich auf die Konsistenz und Leistung des Datenträgers aus.</span><span class="sxs-lookup"><span data-stu-id="c8b77-126">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8b77-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8b77-127">-DefaultProfile</span></span>
<span data-ttu-id="c8b77-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c8b77-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8b77-129">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="c8b77-129">-DiskEncryptionSetId</span></span>
<span data-ttu-id="c8b77-130">Gibt die Ressourcen-ID des vom Kunden verwalteten Datenträger Verschlüsselungs Satzes an.</span><span class="sxs-lookup"><span data-stu-id="c8b77-130">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="c8b77-131">Dies kann nur für verwalteten Datenträger angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c8b77-131">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="c8b77-132">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="c8b77-132">-DiskSizeInGB</span></span>
<span data-ttu-id="c8b77-133">Gibt die Größe für den Datenträger in Gigabyte an.</span><span class="sxs-lookup"><span data-stu-id="c8b77-133">Specifies the size, in gigabytes, for the data disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8b77-134">-LUN</span><span class="sxs-lookup"><span data-stu-id="c8b77-134">-Lun</span></span>
<span data-ttu-id="c8b77-135">Gibt die logische Einheitsnummer (LUN) des Daten Datenträgers an, der von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="c8b77-135">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ChangeWithLun
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8b77-136">-Name</span><span class="sxs-lookup"><span data-stu-id="c8b77-136">-Name</span></span>
<span data-ttu-id="c8b77-137">Gibt den Namen des Daten Datenträgers an, der von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="c8b77-137">Specifies the name of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ChangeWithName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8b77-138">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="c8b77-138">-StorageAccountType</span></span>
<span data-ttu-id="c8b77-139">Der Kontotyp des verwalteten Datenträgers des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="c8b77-139">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="c8b77-140">-VM</span><span class="sxs-lookup"><span data-stu-id="c8b77-140">-VM</span></span>
<span data-ttu-id="c8b77-141">Gibt den virtuellen Computer an, für den das Cmdlet einen Datenträger ändert.</span><span class="sxs-lookup"><span data-stu-id="c8b77-141">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="c8b77-142">Verwenden Sie das Get-AzVM-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c8b77-142">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8b77-143">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="c8b77-143">-WriteAccelerator</span></span>
<span data-ttu-id="c8b77-144">Gibt an, ob WriteAccelerator auf dem Datenträger aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8b77-144">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="c8b77-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8b77-145">CommonParameters</span></span>
<span data-ttu-id="c8b77-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8b77-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8b77-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8b77-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8b77-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c8b77-148">INPUTS</span></span>

### <span data-ttu-id="c8b77-149">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c8b77-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="c8b77-150">System. String</span><span class="sxs-lookup"><span data-stu-id="c8b77-150">System.String</span></span>

### <span data-ttu-id="c8b77-151">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c8b77-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c8b77-152">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. CachingTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="c8b77-152">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="c8b77-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c8b77-153">OUTPUTS</span></span>

### <span data-ttu-id="c8b77-154">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c8b77-154">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="c8b77-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="c8b77-155">NOTES</span></span>

## <span data-ttu-id="c8b77-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c8b77-156">RELATED LINKS</span></span>

[<span data-ttu-id="c8b77-157">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="c8b77-157">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="c8b77-158">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="c8b77-158">Update-AzVM</span></span>](./Update-AzVM.md)


