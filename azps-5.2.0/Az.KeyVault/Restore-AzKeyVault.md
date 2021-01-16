---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
ms.openlocfilehash: 8be76f6eb5cf56e5f4612a175c067a7647576a4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307747"
---
# <span data-ttu-id="2c7bb-101">Restore-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="2c7bb-101">Restore-AzKeyVault</span></span>

## <span data-ttu-id="2c7bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c7bb-102">SYNOPSIS</span></span>
<span data-ttu-id="2c7bb-103">Stellt einen verwalteten HSM vollständig aus einer Sicherung wieder her.</span><span class="sxs-lookup"><span data-stu-id="2c7bb-103">Fully restores a managed HSM from backup.</span></span>

## <span data-ttu-id="2c7bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c7bb-104">SYNTAX</span></span>

### <span data-ttu-id="2c7bb-105">InteractiveStorageName (Standard)</span><span class="sxs-lookup"><span data-stu-id="2c7bb-105">InteractiveStorageName (Default)</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-PassThru] [-HsmName] <String> -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c7bb-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="2c7bb-106">InteractiveStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-PassThru] [-HsmName] <String> -StorageContainerUri <Uri>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c7bb-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="2c7bb-107">InputObjectStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-PassThru] -StorageContainerUri <Uri> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c7bb-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="2c7bb-108">InputObjectStorageName</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-PassThru] -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c7bb-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2c7bb-109">DESCRIPTION</span></span>
<span data-ttu-id="2c7bb-110">Stellt einen verwalteten HSM vollständig aus einer Sicherung wieder her, die in einem Speicherkonto gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="2c7bb-110">Fully restores a managed HSM from a backup stored in a storage account.</span></span>
<span data-ttu-id="2c7bb-111">Wird `Backup-AzKeyVault` zur Sicherung verwendet.</span><span class="sxs-lookup"><span data-stu-id="2c7bb-111">Use `Backup-AzKeyVault` to backup.</span></span>

## <span data-ttu-id="2c7bb-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2c7bb-112">EXAMPLES</span></span>

### <span data-ttu-id="2c7bb-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2c7bb-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"
PS C:\> Restore-AzKeyVault -HsmName myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -BackupFolder "mhsm-myHsm-2020101308504935" -SasToken $sasToken
```

<span data-ttu-id="2c7bb-114">Im Beispiel wird eine Sicherung wiederhergestellt, die in einem Ordner namens "mhsm-myHsm-2020101308504935" des Speichercontainers "https://{accountName}.blob.core.windows.net/{containerName}" gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="2c7bb-114">The example restores a backup stored in a folder named "mhsm-myHsm-2020101308504935" of a storage container "https://{accountName}.blob.core.windows.net/{containerName}".</span></span>

## <span data-ttu-id="2c7bb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c7bb-115">PARAMETERS</span></span>

### <span data-ttu-id="2c7bb-116">-BackupFolder</span><span class="sxs-lookup"><span data-stu-id="2c7bb-116">-BackupFolder</span></span>
<span data-ttu-id="2c7bb-117">Ordnername der Sicherung, z. B. 'mhsm-*-2020101309020403'. Sie kann auch geschachtelt werden, z. B. 'backups/mhsm-*-2020101309020403'.</span><span class="sxs-lookup"><span data-stu-id="2c7bb-117">Folder name of the backup, e.g. 'mhsm-*-2020101309020403'. It can also be nested such as 'backups/mhsm-*-2020101309020403'.</span></span>

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

### <span data-ttu-id="2c7bb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c7bb-118">-DefaultProfile</span></span>
<span data-ttu-id="2c7bb-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2c7bb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c7bb-120">-HsmName</span><span class="sxs-lookup"><span data-stu-id="2c7bb-120">-HsmName</span></span>
<span data-ttu-id="2c7bb-121">Name des HSM.</span><span class="sxs-lookup"><span data-stu-id="2c7bb-121">Name of the HSM.</span></span>

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

### <span data-ttu-id="2c7bb-122">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="2c7bb-122">-HsmObject</span></span>
<span data-ttu-id="2c7bb-123">Verwaltetes HSM-Objekt</span><span class="sxs-lookup"><span data-stu-id="2c7bb-123">Managed HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: InputObjectStorageUri, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c7bb-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c7bb-124">-PassThru</span></span>
<span data-ttu-id="2c7bb-125">Geben Sie "true" zurück, wenn das HSM wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="2c7bb-125">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="2c7bb-126">-SasToken</span><span class="sxs-lookup"><span data-stu-id="2c7bb-126">-SasToken</span></span>
<span data-ttu-id="2c7bb-127">Das SAS (Shared Access Signature)-Token zum Authentifizieren des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="2c7bb-127">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="2c7bb-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2c7bb-128">-StorageAccountName</span></span>
<span data-ttu-id="2c7bb-129">Name des Speicherkontos, in dem die Sicherung gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2c7bb-129">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="2c7bb-130">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="2c7bb-130">-StorageContainerName</span></span>
<span data-ttu-id="2c7bb-131">Name des BLOB-Containers, in dem die Sicherung gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2c7bb-131">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="2c7bb-132">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="2c7bb-132">-StorageContainerUri</span></span>
<span data-ttu-id="2c7bb-133">URI des Speichercontainers, in dem die Sicherung gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2c7bb-133">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="2c7bb-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c7bb-134">-Confirm</span></span>
<span data-ttu-id="2c7bb-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2c7bb-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c7bb-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2c7bb-136">-WhatIf</span></span>
<span data-ttu-id="2c7bb-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2c7bb-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c7bb-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2c7bb-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c7bb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c7bb-139">CommonParameters</span></span>
<span data-ttu-id="2c7bb-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c7bb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c7bb-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c7bb-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c7bb-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2c7bb-142">INPUTS</span></span>

### <span data-ttu-id="2c7bb-143">Keine</span><span class="sxs-lookup"><span data-stu-id="2c7bb-143">None</span></span>

## <span data-ttu-id="2c7bb-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2c7bb-144">OUTPUTS</span></span>

### <span data-ttu-id="2c7bb-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2c7bb-145">System.Boolean</span></span>

## <span data-ttu-id="2c7bb-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2c7bb-146">NOTES</span></span>

## <span data-ttu-id="2c7bb-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2c7bb-147">RELATED LINKS</span></span>
