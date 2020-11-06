---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Disable-AzureRmVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Disable-AzureRmVMDiskEncryption.md
ms.openlocfilehash: 087ae12961d6bd9faf844221772b92c79362d13d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496645"
---
# <span data-ttu-id="1f75b-101">Disable-AzureRmVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="1f75b-101">Disable-AzureRmVMDiskEncryption</span></span>

## <span data-ttu-id="1f75b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1f75b-102">SYNOPSIS</span></span>
<span data-ttu-id="1f75b-103">Deaktiviert die Verschlüsselung auf einem virtuellen IaaS-Computer.</span><span class="sxs-lookup"><span data-stu-id="1f75b-103">Disables encryption on an IaaS virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f75b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f75b-104">SYNTAX</span></span>

```
Disable-AzureRmVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f75b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f75b-105">DESCRIPTION</span></span>
<span data-ttu-id="1f75b-106">Das Cmdlet **Disable-AzureRmVMDiskEncryption** deaktiviert die Verschlüsselung auf einem virtuellen Computer mit einem Dienst (Infrastructure as a Service, IaaS).</span><span class="sxs-lookup"><span data-stu-id="1f75b-106">The **Disable-AzureRmVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="1f75b-107">Dieses Cmdlet wird nur auf virtuellen Windows-Computern und nicht auf virtuellen Linux-Computern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1f75b-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="1f75b-108">Dieses Cmdlet installiert eine Erweiterung auf dem virtuellen Computer, um die Verschlüsselung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="1f75b-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="1f75b-109">Wenn der Parameter *Name* nicht angegeben ist, wird eine Erweiterung mit dem Standardnamen "AzureDiskEncryption für Windows VMS" erstellt.</span><span class="sxs-lookup"><span data-stu-id="1f75b-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="1f75b-110">Vorsicht: Dieses Cmdlet startet den virtuellen Computer neu.</span><span class="sxs-lookup"><span data-stu-id="1f75b-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="1f75b-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1f75b-111">EXAMPLES</span></span>

### <span data-ttu-id="1f75b-112">Beispiel 1: Deaktivieren der Verschlüsselung für alle Volumes auf einem virtuellen Windows-Computer</span><span class="sxs-lookup"><span data-stu-id="1f75b-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzureRMVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="1f75b-113">Mit diesem Befehl wird die Verschlüsselung für Volumes des Typs alle für den virtuellen Computer mit dem Namen VM002 deaktiviert, der zur Ressourcengruppe mit dem Namen Group001 gehört.</span><span class="sxs-lookup"><span data-stu-id="1f75b-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="1f75b-114">Da der Parameter *volumetype* nicht angegeben ist, legt das Cmdlet den Wert auf alle fest.</span><span class="sxs-lookup"><span data-stu-id="1f75b-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="1f75b-115">Beispiel 2: Deaktivieren der Verschlüsselung für Daten-Volumes auf einem virtuellen Windows-Computer</span><span class="sxs-lookup"><span data-stu-id="1f75b-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002";
PS C:\> $VMName = "VM004";
PS C:\> Disable-AzureRMVMDiskEncryption -ResourceGroupName "Group002" -VMName "VM004" -VolumeType "Data"
```

<span data-ttu-id="1f75b-116">Mit diesem Befehl wird die Verschlüsselung für Volumes vom Typ Data für den virtuellen Computer mit dem Namen VM004 deaktiviert, der zur Ressourcengruppe mit dem Namen Group002 gehört.</span><span class="sxs-lookup"><span data-stu-id="1f75b-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="1f75b-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f75b-117">PARAMETERS</span></span>

