---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultKey.md
ms.openlocfilehash: 2cf7c569a8c8d25f89c5006be4295a980186cbe3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664584"
---
# <span data-ttu-id="983fa-101">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="983fa-101">Backup-AzureKeyVaultKey</span></span>

## <span data-ttu-id="983fa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="983fa-102">SYNOPSIS</span></span>
<span data-ttu-id="983fa-103">Sie können einen Schlüssel in einem schlüsseltresor sichern.</span><span class="sxs-lookup"><span data-stu-id="983fa-103">Backs up a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="983fa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="983fa-104">SYNTAX</span></span>

### <span data-ttu-id="983fa-105">ByKeyName (Standard)</span><span class="sxs-lookup"><span data-stu-id="983fa-105">ByKeyName (Default)</span></span>
```
Backup-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="983fa-106">ByKey</span><span class="sxs-lookup"><span data-stu-id="983fa-106">ByKey</span></span>
```
Backup-AzureKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="983fa-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="983fa-107">DESCRIPTION</span></span>
<span data-ttu-id="983fa-108">Mit dem Cmdlet " **Backup-AzureKeyVaultKey** " wird ein angegebener Schlüssel in einem schlüsseltresor gesichert, indem er heruntergeladen und in einer Datei gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="983fa-108">The **Backup-AzureKeyVaultKey** cmdlet backs up a specified key in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="983fa-109">Wenn mehrere Versionen des Schlüssels vorhanden sind, werden alle Versionen in die Sicherung aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="983fa-109">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="983fa-110">Da der heruntergeladene Inhalt verschlüsselt ist, kann er nicht außerhalb des Azure Key Vault verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="983fa-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="983fa-111">Sie können einen gesicherten Schlüssel in einem beliebigen schlüsseltresor des Abonnements wiederherstellen, von dem es gesichert wurde.</span><span class="sxs-lookup"><span data-stu-id="983fa-111">You can restore a backed-up key to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="983fa-112">Typische Gründe für die Verwendung dieses Cmdlets sind:</span><span class="sxs-lookup"><span data-stu-id="983fa-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="983fa-113">Sie möchten eine Kopie Ihres Schlüssels hinterlegen, damit Sie eine Offlinekopie haben, falls Sie Ihren Schlüssel versehentlich in Ihrem schlüsseltresor löschen.</span><span class="sxs-lookup"><span data-stu-id="983fa-113">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your key vault.</span></span>
 
- <span data-ttu-id="983fa-114">Sie haben einen Schlüssel mithilfe von Key Vault erstellt und möchten nun den Schlüssel in einen anderen Azure-Bereich Klonen, sodass Sie ihn aus allen Instanzen ihrer verteilten Anwendung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="983fa-114">You created a key using Key Vault and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="983fa-115">Verwenden Sie das Cmdlet **Backup-AzureKeyVaultKey** , um den Schlüssel im verschlüsselten Format abzurufen, und verwenden Sie dann das Restore-AzureKeyVaultKey-Cmdlet, und geben Sie einen schlüsseltresor im zweiten Bereich an.</span><span class="sxs-lookup"><span data-stu-id="983fa-115">Use the **Backup-AzureKeyVaultKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzureKeyVaultKey cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="983fa-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="983fa-116">EXAMPLES</span></span>

### <span data-ttu-id="983fa-117">Beispiel 1: Sichern eines Schlüssels mit einem automatisch generierten Dateinamen</span><span class="sxs-lookup"><span data-stu-id="983fa-117">Example 1: Back up a key with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'

C:\Users\username\mykeyvault-mykey-1527029447.01191
```

<span data-ttu-id="983fa-118">Dieser Befehl ruft den Schlüssel mit dem Namen MyKey aus dem schlüsseltresor mit dem Namen MyKeyVault ab und speichert eine Sicherungskopie dieses Schlüssels in einer Datei, die automatisch nach ihnen benannt wird, und zeigt den Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="983fa-118">This command retrieves the key named MyKey from the key vault named MyKeyVault and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="983fa-119">Beispiel 2: Sichern eines Schlüssels in einem angegebenen Dateinamen</span><span class="sxs-lookup"><span data-stu-id="983fa-119">Example 2: Back up a key to a specified file name</span></span>
```powershell
PS C:\> Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="983fa-120">Dieser Befehl ruft den Schlüssel mit dem Namen MyKey aus dem Schlüssel vaultnamed MyKeyVault ab und speichert eine Sicherung dieses Schlüssels in einer Datei mit dem Namen Backup. BLOB.</span><span class="sxs-lookup"><span data-stu-id="983fa-120">This command retrieves the key named MyKey from the key vaultnamed MyKeyVault and saves a backup of that key to a file named Backup.blob.</span></span>

