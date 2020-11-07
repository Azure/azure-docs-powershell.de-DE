---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/disable-azvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
ms.openlocfilehash: 6a14a8472ca33fe9dbb15aa2ddf58208764a5a6f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844683"
---
# <span data-ttu-id="bcef8-101">Disable-AzVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="bcef8-101">Disable-AzVMDiskEncryption</span></span>

## <span data-ttu-id="bcef8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bcef8-102">SYNOPSIS</span></span>
<span data-ttu-id="bcef8-103">Deaktiviert die Verschlüsselung auf einem virtuellen IaaS-Computer.</span><span class="sxs-lookup"><span data-stu-id="bcef8-103">Disables encryption on an IaaS virtual machine.</span></span>

## <span data-ttu-id="bcef8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bcef8-104">SYNTAX</span></span>

```
Disable-AzVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcef8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bcef8-105">DESCRIPTION</span></span>
<span data-ttu-id="bcef8-106">Das Cmdlet **Disable-AzVMDiskEncryption** deaktiviert die Verschlüsselung auf einem virtuellen Computer mit einem Dienst (Infrastructure as a Service, IaaS).</span><span class="sxs-lookup"><span data-stu-id="bcef8-106">The **Disable-AzVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="bcef8-107">Dieses Cmdlet wird nur auf virtuellen Windows-Computern und nicht auf virtuellen Linux-Computern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bcef8-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="bcef8-108">Dieses Cmdlet installiert eine Erweiterung auf dem virtuellen Computer, um die Verschlüsselung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="bcef8-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="bcef8-109">Wenn der Parameter *Name* nicht angegeben ist, wird eine Erweiterung mit dem Standardnamen "AzureDiskEncryption für Windows VMS" erstellt.</span><span class="sxs-lookup"><span data-stu-id="bcef8-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="bcef8-110">Vorsicht: Dieses Cmdlet startet den virtuellen Computer neu.</span><span class="sxs-lookup"><span data-stu-id="bcef8-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="bcef8-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bcef8-111">EXAMPLES</span></span>

### <span data-ttu-id="bcef8-112">Beispiel 1: Deaktivieren der Verschlüsselung für alle Volumes auf einem virtuellen Windows-Computer</span><span class="sxs-lookup"><span data-stu-id="bcef8-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="bcef8-113">Mit diesem Befehl wird die Verschlüsselung für Volumes des Typs alle für den virtuellen Computer mit dem Namen VM002 deaktiviert, der zur Ressourcengruppe mit dem Namen Group001 gehört.</span><span class="sxs-lookup"><span data-stu-id="bcef8-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="bcef8-114">Da der Parameter *volumetype* nicht angegeben ist, legt das Cmdlet den Wert auf alle fest.</span><span class="sxs-lookup"><span data-stu-id="bcef8-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="bcef8-115">Beispiel 2: Deaktivieren der Verschlüsselung für Daten-Volumes auf einem virtuellen Windows-Computer</span><span class="sxs-lookup"><span data-stu-id="bcef8-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002";
PS C:\> $VMName = "VM004";
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group002" -VMName "VM004" -VolumeType "Data"
```

<span data-ttu-id="bcef8-116">Mit diesem Befehl wird die Verschlüsselung für Volumes vom Typ Data für den virtuellen Computer mit dem Namen VM004 deaktiviert, der zur Ressourcengruppe mit dem Namen Group002 gehört.</span><span class="sxs-lookup"><span data-stu-id="bcef8-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="bcef8-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="bcef8-117">PARAMETERS</span></span>

