---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/restore-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
ms.openlocfilehash: 36dfd9e5b4e1ddddadb745b2c44ab65b97833baa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931843"
---
# <span data-ttu-id="fe0b9-101">Restore-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="fe0b9-101">Restore-AzKeyVault</span></span>

## <span data-ttu-id="fe0b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe0b9-102">SYNOPSIS</span></span>
<span data-ttu-id="fe0b9-103">Stellt ein verwaltetes HSM vollständig aus der Sicherung wieder her.</span><span class="sxs-lookup"><span data-stu-id="fe0b9-103">Fully restores a managed HSM from backup.</span></span>

## <span data-ttu-id="fe0b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe0b9-104">SYNTAX</span></span>

### <span data-ttu-id="fe0b9-105">InteractiveStorageName (Standard)</span><span class="sxs-lookup"><span data-stu-id="fe0b9-105">InteractiveStorageName (Default)</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] [-HsmName] <String>
 -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe0b9-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="fe0b9-106">InteractiveStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] [-HsmName] <String>
 -StorageContainerUri <Uri> -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe0b9-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="fe0b9-107">InputObjectStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] -StorageContainerUri <Uri>
 -SasToken <SecureString> -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe0b9-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="fe0b9-108">InputObjectStorageName</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe0b9-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fe0b9-109">DESCRIPTION</span></span>
<span data-ttu-id="fe0b9-110">Stellt ein verwaltetes HSM vollständig aus einer in einem Speicherkonto gespeicherten Sicherung wieder her.</span><span class="sxs-lookup"><span data-stu-id="fe0b9-110">Fully restores a managed HSM from a backup stored in a storage account.</span></span>
<span data-ttu-id="fe0b9-111">Wird `Backup-AzKeyVault` zum Sichern verwendet.</span><span class="sxs-lookup"><span data-stu-id="fe0b9-111">Use `Backup-AzKeyVault` to backup.</span></span>

## <span data-ttu-id="fe0b9-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fe0b9-112">EXAMPLES</span></span>

### <span data-ttu-id="fe0b9-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fe0b9-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"
PS C:\> Restore-AzKeyVault -HsmName myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -BackupFolder "mhsm-myHsm-2020101308504935" -SasToken $sasToken
```

<span data-ttu-id="fe0b9-114">Im Beispiel wird eine Sicherung wiederhergestellt, die in einem Ordner mit dem Namen "mhsm-myHsm-2020101308504935" eines Speichercontainers "https://{accountName}.blob.core.windows.net/{containerName}" gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="fe0b9-114">The example restores a backup stored in a folder named "mhsm-myHsm-2020101308504935" of a storage container "https://{accountName}.blob.core.windows.net/{containerName}".</span></span>

## <span data-ttu-id="fe0b9-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fe0b9-115">PARAMETERS</span></span>

### <span data-ttu-id="fe0b9-116">-BackupFolder</span><span class="sxs-lookup"><span data-stu-id="fe0b9-116">-BackupFolder</span></span>
<span data-ttu-id="fe0b9-117">Ordnername der Sicherung, z. B. "mhsm-*-2020101309020403". Sie kann auch geschachtelt werden, z. B. "backups/mhsm-*-2020101309020403".</span><span class="sxs-lookup"><span data-stu-id="fe0b9-117">Folder name of the backup, e.g. 'mhsm-*-2020101309020403'. It can also be nested such as 'backups/mhsm-*-2020101309020403'.</span></span>

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

### <span data-ttu-id="fe0b9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe0b9-118">-DefaultProfile</span></span>
<span data-ttu-id="fe0b9-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fe0b9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe0b9-120">-HsmName</span><span class="sxs-lookup"><span data-stu-id="fe0b9-120">-HsmName</span></span>
<span data-ttu-id="fe0b9-121">Name des HSM.</span><span class="sxs-lookup"><span data-stu-id="fe0b9-121">Name of the HSM.</span></span>

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

### <span data-ttu-id="fe0b9-122">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="fe0b9-122">-HsmObject</span></span>
<span data-ttu-id="fe0b9-123">Verwaltetes HSM-Objekt</span><span class="sxs-lookup"><span data-stu-id="fe0b9-123">Managed HSM object</span></span>

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

### <span data-ttu-id="fe0b9-124">-KeyName</span><span class="sxs-lookup"><span data-stu-id="fe0b9-124">-KeyName</span></span>
<span data-ttu-id="fe0b9-125">Schlüsselname, der wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe0b9-125">Key name to restore.</span></span>

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

### <span data-ttu-id="fe0b9-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe0b9-126">-PassThru</span></span>
<span data-ttu-id="fe0b9-127">Geben Sie "true" zurück, wenn das HSM wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="fe0b9-127">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="fe0b9-128">-SasToken</span><span class="sxs-lookup"><span data-stu-id="fe0b9-128">-SasToken</span></span>
<span data-ttu-id="fe0b9-129">Das SAS-Token (Shared Access Signature), um das Speicherkonto zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="fe0b9-129">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="fe0b9-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fe0b9-130">-StorageAccountName</span></span>
<span data-ttu-id="fe0b9-131">Name des Speicherkontos, in dem die Sicherung gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe0b9-131">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="fe0b9-132">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="fe0b9-132">-StorageContainerName</span></span>
<span data-ttu-id="fe0b9-133">Name des Blobcontainers, in dem die Sicherung gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe0b9-133">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="fe0b9-134">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="fe0b9-134">-StorageContainerUri</span></span>
<span data-ttu-id="fe0b9-135">URI des Speichercontainers, in dem die Sicherung gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe0b9-135">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="fe0b9-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fe0b9-136">-Confirm</span></span>
<span data-ttu-id="fe0b9-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fe0b9-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe0b9-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe0b9-138">-WhatIf</span></span>
<span data-ttu-id="fe0b9-139">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fe0b9-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe0b9-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fe0b9-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe0b9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe0b9-141">CommonParameters</span></span>
<span data-ttu-id="fe0b9-142">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe0b9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe0b9-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe0b9-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe0b9-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fe0b9-144">INPUTS</span></span>

### <span data-ttu-id="fe0b9-145">Keine</span><span class="sxs-lookup"><span data-stu-id="fe0b9-145">None</span></span>

## <span data-ttu-id="fe0b9-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fe0b9-146">OUTPUTS</span></span>

### <span data-ttu-id="fe0b9-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fe0b9-147">System.Boolean</span></span>

## <span data-ttu-id="fe0b9-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fe0b9-148">NOTES</span></span>

## <span data-ttu-id="fe0b9-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fe0b9-149">RELATED LINKS</span></span>
