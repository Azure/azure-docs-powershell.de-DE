---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c01d07f9408804b229921394c24e444b2a4deb8b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170454"
---
# <span data-ttu-id="11bf8-101">Backup-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11bf8-101">Backup-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="11bf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11bf8-102">SYNOPSIS</span></span>
<span data-ttu-id="11bf8-103">Stellt ein von KeyVault verwaltetes Speicherkonto sichern.</span><span class="sxs-lookup"><span data-stu-id="11bf8-103">Backs up a KeyVault-managed storage account.</span></span>

## <span data-ttu-id="11bf8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="11bf8-104">SYNTAX</span></span>

### <span data-ttu-id="11bf8-105">ByStorageAccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="11bf8-105">ByStorageAccountName (Default)</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11bf8-106">ByStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11bf8-106">ByStorageAccount</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11bf8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11bf8-107">DESCRIPTION</span></span>
<span data-ttu-id="11bf8-108">Das **Cmdlet "Backup-AzKeyVaultManagedStorageAccount"** sichern ein angegebenes verwaltetes Speicherkonto in einem Schlüsseltresor, indem es heruntergeladen und in einer Datei gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="11bf8-108">The **Backup-AzKeyVaultManagedStorageAccount** cmdlet backs up a specified managed storage account in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="11bf8-109">Da die heruntergeladenen Inhalte verschlüsselt sind, können sie nicht außerhalb des Azure Key Vault verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="11bf8-109">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="11bf8-110">Sie können ein gesichertes Speicherkonto in einem beliebigen Schlüsseltresor in dem Abonnement wiederherstellen, von dem es gesichert wurde, solange sich der Tresor in derselben Geografie von Azure befindet.</span><span class="sxs-lookup"><span data-stu-id="11bf8-110">You can restore a backed-up storage account to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="11bf8-111">Typische Gründe für die Verwendung dieses Cmdlets sind:</span><span class="sxs-lookup"><span data-stu-id="11bf8-111">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="11bf8-112">Sie möchten eine Offlinekopie des Speicherkontos für den Fall beibehalten, dass Sie das Original versehentlich aus dem Tresor löschen.</span><span class="sxs-lookup"><span data-stu-id="11bf8-112">You want to retain an offline copy of the storage account in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="11bf8-113">Sie haben mit dem Schlüsseltresor ein Konto für verwalteten Speicher erstellt und möchten nun das Objekt in eine andere Azure-Region klonen, damit Sie es in allen Instanzen der verteilten Anwendung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="11bf8-113">You created a managed storage account using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="11bf8-114">Verwenden Sie das Cmdlet **"Backup-AzKeyVaultManagedStorageAccount",** um das verwaltete Speicherkonto im verschlüsselten Format abzurufen, verwenden Sie dann das Cmdlet **"Restore-AzKeyVaultManagedStorageAccount",** und geben Sie einen Schlüsseltresor in der zweiten Region an.</span><span class="sxs-lookup"><span data-stu-id="11bf8-114">Use the **Backup-AzKeyVaultManagedStorageAccount** cmdlet to retrieve the managed storage account in encrypted format and then use the **Restore-AzKeyVaultManagedStorageAccount** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="11bf8-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="11bf8-115">EXAMPLES</span></span>

### <span data-ttu-id="11bf8-116">Beispiel 1: Sichern eines verwalteten Speicherkontos mit einem automatisch generierten Dateinamen</span><span class="sxs-lookup"><span data-stu-id="11bf8-116">Example 1: Back up a managed storage account with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

<span data-ttu-id="11bf8-117">Dieser Befehl ruft das verwaltete Speicherkonto "MyMSAK" aus dem Schlüsseltresor "MyKeyVault" ab, speichert eine Sicherung dieses verwalteten Speicherkontos in einer Datei, die automatisch nach Ihnen benannt wird, und zeigt den Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="11bf8-117">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="11bf8-118">Beispiel 2: Sichern eines verwalteten Speicherkontos unter einem angegebenen Dateinamen</span><span class="sxs-lookup"><span data-stu-id="11bf8-118">Example 2: Back up a managed storage account to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="11bf8-119">Dieser Befehl ruft das verwaltete Speicherkonto "MyMSAK" aus dem Schlüsseltresor "MyKeyVault" ab und speichert eine Sicherung dieses verwalteten Speicherkontos in einer Datei namens "Backup.blob".</span><span class="sxs-lookup"><span data-stu-id="11bf8-119">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file named Backup.blob.</span></span>

