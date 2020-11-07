---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultsecret
schema: 2.0.0
ms.openlocfilehash: cd83d61c64e4111faf7fc6149107e172d0cf0c9f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848251"
---
# <span data-ttu-id="16e26-101">Backup-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="16e26-101">Backup-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="16e26-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="16e26-102">SYNOPSIS</span></span>
<span data-ttu-id="16e26-103">Sichern eines Geheimnisses in einem schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="16e26-103">Backs up a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16e26-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="16e26-104">SYNTAX</span></span>

### <span data-ttu-id="16e26-105">BySecretName (Standard)</span><span class="sxs-lookup"><span data-stu-id="16e26-105">BySecretName (Default)</span></span>
```
Backup-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16e26-106">BySecret</span><span class="sxs-lookup"><span data-stu-id="16e26-106">BySecret</span></span>
```
Backup-AzureKeyVaultSecret [-Secret] <Secret> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16e26-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="16e26-107">DESCRIPTION</span></span>
<span data-ttu-id="16e26-108">Mit dem Cmdlet " **Backup-AzureKeyVaultSecret** " wird ein angegebener Schlüssel in einem Schlüsseldepot gesichert, indem es heruntergeladen und in einer Datei gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="16e26-108">The **Backup-AzureKeyVaultSecret** cmdlet backs up a specified secret in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="16e26-109">Wenn mehrere Versionen des geheimen Schlüssels vorhanden sind, werden alle Versionen in die Sicherung aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="16e26-109">If there are multiple versions of the secret, all versions are included in the backup.</span></span>
<span data-ttu-id="16e26-110">Da der heruntergeladene Inhalt verschlüsselt ist, kann er nicht außerhalb des Azure Key Vault verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="16e26-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="16e26-111">Sie können ein gesichertes Geheimnis in einem beliebigen schlüsseltresor des Abonnements wiederherstellen, von dem es gesichert wurde.</span><span class="sxs-lookup"><span data-stu-id="16e26-111">You can restore a backed-up secret to any key vault in the subscription that it was backed up from.</span></span>

<span data-ttu-id="16e26-112">Typische Gründe für die Verwendung dieses Cmdlets sind:</span><span class="sxs-lookup"><span data-stu-id="16e26-112">Typical reasons to use this cmdlet are:</span></span>

- <span data-ttu-id="16e26-113">Sie möchten eine Kopie Ihres Geheimnisses hinterlegen, damit Sie eine Offlinekopie haben, falls Sie Ihr Kennwort versehentlich in Ihrem schlüsseltresor löschen.</span><span class="sxs-lookup"><span data-stu-id="16e26-113">You want to escrow a copy of your secret, so that you have an offline copy in case you accidentally delete your secret in your key vault.</span></span>
- <span data-ttu-id="16e26-114">Sie haben einem schlüsseltresor ein Kennwort hinzugefügt und möchten das Geheimnis nun in einen anderen Azure-Bereich Klonen, damit Sie es in allen Instanzen ihrer verteilten Anwendung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="16e26-114">You added a secret to a key vault and now want to clone the secret into a different Azure region, so that you can use it from all instances of your distributed application.</span></span> <span data-ttu-id="16e26-115">Verwenden Sie das Backup-AzureKeyVaultSecret-Cmdlet, um das Geheimnis im verschlüsselten Format abzurufen, und verwenden Sie dann das Cmdlet Restore-AzureKeyVaultSecret, und geben Sie einen schlüsseltresor im zweiten Bereich an.</span><span class="sxs-lookup"><span data-stu-id="16e26-115">Use the Backup-AzureKeyVaultSecret cmdlet to retrieve the secret in encrypted format and then use the Restore-AzureKeyVaultSecret cmdlet and specify a key vault in the second region.</span></span> <span data-ttu-id="16e26-116">(Beachten Sie, dass die Regionen zur gleichen geografischen Region gehören müssen.)</span><span class="sxs-lookup"><span data-stu-id="16e26-116">(Note that the regions must belong to the same geography.)</span></span>

## <span data-ttu-id="16e26-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="16e26-117">EXAMPLES</span></span>

