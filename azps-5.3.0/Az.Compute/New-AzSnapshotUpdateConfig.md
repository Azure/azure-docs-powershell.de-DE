---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
ms.openlocfilehash: 1a90a1ff260d143cf4df52ad160b4c05e781bd2e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470866"
---
# <span data-ttu-id="f672d-101">New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="f672d-101">New-AzSnapshotUpdateConfig</span></span>

## <span data-ttu-id="f672d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f672d-102">SYNOPSIS</span></span>
<span data-ttu-id="f672d-103">Erstellt ein konfigurierbares Snapshotaktualisierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="f672d-103">Creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="f672d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f672d-104">SYNTAX</span></span>

```
New-AzSnapshotUpdateConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DiskEncryptionSetId <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f672d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f672d-105">DESCRIPTION</span></span>
<span data-ttu-id="f672d-106">Das **Cmdlet "New-AzSnapshotUpdateConfig"** erstellt ein konfigurierbares Snapshotupdateobjekt.</span><span class="sxs-lookup"><span data-stu-id="f672d-106">The **New-AzSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="f672d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f672d-107">EXAMPLES</span></span>

### <span data-ttu-id="f672d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f672d-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="f672d-109">Der erste Befehl erstellt ein lokales leeres Snapshotupdateobjekt mit einer Größe von 10 GB im Premium_LRS Speicherkontotyp.</span><span class="sxs-lookup"><span data-stu-id="f672d-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="f672d-110">Außerdem wird der Typ des Windows-Betriebssystems festgelegt und Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f672d-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="f672d-111">Mit dem zweiten und dritten Befehl werden der Datenträgerverschlüsselungsschlüssel und die Schlüsselverschlüsselungsschlüsseleinstellungen für das Snapshotupdateobjekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f672d-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="f672d-112">Der letzte Befehl erstellt das Snapshotaktualisierungsobjekt und aktualisiert eine vorhandene Momentaufnahme mit dem Namen 'Snapshot01' in der Ressourcengruppe 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="f672d-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="f672d-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f672d-113">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="f672d-114">Mit diesem Befehl wird eine vorhandene Momentaufnahme mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01" auf eine Datenträgergröße von 10 GB aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f672d-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="f672d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f672d-115">PARAMETERS</span></span>

### <span data-ttu-id="f672d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f672d-116">-DefaultProfile</span></span>
<span data-ttu-id="f672d-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f672d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f672d-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="f672d-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="f672d-119">Gibt das Objekt des Datenträgerverschlüsselungsschlüssels für eine Momentaufnahme an.</span><span class="sxs-lookup"><span data-stu-id="f672d-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="f672d-120">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="f672d-120">-DiskEncryptionSetId</span></span>
<span data-ttu-id="f672d-121">Gibt die Ressourcen-ID des Datenträgerverschlüsselungssets an, mit dem ruhede Verschlüsselung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f672d-121">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="f672d-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="f672d-122">-DiskSizeGB</span></span>
<span data-ttu-id="f672d-123">Gibt die Größe des Datenträgers in GB an.</span><span class="sxs-lookup"><span data-stu-id="f672d-123">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="f672d-124">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="f672d-124">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="f672d-125">"Verschlüsselungseinstellungen aktivieren" aus.</span><span class="sxs-lookup"><span data-stu-id="f672d-125">Enable encryption settings.</span></span>

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

### <span data-ttu-id="f672d-126">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="f672d-126">-EncryptionType</span></span>
<span data-ttu-id="f672d-127">Der Schlüsseltyp, der zum Verschlüsseln der Daten des Datenträgers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f672d-127">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="f672d-128">Verfügbare Werte sind: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span><span class="sxs-lookup"><span data-stu-id="f672d-128">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="f672d-129">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="f672d-129">-KeyEncryptionKey</span></span>
<span data-ttu-id="f672d-130">Gibt den Schlüsselverschlüsselungsschlüssel für eine Momentaufnahme an.</span><span class="sxs-lookup"><span data-stu-id="f672d-130">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="f672d-131">-OsType</span><span class="sxs-lookup"><span data-stu-id="f672d-131">-OsType</span></span>
<span data-ttu-id="f672d-132">Gibt den Betriebssystemtyp an.</span><span class="sxs-lookup"><span data-stu-id="f672d-132">Specifies the OS type.</span></span>

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

### <span data-ttu-id="f672d-133">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f672d-133">-SkuName</span></span>
<span data-ttu-id="f672d-134">Gibt den Namen der SKU des Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="f672d-134">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="f672d-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="f672d-135">-Tag</span></span>
<span data-ttu-id="f672d-136">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="f672d-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f672d-137">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="f672d-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f672d-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f672d-138">-Confirm</span></span>
<span data-ttu-id="f672d-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f672d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f672d-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f672d-140">-WhatIf</span></span>
<span data-ttu-id="f672d-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f672d-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f672d-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f672d-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f672d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f672d-143">CommonParameters</span></span>
<span data-ttu-id="f672d-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f672d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f672d-145">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f672d-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f672d-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f672d-146">INPUTS</span></span>

### <span data-ttu-id="f672d-147">System.String</span><span class="sxs-lookup"><span data-stu-id="f672d-147">System.String</span></span>

### <span data-ttu-id="f672d-148">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="f672d-148">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="f672d-149">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f672d-149">System.Int32</span></span>

### <span data-ttu-id="f672d-150">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f672d-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f672d-151">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f672d-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f672d-152">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="f672d-152">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="f672d-153">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="f672d-153">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="f672d-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f672d-154">OUTPUTS</span></span>

### <span data-ttu-id="f672d-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="f672d-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="f672d-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f672d-156">NOTES</span></span>

## <span data-ttu-id="f672d-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f672d-157">RELATED LINKS</span></span>
