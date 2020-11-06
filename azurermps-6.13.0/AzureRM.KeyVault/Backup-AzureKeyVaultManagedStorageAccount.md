---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 1520acb94ffe587fb96eaa9c2ba565bcf31cc87e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503634"
---
# <span data-ttu-id="60145-101">Backup-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="60145-101">Backup-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="60145-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="60145-102">SYNOPSIS</span></span>
<span data-ttu-id="60145-103">Sichern eines von keyvault verwalteten speicherkontos</span><span class="sxs-lookup"><span data-stu-id="60145-103">Backs up a KeyVault-managed storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60145-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="60145-104">SYNTAX</span></span>

### <span data-ttu-id="60145-105">ByStorageAccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="60145-105">ByStorageAccountName (Default)</span></span>
```
Backup-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60145-106">ByStorageAccount</span><span class="sxs-lookup"><span data-stu-id="60145-106">ByStorageAccount</span></span>
```
Backup-AzureKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="60145-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60145-107">DESCRIPTION</span></span>
<span data-ttu-id="60145-108">Mit dem Cmdlet " **Backup-AzureKeyVaultManagedStorageAccount** " wird ein bestimmtes verwaltetes Speicherkonto in einem schlüsseltresor gesichert, indem es heruntergeladen und in einer Datei gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="60145-108">The **Backup-AzureKeyVaultManagedStorageAccount** cmdlet backs up a specified managed storage account in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="60145-109">Da der heruntergeladene Inhalt verschlüsselt ist, kann er nicht außerhalb des Azure Key Vault verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60145-109">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="60145-110">Sie können ein gesichertes Speicherkonto in einem beliebigen schlüsseltresor des Abonnements wiederherstellen, von dem es gesichert wurde, sofern sich der Tresor im gleichen Azure-geografischen Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="60145-110">You can restore a backed-up storage account to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="60145-111">Typische Gründe für die Verwendung dieses Cmdlets sind:</span><span class="sxs-lookup"><span data-stu-id="60145-111">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="60145-112">Sie möchten eine Offlinekopie des speicherkontos behalten, falls Sie das Original versehentlich aus dem Tresor löschen.</span><span class="sxs-lookup"><span data-stu-id="60145-112">You want to retain an offline copy of the storage account in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="60145-113">Sie haben ein verwaltetes Speicherkonto mithilfe von Key Vault erstellt und möchten nun das Objekt in einen anderen Azure-Bereich Klonen, sodass Sie es in allen Instanzen ihrer verteilten Anwendung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="60145-113">You created a managed storage account using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="60145-114">Verwenden Sie das Cmdlet **Backup-AzureKeyVaultManagedStorageAccount** , um das verwaltete Speicherkonto im verschlüsselten Format abzurufen, und verwenden Sie dann das Cmdlet **Restore-AzureKeyVaultManagedStorageAccount** , und geben Sie einen schlüsseltresor in der zweiten Region an.</span><span class="sxs-lookup"><span data-stu-id="60145-114">Use the **Backup-AzureKeyVaultManagedStorageAccount** cmdlet to retrieve the managed storage account in encrypted format and then use the **Restore-AzureKeyVaultManagedStorageAccount** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="60145-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="60145-115">EXAMPLES</span></span>

### <span data-ttu-id="60145-116">Beispiel 1: Sichern eines verwalteten speicherkontos mit einem automatisch generierten Dateinamen</span><span class="sxs-lookup"><span data-stu-id="60145-116">Example 1: Back up a managed storage account with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzureKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