### <span data-ttu-id="983fa-121">Beispiel 3: Sichern Sie einen zuvor abgerufenen Schlüssel in einem angegebenen Dateinamen, und überschreiben Sie die Zieldatei ohne Aufforderung.</span><span class="sxs-lookup"><span data-stu-id="983fa-121">Example 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $key = Get-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\> Backup-AzureKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="983fa-122">Mit diesem Befehl wird eine Sicherungskopie des Schlüssels mit dem Namen $Key erstellt. Name im Tresor mit dem Namen $Key. Vaultname in eine Datei mit dem Namen "Backup. BLOB", wobei die Datei im Hintergrund überschrieben wird, wenn Sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="983fa-122">This command creates a backup of the key named $key.Name in the vault named $key.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="983fa-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="983fa-123">PARAMETERS</span></span>

### <span data-ttu-id="983fa-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="983fa-124">-DefaultProfile</span></span>
<span data-ttu-id="983fa-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="983fa-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="983fa-126">-Force</span><span class="sxs-lookup"><span data-stu-id="983fa-126">-Force</span></span>
<span data-ttu-id="983fa-127">Überschreiben der angegebenen Datei, sofern vorhanden</span><span class="sxs-lookup"><span data-stu-id="983fa-127">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="983fa-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="983fa-128">-InputObject</span></span>
<span data-ttu-id="983fa-129">Schlüsselpaket, das von der Ausgabe eines Abruf Anrufs in eine Sicherungskopie geleitet wird.</span><span class="sxs-lookup"><span data-stu-id="983fa-129">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="983fa-130">-Name</span><span class="sxs-lookup"><span data-stu-id="983fa-130">-Name</span></span>
<span data-ttu-id="983fa-131">Gibt den Namen des Schlüssels an, der gesichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="983fa-131">Specifies the name of the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="983fa-132">-Outputdatei</span><span class="sxs-lookup"><span data-stu-id="983fa-132">-OutputFile</span></span>
<span data-ttu-id="983fa-133">Gibt die Ausgabedatei an, in der das Sicherungs-BLOB gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="983fa-133">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="983fa-134">Wenn Sie diesen Parameter nicht angeben, generiert dieses Cmdlet einen Dateinamen für Sie.</span><span class="sxs-lookup"><span data-stu-id="983fa-134">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="983fa-135">Wenn Sie den Namen einer vorhandenen Ausgabedatei angeben, wird der Vorgang nicht abgeschlossen, und es wird eine Fehlermeldung zurückgegeben, dass die Sicherungsdatei bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="983fa-135">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="983fa-136">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="983fa-136">-VaultName</span></span>
<span data-ttu-id="983fa-137">Gibt den Namen des Schlüssel Tresors an, der den zu sichernden Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="983fa-137">Specifies the name of the key vault that contains the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="983fa-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="983fa-138">-Confirm</span></span>
<span data-ttu-id="983fa-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="983fa-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="983fa-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="983fa-140">-WhatIf</span></span>
<span data-ttu-id="983fa-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="983fa-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="983fa-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="983fa-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="983fa-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="983fa-143">CommonParameters</span></span>
<span data-ttu-id="983fa-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="983fa-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="983fa-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="983fa-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="983fa-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="983fa-146">INPUTS</span></span>

### <span data-ttu-id="983fa-147">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="983fa-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>
<span data-ttu-id="983fa-148">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="983fa-148">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="983fa-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="983fa-149">OUTPUTS</span></span>

### <span data-ttu-id="983fa-150">System. String</span><span class="sxs-lookup"><span data-stu-id="983fa-150">System.String</span></span>

## <span data-ttu-id="983fa-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="983fa-151">NOTES</span></span>

## <span data-ttu-id="983fa-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="983fa-152">RELATED LINKS</span></span>

[<span data-ttu-id="983fa-153">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="983fa-153">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="983fa-154">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="983fa-154">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="983fa-155">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="983fa-155">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="983fa-156">Wiederherstellen – AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="983fa-156">Restore-AzureKeyVaultKey</span></span>](./Restore-AzureKeyVaultKey.md)

