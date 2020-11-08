---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
ms.openlocfilehash: a18e91a147e60ddc54caacccd8c63f3568bfe2eb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004825"
---
# <span data-ttu-id="17321-101">Set-AzVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="17321-101">Set-AzVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="17321-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="17321-102">SYNOPSIS</span></span>
<span data-ttu-id="17321-103">Aktiviert die Datenträgerverschlüsselung auf einem VM-Skalierungs Satz.</span><span class="sxs-lookup"><span data-stu-id="17321-103">Enables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="17321-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="17321-104">SYNTAX</span></span>

```
Set-AzVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="17321-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17321-105">DESCRIPTION</span></span>
<span data-ttu-id="17321-106">Das Cmdlet " **Satz-AzVmssDiskEncryptionExtension** " ermöglicht die Verschlüsselung auf einem VM-Skalierungs Satz.</span><span class="sxs-lookup"><span data-stu-id="17321-106">The **Set-AzVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span> <span data-ttu-id="17321-107">Dieses Cmdlet ermöglicht die Verschlüsselung durch Installieren der Festplatten Verschlüsselungs Erweiterung auf dem VM-Skalierungs Satz.</span><span class="sxs-lookup"><span data-stu-id="17321-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>

<span data-ttu-id="17321-108">Bei virtuellen Linux-Computern muss der *volumetype* -Parameter vorhanden sein und auf "Data" gesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="17321-108">For Linux virtual machines, the *VolumeType* parameter must be present and must be set to "Data"</span></span>

## <span data-ttu-id="17321-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="17321-109">EXAMPLES</span></span>

### <span data-ttu-id="17321-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="17321-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="17321-111">Mit diesem Befehl wird die Verschlüsselung auf allen Datenträgern aller Windows-VMs in einem VM-Skalierungs Satz aktiviert.</span><span class="sxs-lookup"><span data-stu-id="17321-111">This command enables encryption on all disks of all Windows VMs in a VM scale set.</span></span>

### <span data-ttu-id="17321-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="17321-112">Example 2</span></span>
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

<span data-ttu-id="17321-113">Mit diesem Befehl wird die Verschlüsselung auf den Datenträgern aller Linux-VMs in einem VM-Skalierungs Satz aktiviert.</span><span class="sxs-lookup"><span data-stu-id="17321-113">This command enables encryption on the data disks of all Linux VMs in a VM scale set.</span></span>

## <span data-ttu-id="17321-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="17321-114">PARAMETERS</span></span>

### <span data-ttu-id="17321-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17321-115">-DefaultProfile</span></span>
<span data-ttu-id="17321-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="17321-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17321-117">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="17321-117">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="17321-118">Deaktivieren der automatischen Aktualisierung von Nebenversionen</span><span class="sxs-lookup"><span data-stu-id="17321-118">Disable auto-upgrade of minor version</span></span>

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

### <span data-ttu-id="17321-119">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="17321-119">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="17321-120">Die Quelle des keyvaults, in dem der generierte Verschlüsselungsschlüssel gespeichert wird</span><span class="sxs-lookup"><span data-stu-id="17321-120">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="17321-121">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="17321-121">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="17321-122">Die URL des keyvaults, in dem der generierte Verschlüsselungsschlüssel gespeichert wird</span><span class="sxs-lookup"><span data-stu-id="17321-122">URL of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="17321-123">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="17321-123">-ExtensionName</span></span>
<span data-ttu-id="17321-124">Der Name der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="17321-124">The extension name.</span></span>
<span data-ttu-id="17321-125">Wenn dieser Parameter nicht angegeben ist, werden die Standardwerte AzureDiskEncryption für Windows VMS und AzureDiskEncryptionForLinux für Linux VMs verwendet.</span><span class="sxs-lookup"><span data-stu-id="17321-125">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

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

### <span data-ttu-id="17321-126">-Force</span><span class="sxs-lookup"><span data-stu-id="17321-126">-Force</span></span>
<span data-ttu-id="17321-127">So erzwingen Sie die Aktivierung der Verschlüsselung auf dem Skalierungs Satz für virtuelle Maschinen</span><span class="sxs-lookup"><span data-stu-id="17321-127">To force enabling encryption on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="17321-128">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="17321-128">-ForceUpdate</span></span>
<span data-ttu-id="17321-129">Generieren einer Kategorie für die Erzwingung des Updates</span><span class="sxs-lookup"><span data-stu-id="17321-129">Generate a tag for force update.</span></span>  <span data-ttu-id="17321-130">Dies sollte angegeben werden, um wiederholte Verschlüsselungsvorgänge für denselben virtuellen Computer durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="17321-130">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="17321-131">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="17321-131">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="17321-132">Keyencryption-Algorithmus zum Verschlüsseln des Volume-Verschlüsselungsschlüssels</span><span class="sxs-lookup"><span data-stu-id="17321-132">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

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

### <span data-ttu-id="17321-133">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="17321-133">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="17321-134">Keyvault-URL mit Versionsverwaltung des KeyEncryptionKey, der zum Verschlüsseln des Datenträger Verschlüsselungsschlüssels verwendet wird</span><span class="sxs-lookup"><span data-stu-id="17321-134">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="17321-135">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="17321-135">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="17321-136">Die KeyEncryptionKey des keyvaults, die die zum Verschlüsseln des Datenträger Verschlüsselungsschlüssels verwendete</span><span class="sxs-lookup"><span data-stu-id="17321-136">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="17321-137">-Passphrase</span><span class="sxs-lookup"><span data-stu-id="17321-137">-Passphrase</span></span>
<span data-ttu-id="17321-138">Die in Parametern angegebene Passphrase.</span><span class="sxs-lookup"><span data-stu-id="17321-138">The passphrase specified in parameters.</span></span>
<span data-ttu-id="17321-139">Dieser Parameter funktioniert nur für Linux-VM.</span><span class="sxs-lookup"><span data-stu-id="17321-139">This parameter only works for Linux VM.</span></span>

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

### <span data-ttu-id="17321-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17321-140">-ResourceGroupName</span></span>
<span data-ttu-id="17321-141">Der Ressourcengruppenname, zu dem der VM-Skalierungs Satz gehört</span><span class="sxs-lookup"><span data-stu-id="17321-141">The resource group name to which the VM Scale Set belongs to</span></span>

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

### <span data-ttu-id="17321-142">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="17321-142">-TypeHandlerVersion</span></span>
<span data-ttu-id="17321-143">Die Type Handler-Version.</span><span class="sxs-lookup"><span data-stu-id="17321-143">The type handler version.</span></span>

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

### <span data-ttu-id="17321-144">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="17321-144">-VMScaleSetName</span></span>
<span data-ttu-id="17321-145">Name des Skalierungs Satzes für virtuelle Maschinen</span><span class="sxs-lookup"><span data-stu-id="17321-145">Name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="17321-146">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="17321-146">-VolumeType</span></span>
<span data-ttu-id="17321-147">Gibt den Typ der Volumes für virtuelle Maschinen an, für die der Verschlüsselungsvorgang ausgeführt werden soll: Betriebssystem, Daten oder alle.</span><span class="sxs-lookup"><span data-stu-id="17321-147">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="17321-148">Linux: der **volumetype** -Parameter muss vorhanden sein und muss auf Data gesetzt sein.</span><span class="sxs-lookup"><span data-stu-id="17321-148">Linux: The **VolumeType** parameter must be present and must be set to Data.</span></span> 

<span data-ttu-id="17321-149">Windows: der Parameter **volumetype** , falls vorhanden, muss entweder auf alle oder auf das Betriebssystem eingestellt sein.</span><span class="sxs-lookup"><span data-stu-id="17321-149">Windows: The **VolumeType** parameter, if present, must be set to either All or OS.</span></span> <span data-ttu-id="17321-150">Wenn der Parameter **volumetype** ausgelassen wird, wird standardmäßig "alle" verwendet.</span><span class="sxs-lookup"><span data-stu-id="17321-150">If the **VolumeType** parameter is omitted it defaults to "All".</span></span>


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

### <span data-ttu-id="17321-151">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="17321-151">-Confirm</span></span>
<span data-ttu-id="17321-152">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="17321-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17321-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17321-153">-WhatIf</span></span>
<span data-ttu-id="17321-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="17321-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17321-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="17321-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17321-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17321-156">CommonParameters</span></span>
<span data-ttu-id="17321-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17321-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17321-158">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17321-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17321-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="17321-159">INPUTS</span></span>

### <span data-ttu-id="17321-160">System. String</span><span class="sxs-lookup"><span data-stu-id="17321-160">System.String</span></span>

### <span data-ttu-id="17321-161">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="17321-161">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="17321-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="17321-162">OUTPUTS</span></span>

### <span data-ttu-id="17321-163">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineScaleSetExtension</span><span class="sxs-lookup"><span data-stu-id="17321-163">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="17321-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="17321-164">NOTES</span></span>

## <span data-ttu-id="17321-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="17321-165">RELATED LINKS</span></span>