<span data-ttu-id="60145-117">Dieser Befehl ruft das verwaltete Speicherkonto namens MyMSAK aus dem schlüsseltresor mit dem Namen MyKeyVault ab und speichert eine Sicherung dieses verwalteten speicherkontos in einer Datei, die automatisch nach ihnen benannt wird, und zeigt den Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="60145-117">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="60145-118">Beispiel 2: Sichern eines verwalteten speicherkontos mit einem angegebenen Dateinamen</span><span class="sxs-lookup"><span data-stu-id="60145-118">Example 2: Back up a managed storage account to a specified file name</span></span>
```powershell
PS C:\> Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="60145-119">Dieser Befehl ruft das verwaltete Speicherkonto namens MyMSAK aus dem schlüsseltresor mit dem Namen MyKeyVault ab und speichert eine Sicherungskopie dieses verwalteten speicherkontos in einer Datei mit dem Namen Backup. BLOB.</span><span class="sxs-lookup"><span data-stu-id="60145-119">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file named Backup.blob.</span></span>

### <span data-ttu-id="60145-120">Beispiel 3: Sichern eines zuvor abgerufenen verwalteten speicherkontos mit einem angegebenen Dateinamen, wobei die Zieldatei ohne Aufforderung überschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="60145-120">Example 3: Back up a previously retrieved managed storage account to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $msak = Get-AzureKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzureKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="60145-121">Mit diesem Befehl wird eine Sicherungskopie des verwalteten speicherkontos mit dem Namen $msak erstellt. Name im Tresor mit dem Namen $msak. Vaultname in eine Datei mit dem Namen "Backup. BLOB", wobei die Datei im Hintergrund überschrieben wird, wenn Sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="60145-121">This command creates a backup of the managed storage account named $msak.Name in the vault named $msak.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="60145-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="60145-122">PARAMETERS</span></span>

### <span data-ttu-id="60145-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60145-123">-DefaultProfile</span></span>
<span data-ttu-id="60145-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="60145-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60145-125">-Force</span><span class="sxs-lookup"><span data-stu-id="60145-125">-Force</span></span>
<span data-ttu-id="60145-126">Überschreiben der angegebenen Datei, sofern vorhanden</span><span class="sxs-lookup"><span data-stu-id="60145-126">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="60145-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="60145-127">-InputObject</span></span>
<span data-ttu-id="60145-128">Das zu sichernde Speicherkonto Bündel wird von der Ausgabe eines Abruf Anrufs in die Pipeline übertragen.</span><span class="sxs-lookup"><span data-stu-id="60145-128">Storage account bundle to be backed up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="60145-129">-Name</span><span class="sxs-lookup"><span data-stu-id="60145-129">-Name</span></span>
<span data-ttu-id="60145-130">Geheimer Name.</span><span class="sxs-lookup"><span data-stu-id="60145-130">Secret name.</span></span>
<span data-ttu-id="60145-131">Cmdlet erstellt den FQDN eines geheimen Schlüssels aus Vault-Name, aktuell ausgewählter Umgebung und geheimem Namen.</span><span class="sxs-lookup"><span data-stu-id="60145-131">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="60145-132">-Outputdatei</span><span class="sxs-lookup"><span data-stu-id="60145-132">-OutputFile</span></span>
<span data-ttu-id="60145-133">Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="60145-133">Output file.</span></span>
<span data-ttu-id="60145-134">Die Ausgabedatei zum Speichern der Speicherkonto Sicherung</span><span class="sxs-lookup"><span data-stu-id="60145-134">The output file to store the storage account backup.</span></span>
<span data-ttu-id="60145-135">Wenn keine Angabe erfolgt, wird ein Standarddateiname generiert.</span><span class="sxs-lookup"><span data-stu-id="60145-135">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="60145-136">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="60145-136">-VaultName</span></span>
<span data-ttu-id="60145-137">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="60145-137">Vault name.</span></span>
<span data-ttu-id="60145-138">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="60145-138">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="60145-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="60145-139">-Confirm</span></span>
<span data-ttu-id="60145-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="60145-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60145-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60145-141">-WhatIf</span></span>
<span data-ttu-id="60145-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="60145-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60145-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="60145-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60145-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60145-144">CommonParameters</span></span>
<span data-ttu-id="60145-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60145-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60145-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60145-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60145-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="60145-147">INPUTS</span></span>

### <span data-ttu-id="60145-148">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="60145-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>
<span data-ttu-id="60145-149">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="60145-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="60145-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="60145-150">OUTPUTS</span></span>

### <span data-ttu-id="60145-151">System. String</span><span class="sxs-lookup"><span data-stu-id="60145-151">System.String</span></span>

## <span data-ttu-id="60145-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="60145-152">NOTES</span></span>

## <span data-ttu-id="60145-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="60145-153">RELATED LINKS</span></span>
