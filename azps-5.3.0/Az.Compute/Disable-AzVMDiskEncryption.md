---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/disable-azvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
ms.openlocfilehash: 1aad073ebd1f1a5e14abfd728ba6e6266a2d6fb8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473135"
---
# <span data-ttu-id="41fa7-101">Disable-AzVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="41fa7-101">Disable-AzVMDiskEncryption</span></span>

## <span data-ttu-id="41fa7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41fa7-102">SYNOPSIS</span></span>
<span data-ttu-id="41fa7-103">Deaktiviert die Verschlüsselung auf einem virtuellen IaaS-Computer.</span><span class="sxs-lookup"><span data-stu-id="41fa7-103">Disables encryption on an IaaS virtual machine.</span></span>

## <span data-ttu-id="41fa7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41fa7-104">SYNTAX</span></span>

```
Disable-AzVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41fa7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="41fa7-105">DESCRIPTION</span></span>
<span data-ttu-id="41fa7-106">Das **Cmdlet "Disable-AzVMDiskEncryption"** deaktiviert die Verschlüsselung für eine Infrastruktur als virtuellen Dienstcomputer (IaaS).</span><span class="sxs-lookup"><span data-stu-id="41fa7-106">The **Disable-AzVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="41fa7-107">Dieses Cmdlet wird nur auf virtuellen Computern von Windows und nicht auf virtuellen Linux-Computern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="41fa7-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="41fa7-108">Dieses Cmdlet installiert eine Erweiterung auf dem virtuellen Computer, um die Verschlüsselung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="41fa7-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="41fa7-109">Wenn der *Parameter "Name"* nicht angegeben wird, wird eine Erweiterung mit dem Standardnamen "AzureDiskEncryption for Windows VMs" erstellt.</span><span class="sxs-lookup"><span data-stu-id="41fa7-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="41fa7-110">Vorsicht: Dieses Cmdlet startet den virtuellen Computer neu.</span><span class="sxs-lookup"><span data-stu-id="41fa7-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="41fa7-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="41fa7-111">EXAMPLES</span></span>

### <span data-ttu-id="41fa7-112">Beispiel 1: Deaktivieren der Verschlüsselung für alle Volumes auf einem virtuellen Windows-Computer</span><span class="sxs-lookup"><span data-stu-id="41fa7-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="41fa7-113">Mit diesem Befehl wird die Verschlüsselung für Typvolumen für den virtuellen Computer "VM002" deaktiviert, der zur Ressourcengruppe "Group001" gehört.</span><span class="sxs-lookup"><span data-stu-id="41fa7-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="41fa7-114">Da der *Parameter "VolumeType"* nicht angegeben wird, legt das Cmdlet den Wert auf "All" fest.</span><span class="sxs-lookup"><span data-stu-id="41fa7-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="41fa7-115">Beispiel 2: Deaktivieren der Verschlüsselung für Datenvolumes auf einem virtuellen Windows-Computer</span><span class="sxs-lookup"><span data-stu-id="41fa7-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002"
PS C:\> $VMName = "VM004"
PS C:\> $VolumeType = "Data"
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName $ResourceGroup -VMName $VMName -VolumeType $VolumeType
```

<span data-ttu-id="41fa7-116">Mit diesem Befehl wird die Verschlüsselung für Typdatenvolumen für den virtuellen Computer VM004 deaktiviert, der zur Ressourcengruppe "Group002" gehört.</span><span class="sxs-lookup"><span data-stu-id="41fa7-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="41fa7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41fa7-117">PARAMETERS</span></span>

