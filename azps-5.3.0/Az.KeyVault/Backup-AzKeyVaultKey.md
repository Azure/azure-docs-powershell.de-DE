---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: 88decaffa736f015b8e65aa1217eab4899b07c7c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472362"
---
# <span data-ttu-id="b9b21-101">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b9b21-101">Backup-AzKeyVaultKey</span></span>

## <span data-ttu-id="b9b21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9b21-102">SYNOPSIS</span></span>
<span data-ttu-id="b9b21-103">Sichern eines Schlüssels in einem Schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="b9b21-103">Backs up a key in a key vault.</span></span>

## <span data-ttu-id="b9b21-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9b21-104">SYNTAX</span></span>

### <span data-ttu-id="b9b21-105">ByKeyName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b9b21-105">ByKeyName (Default)</span></span>
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9b21-106">HsmByKeyName</span><span class="sxs-lookup"><span data-stu-id="b9b21-106">HsmByKeyName</span></span>
```
Backup-AzKeyVaultKey -HsmName <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9b21-107">ByKey</span><span class="sxs-lookup"><span data-stu-id="b9b21-107">ByKey</span></span>
```
Backup-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9b21-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b9b21-108">DESCRIPTION</span></span>
<span data-ttu-id="b9b21-109">Das **Cmdlet "Backup-AzKeyVaultKey"** sichern einen angegebenen Schlüssel in einem Schlüsseltresor, indem es ihn herunter- und in einer Datei speichert.</span><span class="sxs-lookup"><span data-stu-id="b9b21-109">The **Backup-AzKeyVaultKey** cmdlet backs up a specified key in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="b9b21-110">Wenn mehrere Versionen des Schlüssels vorhanden sind, sind alle Versionen in der Sicherung enthalten.</span><span class="sxs-lookup"><span data-stu-id="b9b21-110">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="b9b21-111">Da die heruntergeladenen Inhalte verschlüsselt sind, können sie nicht außerhalb des Azure Key Vault verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b9b21-111">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="b9b21-112">Sie können einen gesicherten Schlüssel in einem beliebigen Schlüsseltresor im Abonnement wiederherstellen, von dem er gesichert wurde.</span><span class="sxs-lookup"><span data-stu-id="b9b21-112">You can restore a backed-up key to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="b9b21-113">Typische Gründe für die Verwendung dieses Cmdlets sind:</span><span class="sxs-lookup"><span data-stu-id="b9b21-113">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="b9b21-114">Sie möchten eine Kopie Ihres Schlüssels einsperren, damit Sie über eine Offlinekopie verfügen, falls Sie den Schlüssel versehentlich in Ihrem Schlüsseltresor gelöscht haben.</span><span class="sxs-lookup"><span data-stu-id="b9b21-114">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your key vault.</span></span>
 
- <span data-ttu-id="b9b21-115">Sie haben einen Schlüssel mithilfe des Schlüsseltresor erstellt und möchten den Schlüssel jetzt in eine andere Azure-Region klonen, damit Sie ihn aus allen Instanzen Ihrer verteilten Anwendung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="b9b21-115">You created a key using Key Vault and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="b9b21-116">Verwenden Sie das **Cmdlet "Backup-AzKeyVaultKey",** um den Schlüssel im verschlüsselten Format abzurufen. Verwenden Sie dann das Cmdlet Restore-AzKeyVaultKey, und geben Sie einen Schlüsseltresor in der zweiten Region an.</span><span class="sxs-lookup"><span data-stu-id="b9b21-116">Use the **Backup-AzKeyVaultKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzKeyVaultKey cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="b9b21-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b9b21-117">EXAMPLES</span></span>

### <span data-ttu-id="b9b21-118">Beispiel 1: Sichern eines Schlüssels mit einem automatisch generierten Dateinamen</span><span class="sxs-lookup"><span data-stu-id="b9b21-118">Example 1: Back up a key with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'