### <span data-ttu-id="16e26-118">Beispiel 1: Sichern eines Geheimnisses mit einem automatisch generierten Dateinamen</span><span class="sxs-lookup"><span data-stu-id="16e26-118">Example 1: Back up a secret with an automatically generated file name</span></span>
```
PS C:\>Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="16e26-119">Dieser Befehl ruft den geheimen Namen "MySecret" aus dem schlüsseltresor mit dem Namen MyKeyVault ab und speichert eine Sicherungskopie dieses Geheimnisses in einer Datei, die automatisch nach ihnen benannt wird, und zeigt den Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="16e26-119">This command retrieves the secret named MySecret from the key vault named MyKeyVault and saves a backup of that secret to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="16e26-120">Beispiel 2: Sichern eines Geheimnisses zu einem angegebenen Dateinamen, Überschreiben der vorhandenen Datei ohne Aufforderung</span><span class="sxs-lookup"><span data-stu-id="16e26-120">Example 2: Back up a secret to a specified file name, overwriting the existing file without prompting</span></span>
```
PS C:\>Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force
```

<span data-ttu-id="16e26-121">Dieser Befehl ruft den geheimen Namen "MySecret" aus dem Schlüssel vaultnamed MyKeyVault ab und speichert eine Sicherungskopie dieses Geheimnisses in einer Datei mit dem Namen Backup. BLOB.</span><span class="sxs-lookup"><span data-stu-id="16e26-121">This command retrieves the secret named MySecret from the key vaultnamed MyKeyVault and saves a backup of that secret to a file named Backup.blob.</span></span>

### <span data-ttu-id="16e26-122">Beispiel 3: Sichern eines zuvor abgerufenen Geheimnisses in einem angegebenen Dateinamen</span><span class="sxs-lookup"><span data-stu-id="16e26-122">Example 3: Back up a secret previously retrieved to a specified file name</span></span>
```
PS C:\>$secret = Get-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\>Backup-AzureKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'
```

<span data-ttu-id="16e26-123">Dieser Befehl verwendet den Tresor Namen und den Namen des $Secret Objekts, um den geheimen Schlüssel abzurufen und seine Sicherung in einer Datei mit dem Namen Backup. BLOB zu speichern.</span><span class="sxs-lookup"><span data-stu-id="16e26-123">This command uses the $secret object's vault name and name to retrieves the secret and saves its backup to a file named Backup.blob.</span></span>

## <span data-ttu-id="16e26-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="16e26-124">PARAMETERS</span></span>

### <span data-ttu-id="16e26-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16e26-125">-DefaultProfile</span></span>
<span data-ttu-id="16e26-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="16e26-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16e26-127">-Force</span><span class="sxs-lookup"><span data-stu-id="16e26-127">-Force</span></span>
<span data-ttu-id="16e26-128">Sie werden zur Bestätigung aufgefordert, bevor Sie die Ausgabedatei überschreiben (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="16e26-128">Prompts you for confirmation before overwriting the output file, if that exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16e26-129">-Name</span><span class="sxs-lookup"><span data-stu-id="16e26-129">-Name</span></span>
<span data-ttu-id="16e26-130">Gibt den Namen des zu sichernden Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="16e26-130">Specifies the name of the secret to back up.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16e26-131">-Outputdatei</span><span class="sxs-lookup"><span data-stu-id="16e26-131">-OutputFile</span></span>
<span data-ttu-id="16e26-132">Gibt die Ausgabedatei an, in der das Sicherungs-BLOB gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="16e26-132">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="16e26-133">Wenn Sie diesen Parameter nicht angeben, generiert dieses Cmdlet einen Dateinamen für Sie.</span><span class="sxs-lookup"><span data-stu-id="16e26-133">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="16e26-134">Wenn Sie den Namen einer vorhandenen Ausgabedatei angeben, wird der Vorgang nicht abgeschlossen, und es wird eine Fehlermeldung zurückgegeben, dass die Sicherungsdatei bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="16e26-134">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16e26-135">-Secret</span><span class="sxs-lookup"><span data-stu-id="16e26-135">-Secret</span></span>
<span data-ttu-id="16e26-136">Gibt das Objekt an, dessen Name und Vault für den Sicherungsvorgang verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="16e26-136">Specifies the object whose name and vault should be used for the backup operation.</span></span>

```yaml
Type: Secret
Parameter Sets: BySecret
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16e26-137">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="16e26-137">-VaultName</span></span>
<span data-ttu-id="16e26-138">Gibt den Namen des Schlüssel Tresors an, der das zu sichernde Geheimnis enthält.</span><span class="sxs-lookup"><span data-stu-id="16e26-138">Specifies the name of the key vault that contains the secret to back up.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16e26-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="16e26-139">-Confirm</span></span>
<span data-ttu-id="16e26-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="16e26-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16e26-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16e26-141">-WhatIf</span></span>
<span data-ttu-id="16e26-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="16e26-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16e26-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="16e26-143">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16e26-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16e26-144">CommonParameters</span></span>
<span data-ttu-id="16e26-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16e26-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16e26-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16e26-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16e26-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="16e26-147">INPUTS</span></span>

## <span data-ttu-id="16e26-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="16e26-148">OUTPUTS</span></span>

### <span data-ttu-id="16e26-149">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="16e26-149">String</span></span>
<span data-ttu-id="16e26-150">Das Cmdlet gibt den Pfad der Ausgabedatei zurück, die die Sicherung des Schlüssels enthält.</span><span class="sxs-lookup"><span data-stu-id="16e26-150">The cmdlet returns the path of the output file containing the backup of the key.</span></span>

## <span data-ttu-id="16e26-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="16e26-151">NOTES</span></span>

## <span data-ttu-id="16e26-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="16e26-152">RELATED LINKS</span></span>

[<span data-ttu-id="16e26-153">Satz-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="16e26-153">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="16e26-154">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="16e26-154">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="16e26-155">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="16e26-155">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="16e26-156">Wiederherstellen – AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="16e26-156">Restore-AzureKeyVaultSecret</span></span>](./Restore-AzureKeyVaultSecret.md)

