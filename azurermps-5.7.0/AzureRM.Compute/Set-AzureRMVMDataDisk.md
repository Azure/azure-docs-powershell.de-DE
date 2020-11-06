---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
ms.openlocfilehash: 2f961f144bc322cb1b1b12001ed006bc783ed67e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499026"
---
# <span data-ttu-id="083c9-101">Set-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="083c9-101">Set-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="083c9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="083c9-102">SYNOPSIS</span></span>
<span data-ttu-id="083c9-103">Ändert die Eigenschaften eines Daten Datenträgers einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="083c9-103">Modifies properties of a virtual machine data disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="083c9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="083c9-104">SYNTAX</span></span>

### <span data-ttu-id="083c9-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="083c9-105">ChangeWithName</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="083c9-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="083c9-106">ChangeWithLun</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="083c9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="083c9-107">DESCRIPTION</span></span>
<span data-ttu-id="083c9-108">Das Cmdlet " **Satz-AzureRmVMDataDisk** " ändert die Eigenschaften eines Datenträgers einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="083c9-108">The **Set-AzureRmVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="083c9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="083c9-109">EXAMPLES</span></span>

### <span data-ttu-id="083c9-110">Beispiel 1: Ändern des Cachemodus eines Datenlaufwerks</span><span class="sxs-lookup"><span data-stu-id="083c9-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzureRMVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzureRmVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzureRmVM
```

<span data-ttu-id="083c9-111">Der erste Befehl ruft den virtuellen Computer mit dem Namen ContosoVM07 mithilfe von **Get-AzureRmVM**.</span><span class="sxs-lookup"><span data-stu-id="083c9-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="083c9-112">Der Befehl speichert Sie in der $VM-Variablen.</span><span class="sxs-lookup"><span data-stu-id="083c9-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="083c9-113">Der zweite Befehl ändert den Zwischenspeicherungsmodus für den Datenträger mit dem Namen DataDisk01 auf dem virtuellen Computer in $VM.</span><span class="sxs-lookup"><span data-stu-id="083c9-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="083c9-114">Der Befehl übergibt das Ergebnis an das Update-AzureRmVM-Cmdlet, das Ihre Änderungen implementiert.</span><span class="sxs-lookup"><span data-stu-id="083c9-114">The command passes the result to the Update-AzureRmVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="083c9-115">Eine Änderung des Cachemodus bewirkt, dass der virtuelle Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="083c9-115">A change to the caching mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="083c9-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="083c9-116">PARAMETERS</span></span>

### <span data-ttu-id="083c9-117">-Caching</span><span class="sxs-lookup"><span data-stu-id="083c9-117">-Caching</span></span>
<span data-ttu-id="083c9-118">Gibt den Zwischenspeichermodus des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="083c9-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="083c9-119">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="083c9-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="083c9-120">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="083c9-120">ReadOnly</span></span>
- <span data-ttu-id="083c9-121">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="083c9-121">ReadWrite</span></span>

<span data-ttu-id="083c9-122">Der Standardwert ist ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="083c9-122">The default value is ReadWrite.</span></span>
<span data-ttu-id="083c9-123">Wenn Sie diesen Wert ändern, wird der virtuelle Computer neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="083c9-123">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="083c9-124">Diese Einstellung wirkt sich auf die Konsistenz und Leistung des Datenträgers aus.</span><span class="sxs-lookup"><span data-stu-id="083c9-124">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="083c9-125">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="083c9-125">-DiskSizeInGB</span></span>
<span data-ttu-id="083c9-126">Gibt die Größe für den Datenträger in Gigabyte an.</span><span class="sxs-lookup"><span data-stu-id="083c9-126">Specifies the size, in gigabytes, for the data disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="083c9-127">-LUN</span><span class="sxs-lookup"><span data-stu-id="083c9-127">-Lun</span></span>
<span data-ttu-id="083c9-128">Gibt die logische Einheitsnummer (LUN) des Daten Datenträgers an, der von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="083c9-128">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: Int32
Parameter Sets: ChangeWithLun
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="083c9-129">-Name</span><span class="sxs-lookup"><span data-stu-id="083c9-129">-Name</span></span>
<span data-ttu-id="083c9-130">Gibt den Namen des Daten Datenträgers an, der von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="083c9-130">Specifies the name of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: ChangeWithName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="083c9-131">-VM</span><span class="sxs-lookup"><span data-stu-id="083c9-131">-VM</span></span>
<span data-ttu-id="083c9-132">Gibt den virtuellen Computer an, für den das Cmdlet einen Datenträger ändert.</span><span class="sxs-lookup"><span data-stu-id="083c9-132">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="083c9-133">Verwenden Sie das Get-AzureRmVM-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="083c9-133">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="083c9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="083c9-134">CommonParameters</span></span>
<span data-ttu-id="083c9-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="083c9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="083c9-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="083c9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="083c9-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="083c9-137">INPUTS</span></span>

### <span data-ttu-id="083c9-138">Keine</span><span class="sxs-lookup"><span data-stu-id="083c9-138">None</span></span>
<span data-ttu-id="083c9-139">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="083c9-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="083c9-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="083c9-140">OUTPUTS</span></span>

## <span data-ttu-id="083c9-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="083c9-141">NOTES</span></span>

## <span data-ttu-id="083c9-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="083c9-142">RELATED LINKS</span></span>

[<span data-ttu-id="083c9-143">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="083c9-143">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="083c9-144">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="083c9-144">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


