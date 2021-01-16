---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
ms.openlocfilehash: a171f967a937873b85adcfca732987037e6db0a6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305736"
---
# <span data-ttu-id="23d20-101">Backup-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="23d20-101">Backup-AzKeyVaultSecret</span></span>

## <span data-ttu-id="23d20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23d20-102">SYNOPSIS</span></span>
<span data-ttu-id="23d20-103">Ein Geheimschlüssel in einem Schlüsseltresor wird sichern.</span><span class="sxs-lookup"><span data-stu-id="23d20-103">Backs up a secret in a key vault.</span></span>

## <span data-ttu-id="23d20-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23d20-104">SYNTAX</span></span>

### <span data-ttu-id="23d20-105">BySecretName (Standard)</span><span class="sxs-lookup"><span data-stu-id="23d20-105">BySecretName (Default)</span></span>
```
Backup-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23d20-106">BySecret</span><span class="sxs-lookup"><span data-stu-id="23d20-106">BySecret</span></span>
```
Backup-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23d20-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="23d20-107">DESCRIPTION</span></span>
<span data-ttu-id="23d20-108">Das **Cmdlet "Backup-AzKeyVaultSecret"** sichern einen angegebenen Geheimschlüssel in einem Schlüsseltresor, indem es ihn herunter- und in einer Datei speichert.</span><span class="sxs-lookup"><span data-stu-id="23d20-108">The **Backup-AzKeyVaultSecret** cmdlet backs up a specified secret in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="23d20-109">Wenn mehrere Versionen des geheimen Schlüssels vorhanden sind, sind alle Versionen in der Sicherung enthalten.</span><span class="sxs-lookup"><span data-stu-id="23d20-109">If there are multiple versions of the secret, all versions are included in the backup.</span></span>
<span data-ttu-id="23d20-110">Da die heruntergeladenen Inhalte verschlüsselt sind, können sie nicht außerhalb des Azure Key Vault verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="23d20-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="23d20-111">Sie können einen gesicherten Geheimschlüssel für jeden Schlüsseltresor in dem Abonnement wiederherstellen, von dem es gesichert wurde.</span><span class="sxs-lookup"><span data-stu-id="23d20-111">You can restore a backed-up secret to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="23d20-112">Typische Gründe für die Verwendung dieses Cmdlets sind:</span><span class="sxs-lookup"><span data-stu-id="23d20-112">Typical reasons to use this cmdlet are:</span></span>
- <span data-ttu-id="23d20-113">Sie möchten eine Kopie Ihres geheimen Schlüssels einsperren, damit Sie über eine Offlinekopie verfügen, falls Sie ihr Geheimes versehentlich in Ihrem Schlüsseltresor löschen.</span><span class="sxs-lookup"><span data-stu-id="23d20-113">You want to escrow a copy of your secret, so that you have an offline copy in case you accidentally delete your secret in your key vault.</span></span>
- <span data-ttu-id="23d20-114">Sie haben einem Schlüsseltresor ein Geheimnis hinzugefügt und möchten es nun in eine andere Azure-Region klonen, damit Sie es in allen Instanzen Ihrer verteilten Anwendung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="23d20-114">You added a secret to a key vault and now want to clone the secret into a different Azure region, so that you can use it from all instances of your distributed application.</span></span> <span data-ttu-id="23d20-115">Verwenden Sie das Backup-AzKeyVaultSecret-Cmdlet, um den geheimen Schlüssel im verschlüsselten Format abzurufen. Verwenden Sie dann das Cmdlet Restore-AzKeyVaultSecret, und geben Sie einen Schlüsseltresor in der zweiten Region an.</span><span class="sxs-lookup"><span data-stu-id="23d20-115">Use the Backup-AzKeyVaultSecret cmdlet to retrieve the secret in encrypted format and then use the Restore-AzKeyVaultSecret cmdlet and specify a key vault in the second region.</span></span> <span data-ttu-id="23d20-116">(Beachten Sie, dass die Regionen derselben Geografie angehören müssen.)</span><span class="sxs-lookup"><span data-stu-id="23d20-116">(Note that the regions must belong to the same geography.)</span></span>

## <span data-ttu-id="23d20-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="23d20-117">EXAMPLES</span></span>

### <span data-ttu-id="23d20-118">Beispiel 1: Sichern eines geheimen Schlüssels mit einem automatisch generierten Dateinamen</span><span class="sxs-lookup"><span data-stu-id="23d20-118">Example 1: Back up a secret with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'

