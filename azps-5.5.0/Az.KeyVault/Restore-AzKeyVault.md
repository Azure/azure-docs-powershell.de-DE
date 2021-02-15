---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
ms.openlocfilehash: d1cf3757596a56336c25c46bd6c4e38687888d6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175212"
---
# <span data-ttu-id="39c54-101">Restore-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="39c54-101">Restore-AzKeyVault</span></span>

## <span data-ttu-id="39c54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39c54-102">SYNOPSIS</span></span>
<span data-ttu-id="39c54-103">Stellt einen verwalteten HSM vollständig aus einer Sicherung wieder her.</span><span class="sxs-lookup"><span data-stu-id="39c54-103">Fully restores a managed HSM from backup.</span></span>

## <span data-ttu-id="39c54-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39c54-104">SYNTAX</span></span>

### <span data-ttu-id="39c54-105">InteractiveStorageName (Standard)</span><span class="sxs-lookup"><span data-stu-id="39c54-105">InteractiveStorageName (Default)</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] [-HsmName] <String>
 -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39c54-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="39c54-106">InteractiveStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] [-HsmName] <String>
 -StorageContainerUri <Uri> -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39c54-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="39c54-107">InputObjectStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] -StorageContainerUri <Uri>
 -SasToken <SecureString> -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39c54-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="39c54-108">InputObjectStorageName</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39c54-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="39c54-109">DESCRIPTION</span></span>
<span data-ttu-id="39c54-110">Stellt einen verwalteten HSM vollständig aus einer Sicherung wieder her, die in einem Speicherkonto gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="39c54-110">Fully restores a managed HSM from a backup stored in a storage account.</span></span>
<span data-ttu-id="39c54-111">Wird `Backup-AzKeyVault` zur Sicherung verwendet.</span><span class="sxs-lookup"><span data-stu-id="39c54-111">Use `Backup-AzKeyVault` to backup.</span></span>

## <span data-ttu-id="39c54-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="39c54-112">EXAMPLES</span></span>

### <span data-ttu-id="39c54-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="39c54-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"
PS C:\> Restore-AzKeyVault -HsmName myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -BackupFolder "mhsm-myHsm-2020101308504935" -SasToken $sasToken
```

<span data-ttu-id="39c54-114">Im Beispiel wird eine Sicherung wiederhergestellt, die in einem Ordner namens "mhsm-myHsm-2020101308504935" des Speichercontainers "https://{accountName}.blob.core.windows.net/{containerName}" gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="39c54-114">The example restores a backup stored in a folder named "mhsm-myHsm-2020101308504935" of a storage container "https://{accountName}.blob.core.windows.net/{containerName}".</span></span>

## <span data-ttu-id="39c54-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39c54-115">PARAMETERS</span></span>

### <span data-ttu-id="39c54-116">-BackupFolder</span><span class="sxs-lookup"><span data-stu-id="39c54-116">-BackupFolder</span></span>
<span data-ttu-id="39c54-117">Ordnername der Sicherung, z. B. 'mhsm-*-2020101309020403'. Sie kann auch geschachtelt werden, z. B. 'backups/mhsm-*-2020101309020403'.</span><span class="sxs-lookup"><span data-stu-id="39c54-117">Folder name of the backup, e.g. 'mhsm-*-2020101309020403'. It can also be nested such as 'backups/mhsm-*-2020101309020403'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39c54-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39c54-118">-DefaultProfile</span></span>
<span data-ttu-id="39c54-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39c54-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39c54-120">-HsmName</span><span class="sxs-lookup"><span data-stu-id="39c54-120">-HsmName</span></span>
<span data-ttu-id="39c54-121">Name des HSM.</span><span class="sxs-lookup"><span data-stu-id="39c54-121">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InteractiveStorageUri
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39c54-122">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="39c54-122">-HsmObject</span></span>
<span data-ttu-id="39c54-123">Verwaltetes HSM-Objekt</span><span class="sxs-lookup"><span data-stu-id="39c54-123">Managed HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: InputObjectStorageUri, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39c54-124">-KeyName</span><span class="sxs-lookup"><span data-stu-id="39c54-124">-KeyName</span></span>
<span data-ttu-id="39c54-125">Schlüsselname, der wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="39c54-125">Key name to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39c54-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39c54-126">-PassThru</span></span>
<span data-ttu-id="39c54-127">Geben Sie "true" zurück, wenn das HSM wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="39c54-127">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="39c54-128">-SasToken</span><span class="sxs-lookup"><span data-stu-id="39c54-128">-SasToken</span></span>
<span data-ttu-id="39c54-129">Das SAS (Shared Access Signature)-Token zum Authentifizieren des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="39c54-129">The shared access signature (SAS) token to authenticate the storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39c54-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="39c54-130">-StorageAccountName</span></span>
<span data-ttu-id="39c54-131">Name des Speicherkontos, in dem die Sicherung gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="39c54-131">Name of the storage account where the backup is going to be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39c54-132">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="39c54-132">-StorageContainerName</span></span>
<span data-ttu-id="39c54-133">Name des BLOB-Containers, in dem die Sicherung gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="39c54-133">Name of the blob container where the backup is going to be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39c54-134">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="39c54-134">-StorageContainerUri</span></span>
<span data-ttu-id="39c54-135">URI des Speichercontainers, in dem die Sicherung gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="39c54-135">URI of the storage container where the backup is going to be stored.</span></span>

```yaml
Type: System.Uri
Parameter Sets: InteractiveStorageUri, InputObjectStorageUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39c54-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39c54-136">-Confirm</span></span>
<span data-ttu-id="39c54-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="39c54-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39c54-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="39c54-138">-WhatIf</span></span>
<span data-ttu-id="39c54-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39c54-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39c54-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39c54-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39c54-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39c54-141">CommonParameters</span></span>
<span data-ttu-id="39c54-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39c54-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39c54-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39c54-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39c54-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="39c54-144">INPUTS</span></span>

### <span data-ttu-id="39c54-145">Keine</span><span class="sxs-lookup"><span data-stu-id="39c54-145">None</span></span>

## <span data-ttu-id="39c54-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="39c54-146">OUTPUTS</span></span>

### <span data-ttu-id="39c54-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="39c54-147">System.Boolean</span></span>

## <span data-ttu-id="39c54-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="39c54-148">NOTES</span></span>

## <span data-ttu-id="39c54-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="39c54-149">RELATED LINKS</span></span>
