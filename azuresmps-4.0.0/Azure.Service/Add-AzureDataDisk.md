---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FDEDBF4F-7507-43FF-A983-7E431C0C1950
online version: ''
schema: 2.0.0
ms.openlocfilehash: 967fbaf83efa12bd305fc9fe075a9abffdd62dc3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005941"
---
# <span data-ttu-id="3aa18-101">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="3aa18-101">Add-AzureDataDisk</span></span>

## <span data-ttu-id="3aa18-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3aa18-102">SYNOPSIS</span></span>
<span data-ttu-id="3aa18-103">Fügt einen Daten Datenträger zu einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="3aa18-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="3aa18-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3aa18-104">SYNTAX</span></span>

### <span data-ttu-id="3aa18-105">CreateNew (Standard)</span><span class="sxs-lookup"><span data-stu-id="3aa18-105">CreateNew (Default)</span></span>
```
Add-AzureDataDisk [-CreateNew] [-DiskSizeInGB] <Int32> [-DiskLabel] <String> [-LUN] <Int32>
 [-MediaLocation <String>] [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3aa18-106">Importieren</span><span class="sxs-lookup"><span data-stu-id="3aa18-106">Import</span></span>
```
Add-AzureDataDisk [-Import] [-DiskName] <String> [-LUN] <Int32> [-HostCaching <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="3aa18-107">ImportFrom</span><span class="sxs-lookup"><span data-stu-id="3aa18-107">ImportFrom</span></span>
```
Add-AzureDataDisk [-ImportFrom] [-DiskLabel] <String> [-LUN] <Int32> -MediaLocation <String>
 [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3aa18-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3aa18-108">DESCRIPTION</span></span>
<span data-ttu-id="3aa18-109">Mit dem Cmdlet **Add-AzureDataDisk** wird ein neuer oder vorhandener Daten Datenträger zu einem Azure Virtual Machine-Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3aa18-109">The **Add-AzureDataDisk** cmdlet adds a new or existing data disk to an Azure virtual machine object.</span></span>
<span data-ttu-id="3aa18-110">Verwenden Sie den *CreateNew* -Parameter, um einen neuen Daten Datenträger mit einer angegebenen Größe und Beschriftung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3aa18-110">Use the *CreateNew* parameter to create a new data disk that has a specified size and label.</span></span>
<span data-ttu-id="3aa18-111">Verwenden Sie den Parameter *importieren* , um einen vorhandenen Datenträger aus dem Image-Repository anzufügen.</span><span class="sxs-lookup"><span data-stu-id="3aa18-111">Use the *Import* parameter to attach an existing disk from the image repository.</span></span>
<span data-ttu-id="3aa18-112">Verwenden Sie den *ImportFrom* -Parameter, um einen vorhandenen Datenträger von einem BLOB in einem Speicherkonto anzufügen.</span><span class="sxs-lookup"><span data-stu-id="3aa18-112">Use the *ImportFrom* parameter to attach an existing disk from a blob in a storage account.</span></span>
<span data-ttu-id="3aa18-113">Sie können den Host-Cache-Modus für den angefügten Datenträger angeben.</span><span class="sxs-lookup"><span data-stu-id="3aa18-113">You can specify the host-cache mode of the attached data disk.</span></span>

## <span data-ttu-id="3aa18-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3aa18-114">EXAMPLES</span></span>

### <span data-ttu-id="3aa18-115">Beispiel 1: Importieren einer Datendiskette aus dem Repository</span><span class="sxs-lookup"><span data-stu-id="3aa18-115">Example 1: Import a data disk from the repository</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Add-AzureDataDisk -Import -DiskName "Disk68" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="3aa18-116">Dieser Befehl ruft ein Objekt eines virtuellen Computers für den virtuellen Computer mit dem Namen "VirtualMachine07" im ContosoService-clouddienst ab, indem Sie das Cmdlet " **Get-AzureVM** " verwenden.</span><span class="sxs-lookup"><span data-stu-id="3aa18-116">This command gets a virtual machine object for the virtual machine named VirtualMachine07 in the ContosoService cloud service by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="3aa18-117">Der Befehl übergibt ihn mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3aa18-117">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3aa18-118">Dieser Befehl fügt eine vorhandene Datendiskette aus dem Repository an den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="3aa18-118">That command attaches an existing data disk from the repository to the virtual machine.</span></span>
<span data-ttu-id="3aa18-119">Der Datenträger hat eine LUN von 0.</span><span class="sxs-lookup"><span data-stu-id="3aa18-119">The data disk has a LUN of 0.</span></span>
<span data-ttu-id="3aa18-120">Der Befehl aktualisiert den virtuellen Computer, um Ihre Änderungen mit dem Cmdlet **Update-AzureVM** wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="3aa18-120">The command updates the virtual machine to reflect your changes by using the **Update-AzureVM** cmdlet.</span></span>

### <span data-ttu-id="3aa18-121">Beispiel 2: Hinzufügen eines neuen Daten Datenträgers</span><span class="sxs-lookup"><span data-stu-id="3aa18-121">Example 2: Add a new data disk</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine08" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 128 -DiskLabel "main" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="3aa18-122">Dieser Befehl ruft ein Objekt eines virtuellen Computers für den virtuellen Computer mit dem Namen VirtualMachine08 ab.</span><span class="sxs-lookup"><span data-stu-id="3aa18-122">This command gets a virtual machine object for the virtual machine named VirtualMachine08.</span></span>
<span data-ttu-id="3aa18-123">Der Befehl übergibt ihn an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3aa18-123">The command passes it to the current cmdlet.</span></span>
<span data-ttu-id="3aa18-124">Dieser Befehl fügt einen neuen Daten Datenträger mit dem Namen "MyNewDisk. VHD" an.</span><span class="sxs-lookup"><span data-stu-id="3aa18-124">That command attaches a new data disk named MyNewDisk.vhd.</span></span>
<span data-ttu-id="3aa18-125">Das Cmdlet erstellt den Datenträger im VHD-Container im Standardspeicher Konto des aktuellen Abonnements.</span><span class="sxs-lookup"><span data-stu-id="3aa18-125">The cmdlet creates the disk in the vhds container in the default storage account of the current subscription.</span></span>
<span data-ttu-id="3aa18-126">Der Befehl aktualisiert den virtuellen Computer, um Ihre Änderungen wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="3aa18-126">The command updates the virtual machine to reflect your changes.</span></span>

### <span data-ttu-id="3aa18-127">Beispiel 3: Hinzufügen eines Daten Datenträgers von einem angegebenen Speicherort</span><span class="sxs-lookup"><span data-stu-id="3aa18-127">Example 3: Add a data disk from a specified location</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "Database" | Add-AzureDataDisk -ImportFrom -MediaLocation "https://contosostorage.blob.core.windows.net/container07/Disk14.vhd" -DiskLabel "main" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="3aa18-128">Dieser Befehl ruft ein Objekt eines virtuellen Computers für den virtuellen Computer mit dem Namen Database ab.</span><span class="sxs-lookup"><span data-stu-id="3aa18-128">This command gets a virtual machine object for the virtual machine named Database.</span></span>
<span data-ttu-id="3aa18-129">Der Befehl übergibt ihn an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3aa18-129">The command passes it to the current cmdlet.</span></span>
<span data-ttu-id="3aa18-130">Mit diesem Befehl wird eine vorhandene Datendiskette mit dem Namen Disk14. VHD vom angegebenen Speicherort angefügt.</span><span class="sxs-lookup"><span data-stu-id="3aa18-130">That command attaches an existing data disk named Disk14.vhd from the specified location.</span></span>
<span data-ttu-id="3aa18-131">Der Befehl aktualisiert den virtuellen Computer, um Ihre Änderungen wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="3aa18-131">The command updates the virtual machine to reflect your changes.</span></span>

## <span data-ttu-id="3aa18-132">Parameter</span><span class="sxs-lookup"><span data-stu-id="3aa18-132">PARAMETERS</span></span>

### <span data-ttu-id="3aa18-133">-CreateNew</span><span class="sxs-lookup"><span data-stu-id="3aa18-133">-CreateNew</span></span>
<span data-ttu-id="3aa18-134">Gibt an, dass dieses Cmdlet einen Daten Datenträger erstellt.</span><span class="sxs-lookup"><span data-stu-id="3aa18-134">Indicates that this cmdlet creates a data disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aa18-135">-DiskLabel</span><span class="sxs-lookup"><span data-stu-id="3aa18-135">-DiskLabel</span></span>
<span data-ttu-id="3aa18-136">Gibt die Datenträgerbeschriftung für einen neuen Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="3aa18-136">Specifies the disk label for a new data disk.</span></span>

```yaml
Type: String
Parameter Sets: CreateNew, ImportFrom
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aa18-137">-Daten Trägername</span><span class="sxs-lookup"><span data-stu-id="3aa18-137">-DiskName</span></span>
<span data-ttu-id="3aa18-138">Gibt den Namen eines Daten Datenträgers im Datenträger-Repository an.</span><span class="sxs-lookup"><span data-stu-id="3aa18-138">Specifies the name of a data disk in the disk repository.</span></span>

```yaml
Type: String
Parameter Sets: Import
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3aa18-139">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="3aa18-139">-DiskSizeInGB</span></span>
<span data-ttu-id="3aa18-140">Gibt die Größe des logischen Datenträgers in Gigabyte für einen neuen Daten Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="3aa18-140">Specifies the logical disk size, in gigabytes, for a new data disk.</span></span>

```yaml
Type: Int32
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aa18-141">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="3aa18-141">-HostCaching</span></span>
<span data-ttu-id="3aa18-142">Gibt die Einstellungen für die Zwischenspeicherung auf Hostebene des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="3aa18-142">Specifies the host level caching settings of the disk.</span></span>
<span data-ttu-id="3aa18-143">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="3aa18-143">Valid values are:</span></span> 

- <span data-ttu-id="3aa18-144">Keine</span><span class="sxs-lookup"><span data-stu-id="3aa18-144">None</span></span> 
- <span data-ttu-id="3aa18-145">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="3aa18-145">ReadOnly</span></span> 
- <span data-ttu-id="3aa18-146">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3aa18-146">ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aa18-147">-Import</span><span class="sxs-lookup"><span data-stu-id="3aa18-147">-Import</span></span>
<span data-ttu-id="3aa18-148">Gibt an, dass dieses Cmdlet einen vorhandenen Daten Datenträger aus dem Image-Repository importiert.</span><span class="sxs-lookup"><span data-stu-id="3aa18-148">Indicates that this cmdlet imports an existing data disk from the image repository.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Import
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aa18-149">-ImportFrom</span><span class="sxs-lookup"><span data-stu-id="3aa18-149">-ImportFrom</span></span>
<span data-ttu-id="3aa18-150">Gibt an, dass dieses Cmdlet einen vorhandenen Daten Datenträger aus einem BLOB in einem Speicherkonto importiert.</span><span class="sxs-lookup"><span data-stu-id="3aa18-150">Indicates that this cmdlet imports an existing data disk from a blob in a storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ImportFrom
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aa18-151">-Information</span><span class="sxs-lookup"><span data-stu-id="3aa18-151">-InformationAction</span></span>
<span data-ttu-id="3aa18-152">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="3aa18-152">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3aa18-153">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3aa18-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3aa18-154">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="3aa18-154">Continue</span></span>
- <span data-ttu-id="3aa18-155">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="3aa18-155">Ignore</span></span>
- <span data-ttu-id="3aa18-156">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="3aa18-156">Inquire</span></span>
- <span data-ttu-id="3aa18-157">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3aa18-157">SilentlyContinue</span></span>
- <span data-ttu-id="3aa18-158">Beenden</span><span class="sxs-lookup"><span data-stu-id="3aa18-158">Stop</span></span>
- <span data-ttu-id="3aa18-159">Anhalten</span><span class="sxs-lookup"><span data-stu-id="3aa18-159">Suspend</span></span>

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

### <span data-ttu-id="3aa18-160">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3aa18-160">-InformationVariable</span></span>
<span data-ttu-id="3aa18-161">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="3aa18-161">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3aa18-162">-LUN</span><span class="sxs-lookup"><span data-stu-id="3aa18-162">-LUN</span></span>
<span data-ttu-id="3aa18-163">Gibt die logische Einheitsnummer (LUN) für das Datenlaufwerk auf dem virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="3aa18-163">Specifies the logical unit number (LUN) for the data drive in the virtual machine.</span></span>
<span data-ttu-id="3aa18-164">Gültige Werte sind: 0 bis 15.</span><span class="sxs-lookup"><span data-stu-id="3aa18-164">Valid values are: 0 through 15.</span></span>
<span data-ttu-id="3aa18-165">Jeder Datenträger muss über eine eindeutige LUN verfügen.</span><span class="sxs-lookup"><span data-stu-id="3aa18-165">Each data disk must have a unique LUN.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aa18-166">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="3aa18-166">-MediaLocation</span></span>
<span data-ttu-id="3aa18-167">Gibt den Speicherort des BLOB in einem Azure Storage-Konto an, in dem dieses Cmdlet den Daten Datenträger speichert.</span><span class="sxs-lookup"><span data-stu-id="3aa18-167">Specifies the location of the blob in an Azure storage account where this cmdlet stores the data disk.</span></span>
<span data-ttu-id="3aa18-168">Wenn Sie keinen Speicherort angeben, speichert das Cmdlet den Daten Datenträger im VHD-Container im Standardspeicher Konto für das aktuelle Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3aa18-168">If you do not specify a location, the cmdlet stores the data disk in the vhds container in the default storage account for the current subscription.</span></span>
<span data-ttu-id="3aa18-169">Wenn kein VHD-Container vorhanden ist, erstellt das Cmdlet einen VHD-Container.</span><span class="sxs-lookup"><span data-stu-id="3aa18-169">If a vhds container does not exist, the cmdlet creates a vhds container.</span></span>

```yaml
Type: String
Parameter Sets: CreateNew
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ImportFrom
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3aa18-170">-Profil</span><span class="sxs-lookup"><span data-stu-id="3aa18-170">-Profile</span></span>
<span data-ttu-id="3aa18-171">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="3aa18-171">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3aa18-172">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="3aa18-172">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3aa18-173">-VM</span><span class="sxs-lookup"><span data-stu-id="3aa18-173">-VM</span></span>
<span data-ttu-id="3aa18-174">Gibt das Objekt des virtuellen Computers an, an das dieses Cmdlet einen Daten Datenträger anfügt.</span><span class="sxs-lookup"><span data-stu-id="3aa18-174">Specifies the virtual machine object to which this cmdlet attaches a data disk.</span></span>
<span data-ttu-id="3aa18-175">Verwenden Sie das Cmdlet **Get-AzureVM** , um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3aa18-175">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="3aa18-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aa18-176">CommonParameters</span></span>
<span data-ttu-id="3aa18-177">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3aa18-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aa18-178">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3aa18-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aa18-179">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3aa18-179">INPUTS</span></span>

## <span data-ttu-id="3aa18-180">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3aa18-180">OUTPUTS</span></span>

## <span data-ttu-id="3aa18-181">Notizen</span><span class="sxs-lookup"><span data-stu-id="3aa18-181">NOTES</span></span>

## <span data-ttu-id="3aa18-182">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3aa18-182">RELATED LINKS</span></span>

[<span data-ttu-id="3aa18-183">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="3aa18-183">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="3aa18-184">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="3aa18-184">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="3aa18-185">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="3aa18-185">Remove-AzureDataDisk</span></span>](./Remove-AzureDataDisk.md)

[<span data-ttu-id="3aa18-186">Satz-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="3aa18-186">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)

[<span data-ttu-id="3aa18-187">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="3aa18-187">Update-AzureVM</span></span>](./Update-AzureVM.md)


