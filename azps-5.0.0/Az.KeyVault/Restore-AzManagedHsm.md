---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsm.md
ms.openlocfilehash: 97e5c836d7d6b209d31851264047c6df894d77a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180412"
---
# <span data-ttu-id="bb071-101">Restore-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="bb071-101">Restore-AzManagedHsm</span></span>

## <span data-ttu-id="bb071-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bb071-102">SYNOPSIS</span></span>
<span data-ttu-id="bb071-103">Stellt ein verwaltetes HSM vollständig aus einer Sicherung wieder her.</span><span class="sxs-lookup"><span data-stu-id="bb071-103">Fully restores a managed HSM from backup.</span></span>

## <span data-ttu-id="bb071-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb071-104">SYNTAX</span></span>

### <span data-ttu-id="bb071-105">InteractiveStorageName (Standard)</span><span class="sxs-lookup"><span data-stu-id="bb071-105">InteractiveStorageName (Default)</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] [-Name] <String> -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb071-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="bb071-106">InteractiveStorageUri</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] [-Name] <String> -StorageContainerUri <Uri>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb071-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="bb071-107">InputObjectStorageUri</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] -StorageContainerUri <Uri> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb071-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="bb071-108">InputObjectStorageName</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb071-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb071-109">DESCRIPTION</span></span>
<span data-ttu-id="bb071-110">Stellt ein verwaltetes HSM vollständig aus einer in einem Speicherkonto gespeicherten Sicherung wieder her.</span><span class="sxs-lookup"><span data-stu-id="bb071-110">Fully restores a managed HSM from a backup stored in a storage account.</span></span>
<span data-ttu-id="bb071-111">Verwenden `Backup-AzManagedHsm` Sie diese zum Sichern.</span><span class="sxs-lookup"><span data-stu-id="bb071-111">Use `Backup-AzManagedHsm` to backup.</span></span>

## <span data-ttu-id="bb071-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bb071-112">EXAMPLES</span></span>

### <span data-ttu-id="bb071-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bb071-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"
PS C:\> Restore-AzManagedHsm -Name myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -BackupFolder "mhsm-myHsm-2020101308504935" -SasToken $sasToken
```

<span data-ttu-id="bb071-114">Im Beispiel wird eine Sicherung wiederhergestellt, die in einem Ordner namens "mhsm-myHsm-2020101308504935" eines Speichercontainers "https://{Accountname}. BLOB. Core. Windows. net/{Containername}" gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="bb071-114">The example restores a backup stored in a folder named "mhsm-myHsm-2020101308504935" of a storage container "https://{accountName}.blob.core.windows.net/{containerName}".</span></span>

## <span data-ttu-id="bb071-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb071-115">PARAMETERS</span></span>

### <span data-ttu-id="bb071-116">-BackupFolder auf</span><span class="sxs-lookup"><span data-stu-id="bb071-116">-BackupFolder</span></span>
<span data-ttu-id="bb071-117">Ordnername der Sicherung, beispielsweise "mhsm- *-2020101309020403". Sie kann auch wie "Backups/mhsm-2020101309020403" geschachtelt werden*.</span><span class="sxs-lookup"><span data-stu-id="bb071-117">Folder name of the backup, e.g. 'mhsm- *-2020101309020403'. It can also be nested such as 'backups/mhsm-* -2020101309020403'.</span></span>

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

### <span data-ttu-id="bb071-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb071-118">-DefaultProfile</span></span>
<span data-ttu-id="bb071-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bb071-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb071-120">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="bb071-120">-HsmObject</span></span>
<span data-ttu-id="bb071-121">Verwaltetes HSM-Objekt</span><span class="sxs-lookup"><span data-stu-id="bb071-121">Managed HSM object</span></span>

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

### <span data-ttu-id="bb071-122">-Name</span><span class="sxs-lookup"><span data-stu-id="bb071-122">-Name</span></span>
<span data-ttu-id="bb071-123">Der Name des HSM.</span><span class="sxs-lookup"><span data-stu-id="bb071-123">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InteractiveStorageUri
Aliases: HsmName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb071-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb071-124">-PassThru</span></span>
<span data-ttu-id="bb071-125">Gibt true zurück, wenn das HSM wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="bb071-125">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="bb071-126">-SasToken</span><span class="sxs-lookup"><span data-stu-id="bb071-126">-SasToken</span></span>
<span data-ttu-id="bb071-127">Das SAS-Token (Shared Access Signature) zur Authentifizierung des speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="bb071-127">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="bb071-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bb071-128">-StorageAccountName</span></span>
<span data-ttu-id="bb071-129">Der Name des speicherkontos, in dem die Sicherung gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bb071-129">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="bb071-130">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="bb071-130">-StorageContainerName</span></span>
<span data-ttu-id="bb071-131">Der Name des BLOB-Containers, in dem die Sicherung gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bb071-131">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="bb071-132">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="bb071-132">-StorageContainerUri</span></span>
<span data-ttu-id="bb071-133">Der URI des Speichercontainers, in dem die Sicherung gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bb071-133">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="bb071-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bb071-134">-Confirm</span></span>
<span data-ttu-id="bb071-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bb071-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb071-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb071-136">-WhatIf</span></span>
<span data-ttu-id="bb071-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bb071-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb071-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bb071-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb071-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb071-139">CommonParameters</span></span>
<span data-ttu-id="bb071-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb071-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb071-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb071-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb071-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bb071-142">INPUTS</span></span>

### <span data-ttu-id="bb071-143">Keine</span><span class="sxs-lookup"><span data-stu-id="bb071-143">None</span></span>

## <span data-ttu-id="bb071-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bb071-144">OUTPUTS</span></span>

### <span data-ttu-id="bb071-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bb071-145">System.Boolean</span></span>

## <span data-ttu-id="bb071-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="bb071-146">NOTES</span></span>

## <span data-ttu-id="bb071-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bb071-147">RELATED LINKS</span></span>
