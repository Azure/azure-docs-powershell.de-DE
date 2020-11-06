---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdiskupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmDiskUpdateConfig.md
ms.openlocfilehash: 1aee03af5a326585f9578a2f3eef378c3b783431
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504497"
---
# <span data-ttu-id="cfcc1-101">New-AzureRmDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="cfcc1-101">New-AzureRmDiskUpdateConfig</span></span>

## <span data-ttu-id="cfcc1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cfcc1-102">SYNOPSIS</span></span>
<span data-ttu-id="cfcc1-103">Erstellt ein konfigurierbares Datenträger Aktualisierungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="cfcc1-103">Creates a configurable disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfcc1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfcc1-104">SYNTAX</span></span>

```
New-AzureRmDiskUpdateConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Tag] <Hashtable>] [-DiskIOPSReadWrite <Int32>] [-DiskMBpsReadWrite <Int32>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cfcc1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cfcc1-105">DESCRIPTION</span></span>
<span data-ttu-id="cfcc1-106">Mit dem Cmdlet **New-AzureRmDiskUpdateConfig** wird ein konfigurierbares Datenträger Aktualisierungs Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="cfcc1-106">The **New-AzureRmDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="cfcc1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cfcc1-107">EXAMPLES</span></span>

### <span data-ttu-id="cfcc1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cfcc1-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="cfcc1-109">Der erste Befehl erstellt ein lokales leeres Datenträger Aktualisierungs Objekt mit der Größe 10 GB in Premium_LRS Speicher Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="cfcc1-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="cfcc1-110">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="cfcc1-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="cfcc1-111">Der zweite und der dritte Befehl legen die Einstellungen für den Datenträgerverschlüsselungsschlüssel und den Schlüssel Verschlüsselungsschlüssel für das Datenträger Aktualisierungs Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="cfcc1-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="cfcc1-112">Der letzte Befehl übernimmt das Datenträger Aktualisierungs Objekt und aktualisiert einen vorhandenen Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="cfcc1-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="cfcc1-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="cfcc1-113">Example 2</span></span>
```
PS C:\> New-AzureRmDiskUpdateConfig -DiskSizeGB 10 | Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="cfcc1-114">Mit diesem Befehl wird ein vorhandener Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01" auf 10 GB Festplattengröße aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cfcc1-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="cfcc1-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="cfcc1-115">PARAMETERS</span></span>

### <span data-ttu-id="cfcc1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfcc1-116">-DefaultProfile</span></span>
<span data-ttu-id="cfcc1-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cfcc1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfcc1-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="cfcc1-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="cfcc1-119">Gibt das Datenträgerverschlüsselungsschlüssel Objekt auf einem Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="cfcc1-119">Specifies the disk encryption key object on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfcc1-120">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="cfcc1-120">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="cfcc1-121">Die Anzahl der für diesen Datenträger zulässigen IOPS; nur Settable für UltraSSD-Datenträger.</span><span class="sxs-lookup"><span data-stu-id="cfcc1-121">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="cfcc1-122">Ein Vorgang kann zwischen 4K-und 256 KB-Bytes übertragen.</span><span class="sxs-lookup"><span data-stu-id="cfcc1-122">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfcc1-123">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="cfcc1-123">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="cfcc1-124">Die für diesen Datenträger zulässige Bandbreite; nur Settable für UltraSSD-Datenträger.</span><span class="sxs-lookup"><span data-stu-id="cfcc1-124">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="cfcc1-125">Mbit/s bedeutet, dass Millionen von Bytes pro Sekunde-MB hier die ISO-Notation von Potenzen von 10 verwenden.</span><span class="sxs-lookup"><span data-stu-id="cfcc1-125">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfcc1-126">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="cfcc1-126">-DiskSizeGB</span></span>
<span data-ttu-id="cfcc1-127">Gibt die Größe des Datenträgers in GB an.</span><span class="sxs-lookup"><span data-stu-id="cfcc1-127">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfcc1-128">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="cfcc1-128">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="cfcc1-129">Aktivieren Sie Verschlüsselungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="cfcc1-129">Enable encryption settings.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfcc1-130">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="cfcc1-130">-KeyEncryptionKey</span></span>
<span data-ttu-id="cfcc1-131">Gibt den Schlüssel Verschlüsselungsschlüssel auf einem Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="cfcc1-131">Specifies the Key encryption key on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfcc1-132">-OsType</span><span class="sxs-lookup"><span data-stu-id="cfcc1-132">-OsType</span></span>
<span data-ttu-id="cfcc1-133">Gibt den Betriebssystemtyp an.</span><span class="sxs-lookup"><span data-stu-id="cfcc1-133">Specifies the OS type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfcc1-134">-SkuName</span><span class="sxs-lookup"><span data-stu-id="cfcc1-134">-SkuName</span></span>
<span data-ttu-id="cfcc1-135">Gibt den SKU-Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="cfcc1-135">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="cfcc1-136">Verfügbare Werte sind Standard_LRS, Premium_LRS, StandardSSD_LRS und UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="cfcc1-136">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="cfcc1-137">UltraSSD_LRS können nur mit einem leeren Wert für den createoption-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cfcc1-137">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfcc1-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="cfcc1-138">-Tag</span></span>
<span data-ttu-id="cfcc1-139">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="cfcc1-139">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cfcc1-140">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="cfcc1-140">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfcc1-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cfcc1-141">-Confirm</span></span>
<span data-ttu-id="cfcc1-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cfcc1-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfcc1-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfcc1-143">-WhatIf</span></span>
<span data-ttu-id="cfcc1-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cfcc1-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cfcc1-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cfcc1-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfcc1-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfcc1-146">CommonParameters</span></span>
<span data-ttu-id="cfcc1-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfcc1-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfcc1-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfcc1-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfcc1-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cfcc1-149">INPUTS</span></span>

### <span data-ttu-id="cfcc1-150">System. String</span><span class="sxs-lookup"><span data-stu-id="cfcc1-150">System.String</span></span>

### <span data-ttu-id="cfcc1-151">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 21.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="cfcc1-151">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="cfcc1-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="cfcc1-152">System.Int32</span></span>

### <span data-ttu-id="cfcc1-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cfcc1-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="cfcc1-154">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="cfcc1-154">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="cfcc1-155">Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="cfcc1-155">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="cfcc1-156">Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="cfcc1-156">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="cfcc1-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cfcc1-157">OUTPUTS</span></span>

### <span data-ttu-id="cfcc1-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="cfcc1-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="cfcc1-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="cfcc1-159">NOTES</span></span>

## <span data-ttu-id="cfcc1-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cfcc1-160">RELATED LINKS</span></span>
