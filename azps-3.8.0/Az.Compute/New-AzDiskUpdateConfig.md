---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
ms.openlocfilehash: f6c60538062f39f15e37773604aee302793134f1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996165"
---
# <span data-ttu-id="38d7f-101">New-AzDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="38d7f-101">New-AzDiskUpdateConfig</span></span>

## <span data-ttu-id="38d7f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="38d7f-102">SYNOPSIS</span></span>
<span data-ttu-id="38d7f-103">Erstellt ein konfigurierbares Datenträger Aktualisierungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="38d7f-103">Creates a configurable disk update object.</span></span>

## <span data-ttu-id="38d7f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="38d7f-104">SYNTAX</span></span>

```
New-AzDiskUpdateConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Tag] <Hashtable>] [-DiskIOPSReadWrite <Int32>] [-DiskMBpsReadWrite <Int32>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DiskEncryptionSetId <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38d7f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="38d7f-105">DESCRIPTION</span></span>
<span data-ttu-id="38d7f-106">Mit dem Cmdlet **New-AzDiskUpdateConfig** wird ein konfigurierbares Datenträger Aktualisierungs Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="38d7f-106">The **New-AzDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="38d7f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="38d7f-107">EXAMPLES</span></span>

### <span data-ttu-id="38d7f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="38d7f-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="38d7f-109">Der erste Befehl erstellt ein lokales leeres Datenträger Aktualisierungs Objekt mit der Größe 10 GB in Premium_LRS Speicher Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="38d7f-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="38d7f-110">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="38d7f-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="38d7f-111">Der zweite und der dritte Befehl legen die Einstellungen für den Datenträgerverschlüsselungsschlüssel und den Schlüssel Verschlüsselungsschlüssel für das Datenträger Aktualisierungs Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="38d7f-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="38d7f-112">Der letzte Befehl übernimmt das Datenträger Aktualisierungs Objekt und aktualisiert einen vorhandenen Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="38d7f-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="38d7f-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="38d7f-113">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="38d7f-114">Mit diesem Befehl wird ein vorhandener Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01" auf 10 GB Festplattengröße aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="38d7f-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="38d7f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="38d7f-115">PARAMETERS</span></span>

### <span data-ttu-id="38d7f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38d7f-116">-DefaultProfile</span></span>
<span data-ttu-id="38d7f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="38d7f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38d7f-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="38d7f-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="38d7f-119">Gibt das Datenträgerverschlüsselungsschlüssel Objekt auf einem Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="38d7f-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="38d7f-120">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="38d7f-120">-DiskEncryptionSetId</span></span>
<span data-ttu-id="38d7f-121">Gibt die Ressourcen-ID des Datenträger Verschlüsselungs Satzes an, mit dem die Verschlüsselung im Ruhezustand aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="38d7f-121">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="38d7f-122">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="38d7f-122">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="38d7f-123">Die Anzahl der für diesen Datenträger zulässigen IOPS; nur Settable für UltraSSD-Datenträger.</span><span class="sxs-lookup"><span data-stu-id="38d7f-123">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="38d7f-124">Ein Vorgang kann zwischen 4K-und 256 KB-Bytes übertragen.</span><span class="sxs-lookup"><span data-stu-id="38d7f-124">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="38d7f-125">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="38d7f-125">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="38d7f-126">Die für diesen Datenträger zulässige Bandbreite; nur Settable für UltraSSD-Datenträger.</span><span class="sxs-lookup"><span data-stu-id="38d7f-126">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="38d7f-127">Mbit/s bedeutet, dass Millionen von Bytes pro Sekunde-MB hier die ISO-Notation von Potenzen von 10 verwenden.</span><span class="sxs-lookup"><span data-stu-id="38d7f-127">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="38d7f-128">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="38d7f-128">-DiskSizeGB</span></span>
<span data-ttu-id="38d7f-129">Gibt die Größe des Datenträgers in GB an.</span><span class="sxs-lookup"><span data-stu-id="38d7f-129">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="38d7f-130">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="38d7f-130">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="38d7f-131">Aktivieren Sie Verschlüsselungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="38d7f-131">Enable encryption settings.</span></span>

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

### <span data-ttu-id="38d7f-132">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="38d7f-132">-EncryptionType</span></span>
<span data-ttu-id="38d7f-133">Der Typ des Schlüssels, der zum Verschlüsseln der Daten des Datenträgers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="38d7f-133">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="38d7f-134">Die verfügbaren Werte lauten: ' EncryptionAtRestWithPlatformKey ', ' EncryptionAtRestWithCustomerKey '</span><span class="sxs-lookup"><span data-stu-id="38d7f-134">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="38d7f-135">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="38d7f-135">-KeyEncryptionKey</span></span>
<span data-ttu-id="38d7f-136">Gibt den Schlüssel Verschlüsselungsschlüssel auf einem Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="38d7f-136">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="38d7f-137">-OsType</span><span class="sxs-lookup"><span data-stu-id="38d7f-137">-OsType</span></span>
<span data-ttu-id="38d7f-138">Gibt den Betriebssystemtyp an.</span><span class="sxs-lookup"><span data-stu-id="38d7f-138">Specifies the OS type.</span></span>

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

### <span data-ttu-id="38d7f-139">-SkuName</span><span class="sxs-lookup"><span data-stu-id="38d7f-139">-SkuName</span></span>
<span data-ttu-id="38d7f-140">Gibt den SKU-Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="38d7f-140">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="38d7f-141">Verfügbare Werte sind Standard_LRS, Premium_LRS, StandardSSD_LRS und UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="38d7f-141">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="38d7f-142">UltraSSD_LRS können nur mit einem leeren Wert für den createoption-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="38d7f-142">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="38d7f-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="38d7f-143">-Tag</span></span>
<span data-ttu-id="38d7f-144">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="38d7f-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="38d7f-145">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="38d7f-145">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="38d7f-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="38d7f-146">-Confirm</span></span>
<span data-ttu-id="38d7f-147">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="38d7f-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38d7f-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38d7f-148">-WhatIf</span></span>
<span data-ttu-id="38d7f-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="38d7f-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38d7f-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="38d7f-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38d7f-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38d7f-151">CommonParameters</span></span>
<span data-ttu-id="38d7f-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38d7f-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38d7f-153">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38d7f-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38d7f-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="38d7f-154">INPUTS</span></span>

### <span data-ttu-id="38d7f-155">System. String</span><span class="sxs-lookup"><span data-stu-id="38d7f-155">System.String</span></span>

### <span data-ttu-id="38d7f-156">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="38d7f-156">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="38d7f-157">System. Int32</span><span class="sxs-lookup"><span data-stu-id="38d7f-157">System.Int32</span></span>

### <span data-ttu-id="38d7f-158">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="38d7f-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="38d7f-159">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="38d7f-159">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="38d7f-160">Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="38d7f-160">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="38d7f-161">Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="38d7f-161">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="38d7f-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="38d7f-162">OUTPUTS</span></span>

### <span data-ttu-id="38d7f-163">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="38d7f-163">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="38d7f-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="38d7f-164">NOTES</span></span>

## <span data-ttu-id="38d7f-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="38d7f-165">RELATED LINKS</span></span>