C:\Users\username\mykeyvault-mykey-1527029447.01191
```

<span data-ttu-id="b9b21-119">Dieser Befehl ruft den Schlüssel namens "MyKey" aus dem Schlüsseltresor "MyKeyVault" ab, speichert eine Sicherung dieses Schlüssels in einer Datei, die automatisch nach Ihnen benannt wird, und zeigt den Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="b9b21-119">This command retrieves the key named MyKey from the key vault named MyKeyVault and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="b9b21-120">Beispiel 2: Sichern eines Schlüssels unter einem angegebenen Dateinamen</span><span class="sxs-lookup"><span data-stu-id="b9b21-120">Example 2: Back up a key to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="b9b21-121">Dieser Befehl ruft den Schlüssel namens "MyKey" aus dem Schlüsseltresornamen "MyKeyVault" ab und speichert eine Sicherung dieses Schlüssels in einer Datei namens "Backup.blob".</span><span class="sxs-lookup"><span data-stu-id="b9b21-121">This command retrieves the key named MyKey from the key vaultnamed MyKeyVault and saves a backup of that key to a file named Backup.blob.</span></span>

### <span data-ttu-id="b9b21-122">Beispiel 3: Sichern eines zuvor abgerufenen Schlüssels unter einem angegebenen Dateinamen, Überschreiben der Zieldatei ohne Eingabeaufforderung.</span><span class="sxs-lookup"><span data-stu-id="b9b21-122">Example 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\> Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="b9b21-123">Dieser Befehl erstellt eine Sicherung des Schlüssels namens $key. Name im Tresor namens $key. VaultName in eine Datei mit dem Namen "Backup.blob", und überschreiben die Datei, sofern sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b9b21-123">This command creates a backup of the key named $key.Name in the vault named $key.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="b9b21-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9b21-124">PARAMETERS</span></span>

### <span data-ttu-id="b9b21-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9b21-125">-DefaultProfile</span></span>
<span data-ttu-id="b9b21-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="b9b21-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9b21-127">-Force</span><span class="sxs-lookup"><span data-stu-id="b9b21-127">-Force</span></span>
<span data-ttu-id="b9b21-128">Überschreiben der vorhandenen Datei</span><span class="sxs-lookup"><span data-stu-id="b9b21-128">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="b9b21-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="b9b21-129">-HsmName</span></span>
<span data-ttu-id="b9b21-130">HSM-Name.</span><span class="sxs-lookup"><span data-stu-id="b9b21-130">HSM name.</span></span> <span data-ttu-id="b9b21-131">Das Cmdlet erstellt den FQDN eines verwalteten HSM basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="b9b21-131">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByKeyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b21-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9b21-132">-InputObject</span></span>
<span data-ttu-id="b9b21-133">Key bundle to back up, pipelined in from the output of a retrieval call.</span><span class="sxs-lookup"><span data-stu-id="b9b21-133">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="b9b21-134">-Name</span><span class="sxs-lookup"><span data-stu-id="b9b21-134">-Name</span></span>
<span data-ttu-id="b9b21-135">Gibt den Namen des zu sichernden Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="b9b21-135">Specifies the name of the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, HsmByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b21-136">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="b9b21-136">-OutputFile</span></span>
<span data-ttu-id="b9b21-137">Gibt die Ausgabedatei an, in der das Sicherungs-BLOB gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="b9b21-137">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="b9b21-138">Wenn Sie diesen Parameter nicht angeben, generiert dieses Cmdlet einen Dateinamen für Sie.</span><span class="sxs-lookup"><span data-stu-id="b9b21-138">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="b9b21-139">Wenn Sie den Namen einer vorhandenen Ausgabedatei angeben, wird der Vorgang nicht abgeschlossen und eine Fehlermeldung zurückgegeben, dass die Sicherungsdatei bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b9b21-139">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="b9b21-140">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b9b21-140">-VaultName</span></span>
<span data-ttu-id="b9b21-141">Gibt den Namen des Schlüsseltresor an, der den zu sichernden Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="b9b21-141">Specifies the name of the key vault that contains the key to back up.</span></span>

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

### <span data-ttu-id="b9b21-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9b21-142">-Confirm</span></span>
<span data-ttu-id="b9b21-143">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b9b21-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9b21-144">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b9b21-144">-WhatIf</span></span>
<span data-ttu-id="b9b21-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b9b21-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9b21-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b9b21-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9b21-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9b21-147">CommonParameters</span></span>
<span data-ttu-id="b9b21-148">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9b21-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9b21-149">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9b21-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9b21-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b9b21-150">INPUTS</span></span>

### <span data-ttu-id="b9b21-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="b9b21-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="b9b21-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b9b21-152">OUTPUTS</span></span>

### <span data-ttu-id="b9b21-153">System.String</span><span class="sxs-lookup"><span data-stu-id="b9b21-153">System.String</span></span>

## <span data-ttu-id="b9b21-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b9b21-154">NOTES</span></span>

## <span data-ttu-id="b9b21-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b9b21-155">RELATED LINKS</span></span>

[<span data-ttu-id="b9b21-156">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b9b21-156">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="b9b21-157">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b9b21-157">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="b9b21-158">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b9b21-158">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="b9b21-159">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b9b21-159">Restore-AzKeyVaultKey</span></span>](./Restore-AzKeyVaultKey.md)