### <span data-ttu-id="11bf8-120">Beispiel 3: Sichern sie ein zuvor abgerufenes Konto für verwalteten Speicher unter einem angegebenen Dateinamen, und überschreiben Sie die Zieldatei ohne Eingabeaufforderung.</span><span class="sxs-lookup"><span data-stu-id="11bf8-120">Example 3: Back up a previously retrieved managed storage account to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $msak = Get-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="11bf8-121">Dieser Befehl erstellt eine Sicherung des verwalteten Speicherkontos namens $msak. Name im Tresor namens $msak. VaultName in eine Datei mit dem Namen "Backup.blob", und überschreiben die Datei, sofern sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="11bf8-121">This command creates a backup of the managed storage account named $msak.Name in the vault named $msak.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="11bf8-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11bf8-122">PARAMETERS</span></span>

### <span data-ttu-id="11bf8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11bf8-123">-DefaultProfile</span></span>
<span data-ttu-id="11bf8-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="11bf8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11bf8-125">-Force</span><span class="sxs-lookup"><span data-stu-id="11bf8-125">-Force</span></span>
<span data-ttu-id="11bf8-126">Überschreiben der vorhandenen Datei</span><span class="sxs-lookup"><span data-stu-id="11bf8-126">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="11bf8-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11bf8-127">-InputObject</span></span>
<span data-ttu-id="11bf8-128">Das Speicherkontobündel, das gesichert werden soll, wird über die Ausgabe eines Abrufaufrufs pipelineiert.</span><span class="sxs-lookup"><span data-stu-id="11bf8-128">Storage account bundle to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByStorageAccount
Aliases: StorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11bf8-129">-Name</span><span class="sxs-lookup"><span data-stu-id="11bf8-129">-Name</span></span>
<span data-ttu-id="11bf8-130">Geheimer Name.</span><span class="sxs-lookup"><span data-stu-id="11bf8-130">Secret name.</span></span>
<span data-ttu-id="11bf8-131">Das Cmdlet erstellt den FQDN eines Geheimen aus dem Namen des Tresors, die aktuell ausgewählte Umgebung und den geheimen Namen.</span><span class="sxs-lookup"><span data-stu-id="11bf8-131">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11bf8-132">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="11bf8-132">-OutputFile</span></span>
<span data-ttu-id="11bf8-133">Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="11bf8-133">Output file.</span></span>
<span data-ttu-id="11bf8-134">Die Ausgabedatei zum Speichern der Speicherkontosicherung.</span><span class="sxs-lookup"><span data-stu-id="11bf8-134">The output file to store the storage account backup.</span></span>
<span data-ttu-id="11bf8-135">Wenn nichts angegeben wird, wird ein Standarddateiname generiert.</span><span class="sxs-lookup"><span data-stu-id="11bf8-135">If not specified, a default filename will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11bf8-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="11bf8-136">-VaultName</span></span>
<span data-ttu-id="11bf8-137">Name des Tresors.</span><span class="sxs-lookup"><span data-stu-id="11bf8-137">Vault name.</span></span>
<span data-ttu-id="11bf8-138">Das Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="11bf8-138">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11bf8-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11bf8-139">-Confirm</span></span>
<span data-ttu-id="11bf8-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="11bf8-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11bf8-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="11bf8-141">-WhatIf</span></span>
<span data-ttu-id="11bf8-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="11bf8-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11bf8-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="11bf8-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11bf8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11bf8-144">CommonParameters</span></span>
<span data-ttu-id="11bf8-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11bf8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11bf8-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11bf8-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11bf8-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="11bf8-147">INPUTS</span></span>

### <span data-ttu-id="11bf8-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="11bf8-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="11bf8-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="11bf8-149">OUTPUTS</span></span>

### <span data-ttu-id="11bf8-150">System.String</span><span class="sxs-lookup"><span data-stu-id="11bf8-150">System.String</span></span>

## <span data-ttu-id="11bf8-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="11bf8-151">NOTES</span></span>

## <span data-ttu-id="11bf8-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="11bf8-152">RELATED LINKS</span></span>
