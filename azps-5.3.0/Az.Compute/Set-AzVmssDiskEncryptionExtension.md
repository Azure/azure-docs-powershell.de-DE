---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
ms.openlocfilehash: a18e91a147e60ddc54caacccd8c63f3568bfe2eb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470830"
---
# <span data-ttu-id="22a6a-101">Set-AzVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="22a6a-101">Set-AzVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="22a6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22a6a-102">SYNOPSIS</span></span>
<span data-ttu-id="22a6a-103">Ermöglicht die Datenträgerverschlüsselung für einen VM-Skalierungssatz.</span><span class="sxs-lookup"><span data-stu-id="22a6a-103">Enables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="22a6a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22a6a-104">SYNTAX</span></span>

```
Set-AzVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22a6a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="22a6a-105">DESCRIPTION</span></span>
<span data-ttu-id="22a6a-106">Das **Cmdlet Set-AzVmssDiskEncryptionExtension** ermöglicht die Verschlüsselung auf einem VM-Skalierungssatz.</span><span class="sxs-lookup"><span data-stu-id="22a6a-106">The **Set-AzVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span> <span data-ttu-id="22a6a-107">Dieses Cmdlet ermöglicht die Verschlüsselung durch Installieren der Datenträgerverschlüsselungserweiterung auf dem VM-Skalierungssatz.</span><span class="sxs-lookup"><span data-stu-id="22a6a-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>

<span data-ttu-id="22a6a-108">Bei virtuellen Linux-Computern muss *der VolumeType-Parameter* vorhanden sein und auf "Data" festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="22a6a-108">For Linux virtual machines, the *VolumeType* parameter must be present and must be set to "Data"</span></span>

## <span data-ttu-id="22a6a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="22a6a-109">EXAMPLES</span></span>

### <span data-ttu-id="22a6a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="22a6a-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="22a6a-111">Dieser Befehl ermöglicht die Verschlüsselung auf allen Datenträgern aller Windows-VMs in einem VM-Skalierungssatz.</span><span class="sxs-lookup"><span data-stu-id="22a6a-111">This command enables encryption on all disks of all Windows VMs in a VM scale set.</span></span>

### <span data-ttu-id="22a6a-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="22a6a-112">Example 2</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "Data"

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
 -VolumeType $volumeType
```

<span data-ttu-id="22a6a-113">Dieser Befehl ermöglicht die Verschlüsselung der Datendatenträger aller Linux-VMs in einem VM-Skalierungssatz.</span><span class="sxs-lookup"><span data-stu-id="22a6a-113">This command enables encryption on the data disks of all Linux VMs in a VM scale set.</span></span>

## <span data-ttu-id="22a6a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22a6a-114">PARAMETERS</span></span>

### <span data-ttu-id="22a6a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22a6a-115">-DefaultProfile</span></span>
<span data-ttu-id="22a6a-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="22a6a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22a6a-117">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="22a6a-117">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="22a6a-118">Deaktivieren des automatischen Upgrades der Nebenversion</span><span class="sxs-lookup"><span data-stu-id="22a6a-118">Disable auto-upgrade of minor version</span></span>

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

### <span data-ttu-id="22a6a-119">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="22a6a-119">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="22a6a-120">ResourceID des KeyVault-</span><span class="sxs-lookup"><span data-stu-id="22a6a-120">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22a6a-121">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="22a6a-121">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="22a6a-122">DIE URL des KeyVault, in dem der generierte Verschlüsselungsschlüssel platziert wird</span><span class="sxs-lookup"><span data-stu-id="22a6a-122">URL of the KeyVault where generated encryption key will be placed to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22a6a-123">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="22a6a-123">-ExtensionName</span></span>
<span data-ttu-id="22a6a-124">Der Erweiterungsname.</span><span class="sxs-lookup"><span data-stu-id="22a6a-124">The extension name.</span></span>
<span data-ttu-id="22a6a-125">Wenn dieser Parameter nicht angegeben wird, werden die Standardwerte "AzureDiskEncryption" für Windows-VMs und "AzureDiskEncryptionForLinux für Linux-VMs" verwendet.</span><span class="sxs-lookup"><span data-stu-id="22a6a-125">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

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

