---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssDiskEncryptionExtension.md
ms.openlocfilehash: aeac00806ef77d756dc8060b06f7baa995568fbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503017"
---
# <span data-ttu-id="2a91d-101">Set-AzureRmVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="2a91d-101">Set-AzureRmVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="2a91d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2a91d-102">SYNOPSIS</span></span>
<span data-ttu-id="2a91d-103">Aktiviert die Datenträgerverschlüsselung auf einem VM-Skalierungs Satz.</span><span class="sxs-lookup"><span data-stu-id="2a91d-103">Enables disk encryption on a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a91d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a91d-104">SYNTAX</span></span>

```
Set-AzureRmVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a91d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2a91d-105">DESCRIPTION</span></span>
<span data-ttu-id="2a91d-106">Das Cmdlet " **Satz-AzureRmVmssDiskEncryptionExtension** " ermöglicht die Verschlüsselung auf einem VM-Skalierungs Satz.</span><span class="sxs-lookup"><span data-stu-id="2a91d-106">The **Set-AzureRmVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span>
<span data-ttu-id="2a91d-107">Dieses Cmdlet ermöglicht die Verschlüsselung durch Installieren der Festplatten Verschlüsselungs Erweiterung auf dem VM-Skalierungs Satz.</span><span class="sxs-lookup"><span data-stu-id="2a91d-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>
<span data-ttu-id="2a91d-108">Wenn kein *Name* -Parameter angegeben ist, wird eine Erweiterung mit dem Standardnamen AzureDiskEncryption für virtuelle Computer installiert, auf denen das Windows-Betriebssystem oder AzureDiskEncryptionForLinux für Linux-Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2a91d-108">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>

## <span data-ttu-id="2a91d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2a91d-109">EXAMPLES</span></span>

### <span data-ttu-id="2a91d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2a91d-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
PS C:\> Set-AzureRmVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="2a91d-111">Mit diesem Befehl wird die Verschlüsselung auf allen Datenträgern aller VMS im VM-Skalierungs Satz aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2a91d-111">This command enables encryption on all disks of all VMs in the VM scale set.</span></span>

## <span data-ttu-id="2a91d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a91d-112">PARAMETERS</span></span>

### <span data-ttu-id="2a91d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a91d-113">-DefaultProfile</span></span>
<span data-ttu-id="2a91d-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2a91d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a91d-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="2a91d-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="2a91d-116">Deaktivieren der automatischen Aktualisierung von Nebenversionen</span><span class="sxs-lookup"><span data-stu-id="2a91d-116">Disable auto-upgrade of minor version</span></span>

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

### <span data-ttu-id="2a91d-117">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="2a91d-117">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="2a91d-118">Die Quelle des keyvaults, in dem der generierte Verschlüsselungsschlüssel gespeichert wird</span><span class="sxs-lookup"><span data-stu-id="2a91d-118">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="2a91d-119">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="2a91d-119">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="2a91d-120">Die URL des keyvaults, in dem der generierte Verschlüsselungsschlüssel gespeichert wird</span><span class="sxs-lookup"><span data-stu-id="2a91d-120">URL of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="2a91d-121">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="2a91d-121">-ExtensionName</span></span>
<span data-ttu-id="2a91d-122">Der Name der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="2a91d-122">The extension name.</span></span>
<span data-ttu-id="2a91d-123">Wenn dieser Parameter nicht angegeben ist, werden die Standardwerte AzureDiskEncryption für Windows VMS und AzureDiskEncryptionForLinux für Linux VMs verwendet.</span><span class="sxs-lookup"><span data-stu-id="2a91d-123">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

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

### <span data-ttu-id="2a91d-124">-Force</span><span class="sxs-lookup"><span data-stu-id="2a91d-124">-Force</span></span>
<span data-ttu-id="2a91d-125">So erzwingen Sie die Aktivierung der Verschlüsselung auf dem Skalierungs Satz für virtuelle Maschinen</span><span class="sxs-lookup"><span data-stu-id="2a91d-125">To force enabling encryption on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="2a91d-126">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="2a91d-126">-ForceUpdate</span></span>
<span data-ttu-id="2a91d-127">Generieren einer Kategorie für die Erzwingung des Updates</span><span class="sxs-lookup"><span data-stu-id="2a91d-127">Generate a tag for force update.</span></span>  <span data-ttu-id="2a91d-128">Dies sollte angegeben werden, um wiederholte Verschlüsselungsvorgänge für denselben virtuellen Computer durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="2a91d-128">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="2a91d-129">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="2a91d-129">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="2a91d-130">Keyencryption-Algorithmus zum Verschlüsseln des Volume-Verschlüsselungsschlüssels</span><span class="sxs-lookup"><span data-stu-id="2a91d-130">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

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

### <span data-ttu-id="2a91d-131">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="2a91d-131">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="2a91d-132">Keyvault-URL mit Versionsverwaltung des KeyEncryptionKey, der zum Verschlüsseln des Datenträger Verschlüsselungsschlüssels verwendet wird</span><span class="sxs-lookup"><span data-stu-id="2a91d-132">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="2a91d-133">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="2a91d-133">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="2a91d-134">Die KeyEncryptionKey des keyvaults, die die zum Verschlüsseln des Datenträger Verschlüsselungsschlüssels verwendete</span><span class="sxs-lookup"><span data-stu-id="2a91d-134">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="2a91d-135">-Passphrase</span><span class="sxs-lookup"><span data-stu-id="2a91d-135">-Passphrase</span></span>
<span data-ttu-id="2a91d-136">Die in Parametern angegebene Passphrase.</span><span class="sxs-lookup"><span data-stu-id="2a91d-136">The passphrase specified in parameters.</span></span>
<span data-ttu-id="2a91d-137">Dieser Parameter funktioniert nur für Linux-VM.</span><span class="sxs-lookup"><span data-stu-id="2a91d-137">This parameter only works for Linux VM.</span></span>

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

### <span data-ttu-id="2a91d-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a91d-138">-ResourceGroupName</span></span>
<span data-ttu-id="2a91d-139">Der Ressourcengruppenname, zu dem der VM-Skalierungs Satz gehört</span><span class="sxs-lookup"><span data-stu-id="2a91d-139">The resource group name to which the VM Scale Set belongs to</span></span>

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

### <span data-ttu-id="2a91d-140">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="2a91d-140">-TypeHandlerVersion</span></span>
<span data-ttu-id="2a91d-141">Die Type Handler-Version.</span><span class="sxs-lookup"><span data-stu-id="2a91d-141">The type handler version.</span></span>

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

### <span data-ttu-id="2a91d-142">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="2a91d-142">-VMScaleSetName</span></span>
<span data-ttu-id="2a91d-143">Name des Skalierungs Satzes für virtuelle Maschinen</span><span class="sxs-lookup"><span data-stu-id="2a91d-143">Name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="2a91d-144">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="2a91d-144">-VolumeType</span></span>
<span data-ttu-id="2a91d-145">Typ des Volumes (Betriebssystem oder Daten) zum Durchführen eines Verschlüsselungsvorgangs</span><span class="sxs-lookup"><span data-stu-id="2a91d-145">Type of the volume (OS or Data) to perform encryption operation</span></span>

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

### <span data-ttu-id="2a91d-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2a91d-146">-Confirm</span></span>
<span data-ttu-id="2a91d-147">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2a91d-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a91d-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a91d-148">-WhatIf</span></span>
<span data-ttu-id="2a91d-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2a91d-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a91d-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2a91d-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a91d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a91d-151">CommonParameters</span></span>
<span data-ttu-id="2a91d-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a91d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a91d-153">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a91d-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a91d-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2a91d-154">INPUTS</span></span>

### <span data-ttu-id="2a91d-155">System. String</span><span class="sxs-lookup"><span data-stu-id="2a91d-155">System.String</span></span>

### <span data-ttu-id="2a91d-156">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="2a91d-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2a91d-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2a91d-157">OUTPUTS</span></span>

### <span data-ttu-id="2a91d-158">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineScaleSetExtension</span><span class="sxs-lookup"><span data-stu-id="2a91d-158">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="2a91d-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="2a91d-159">NOTES</span></span>

## <span data-ttu-id="2a91d-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2a91d-160">RELATED LINKS</span></span>
