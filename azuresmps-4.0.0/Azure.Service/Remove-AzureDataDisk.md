---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D563ACF6-6BCD-4463-8731-175BA047A74D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ceb2af6b359d5b9660397ef654d6c56e045ce64
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006372"
---
# <span data-ttu-id="c4404-101">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="c4404-101">Remove-AzureDataDisk</span></span>

## <span data-ttu-id="c4404-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c4404-102">SYNOPSIS</span></span>
<span data-ttu-id="c4404-103">Entfernt einen Datenträger von einem Azure Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="c4404-103">Removes a data disk from an Azure virtual machine.</span></span>

## <span data-ttu-id="c4404-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4404-104">SYNTAX</span></span>

```
Remove-AzureDataDisk [-LUN] <Int32> [-DeleteVHD] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c4404-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4404-105">DESCRIPTION</span></span>
<span data-ttu-id="c4404-106">Das Cmdlet **Remove-AzureDataDisk** entfernt einen Daten Datenträger von einem virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="c4404-106">The **Remove-AzureDataDisk** cmdlet removes a data disk from an Azure virtual machine.</span></span>
<span data-ttu-id="c4404-107">Standardmäßig entfernt dieses Cmdlet das Datenträger-BLOB nicht aus dem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="c4404-107">By default, this cmdlet does not remove the data disk blob from the storage account.</span></span>

## <span data-ttu-id="c4404-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4404-108">EXAMPLES</span></span>

### <span data-ttu-id="c4404-109">Beispiel 1: Entfernen eines Daten Datenträgers</span><span class="sxs-lookup"><span data-stu-id="c4404-109">Example 1: Remove a data disk</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0
```

<span data-ttu-id="c4404-110">Dieser Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine07 im Dienst ContosoService mit dem Cmdlet **Get-AzureVM** ab.</span><span class="sxs-lookup"><span data-stu-id="c4404-110">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="c4404-111">Der Befehl übergibt den virtuellen Computer mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4404-111">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c4404-112">Das aktuelle Cmdlet entfernt den Daten Datenträger mit der LUN 0.</span><span class="sxs-lookup"><span data-stu-id="c4404-112">The current cmdlet removes the data disk that has the LUN 0.</span></span>

### <span data-ttu-id="c4404-113">Beispiel 2: Entfernen eines Daten Datenträgers und der virtuellen Festplattendatei</span><span class="sxs-lookup"><span data-stu-id="c4404-113">Example 2: Remove a data disk and the virtual hard disk file</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0 -DeleteVHD | Update-AzureVM
```

<span data-ttu-id="c4404-114">Dieser Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine07 im Dienst mit dem Namen ContosoService.</span><span class="sxs-lookup"><span data-stu-id="c4404-114">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService.</span></span>
<span data-ttu-id="c4404-115">Der Befehl übergibt den virtuellen Computer an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4404-115">The command passes the virtual machine to the current cmdlet.</span></span>
<span data-ttu-id="c4404-116">Das aktuelle Cmdlet entfernt den Daten Datenträger mit der LUN 0.</span><span class="sxs-lookup"><span data-stu-id="c4404-116">The current cmdlet removes the data disk that has the LUN 0.</span></span>
<span data-ttu-id="c4404-117">Der Befehl enthält den *DeleteVHD* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="c4404-117">The command includes the *DeleteVHD* parameter.</span></span>
<span data-ttu-id="c4404-118">Daher wird auch die zugrunde liegende virtuelle Festplatte gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c4404-118">Therefore, it also deletes the underlying virtual hard disk.</span></span>
<span data-ttu-id="c4404-119">Der Befehl aktualisiert den virtuellen Computer, um Ihre Änderungen mit dem Cmdlet **Update-AzureVM** wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="c4404-119">The command updates the virtual machine to reflect your changes by using the **Update-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="c4404-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4404-120">PARAMETERS</span></span>

### <span data-ttu-id="c4404-121">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="c4404-121">-DeleteVHD</span></span>
<span data-ttu-id="c4404-122">Gibt an, dass das Cmdlet den Datenträger und die virtuelle Festplatte (VHD) aus dem BLOB-Speicher entfernt.</span><span class="sxs-lookup"><span data-stu-id="c4404-122">Indicates that this cmdlet removes the data disk and the virtual hard disk (VHD) from blob storage.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4404-123">-Information</span><span class="sxs-lookup"><span data-stu-id="c4404-123">-InformationAction</span></span>
<span data-ttu-id="c4404-124">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="c4404-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c4404-125">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c4404-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c4404-126">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="c4404-126">Continue</span></span>
- <span data-ttu-id="c4404-127">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="c4404-127">Ignore</span></span>
- <span data-ttu-id="c4404-128">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="c4404-128">Inquire</span></span>
- <span data-ttu-id="c4404-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c4404-129">SilentlyContinue</span></span>
- <span data-ttu-id="c4404-130">Beenden</span><span class="sxs-lookup"><span data-stu-id="c4404-130">Stop</span></span>
- <span data-ttu-id="c4404-131">Anhalten</span><span class="sxs-lookup"><span data-stu-id="c4404-131">Suspend</span></span>

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

### <span data-ttu-id="c4404-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c4404-132">-InformationVariable</span></span>
<span data-ttu-id="c4404-133">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="c4404-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c4404-134">-LUN</span><span class="sxs-lookup"><span data-stu-id="c4404-134">-LUN</span></span>
<span data-ttu-id="c4404-135">Gibt die logische Einheitsnummer (LUN) für das Datenlaufwerk auf dem virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="c4404-135">Specifies the logical unit number (LUN) for the data drive in the virtual machine.</span></span>
<span data-ttu-id="c4404-136">Gültige Werte sind: 0 bis 15.</span><span class="sxs-lookup"><span data-stu-id="c4404-136">Valid values are: 0 through 15.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4404-137">-Profil</span><span class="sxs-lookup"><span data-stu-id="c4404-137">-Profile</span></span>
<span data-ttu-id="c4404-138">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="c4404-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c4404-139">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="c4404-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c4404-140">-VM</span><span class="sxs-lookup"><span data-stu-id="c4404-140">-VM</span></span>
<span data-ttu-id="c4404-141">Gibt das Objekt des virtuellen Computers an, das an den Daten Datenträger angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="c4404-141">Specifies the virtual machine object that is attached to the data disk.</span></span>
<span data-ttu-id="c4404-142">Verwenden Sie das Cmdlet **Get-AzureVM** , um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c4404-142">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="c4404-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4404-143">CommonParameters</span></span>
<span data-ttu-id="c4404-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4404-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4404-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4404-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4404-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c4404-146">INPUTS</span></span>

## <span data-ttu-id="c4404-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c4404-147">OUTPUTS</span></span>

## <span data-ttu-id="c4404-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="c4404-148">NOTES</span></span>

## <span data-ttu-id="c4404-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c4404-149">RELATED LINKS</span></span>

[<span data-ttu-id="c4404-150">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="c4404-150">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="c4404-151">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="c4404-151">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="c4404-152">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="c4404-152">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="c4404-153">Satz-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="c4404-153">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)

[<span data-ttu-id="c4404-154">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="c4404-154">Update-AzureVM</span></span>](./Update-AzureVM.md)


