---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 64EF867E-5142-4317-9552-8BC94117208D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 899ecd0256bc3d6f88b8f942fa488db444a9bb41
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006272"
---
# <span data-ttu-id="91a10-101">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="91a10-101">Set-AzureDataDisk</span></span>

## <span data-ttu-id="91a10-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="91a10-102">SYNOPSIS</span></span>
<span data-ttu-id="91a10-103">Ändert die Host Zwischenspeicherung eines vorhandenen Datenlaufwerks auf einem virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="91a10-103">Modifies the host caching of an existing data disk on an Azure virtual machine.</span></span>

## <span data-ttu-id="91a10-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="91a10-104">SYNTAX</span></span>

### <span data-ttu-id="91a10-105">NORESIZE</span><span class="sxs-lookup"><span data-stu-id="91a10-105">NoResize</span></span>
```
Set-AzureDataDisk [-HostCaching] <String> [-LUN] <Int32> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="91a10-106">Größe</span><span class="sxs-lookup"><span data-stu-id="91a10-106">Resize</span></span>
```
Set-AzureDataDisk [-DiskName] <String> [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="91a10-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91a10-107">DESCRIPTION</span></span>
<span data-ttu-id="91a10-108">Das Cmdlet " **Satz-AzureDataDisk** " ändert die Cache Attribute eines vorhandenen Datenlaufwerks auf einem Azure Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="91a10-108">The **Set-AzureDataDisk** cmdlet modifies the cache attributes of an existing data disk on an Azure virtual machine.</span></span>
<span data-ttu-id="91a10-109">Geben Sie an, welcher Datenträger durch die logische einheitennummer (Logical Unit Number, LUN) aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="91a10-109">Specify which data disk to update by its logical unit number (LUN).</span></span>

## <span data-ttu-id="91a10-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91a10-110">EXAMPLES</span></span>

### <span data-ttu-id="91a10-111">Beispiel 1: Ändern der Host Zwischenspeicherung für einen Datenträger</span><span class="sxs-lookup"><span data-stu-id="91a10-111">Example 1: Modify the host caching for a data disk</span></span>
```
PS C:\> Get-AzureVM "ContosoService" | Set-AzureDataDisk -VM "VirtualMachine07" -LUN 2 -HostCaching ReadOnly | Update-AzureVM
```

<span data-ttu-id="91a10-112">Dieser Befehl ruft die virtuellen Computer ab, die mit dem Cmdlet **Get-AzureVM** auf dem Dienst mit dem Namen ContosoService ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="91a10-112">This command gets the virtual machines that run on the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="91a10-113">Der Befehl übergibt Sie mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91a10-113">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="91a10-114">Dieses Cmdlet legt den Datenträger bei LUN 2 des virtuellen Computers mit dem Namen "VirtualMachine07" so fest, dass die ReadOnly-Host Zwischenspeicherung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="91a10-114">That cmdlet sets the data disk at LUN 2 of the virtual machine named VirtualMachine07 to use ReadOnly host caching.</span></span>
<span data-ttu-id="91a10-115">Der Befehl aktualisiert den virtuellen Computer, um Ihre Änderungen mit dem Cmdlet **Update-AzureVM** wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="91a10-115">The command updates the virtual machine to reflect your changes by using the **Update-AzureVM** cmdlet.</span></span>

### <span data-ttu-id="91a10-116">Beispiel 2: Ändern der Host Zwischenspeicherung für alle Datenlaufwerke auf einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="91a10-116">Example 2: Modify the host caching for all data disks on a virtual machine</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk | Set-AzureDataDisk -HostCaching ReadWrite | Update-AzureVM
```

<span data-ttu-id="91a10-117">Dieser Befehl ruft ein Objekt für den virtuellen Computer mit dem Namen VirtualMachine07 im ContosoService-clouddienst ab.</span><span class="sxs-lookup"><span data-stu-id="91a10-117">This command gets an object for the virtual machine named VirtualMachine07 on the ContosoService cloud service.</span></span>
<span data-ttu-id="91a10-118">Der Befehl übergibt ihn an das Cmdlet " **Get-AzureDataDisk** ", das die Datenlaufwerke für diesen virtuellen Computer abruft.</span><span class="sxs-lookup"><span data-stu-id="91a10-118">The command passes it to the **Get-AzureDataDisk** cmdlet, which gets the data disks for that virtual machine.</span></span>
<span data-ttu-id="91a10-119">Das aktuelle Cmdlet legt dann den Host Zwischenspeichermodus für jeden Datenträger auf ReadWrite fest.</span><span class="sxs-lookup"><span data-stu-id="91a10-119">The current cmdlet then sets the host caching mode of each data disks to ReadWrite.</span></span>
<span data-ttu-id="91a10-120">Der Befehl aktualisiert den virtuellen Computer, um Ihre Änderungen wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="91a10-120">The command updates the virtual machine to reflect your changes.</span></span>

## <span data-ttu-id="91a10-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="91a10-121">PARAMETERS</span></span>

### <span data-ttu-id="91a10-122">-Daten Trägername</span><span class="sxs-lookup"><span data-stu-id="91a10-122">-DiskName</span></span>
<span data-ttu-id="91a10-123">Gibt den Namen der Daten Datenträgerkonfiguration an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="91a10-123">Specifies the name of the data disk configuration that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: Resize
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a10-124">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="91a10-124">-HostCaching</span></span>

> [!WARNING]
> <span data-ttu-id="91a10-125">Datenträgerzwischenspeicherung wird für Datenträger 4 tib und größer nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="91a10-125">Disk Caching is not supported for disks 4 TiB and larger.</span></span> <span data-ttu-id="91a10-126">Wenn mehrere Datenträger an Ihren Computer angeschlossen sind, unterstützt jeder Datenträger, der kleiner als 4 tib ist, die Zwischenspeicherung.</span><span class="sxs-lookup"><span data-stu-id="91a10-126">If multiple disks are attached to your VM, each disk that is smaller than 4 TiB will support caching.</span></span>
>
> <span data-ttu-id="91a10-127">Durch Ändern der Cacheeinstellung eines Azure-Datenträgers wird der Zieldatenträger abgetrennt und erneut angefügt.</span><span class="sxs-lookup"><span data-stu-id="91a10-127">Changing the cache setting of an Azure disk detaches and re-attaches the target disk.</span></span> <span data-ttu-id="91a10-128">Wenn es sich um den Betriebssystemdatenträger handelt, wird der VM neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="91a10-128">If it is the operating system disk, the VM is restarted.</span></span> <span data-ttu-id="91a10-129">Beenden Sie alle Anwendungen/Dienste, die von dieser Unterbrechung betroffen sein könnten, bevor Sie die Festplatten-Cache-Einstellung ändern.</span><span class="sxs-lookup"><span data-stu-id="91a10-129">Stop all applications/services that might be affected by this disruption before changing the disk cache setting.</span></span> <span data-ttu-id="91a10-130">Wenn Sie diese Empfehlungen nicht befolgen, kann dies zu Datenbeschädigungen führen.</span><span class="sxs-lookup"><span data-stu-id="91a10-130">Not following those recommendations could lead to data corruption.</span></span>

<span data-ttu-id="91a10-131">Gibt die Einstellungen für die Zwischenspeicherung auf Hostebene des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="91a10-131">Specifies the host level caching settings of the disk.</span></span>
<span data-ttu-id="91a10-132">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="91a10-132">Valid values are:</span></span>

- <span data-ttu-id="91a10-133">Keine</span><span class="sxs-lookup"><span data-stu-id="91a10-133">None</span></span>
- <span data-ttu-id="91a10-134">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="91a10-134">ReadOnly</span></span>
- <span data-ttu-id="91a10-135">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="91a10-135">ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: NoResize
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a10-136">-Information</span><span class="sxs-lookup"><span data-stu-id="91a10-136">-InformationAction</span></span>
<span data-ttu-id="91a10-137">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="91a10-137">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="91a10-138">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="91a10-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="91a10-139">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="91a10-139">Continue</span></span>
- <span data-ttu-id="91a10-140">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="91a10-140">Ignore</span></span>
- <span data-ttu-id="91a10-141">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="91a10-141">Inquire</span></span>
- <span data-ttu-id="91a10-142">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="91a10-142">SilentlyContinue</span></span>
- <span data-ttu-id="91a10-143">Beenden</span><span class="sxs-lookup"><span data-stu-id="91a10-143">Stop</span></span>
- <span data-ttu-id="91a10-144">Anhalten</span><span class="sxs-lookup"><span data-stu-id="91a10-144">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a10-145">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="91a10-145">-InformationVariable</span></span>
<span data-ttu-id="91a10-146">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="91a10-146">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a10-147">-LUN</span><span class="sxs-lookup"><span data-stu-id="91a10-147">-LUN</span></span>
<span data-ttu-id="91a10-148">Gibt die LUN für das Datenlaufwerk auf dem virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="91a10-148">Specifies the LUN for the data drive in the virtual machine.</span></span>
<span data-ttu-id="91a10-149">Gültige Werte sind: 0 bis 15.</span><span class="sxs-lookup"><span data-stu-id="91a10-149">Valid values are: 0 through 15.</span></span>

```yaml
Type: Int32
Parameter Sets: NoResize
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a10-150">-Profil</span><span class="sxs-lookup"><span data-stu-id="91a10-150">-Profile</span></span>
<span data-ttu-id="91a10-151">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="91a10-151">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="91a10-152">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="91a10-152">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a10-153">-ResizedSizeInGB</span><span class="sxs-lookup"><span data-stu-id="91a10-153">-ResizedSizeInGB</span></span>
<span data-ttu-id="91a10-154">Gibt die neue Größe (in GB) für den Daten Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="91a10-154">Specifies the new size, in gigabytes, for the data disk.</span></span>
<span data-ttu-id="91a10-155">Die neue Größe muss größer als die aktuelle Größe sein.</span><span class="sxs-lookup"><span data-stu-id="91a10-155">The new size must be larger than the current size.</span></span>

```yaml
Type: Int32
Parameter Sets: Resize
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a10-156">-VM</span><span class="sxs-lookup"><span data-stu-id="91a10-156">-VM</span></span>
<span data-ttu-id="91a10-157">Gibt das Objekt des virtuellen Computers an, das an den Daten Datenträger angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="91a10-157">Specifies the virtual machine object that is attached to the data disk.</span></span>
<span data-ttu-id="91a10-158">Verwenden Sie das Cmdlet **Get-AzureVM** , um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="91a10-158">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91a10-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91a10-159">CommonParameters</span></span>
<span data-ttu-id="91a10-160">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91a10-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91a10-161">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91a10-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91a10-162">Eingaben</span><span class="sxs-lookup"><span data-stu-id="91a10-162">INPUTS</span></span>

## <span data-ttu-id="91a10-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="91a10-163">OUTPUTS</span></span>

## <span data-ttu-id="91a10-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="91a10-164">NOTES</span></span>

## <span data-ttu-id="91a10-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="91a10-165">RELATED LINKS</span></span>

[<span data-ttu-id="91a10-166">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="91a10-166">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="91a10-167">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="91a10-167">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="91a10-168">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="91a10-168">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="91a10-169">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="91a10-169">Remove-AzureDataDisk</span></span>](./Remove-AzureDataDisk.md)

[<span data-ttu-id="91a10-170">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="91a10-170">Update-AzureVM</span></span>](./Update-AzureVM.md)


