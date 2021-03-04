---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
ms.openlocfilehash: 7f163a80efe4e10f0107298351c59a72bfaaceb0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944218"
---
# <span data-ttu-id="0041d-101">Set-AzVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="0041d-101">Set-AzVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="0041d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0041d-102">SYNOPSIS</span></span>
<span data-ttu-id="0041d-103">Aktiviert die Datenträgerverschlüsselung für einen VM-Skalierungssatz.</span><span class="sxs-lookup"><span data-stu-id="0041d-103">Enables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="0041d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0041d-104">SYNTAX</span></span>

```
Set-AzVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0041d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0041d-105">DESCRIPTION</span></span>
<span data-ttu-id="0041d-106">Das **Cmdlet Set-AzVmssDiskEncryptionExtension** ermöglicht die Verschlüsselung für einen VM-Skalierungssatz.</span><span class="sxs-lookup"><span data-stu-id="0041d-106">The **Set-AzVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span> <span data-ttu-id="0041d-107">Dieses Cmdlet ermöglicht die Verschlüsselung, indem die Datenträgerverschlüsselungserweiterung im VM-Skalierungssatz installiert wird.</span><span class="sxs-lookup"><span data-stu-id="0041d-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>

<span data-ttu-id="0041d-108">Bei virtuellen Linux-Computern muss *der Parameter VolumeType* vorhanden sein und auf "Daten" festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="0041d-108">For Linux virtual machines, the *VolumeType* parameter must be present and must be set to "Data"</span></span>

## <span data-ttu-id="0041d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0041d-109">EXAMPLES</span></span>

### <span data-ttu-id="0041d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0041d-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="0041d-111">Dieser Befehl ermöglicht die Verschlüsselung auf allen Datenträgern aller Windows-VMs in einem VM-Skalierungssatz.</span><span class="sxs-lookup"><span data-stu-id="0041d-111">This command enables encryption on all disks of all Windows VMs in a VM scale set.</span></span>

### <span data-ttu-id="0041d-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0041d-112">Example 2</span></span>
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

<span data-ttu-id="0041d-113">Dieser Befehl ermöglicht die Verschlüsselung auf den Datenträgern aller Linux-VMs in einem VM-Skalierungssatz.</span><span class="sxs-lookup"><span data-stu-id="0041d-113">This command enables encryption on the data disks of all Linux VMs in a VM scale set.</span></span>

## <span data-ttu-id="0041d-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0041d-114">PARAMETERS</span></span>

### <span data-ttu-id="0041d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0041d-115">-DefaultProfile</span></span>
<span data-ttu-id="0041d-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0041d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0041d-117">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="0041d-117">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="0041d-118">Deaktivieren des automatischen Upgrades der Nebenversion</span><span class="sxs-lookup"><span data-stu-id="0041d-118">Disable auto-upgrade of minor version</span></span>

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

### <span data-ttu-id="0041d-119">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="0041d-119">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="0041d-120">ResourceID des KeyVault-</span><span class="sxs-lookup"><span data-stu-id="0041d-120">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="0041d-121">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="0041d-121">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="0041d-122">URL des KeyVault, in dem der generierte Verschlüsselungsschlüssel platziert wird</span><span class="sxs-lookup"><span data-stu-id="0041d-122">URL of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="0041d-123">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="0041d-123">-ExtensionName</span></span>
<span data-ttu-id="0041d-124">Der Erweiterungsname.</span><span class="sxs-lookup"><span data-stu-id="0041d-124">The extension name.</span></span>
<span data-ttu-id="0041d-125">Wenn dieser Parameter nicht angegeben ist, werden standardmäßig AzureDiskEncryption für Windows VMs und AzureDiskEncryptionForLinux für Linux VMs verwendet.</span><span class="sxs-lookup"><span data-stu-id="0041d-125">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

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

### <span data-ttu-id="0041d-126">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="0041d-126">-Force</span></span>
<span data-ttu-id="0041d-127">So erzwingen Sie die Aktivierung der Verschlüsselung für den Skalierungssatz des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="0041d-127">To force enabling encryption on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="0041d-128">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="0041d-128">-ForceUpdate</span></span>
<span data-ttu-id="0041d-129">Generieren Sie ein Tag für das Erzwingen der Aktualisierung.</span><span class="sxs-lookup"><span data-stu-id="0041d-129">Generate a tag for force update.</span></span>  <span data-ttu-id="0041d-130">Dies sollte für wiederholte Verschlüsselungsvorgänge auf derselben VM verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0041d-130">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="0041d-131">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="0041d-131">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="0041d-132">KeyEncryption Algorithm used to encrypt the volume encryption key</span><span class="sxs-lookup"><span data-stu-id="0041d-132">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

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

### <span data-ttu-id="0041d-133">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="0041d-133">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="0041d-134">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span><span class="sxs-lookup"><span data-stu-id="0041d-134">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="0041d-135">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="0041d-135">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="0041d-136">ResourceID des KeyVault, das den KeyEncryptionKey enthält, der zum Verschlüsseln des Datenträgerverschlüsselungsschlüssels verwendet wird</span><span class="sxs-lookup"><span data-stu-id="0041d-136">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="0041d-137">-Passphrase</span><span class="sxs-lookup"><span data-stu-id="0041d-137">-Passphrase</span></span>
<span data-ttu-id="0041d-138">Die in Parametern angegebene Passphrase.</span><span class="sxs-lookup"><span data-stu-id="0041d-138">The passphrase specified in parameters.</span></span>
<span data-ttu-id="0041d-139">Dieser Parameter funktioniert nur für Linux VM.</span><span class="sxs-lookup"><span data-stu-id="0041d-139">This parameter only works for Linux VM.</span></span>

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

### <span data-ttu-id="0041d-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0041d-140">-ResourceGroupName</span></span>
<span data-ttu-id="0041d-141">Der Ressourcengruppenname, zu dem der VM-Skalierungssatz gehört</span><span class="sxs-lookup"><span data-stu-id="0041d-141">The resource group name to which the VM Scale Set belongs to</span></span>

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

### <span data-ttu-id="0041d-142">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="0041d-142">-TypeHandlerVersion</span></span>
<span data-ttu-id="0041d-143">Die Typhandlerversion.</span><span class="sxs-lookup"><span data-stu-id="0041d-143">The type handler version.</span></span>

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

### <span data-ttu-id="0041d-144">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="0041d-144">-VMScaleSetName</span></span>
<span data-ttu-id="0041d-145">Name des Skalierungssets für virtuelle Computer</span><span class="sxs-lookup"><span data-stu-id="0041d-145">Name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="0041d-146">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="0041d-146">-VolumeType</span></span>
<span data-ttu-id="0041d-147">Gibt den Typ der Virtuellen Computervolumes an, auf denen verschlüsselungsvorgang ausgeführt werden soll: Betriebssystem, Daten oder Alle.</span><span class="sxs-lookup"><span data-stu-id="0041d-147">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="0041d-148">Linux: Der **Parameter VolumeType** muss vorhanden sein und auf Daten festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="0041d-148">Linux: The **VolumeType** parameter must be present and must be set to Data.</span></span> 

<span data-ttu-id="0041d-149">Windows: Der **Parameter VolumeType** muss, sofern vorhanden, entweder auf Alle oder Betriebssystem festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="0041d-149">Windows: The **VolumeType** parameter, if present, must be set to either All or OS.</span></span> <span data-ttu-id="0041d-150">Fehlt der **Parameter VolumeType,** wird standardmäßig "Alles" verwendet.</span><span class="sxs-lookup"><span data-stu-id="0041d-150">If the **VolumeType** parameter is omitted it defaults to "All".</span></span>


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

### <span data-ttu-id="0041d-151">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0041d-151">-Confirm</span></span>
<span data-ttu-id="0041d-152">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0041d-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0041d-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0041d-153">-WhatIf</span></span>
<span data-ttu-id="0041d-154">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0041d-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0041d-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0041d-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0041d-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0041d-156">CommonParameters</span></span>
<span data-ttu-id="0041d-157">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0041d-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0041d-158">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0041d-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0041d-159">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0041d-159">INPUTS</span></span>

### <span data-ttu-id="0041d-160">System.String</span><span class="sxs-lookup"><span data-stu-id="0041d-160">System.String</span></span>

### <span data-ttu-id="0041d-161">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0041d-161">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0041d-162">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0041d-162">OUTPUTS</span></span>

### <span data-ttu-id="0041d-163">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span><span class="sxs-lookup"><span data-stu-id="0041d-163">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="0041d-164">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0041d-164">NOTES</span></span>

## <span data-ttu-id="0041d-165">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0041d-165">RELATED LINKS</span></span>