### <span data-ttu-id="bcef8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcef8-118">-DefaultProfile</span></span>
<span data-ttu-id="bcef8-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bcef8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcef8-120">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="bcef8-120">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="bcef8-121">Gibt an, dass dieses Cmdlet die automatische Aktualisierung der Nebenversion der Erweiterung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="bcef8-121">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcef8-122">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="bcef8-122">-ExtensionPublisherName</span></span>
<span data-ttu-id="bcef8-123">Der Name des Erweiterungs Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="bcef8-123">The extension publisher name.</span></span> <span data-ttu-id="bcef8-124">Geben Sie diesen Parameter nur an, um den Standardwert "Microsoft. Azure. Security" zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="bcef8-124">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcef8-125">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="bcef8-125">-ExtensionType</span></span>
<span data-ttu-id="bcef8-126">Der Erweiterungstyp.</span><span class="sxs-lookup"><span data-stu-id="bcef8-126">The extension type.</span></span> <span data-ttu-id="bcef8-127">Geben Sie diesen Parameter an, um den Standardwert "AzureDiskEncryption" für Windows-VMS und "AzureDiskEncryptionForLinux" für Linux-VMs zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="bcef8-127">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcef8-128">-Force</span><span class="sxs-lookup"><span data-stu-id="bcef8-128">-Force</span></span>
<span data-ttu-id="bcef8-129">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="bcef8-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bcef8-130">-Name</span><span class="sxs-lookup"><span data-stu-id="bcef8-130">-Name</span></span>
<span data-ttu-id="bcef8-131">Gibt an der Name der Azure Resource Manager (Arm)-Ressource, die die Erweiterung darstellt.</span><span class="sxs-lookup"><span data-stu-id="bcef8-131">Specifes the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="bcef8-132">Wenn dieser Parameter nicht angegeben wird, ist dieses Cmdlet standardmäßig auf "AzureDiskEncryption für Windows-VMS" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bcef8-132">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcef8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcef8-133">-ResourceGroupName</span></span>
<span data-ttu-id="bcef8-134">Gibt den Ressourcengruppennamen der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="bcef8-134">Specifies the resource group name of the virtual machine.</span></span>

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

### <span data-ttu-id="bcef8-135">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="bcef8-135">-TypeHandlerVersion</span></span>
<span data-ttu-id="bcef8-136">Gibt die Version der Verschlüsselungs Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="bcef8-136">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="bcef8-137">Wenn Sie keinen Wert für diesen Parameter angeben, wird die neueste Version der Erweiterung verwendet.</span><span class="sxs-lookup"><span data-stu-id="bcef8-137">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcef8-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="bcef8-138">-VMName</span></span>
<span data-ttu-id="bcef8-139">Gibt den Namen des virtuellen Computers an, auf dem dieses Cmdlet die Verschlüsselung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="bcef8-139">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcef8-140">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="bcef8-140">-VolumeType</span></span>
<span data-ttu-id="bcef8-141">Gibt den Typ der virtuellen Maschinen-Volumes an, um den Verschlüsselungsvorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="bcef8-141">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="bcef8-142">Bei Windows-virtuellen Computern sind gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="bcef8-142">For Windows virtual machines, valid values are:</span></span> 

- <span data-ttu-id="bcef8-143">Alle</span><span class="sxs-lookup"><span data-stu-id="bcef8-143">All</span></span>
- <span data-ttu-id="bcef8-144">OS</span><span class="sxs-lookup"><span data-stu-id="bcef8-144">OS</span></span>
- <span data-ttu-id="bcef8-145">Daten.</span><span class="sxs-lookup"><span data-stu-id="bcef8-145">Data.</span></span>
<span data-ttu-id="bcef8-146">Wenn Sie keinen Wert für diesen Parameter angeben, lautet der Standardwert alle.</span><span class="sxs-lookup"><span data-stu-id="bcef8-146">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="bcef8-147">Die Option "Verschlüsselung deaktivieren" wird derzeit für Linux nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bcef8-147">Disable encryption is not currently supported for Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcef8-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bcef8-148">-Confirm</span></span>
<span data-ttu-id="bcef8-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bcef8-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcef8-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcef8-150">-WhatIf</span></span>
<span data-ttu-id="bcef8-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bcef8-151">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="bcef8-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bcef8-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcef8-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcef8-153">CommonParameters</span></span>
<span data-ttu-id="bcef8-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcef8-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcef8-155">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcef8-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcef8-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bcef8-156">INPUTS</span></span>

### <span data-ttu-id="bcef8-157">Keine</span><span class="sxs-lookup"><span data-stu-id="bcef8-157">None</span></span>
<span data-ttu-id="bcef8-158">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="bcef8-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bcef8-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bcef8-159">OUTPUTS</span></span>

### <span data-ttu-id="bcef8-160">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="bcef8-160">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="bcef8-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="bcef8-161">NOTES</span></span>

## <span data-ttu-id="bcef8-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bcef8-162">RELATED LINKS</span></span>

[<span data-ttu-id="bcef8-163">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="bcef8-163">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="bcef8-164">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="bcef8-164">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="bcef8-165">Satz-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="bcef8-165">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