### <span data-ttu-id="22a6a-126">-Force</span><span class="sxs-lookup"><span data-stu-id="22a6a-126">-Force</span></span>
<span data-ttu-id="22a6a-127">So erzwingen Sie die Aktivierung der Verschlüsselung für den Skalierungssatz des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="22a6a-127">To force enabling encryption on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="22a6a-128">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="22a6a-128">-ForceUpdate</span></span>
<span data-ttu-id="22a6a-129">Generieren Sie ein Tag, um eine Aktualisierung zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="22a6a-129">Generate a tag for force update.</span></span>  <span data-ttu-id="22a6a-130">Dies sollte für wiederholte Verschlüsselungsvorgänge auf derselben VM verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="22a6a-130">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="22a6a-131">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="22a6a-131">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="22a6a-132">KeyEncryption Algorithm used to encrypt the volume encryption key</span><span class="sxs-lookup"><span data-stu-id="22a6a-132">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22a6a-133">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="22a6a-133">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="22a6a-134">Versionsed KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span><span class="sxs-lookup"><span data-stu-id="22a6a-134">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="22a6a-135">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="22a6a-135">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="22a6a-136">ResourceID des KeyVault mit dem KeyEncryptionKey, der zum Verschlüsseln des Datenträgerverschlüsselungsschlüssels verwendet wird</span><span class="sxs-lookup"><span data-stu-id="22a6a-136">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="22a6a-137">-Passphrase</span><span class="sxs-lookup"><span data-stu-id="22a6a-137">-Passphrase</span></span>
<span data-ttu-id="22a6a-138">Die in Parametern angegebene Passphrase.</span><span class="sxs-lookup"><span data-stu-id="22a6a-138">The passphrase specified in parameters.</span></span>
<span data-ttu-id="22a6a-139">Dieser Parameter funktioniert nur für Linux VM.</span><span class="sxs-lookup"><span data-stu-id="22a6a-139">This parameter only works for Linux VM.</span></span>

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

### <span data-ttu-id="22a6a-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22a6a-140">-ResourceGroupName</span></span>
<span data-ttu-id="22a6a-141">Der Name der Ressourcengruppe, zu der der VM Scale Set gehört</span><span class="sxs-lookup"><span data-stu-id="22a6a-141">The resource group name to which the VM Scale Set belongs to</span></span>

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

### <span data-ttu-id="22a6a-142">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="22a6a-142">-TypeHandlerVersion</span></span>
<span data-ttu-id="22a6a-143">Die Typhandlerversion.</span><span class="sxs-lookup"><span data-stu-id="22a6a-143">The type handler version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22a6a-144">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="22a6a-144">-VMScaleSetName</span></span>
<span data-ttu-id="22a6a-145">Name des Skalierungssets für den virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="22a6a-145">Name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22a6a-146">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="22a6a-146">-VolumeType</span></span>
<span data-ttu-id="22a6a-147">Gibt den Typ der Virtuellen Computervolumes an, für die Verschlüsselungsvorgang ausgeführt werden soll: Betriebssystem, Daten oder Alle.</span><span class="sxs-lookup"><span data-stu-id="22a6a-147">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="22a6a-148">Linux: Der **Parameter "VolumeType"** muss vorhanden sein und auf "Data" festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="22a6a-148">Linux: The **VolumeType** parameter must be present and must be set to Data.</span></span> 

<span data-ttu-id="22a6a-149">Windows: Der **VolumeType-Parameter** muss , sofern vorhanden, auf "All" oder "OS" festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="22a6a-149">Windows: The **VolumeType** parameter, if present, must be set to either All or OS.</span></span> <span data-ttu-id="22a6a-150">Wenn der **Parameter "VolumeType"** nicht angegeben wird, wird standardmäßig "All" verwendet.</span><span class="sxs-lookup"><span data-stu-id="22a6a-150">If the **VolumeType** parameter is omitted it defaults to "All".</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22a6a-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22a6a-151">-Confirm</span></span>
<span data-ttu-id="22a6a-152">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="22a6a-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22a6a-153">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="22a6a-153">-WhatIf</span></span>
<span data-ttu-id="22a6a-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="22a6a-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22a6a-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="22a6a-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22a6a-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22a6a-156">CommonParameters</span></span>
<span data-ttu-id="22a6a-157">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22a6a-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22a6a-158">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22a6a-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22a6a-159">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="22a6a-159">INPUTS</span></span>

### <span data-ttu-id="22a6a-160">System.String</span><span class="sxs-lookup"><span data-stu-id="22a6a-160">System.String</span></span>

### <span data-ttu-id="22a6a-161">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="22a6a-161">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="22a6a-162">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="22a6a-162">OUTPUTS</span></span>

### <span data-ttu-id="22a6a-163">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span><span class="sxs-lookup"><span data-stu-id="22a6a-163">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="22a6a-164">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="22a6a-164">NOTES</span></span>

## <span data-ttu-id="22a6a-165">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="22a6a-165">RELATED LINKS</span></span>