### <span data-ttu-id="1f75b-118">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="1f75b-118">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="1f75b-119">Gibt an, dass dieses Cmdlet die automatische Aktualisierung der Nebenversion der Erweiterung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="1f75b-119">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f75b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="1f75b-120">-Force</span></span>
<span data-ttu-id="1f75b-121">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="1f75b-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1f75b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1f75b-122">-Name</span></span>
<span data-ttu-id="1f75b-123">Gibt an der Name der Azure Resource Manager (Arm)-Ressource, die die Erweiterung darstellt.</span><span class="sxs-lookup"><span data-stu-id="1f75b-123">Specifes the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="1f75b-124">Wenn dieser Parameter nicht angegeben wird, ist dieses Cmdlet standardmäßig auf "AzureDiskEncryption für Windows-VMS" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1f75b-124">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

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

### <span data-ttu-id="1f75b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f75b-125">-ResourceGroupName</span></span>
<span data-ttu-id="1f75b-126">Gibt den Ressourcengruppennamen der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="1f75b-126">Specifies the resource group name of the virtual machine.</span></span>

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

### <span data-ttu-id="1f75b-127">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="1f75b-127">-TypeHandlerVersion</span></span>
<span data-ttu-id="1f75b-128">Gibt die Version der Verschlüsselungs Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="1f75b-128">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="1f75b-129">Wenn Sie keinen Wert für diesen Parameter angeben, wird die neueste Version der Erweiterung verwendet.</span><span class="sxs-lookup"><span data-stu-id="1f75b-129">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

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

### <span data-ttu-id="1f75b-130">-VMName</span><span class="sxs-lookup"><span data-stu-id="1f75b-130">-VMName</span></span>
<span data-ttu-id="1f75b-131">Gibt den Namen des virtuellen Computers an, auf dem dieses Cmdlet die Verschlüsselung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="1f75b-131">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

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

### <span data-ttu-id="1f75b-132">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="1f75b-132">-VolumeType</span></span>
<span data-ttu-id="1f75b-133">Gibt den Typ der virtuellen Maschinen-Volumes an, um den Verschlüsselungsvorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="1f75b-133">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="1f75b-134">Bei Windows-virtuellen Computern sind gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="1f75b-134">For Windows virtual machines, valid values are:</span></span> 

- <span data-ttu-id="1f75b-135">Alle</span><span class="sxs-lookup"><span data-stu-id="1f75b-135">All</span></span>
- <span data-ttu-id="1f75b-136">OS</span><span class="sxs-lookup"><span data-stu-id="1f75b-136">OS</span></span>
- <span data-ttu-id="1f75b-137">Daten.</span><span class="sxs-lookup"><span data-stu-id="1f75b-137">Data.</span></span>
<span data-ttu-id="1f75b-138">Wenn Sie keinen Wert für diesen Parameter angeben, lautet der Standardwert alle.</span><span class="sxs-lookup"><span data-stu-id="1f75b-138">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="1f75b-139">Die Option "Verschlüsselung deaktivieren" wird derzeit für Linux nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1f75b-139">Disable encryption is not currently supported for Linux.</span></span>

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

### <span data-ttu-id="1f75b-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1f75b-140">-Confirm</span></span>
<span data-ttu-id="1f75b-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1f75b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f75b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f75b-142">-WhatIf</span></span>
<span data-ttu-id="1f75b-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1f75b-143">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="1f75b-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1f75b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f75b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f75b-145">CommonParameters</span></span>
<span data-ttu-id="1f75b-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f75b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f75b-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f75b-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f75b-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1f75b-148">INPUTS</span></span>

### <span data-ttu-id="1f75b-149">Keine</span><span class="sxs-lookup"><span data-stu-id="1f75b-149">None</span></span>
<span data-ttu-id="1f75b-150">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="1f75b-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1f75b-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1f75b-151">OUTPUTS</span></span>

### <span data-ttu-id="1f75b-152">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="1f75b-152">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="1f75b-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="1f75b-153">NOTES</span></span>

## <span data-ttu-id="1f75b-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1f75b-154">RELATED LINKS</span></span>

[<span data-ttu-id="1f75b-155">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="1f75b-155">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="1f75b-156">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="1f75b-156">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="1f75b-157">Satz-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="1f75b-157">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