C:\Users\username\mykeyvault-mysecret-1527029447.01191
```

<span data-ttu-id="23d20-119">Dieser Befehl ruft den geheimen Namen "MySecret" aus dem Schlüsseltresor "MyKeyVault" ab, speichert eine Sicherung dieses Geheimschlüssels in einer Datei, die automatisch nach Ihnen benannt wird, und zeigt den Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="23d20-119">This command retrieves the secret named MySecret from the key vault named MyKeyVault and saves a backup of that secret to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="23d20-120">Beispiel 2: Sichern eines Geheimtipps für einen angegebenen Dateinamen, Überschreiben der vorhandenen Datei ohne Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="23d20-120">Example 2: Back up a secret to a specified file name, overwriting the existing file without prompting</span></span>
```powershell
PS C:\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="23d20-121">Dieser Befehl ruft den geheimen Namen "MySecret" aus dem Schlüsseltresor "MyKeyVault" ab und speichert eine Sicherung dieses Geheimschlüssels in einer Datei mit dem Namen "Backup.blob".</span><span class="sxs-lookup"><span data-stu-id="23d20-121">This command retrieves the secret named MySecret from the key vaultnamed MyKeyVault and saves a backup of that secret to a file named Backup.blob.</span></span>

### <span data-ttu-id="23d20-122">Beispiel 3: Sichern eines geheimen Schlüssels, der zuvor unter einem angegebenen Dateinamen abgerufen wurde</span><span class="sxs-lookup"><span data-stu-id="23d20-122">Example 3: Back up a secret previously retrieved to a specified file name</span></span>
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\> Backup-AzKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="23d20-123">Dieser Befehl verwendet den $secret und Den Namen des $secret objekts, um den geheimen Schlüssel abzurufen, und speichert seine Sicherung in einer Datei namens "Backup.BLOB".</span><span class="sxs-lookup"><span data-stu-id="23d20-123">This command uses the $secret object's vault name and name to retrieves the secret and saves its backup to a file named Backup.blob.</span></span>

## <span data-ttu-id="23d20-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23d20-124">PARAMETERS</span></span>

### <span data-ttu-id="23d20-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23d20-125">-DefaultProfile</span></span>
<span data-ttu-id="23d20-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="23d20-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23d20-127">-Force</span><span class="sxs-lookup"><span data-stu-id="23d20-127">-Force</span></span>
<span data-ttu-id="23d20-128">Fordert Sie zur Bestätigung auf, bevor Sie die Ausgabedatei überschreiben, sofern diese vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="23d20-128">Prompts you for confirmation before overwriting the output file, if that exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d20-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23d20-129">-InputObject</span></span>
<span data-ttu-id="23d20-130">Das Geheime, das gesichert werden soll, wird aus der Ausgabe eines Abrufanrufs pipelineiert.</span><span class="sxs-lookup"><span data-stu-id="23d20-130">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: BySecret
Aliases: Secret

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23d20-131">-Name</span><span class="sxs-lookup"><span data-stu-id="23d20-131">-Name</span></span>
<span data-ttu-id="23d20-132">Gibt den Namen des zu sichernden Geheimtipps an.</span><span class="sxs-lookup"><span data-stu-id="23d20-132">Specifies the name of the secret to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d20-133">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="23d20-133">-OutputFile</span></span>
<span data-ttu-id="23d20-134">Gibt die Ausgabedatei an, in der das Sicherungs-BLOB gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="23d20-134">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="23d20-135">Wenn Sie diesen Parameter nicht angeben, generiert dieses Cmdlet einen Dateinamen für Sie.</span><span class="sxs-lookup"><span data-stu-id="23d20-135">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="23d20-136">Wenn Sie den Namen einer vorhandenen Ausgabedatei angeben, wird der Vorgang nicht abgeschlossen und eine Fehlermeldung zurückgegeben, dass die Sicherungsdatei bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="23d20-136">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="23d20-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="23d20-137">-VaultName</span></span>
<span data-ttu-id="23d20-138">Gibt den Namen des Schlüsseltresor an, der das zu sichernde Geheimnis enthält.</span><span class="sxs-lookup"><span data-stu-id="23d20-138">Specifies the name of the key vault that contains the secret to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d20-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23d20-139">-Confirm</span></span>
<span data-ttu-id="23d20-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="23d20-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d20-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="23d20-141">-WhatIf</span></span>
<span data-ttu-id="23d20-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="23d20-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23d20-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="23d20-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d20-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23d20-144">CommonParameters</span></span>
<span data-ttu-id="23d20-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23d20-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23d20-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23d20-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23d20-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="23d20-147">INPUTS</span></span>

### <span data-ttu-id="23d20-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="23d20-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="23d20-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="23d20-149">OUTPUTS</span></span>

### <span data-ttu-id="23d20-150">System.String</span><span class="sxs-lookup"><span data-stu-id="23d20-150">System.String</span></span>

## <span data-ttu-id="23d20-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="23d20-151">NOTES</span></span>

## <span data-ttu-id="23d20-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="23d20-152">RELATED LINKS</span></span>

[<span data-ttu-id="23d20-153">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="23d20-153">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="23d20-154">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="23d20-154">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="23d20-155">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="23d20-155">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="23d20-156">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="23d20-156">Restore-AzKeyVaultSecret</span></span>](./Restore-AzKeyVaultSecret.md)

