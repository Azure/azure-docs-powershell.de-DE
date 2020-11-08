---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C6DFD49F-26A5-4199-A844-CA0FC405BEDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: f9fc407e2cf7375708fe82253f3d2fb40eb78f60
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006403"
---
# <span data-ttu-id="7d6b1-101">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="7d6b1-101">New-AzureVMConfig</span></span>

## <span data-ttu-id="7d6b1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7d6b1-102">SYNOPSIS</span></span>
<span data-ttu-id="7d6b1-103">Erstellt ein Azure Virtual Machine-Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="7d6b1-103">Creates an Azure virtual machine configuration object.</span></span>

## <span data-ttu-id="7d6b1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d6b1-104">SYNTAX</span></span>

### <span data-ttu-id="7d6b1-105">Bildname (Standard)</span><span class="sxs-lookup"><span data-stu-id="7d6b1-105">ImageName (Default)</span></span>
```
New-AzureVMConfig [-Name] <String> [-InstanceSize] <String> [[-HostCaching] <String>]
 [[-AvailabilitySetName] <String>] [[-Label] <String>] [-ImageName] <String> [[-MediaLocation] <String>]
 [[-DiskLabel] <String>] [-DisableBootDiagnostics] [-LicenseType <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7d6b1-106">Daten Trägername</span><span class="sxs-lookup"><span data-stu-id="7d6b1-106">DiskName</span></span>
```
New-AzureVMConfig [-Name] <String> [-InstanceSize] <String> [[-HostCaching] <String>]
 [[-AvailabilitySetName] <String>] [[-Label] <String>] [-DiskName] <String> [-DisableBootDiagnostics]
 [-LicenseType <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7d6b1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7d6b1-107">DESCRIPTION</span></span>
<span data-ttu-id="7d6b1-108">Mit dem Cmdlet **New-AzureVMConfig** wird ein Azure Virtual Machine-Konfigurationsobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="7d6b1-108">The **New-AzureVMConfig** cmdlet creates an Azure  virtual machine configuration object.</span></span>
<span data-ttu-id="7d6b1-109">Sie können dieses Objekt verwenden, um eine neue Bereitstellung durchzuführen und eine neue virtuelle Maschine zu einer vorhandenen Bereitstellung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="7d6b1-109">You can use this object to perform a new deployment and add a new virtual machine to an existing deployment.</span></span>

## <span data-ttu-id="7d6b1-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7d6b1-110">EXAMPLES</span></span>

### <span data-ttu-id="7d6b1-111">Beispiel 1: Erstellen einer Windows Virtual Machine-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="7d6b1-111">Example 1: Create a Windows virtual machine configuration</span></span>
```
PS C:\> $Image = (Get-AzureVMImage)[4].ImageName 
C:\PS> New-AzureVMConfig -Name "MyVM1" -InstanceSize ExtraSmall -ImageName $Image | Add-AzureProvisioningConfig -Windows -Password $AdminPassword | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "Datadisk1" -LUN 0 | New-AzureVM -ServiceName "MySvc1"
```

<span data-ttu-id="7d6b1-112">Mit diesem Befehl wird eine Windows Virtual Machine-Konfiguration mit Betriebssystemdatenträger, Datenträger und Bereitstellungskonfiguration erstellt.</span><span class="sxs-lookup"><span data-stu-id="7d6b1-112">This command creates a Windows virtual machine configuration with operating system disk, data disk and provisioning configuration.</span></span>
<span data-ttu-id="7d6b1-113">Diese Konfiguration wird dann zum Erstellen eines neuen virtuellen Computers verwendet.</span><span class="sxs-lookup"><span data-stu-id="7d6b1-113">This configuration is then used to create a new virtual machine.</span></span>

### <span data-ttu-id="7d6b1-114">Beispiel 2: Erstellen einer Linux-Konfiguration für virtuelle Maschinen</span><span class="sxs-lookup"><span data-stu-id="7d6b1-114">Example 2: Create a Linux virtual machine configuration</span></span>
```
PS C:\> $Image = (Get-AzureVMImage)[7].ImageName
C:\PS> New-AzureVMConfig -Name "MyVM1" -InstanceSize ExtraSmall -ImageName $Image | Add-AzureProvisioningConfig -Linux -LinuxUser $LinuxUser -Password $AdminPassword | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "Datadisk1" -LUN 0 | New-AzureVM -ServiceName "MySvc1"
```

<span data-ttu-id="7d6b1-115">Mit diesem Befehl wird eine neue Linux Virtual Machine-Konfiguration mit Betriebssystemdatenträger, Datenträger und Bereitstellungskonfiguration erstellt.</span><span class="sxs-lookup"><span data-stu-id="7d6b1-115">This command creates a new Linux virtual machine configuration with operating system disk, data disk and provisioning configuration.</span></span>
<span data-ttu-id="7d6b1-116">Diese Konfiguration wird dann zum Erstellen eines neuen virtuellen Computers verwendet.</span><span class="sxs-lookup"><span data-stu-id="7d6b1-116">This configuration is then used to create a new virtual machine.</span></span>

## <span data-ttu-id="7d6b1-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d6b1-117">PARAMETERS</span></span>

### <span data-ttu-id="7d6b1-118">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="7d6b1-118">-AvailabilitySetName</span></span>
<span data-ttu-id="7d6b1-119">Gibt den Namen des Verfügbarkeits Satzes an.</span><span class="sxs-lookup"><span data-stu-id="7d6b1-119">Specifies the name of the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6b1-120">-DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="7d6b1-120">-DisableBootDiagnostics</span></span>
<span data-ttu-id="7d6b1-121">Gibt an, dass die Konfiguration die Start Diagnose deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7d6b1-121">Indicates that the configuration disables boot diagnostics.</span></span>
<span data-ttu-id="7d6b1-122">Standardmäßig ist die Start Diagnose auf dem virtuellen Computer aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7d6b1-122">By default, boot diagnostics are enabled on the virtual machine.</span></span>

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

### <span data-ttu-id="7d6b1-123">-DiskLabel</span><span class="sxs-lookup"><span data-stu-id="7d6b1-123">-DiskLabel</span></span>
<span data-ttu-id="7d6b1-124">Gibt eine Bezeichnung für den Betriebssystemdatenträger an.</span><span class="sxs-lookup"><span data-stu-id="7d6b1-124">Specifies a label for the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: ImageName
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6b1-125">-Daten Trägername</span><span class="sxs-lookup"><span data-stu-id="7d6b1-125">-DiskName</span></span>
<span data-ttu-id="7d6b1-126">Gibt einen Namen für den Betriebssystemdatenträger an.</span><span class="sxs-lookup"><span data-stu-id="7d6b1-126">Specifies a name for the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: DiskName
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6b1-127">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="7d6b1-127">-HostCaching</span></span>
<span data-ttu-id="7d6b1-128">Gibt den Host Zwischenspeicherungsmodus für den Datenträger des Betriebssystems an.</span><span class="sxs-lookup"><span data-stu-id="7d6b1-128">Specifies the host caching mode for the operating system disk.</span></span>

<span data-ttu-id="7d6b1-129">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="7d6b1-129">Valid values are:</span></span>

- <span data-ttu-id="7d6b1-130">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="7d6b1-130">ReadOnly</span></span>
- <span data-ttu-id="7d6b1-131">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7d6b1-131">ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6b1-132">-Bildname</span><span class="sxs-lookup"><span data-stu-id="7d6b1-132">-ImageName</span></span>
<span data-ttu-id="7d6b1-133">Gibt den Namen des virtuellen Computer Bilds an, das für den Datenträger des Betriebssystems verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d6b1-133">Specifies the name of the virtual machine image to use for the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: ImageName
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6b1-134">-Information</span><span class="sxs-lookup"><span data-stu-id="7d6b1-134">-InformationAction</span></span>
<span data-ttu-id="7d6b1-135">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="7d6b1-135">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7d6b1-136">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7d6b1-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7d6b1-137">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="7d6b1-137">Continue</span></span>
- <span data-ttu-id="7d6b1-138">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="7d6b1-138">Ignore</span></span>
- <span data-ttu-id="7d6b1-139">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="7d6b1-139">Inquire</span></span>
- <span data-ttu-id="7d6b1-140">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7d6b1-140">SilentlyContinue</span></span>
- <span data-ttu-id="7d6b1-141">Beenden</span><span class="sxs-lookup"><span data-stu-id="7d6b1-141">Stop</span></span>
- <span data-ttu-id="7d6b1-142">Anhalten</span><span class="sxs-lookup"><span data-stu-id="7d6b1-142">Suspend</span></span>

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

### <span data-ttu-id="7d6b1-143">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7d6b1-143">-InformationVariable</span></span>
<span data-ttu-id="7d6b1-144">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="7d6b1-144">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7d6b1-145">-Instanzen</span><span class="sxs-lookup"><span data-stu-id="7d6b1-145">-InstanceSize</span></span>
<span data-ttu-id="7d6b1-146">Gibt die Größe der Instanz an.</span><span class="sxs-lookup"><span data-stu-id="7d6b1-146">Specifies the size of the instance.</span></span>

<span data-ttu-id="7d6b1-147">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7d6b1-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7d6b1-148">ExtraSmall</span><span class="sxs-lookup"><span data-stu-id="7d6b1-148">ExtraSmall</span></span>
- <span data-ttu-id="7d6b1-149">Kleine</span><span class="sxs-lookup"><span data-stu-id="7d6b1-149">Small</span></span>
- <span data-ttu-id="7d6b1-150">Mittel</span><span class="sxs-lookup"><span data-stu-id="7d6b1-150">Medium</span></span>
- <span data-ttu-id="7d6b1-151">Große</span><span class="sxs-lookup"><span data-stu-id="7d6b1-151">Large</span></span>
- <span data-ttu-id="7d6b1-152">Extra Large</span><span class="sxs-lookup"><span data-stu-id="7d6b1-152">ExtraLarge</span></span>
- <span data-ttu-id="7d6b1-153">A5</span><span class="sxs-lookup"><span data-stu-id="7d6b1-153">A5</span></span>
- <span data-ttu-id="7d6b1-154">A6</span><span class="sxs-lookup"><span data-stu-id="7d6b1-154">A6</span></span>
- <span data-ttu-id="7d6b1-155">A7</span><span class="sxs-lookup"><span data-stu-id="7d6b1-155">A7</span></span>
- <span data-ttu-id="7d6b1-156">A8</span><span class="sxs-lookup"><span data-stu-id="7d6b1-156">A8</span></span>
- <span data-ttu-id="7d6b1-157">A9</span><span class="sxs-lookup"><span data-stu-id="7d6b1-157">A9</span></span>
- <span data-ttu-id="7d6b1-158">Basic_A0</span><span class="sxs-lookup"><span data-stu-id="7d6b1-158">Basic_A0</span></span>
- <span data-ttu-id="7d6b1-159">Basic_A1</span><span class="sxs-lookup"><span data-stu-id="7d6b1-159">Basic_A1</span></span>
- <span data-ttu-id="7d6b1-160">Basic_A2</span><span class="sxs-lookup"><span data-stu-id="7d6b1-160">Basic_A2</span></span>
- <span data-ttu-id="7d6b1-161">Basic_A3</span><span class="sxs-lookup"><span data-stu-id="7d6b1-161">Basic_A3</span></span>
- <span data-ttu-id="7d6b1-162">Basic_A4</span><span class="sxs-lookup"><span data-stu-id="7d6b1-162">Basic_A4</span></span>
- <span data-ttu-id="7d6b1-163">Standard_D1</span><span class="sxs-lookup"><span data-stu-id="7d6b1-163">Standard_D1</span></span>
- <span data-ttu-id="7d6b1-164">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="7d6b1-164">Standard_D2</span></span>
- <span data-ttu-id="7d6b1-165">Standard_D3</span><span class="sxs-lookup"><span data-stu-id="7d6b1-165">Standard_D3</span></span>
- <span data-ttu-id="7d6b1-166">Standard_D4</span><span class="sxs-lookup"><span data-stu-id="7d6b1-166">Standard_D4</span></span>
- <span data-ttu-id="7d6b1-167">Standard_D11</span><span class="sxs-lookup"><span data-stu-id="7d6b1-167">Standard_D11</span></span>
- <span data-ttu-id="7d6b1-168">Standard_D12</span><span class="sxs-lookup"><span data-stu-id="7d6b1-168">Standard_D12</span></span>
- <span data-ttu-id="7d6b1-169">Standard_D13</span><span class="sxs-lookup"><span data-stu-id="7d6b1-169">Standard_D13</span></span>
- <span data-ttu-id="7d6b1-170">Standard_D14</span><span class="sxs-lookup"><span data-stu-id="7d6b1-170">Standard_D14</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d6b1-171">-Label</span><span class="sxs-lookup"><span data-stu-id="7d6b1-171">-Label</span></span>
<span data-ttu-id="7d6b1-172">Gibt eine Beschriftung an, die dem virtuellen Computer zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d6b1-172">Specifies a label to assign to the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d6b1-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="7d6b1-173">-LicenseType</span></span>
<span data-ttu-id="7d6b1-174">Gibt den Typ der Lizenz für ein Bild oder einen Datenträger an, der lokal lizenziert ist.</span><span class="sxs-lookup"><span data-stu-id="7d6b1-174">Specifies the type of license for an image or disk that is licensed on-premises.</span></span>
<span data-ttu-id="7d6b1-175">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7d6b1-175">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7d6b1-176">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="7d6b1-176">Windows_Client</span></span>
- <span data-ttu-id="7d6b1-177">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="7d6b1-177">Windows_Server</span></span> 

<span data-ttu-id="7d6b1-178">Geben Sie diesen Parameter nur für Bilder an, die das Betriebssystem Windows Server enthalten.</span><span class="sxs-lookup"><span data-stu-id="7d6b1-178">Specify this parameter only for images that contain the Windows Server operating system.</span></span>

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

### <span data-ttu-id="7d6b1-179">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="7d6b1-179">-MediaLocation</span></span>
<span data-ttu-id="7d6b1-180">Gibt den Azure-Speicherort für den neuen virtuellen Computer Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="7d6b1-180">Specifies the Azure storage location for the new virtual machine disk.</span></span>

```yaml
Type: String
Parameter Sets: ImageName
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6b1-181">-Name</span><span class="sxs-lookup"><span data-stu-id="7d6b1-181">-Name</span></span>
<span data-ttu-id="7d6b1-182">Gibt den Namen der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="7d6b1-182">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d6b1-183">-Profil</span><span class="sxs-lookup"><span data-stu-id="7d6b1-183">-Profile</span></span>
<span data-ttu-id="7d6b1-184">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="7d6b1-184">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7d6b1-185">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="7d6b1-185">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7d6b1-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d6b1-186">CommonParameters</span></span>
<span data-ttu-id="7d6b1-187">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d6b1-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d6b1-188">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d6b1-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d6b1-189">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7d6b1-189">INPUTS</span></span>

## <span data-ttu-id="7d6b1-190">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7d6b1-190">OUTPUTS</span></span>

## <span data-ttu-id="7d6b1-191">Notizen</span><span class="sxs-lookup"><span data-stu-id="7d6b1-191">NOTES</span></span>

## <span data-ttu-id="7d6b1-192">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7d6b1-192">RELATED LINKS</span></span>

