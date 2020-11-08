---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 02DB15F5-5CE0-4FF0-8863-AF1B2BA5E775
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41f72ace02132ba4184af08e995404b47f76d0b0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006034"
---
# <span data-ttu-id="8d5a8-101">Set-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="8d5a8-101">Set-AzureOSDisk</span></span>

## <span data-ttu-id="8d5a8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8d5a8-102">SYNOPSIS</span></span>
<span data-ttu-id="8d5a8-103">Ändert den Host Cachemodus eines Azure Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="8d5a8-103">Modifies the host cache mode of an Azure virtual machine.</span></span>

## <span data-ttu-id="8d5a8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d5a8-104">SYNTAX</span></span>

### <span data-ttu-id="8d5a8-105">NORESIZE</span><span class="sxs-lookup"><span data-stu-id="8d5a8-105">NoResize</span></span>
```
Set-AzureOSDisk [-HostCaching] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8d5a8-106">Größe</span><span class="sxs-lookup"><span data-stu-id="8d5a8-106">Resize</span></span>
```
Set-AzureOSDisk [[-HostCaching] <String>] [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d5a8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d5a8-107">DESCRIPTION</span></span>
<span data-ttu-id="8d5a8-108">Das Cmdlet " **Satz-AzureOSDisk** " ändert den Host Cachemodus des Betriebssystemdatenträgers einer virtuellen Azure-Maschine.</span><span class="sxs-lookup"><span data-stu-id="8d5a8-108">The **Set-AzureOSDisk** cmdlet modifies the host cache mode of the operating system disk of an Azure virtual machine.</span></span>
<span data-ttu-id="8d5a8-109">Die unterstützten Host Cache Modi sind ReadOnly und ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="8d5a8-109">The supported host cache modes are ReadOnly and ReadWrite.</span></span>
<span data-ttu-id="8d5a8-110">Wenn Sie dieses Cmdlet auf einem virtuellen Computer ausführen, der ausgeführt wird, wird dieser virtuelle Computer neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="8d5a8-110">If you run this cmdlet on a virtual machine that is running, that virtual machine restarts.</span></span>

## <span data-ttu-id="8d5a8-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8d5a8-111">EXAMPLES</span></span>

### <span data-ttu-id="8d5a8-112">Beispiel 1: Einrichten des Host Cachemodus für ReadOnly mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="8d5a8-112">Example 1: Set the host cache mode to ReadOnly by using the pipeline</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02" | Set-AzureOSDisk -HostCaching "ReadOnly"
```

<span data-ttu-id="8d5a8-113">Dieser Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine02 im Dienst ContosoService mit dem Cmdlet **Get-AzureVM** ab.</span><span class="sxs-lookup"><span data-stu-id="8d5a8-113">This command gets the virtual machine named VirtualMachine02 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="8d5a8-114">Der Befehl übergibt den virtuellen Computer mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d5a8-114">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8d5a8-115">Das aktuelle Cmdlet legt den Host Cachemodus des Betriebssystemdatenträgers dieses virtuellen Computers auf ReadOnly fest.</span><span class="sxs-lookup"><span data-stu-id="8d5a8-115">The current cmdlet sets the host cache mode of the operating system disk of that virtual machine to be ReadOnly.</span></span>

### <span data-ttu-id="8d5a8-116">Beispiel 2: Einrichten des Host Cachemodus auf ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8d5a8-116">Example 2: Set the host cache mode to ReadWrite</span></span>
```
PS C:\> $VM = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02"
PS C:\> Set-AzureOSDisk "ReadWrite" -VM $myVM2
```

<span data-ttu-id="8d5a8-117">Der erste Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine02 im Dienst mit dem Namen ContosoService ab und speichert ihn dann in der Variablen.</span><span class="sxs-lookup"><span data-stu-id="8d5a8-117">The first command gets the virtual machine named VirtualMachine02 in the service named ContosoService, and then stores it in the variable.</span></span>

<span data-ttu-id="8d5a8-118">Mit dem zweiten Befehl wird der Host Cachemodus des Betriebssystemdatenträgers dieses virtuellen Computers auf ReadWrite festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8d5a8-118">The second command sets the host cache mode of the operating system disk of that virtual machine to be ReadWrite.</span></span>

## <span data-ttu-id="8d5a8-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d5a8-119">PARAMETERS</span></span>

### <span data-ttu-id="8d5a8-120">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="8d5a8-120">-HostCaching</span></span>
<span data-ttu-id="8d5a8-121">Gibt das Host Cache Attribut für den Betriebssystemdatenträger an.</span><span class="sxs-lookup"><span data-stu-id="8d5a8-121">Specifies the host cache attribute for the operating system disk.</span></span>
<span data-ttu-id="8d5a8-122">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="8d5a8-122">Valid values are:</span></span> 

- <span data-ttu-id="8d5a8-123">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="8d5a8-123">ReadOnly</span></span> 
- <span data-ttu-id="8d5a8-124">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8d5a8-124">ReadWrite</span></span>

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

```yaml
Type: String
Parameter Sets: Resize
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5a8-125">-Information</span><span class="sxs-lookup"><span data-stu-id="8d5a8-125">-InformationAction</span></span>
<span data-ttu-id="8d5a8-126">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="8d5a8-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8d5a8-127">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8d5a8-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8d5a8-128">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="8d5a8-128">Continue</span></span>
- <span data-ttu-id="8d5a8-129">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="8d5a8-129">Ignore</span></span>
- <span data-ttu-id="8d5a8-130">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="8d5a8-130">Inquire</span></span>
- <span data-ttu-id="8d5a8-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8d5a8-131">SilentlyContinue</span></span>
- <span data-ttu-id="8d5a8-132">Beenden</span><span class="sxs-lookup"><span data-stu-id="8d5a8-132">Stop</span></span>
- <span data-ttu-id="8d5a8-133">Anhalten</span><span class="sxs-lookup"><span data-stu-id="8d5a8-133">Suspend</span></span>

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

### <span data-ttu-id="8d5a8-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8d5a8-134">-InformationVariable</span></span>
<span data-ttu-id="8d5a8-135">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="8d5a8-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8d5a8-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="8d5a8-136">-Profile</span></span>
<span data-ttu-id="8d5a8-137">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="8d5a8-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8d5a8-138">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="8d5a8-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8d5a8-139">-ResizedSizeInGB</span><span class="sxs-lookup"><span data-stu-id="8d5a8-139">-ResizedSizeInGB</span></span>
<span data-ttu-id="8d5a8-140">Gibt eine neue Größe (in GB) für den Betriebssystemdatenträger an.</span><span class="sxs-lookup"><span data-stu-id="8d5a8-140">Specifies a new size, in gigabytes, for the operating system disk.</span></span>
<span data-ttu-id="8d5a8-141">Die Größe muss größer als die aktuelle Größe sein.</span><span class="sxs-lookup"><span data-stu-id="8d5a8-141">The size must be larger than the current size.</span></span>

```yaml
Type: Int32
Parameter Sets: Resize
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5a8-142">-VM</span><span class="sxs-lookup"><span data-stu-id="8d5a8-142">-VM</span></span>
<span data-ttu-id="8d5a8-143">Gibt den virtuellen Computer an, für den dieses Cmdlet den Datenträger des Betriebssystems ändert.</span><span class="sxs-lookup"><span data-stu-id="8d5a8-143">Specifies the virtual machine for which this cmdlet modifies the operating system disk.</span></span>
<span data-ttu-id="8d5a8-144">Verwenden Sie das Cmdlet **Get-AzureVM** , um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8d5a8-144">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="8d5a8-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d5a8-145">CommonParameters</span></span>
<span data-ttu-id="8d5a8-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d5a8-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d5a8-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d5a8-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d5a8-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8d5a8-148">INPUTS</span></span>

## <span data-ttu-id="8d5a8-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8d5a8-149">OUTPUTS</span></span>

## <span data-ttu-id="8d5a8-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="8d5a8-150">NOTES</span></span>

## <span data-ttu-id="8d5a8-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8d5a8-151">RELATED LINKS</span></span>

[<span data-ttu-id="8d5a8-152">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="8d5a8-152">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="8d5a8-153">Get-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="8d5a8-153">Get-AzureOSDisk</span></span>](./Get-AzureOSDisk.md)

[<span data-ttu-id="8d5a8-154">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="8d5a8-154">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="8d5a8-155">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="8d5a8-155">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="8d5a8-156">Satz-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="8d5a8-156">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)

[<span data-ttu-id="8d5a8-157">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="8d5a8-157">Update-AzureVM</span></span>](./Update-AzureVM.md)


