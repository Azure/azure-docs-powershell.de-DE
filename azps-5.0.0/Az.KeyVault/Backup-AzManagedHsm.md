---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsm.md
ms.openlocfilehash: 5353adade342b7f73cf60ff6b0befa88f4a3da73
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175526"
---
# <span data-ttu-id="ba608-101">Backup-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="ba608-101">Backup-AzManagedHsm</span></span>

## <span data-ttu-id="ba608-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ba608-102">SYNOPSIS</span></span>
<span data-ttu-id="ba608-103">Vollständiges Sichern eines verwalteten HSM.</span><span class="sxs-lookup"><span data-stu-id="ba608-103">Fully backup a managed HSM.</span></span>

## <span data-ttu-id="ba608-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba608-104">SYNTAX</span></span>

### <span data-ttu-id="ba608-105">InteractiveStorageName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ba608-105">InteractiveStorageName (Default)</span></span>
```
Backup-AzManagedHsm [-Name] <String> -StorageAccountName <String> -StorageContainerName <String>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba608-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="ba608-106">InteractiveStorageUri</span></span>
```
Backup-AzManagedHsm [-Name] <String> -StorageContainerUri <Uri> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba608-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="ba608-107">InputObjectStorageUri</span></span>
```
Backup-AzManagedHsm -StorageContainerUri <Uri> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba608-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="ba608-108">InputObjectStorageName</span></span>
```
Backup-AzManagedHsm -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba608-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba608-109">DESCRIPTION</span></span>
<span data-ttu-id="ba608-110">Vollständiges Sichern eines verwalteten HSM auf einem Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="ba608-110">Fully backup a managed HSM to a storage account.</span></span>
<span data-ttu-id="ba608-111">`Restore-AzManagedHsm`Wird zum Wiederherstellen der Sicherung verwendet.</span><span class="sxs-lookup"><span data-stu-id="ba608-111">Use `Restore-AzManagedHsm` to restore the backup.</span></span>

## <span data-ttu-id="ba608-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ba608-112">EXAMPLES</span></span>

### <span data-ttu-id="ba608-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ba608-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"

PS C:\> Backup-AzManagedHsm -Name myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -SasToken $sasToken

https://{accountName}.blob.core.windows.net/{containerName}/{backupFolder}
```

<span data-ttu-id="ba608-114">Das Cmdlet erstellt einen Ordner (in der Regel benannt `mhsm-{name}-{timestamp}` ) im Speichercontainer, speichert die Sicherung in diesem Ordner und gibt den Ordner-URI aus.</span><span class="sxs-lookup"><span data-stu-id="ba608-114">The cmdlet will create a folder (typically named `mhsm-{name}-{timestamp}`) in the storage container, store the backup in that folder and output the folder URI.</span></span>

## <span data-ttu-id="ba608-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba608-115">PARAMETERS</span></span>

### <span data-ttu-id="ba608-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba608-116">-DefaultProfile</span></span>
<span data-ttu-id="ba608-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ba608-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba608-118">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="ba608-118">-HsmObject</span></span>
<span data-ttu-id="ba608-119">Verwaltetes HSM-Objekt</span><span class="sxs-lookup"><span data-stu-id="ba608-119">Managed HSM object</span></span>

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

### <span data-ttu-id="ba608-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ba608-120">-Name</span></span>
<span data-ttu-id="ba608-121">Der Name des HSM.</span><span class="sxs-lookup"><span data-stu-id="ba608-121">Name of the HSM.</span></span>

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

### <span data-ttu-id="ba608-122">-SasToken</span><span class="sxs-lookup"><span data-stu-id="ba608-122">-SasToken</span></span>
<span data-ttu-id="ba608-123">Das SAS-Token (Shared Access Signature) zur Authentifizierung des speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="ba608-123">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="ba608-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ba608-124">-StorageAccountName</span></span>
<span data-ttu-id="ba608-125">Der Name des speicherkontos, in dem die Sicherung gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ba608-125">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="ba608-126">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="ba608-126">-StorageContainerName</span></span>
<span data-ttu-id="ba608-127">Der Name des BLOB-Containers, in dem die Sicherung gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ba608-127">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="ba608-128">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="ba608-128">-StorageContainerUri</span></span>
<span data-ttu-id="ba608-129">Der URI des Speichercontainers, in dem die Sicherung gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ba608-129">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="ba608-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ba608-130">-Confirm</span></span>
<span data-ttu-id="ba608-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ba608-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba608-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba608-132">-WhatIf</span></span>
<span data-ttu-id="ba608-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ba608-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba608-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ba608-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba608-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba608-135">CommonParameters</span></span>
<span data-ttu-id="ba608-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba608-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba608-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba608-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba608-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ba608-138">INPUTS</span></span>

### <span data-ttu-id="ba608-139">Keine</span><span class="sxs-lookup"><span data-stu-id="ba608-139">None</span></span>

## <span data-ttu-id="ba608-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ba608-140">OUTPUTS</span></span>

### <span data-ttu-id="ba608-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ba608-141">System.String</span></span>

## <span data-ttu-id="ba608-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="ba608-142">NOTES</span></span>

## <span data-ttu-id="ba608-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ba608-143">RELATED LINKS</span></span>
