---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshotConfig.md
ms.openlocfilehash: 032868a1dc1e183a2dd4adea31bbf693cdd7d1ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505182"
---
# <span data-ttu-id="58a2b-101">New-AzureRmSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="58a2b-101">New-AzureRmSnapshotConfig</span></span>

## <span data-ttu-id="58a2b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="58a2b-102">SYNOPSIS</span></span>
<span data-ttu-id="58a2b-103">Erstellt ein konfigurierbares Snapshot-Objekt.</span><span class="sxs-lookup"><span data-stu-id="58a2b-103">Creates a configurable snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58a2b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="58a2b-104">SYNTAX</span></span>

```
New-AzureRmSnapshotConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Tag <Hashtable>] [-CreateOption <DiskCreateOption>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58a2b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="58a2b-105">DESCRIPTION</span></span>
<span data-ttu-id="58a2b-106">Mit dem Cmdlet **New-AzureRmSnapshotConfig** wird ein konfigurierbares Snapshot-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="58a2b-106">The **New-AzureRmSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="58a2b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="58a2b-107">EXAMPLES</span></span>

### <span data-ttu-id="58a2b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="58a2b-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzureRmSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzureRmSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="58a2b-109">Der erste Befehl erstellt ein lokales leeres snapshotobjekt mit der Größe 5GB in Standard_LRS Speicher Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="58a2b-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="58a2b-110">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="58a2b-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="58a2b-111">Der zweite und der dritte Befehl legen die Einstellungen für den Datenträgerverschlüsselungsschlüssel und den Schlüssel Verschlüsselungsschlüssel für das Snapshot-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="58a2b-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="58a2b-112">Der letzte Befehl übernimmt das Snapshot-Objekt und erstellt einen Schnappschuss mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="58a2b-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="58a2b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="58a2b-113">PARAMETERS</span></span>

### <span data-ttu-id="58a2b-114">-Createoption</span><span class="sxs-lookup"><span data-stu-id="58a2b-114">-CreateOption</span></span>
<span data-ttu-id="58a2b-115">Gibt an, ob dieses Cmdlet einen Datenträger auf dem virtuellen Computer von einer Plattform oder einem Benutzerbild erstellt, einen leeren Datenträger erstellt oder einen vorhandenen Datenträger anfügt.</span><span class="sxs-lookup"><span data-stu-id="58a2b-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.DiskCreateOption]
Parameter Sets: (All)
Aliases: 
Accepted values: Empty, Attach, FromImage, Import, Copy

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58a2b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58a2b-116">-DefaultProfile</span></span>
<span data-ttu-id="58a2b-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="58a2b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58a2b-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="58a2b-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="58a2b-119">Gibt das Datenträgerverschlüsselungsschlüssel Objekt für einen Schnappschuss an.</span><span class="sxs-lookup"><span data-stu-id="58a2b-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="58a2b-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="58a2b-120">-DiskSizeGB</span></span>
<span data-ttu-id="58a2b-121">Gibt die Größe des Datenträgers in GB an.</span><span class="sxs-lookup"><span data-stu-id="58a2b-121">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58a2b-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="58a2b-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="58a2b-123">Aktivieren Sie Verschlüsselungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="58a2b-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="58a2b-124">-Imagereference</span><span class="sxs-lookup"><span data-stu-id="58a2b-124">-ImageReference</span></span>
<span data-ttu-id="58a2b-125">Gibt den Bildverweis auf einen Schnappschuss an.</span><span class="sxs-lookup"><span data-stu-id="58a2b-125">Specifies the image reference on a snapshot.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDiskReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58a2b-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="58a2b-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="58a2b-127">Gibt den Schlüssel Verschlüsselungsschlüssel für einen Schnappschuss an.</span><span class="sxs-lookup"><span data-stu-id="58a2b-127">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="58a2b-128">-Standort</span><span class="sxs-lookup"><span data-stu-id="58a2b-128">-Location</span></span>
<span data-ttu-id="58a2b-129">Gibt einen Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="58a2b-129">Specifies a location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58a2b-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="58a2b-130">-OsType</span></span>
<span data-ttu-id="58a2b-131">Gibt den Betriebssystemtyp an.</span><span class="sxs-lookup"><span data-stu-id="58a2b-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="58a2b-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="58a2b-132">-SkuName</span></span>
<span data-ttu-id="58a2b-133">Gibt den SKU-Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="58a2b-133">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes]
Parameter Sets: (All)
Aliases: AccountType
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58a2b-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="58a2b-134">-SourceResourceId</span></span>
<span data-ttu-id="58a2b-135">Gibt die Quellressourcen-ID an.</span><span class="sxs-lookup"><span data-stu-id="58a2b-135">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="58a2b-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="58a2b-136">-SourceUri</span></span>
<span data-ttu-id="58a2b-137">Gibt den Quell-URI an.</span><span class="sxs-lookup"><span data-stu-id="58a2b-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="58a2b-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="58a2b-138">-StorageAccountId</span></span>
<span data-ttu-id="58a2b-139">Gibt die Speicherkonto-ID an.</span><span class="sxs-lookup"><span data-stu-id="58a2b-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="58a2b-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="58a2b-140">-Tag</span></span>
<span data-ttu-id="58a2b-141">Gibt an, dass Ressourcen und Ressourcengruppen mit einer Reihe von Name-Wert-Paaren gekennzeichnet werden können.</span><span class="sxs-lookup"><span data-stu-id="58a2b-141">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58a2b-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="58a2b-142">-Confirm</span></span>
<span data-ttu-id="58a2b-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="58a2b-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58a2b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58a2b-144">-WhatIf</span></span>
<span data-ttu-id="58a2b-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="58a2b-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58a2b-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="58a2b-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58a2b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58a2b-147">CommonParameters</span></span>
<span data-ttu-id="58a2b-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58a2b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58a2b-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58a2b-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58a2b-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="58a2b-150">INPUTS</span></span>

### <span data-ttu-id="58a2b-151">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. StorageAccountTypes, Microsoft. Azure. Management. COMPUTE, Version = 14.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="58a2b-151">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>
<span data-ttu-id="58a2b-152">System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. String System. Collections. Hashtable System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable` 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="58a2b-152">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String System.Collections.Hashtable System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="58a2b-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="58a2b-153">OUTPUTS</span></span>

### <span data-ttu-id="58a2b-154">Microsoft. Azure. Management. Compute. Models. Snapshot</span><span class="sxs-lookup"><span data-stu-id="58a2b-154">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="58a2b-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="58a2b-155">NOTES</span></span>

## <span data-ttu-id="58a2b-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="58a2b-156">RELATED LINKS</span></span>

