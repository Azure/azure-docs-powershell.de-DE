---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVault.md
ms.openlocfilehash: 7d2bb9d961b5fba7ecd5e0d83f8d86ac1a930c75
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147724"
---
# <span data-ttu-id="46715-101">Backup-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="46715-101">Backup-AzKeyVault</span></span>

## <span data-ttu-id="46715-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46715-102">SYNOPSIS</span></span>
<span data-ttu-id="46715-103">Vollständige Sicherung eines verwalteten HSM.</span><span class="sxs-lookup"><span data-stu-id="46715-103">Fully backup a managed HSM.</span></span>

## <span data-ttu-id="46715-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46715-104">SYNTAX</span></span>

### <span data-ttu-id="46715-105">InteractiveStorageName (Standard)</span><span class="sxs-lookup"><span data-stu-id="46715-105">InteractiveStorageName (Default)</span></span>
```
Backup-AzKeyVault [-HsmName] <String> -StorageAccountName <String> -StorageContainerName <String>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46715-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="46715-106">InteractiveStorageUri</span></span>
```
Backup-AzKeyVault [-HsmName] <String> -StorageContainerUri <Uri> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46715-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="46715-107">InputObjectStorageUri</span></span>
```
Backup-AzKeyVault -StorageContainerUri <Uri> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46715-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="46715-108">InputObjectStorageName</span></span>
```
Backup-AzKeyVault -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46715-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46715-109">DESCRIPTION</span></span>
<span data-ttu-id="46715-110">Vollständige Sicherung eines verwalteten HSM in einem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="46715-110">Fully backup a managed HSM to a storage account.</span></span>
<span data-ttu-id="46715-111">Wird `Restore-AzKeyVault` verwendet, um die Sicherung wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="46715-111">Use `Restore-AzKeyVault` to restore the backup.</span></span>

## <span data-ttu-id="46715-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="46715-112">EXAMPLES</span></span>

### <span data-ttu-id="46715-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="46715-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"

PS C:\> Backup-AzKeyVault -HsmName myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -SasToken $sasToken

https://{accountName}.blob.core.windows.net/{containerName}/{backupFolder}
```

<span data-ttu-id="46715-114">Das Cmdlet erstellt einen Ordner (normalerweise mit dem Namen) im Speichercontainer, speichern die Sicherung in diesem Ordner und `mhsm-{name}-{timestamp}` gibt den Ordner-URI aus.</span><span class="sxs-lookup"><span data-stu-id="46715-114">The cmdlet will create a folder (typically named `mhsm-{name}-{timestamp}`) in the storage container, store the backup in that folder and output the folder URI.</span></span>

## <span data-ttu-id="46715-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46715-115">PARAMETERS</span></span>

### <span data-ttu-id="46715-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46715-116">-DefaultProfile</span></span>
<span data-ttu-id="46715-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="46715-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46715-118">-HsmName</span><span class="sxs-lookup"><span data-stu-id="46715-118">-HsmName</span></span>
<span data-ttu-id="46715-119">Name des HSM.</span><span class="sxs-lookup"><span data-stu-id="46715-119">Name of the HSM.</span></span>

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

### <span data-ttu-id="46715-120">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="46715-120">-HsmObject</span></span>
<span data-ttu-id="46715-121">Verwaltetes HSM-Objekt</span><span class="sxs-lookup"><span data-stu-id="46715-121">Managed HSM object</span></span>

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

### <span data-ttu-id="46715-122">-SasToken</span><span class="sxs-lookup"><span data-stu-id="46715-122">-SasToken</span></span>
<span data-ttu-id="46715-123">Das SAS (Shared Access Signature)-Token zum Authentifizieren des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="46715-123">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="46715-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="46715-124">-StorageAccountName</span></span>
<span data-ttu-id="46715-125">Name des Speicherkontos, in dem die Sicherung gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="46715-125">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="46715-126">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="46715-126">-StorageContainerName</span></span>
<span data-ttu-id="46715-127">Name des BLOB-Containers, in dem die Sicherung gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="46715-127">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="46715-128">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="46715-128">-StorageContainerUri</span></span>
<span data-ttu-id="46715-129">URI des Speichercontainers, in dem die Sicherung gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="46715-129">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="46715-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46715-130">-Confirm</span></span>
<span data-ttu-id="46715-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46715-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46715-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="46715-132">-WhatIf</span></span>
<span data-ttu-id="46715-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46715-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46715-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46715-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46715-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46715-135">CommonParameters</span></span>
<span data-ttu-id="46715-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46715-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46715-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46715-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46715-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="46715-138">INPUTS</span></span>

### <span data-ttu-id="46715-139">Keine</span><span class="sxs-lookup"><span data-stu-id="46715-139">None</span></span>

## <span data-ttu-id="46715-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="46715-140">OUTPUTS</span></span>

### <span data-ttu-id="46715-141">System.String</span><span class="sxs-lookup"><span data-stu-id="46715-141">System.String</span></span>

## <span data-ttu-id="46715-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="46715-142">NOTES</span></span>

## <span data-ttu-id="46715-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="46715-143">RELATED LINKS</span></span>