### <span data-ttu-id="41fa7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41fa7-118">-DefaultProfile</span></span>
<span data-ttu-id="41fa7-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="41fa7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41fa7-120">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="41fa7-120">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="41fa7-121">Gibt an, dass dieses Cmdlet das automatische Upgrade der Nebenversion der Erweiterung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="41fa7-121">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41fa7-122">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="41fa7-122">-ExtensionPublisherName</span></span>
<span data-ttu-id="41fa7-123">Der Herausgebername der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="41fa7-123">The extension publisher name.</span></span> <span data-ttu-id="41fa7-124">Geben Sie diesen Parameter nur an, um den Standardwert von "Microsoft.Azure.Security" zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="41fa7-124">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="41fa7-125">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="41fa7-125">-ExtensionType</span></span>
<span data-ttu-id="41fa7-126">Der Erweiterungstyp.</span><span class="sxs-lookup"><span data-stu-id="41fa7-126">The extension type.</span></span> <span data-ttu-id="41fa7-127">Geben Sie diesen Parameter an, um den Standardwert von "AzureDiskEncryption" für Windows-VMs und "AzureDiskEncryptionForLinux" für Linux-VMs außer Kraft zu setzen.</span><span class="sxs-lookup"><span data-stu-id="41fa7-127">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="41fa7-128">-Force</span><span class="sxs-lookup"><span data-stu-id="41fa7-128">-Force</span></span>
<span data-ttu-id="41fa7-129">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="41fa7-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="41fa7-130">-Name</span><span class="sxs-lookup"><span data-stu-id="41fa7-130">-Name</span></span>
<span data-ttu-id="41fa7-131">Gibt den Namen der Azure Resource Manager (ARM) an, die die Erweiterung darstellt.</span><span class="sxs-lookup"><span data-stu-id="41fa7-131">Specifies the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="41fa7-132">Wenn dieser Parameter nicht angegeben wird, wird für dieses Cmdlet standardmäßig "AzureDiskEncryption for Windows VMs" verwendet.</span><span class="sxs-lookup"><span data-stu-id="41fa7-132">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41fa7-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41fa7-133">-ResourceGroupName</span></span>
<span data-ttu-id="41fa7-134">Gibt den Ressourcengruppennamen des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="41fa7-134">Specifies the resource group name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41fa7-135">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="41fa7-135">-TypeHandlerVersion</span></span>
<span data-ttu-id="41fa7-136">Gibt die Version der Verschlüsselungserweiterung an.</span><span class="sxs-lookup"><span data-stu-id="41fa7-136">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="41fa7-137">Wenn Sie keinen Wert für diesen Parameter angeben, wird die neueste Version der Erweiterung verwendet.</span><span class="sxs-lookup"><span data-stu-id="41fa7-137">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41fa7-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="41fa7-138">-VMName</span></span>
<span data-ttu-id="41fa7-139">Gibt den Namen des virtuellen Computers an, auf dem dieses Cmdlet die Verschlüsselung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="41fa7-139">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41fa7-140">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="41fa7-140">-VolumeType</span></span>
<span data-ttu-id="41fa7-141">Gibt den Typ der Volumen virtueller Computer an, um den Verschlüsselungsvorgang durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="41fa7-141">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="41fa7-142">Für virtuelle Computer von Windows gelten die gültigen Werte:</span><span class="sxs-lookup"><span data-stu-id="41fa7-142">For Windows virtual machines, valid values are:</span></span> 
- <span data-ttu-id="41fa7-143">Alle</span><span class="sxs-lookup"><span data-stu-id="41fa7-143">All</span></span>
- <span data-ttu-id="41fa7-144">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="41fa7-144">OS</span></span>
- <span data-ttu-id="41fa7-145">Daten.</span><span class="sxs-lookup"><span data-stu-id="41fa7-145">Data.</span></span>
<span data-ttu-id="41fa7-146">Wenn Sie keinen Wert für diesen Parameter angeben, ist der Standardwert "Alle".</span><span class="sxs-lookup"><span data-stu-id="41fa7-146">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="41fa7-147">Die Verschlüsselung deaktivieren wird derzeit für Linux nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="41fa7-147">Disable encryption is not currently supported for Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41fa7-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41fa7-148">-Confirm</span></span>
<span data-ttu-id="41fa7-149">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="41fa7-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41fa7-150">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="41fa7-150">-WhatIf</span></span>
<span data-ttu-id="41fa7-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="41fa7-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41fa7-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="41fa7-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41fa7-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41fa7-153">CommonParameters</span></span>
<span data-ttu-id="41fa7-154">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41fa7-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41fa7-155">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="41fa7-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41fa7-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="41fa7-156">INPUTS</span></span>

### <span data-ttu-id="41fa7-157">System.String</span><span class="sxs-lookup"><span data-stu-id="41fa7-157">System.String</span></span>

### <span data-ttu-id="41fa7-158">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="41fa7-158">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="41fa7-159">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="41fa7-159">OUTPUTS</span></span>

### <span data-ttu-id="41fa7-160">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="41fa7-160">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="41fa7-161">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="41fa7-161">NOTES</span></span>

## <span data-ttu-id="41fa7-162">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="41fa7-162">RELATED LINKS</span></span>

[<span data-ttu-id="41fa7-163">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="41fa7-163">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="41fa7-164">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="41fa7-164">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="41fa7-165">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="41fa7-165">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


