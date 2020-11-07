---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://go.microsoft.com/fwlink/?LinkId=690296
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultSecret.md
ms.openlocfilehash: c53006a4f059fe1f243d9e0bf7a4c701a4c417a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665375"
---
# <span data-ttu-id="37235-101">Backup-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="37235-101">Backup-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="37235-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="37235-102">SYNOPSIS</span></span>
<span data-ttu-id="37235-103">Sichern eines Geheimnisses in einem schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="37235-103">Backs up a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37235-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="37235-104">SYNTAX</span></span>

### <span data-ttu-id="37235-105">BySecretName (Standard)</span><span class="sxs-lookup"><span data-stu-id="37235-105">BySecretName (Default)</span></span>
```
Backup-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37235-106">BySecret</span><span class="sxs-lookup"><span data-stu-id="37235-106">BySecret</span></span>
```
Backup-AzureKeyVaultSecret [-Secret] <Secret> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37235-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37235-107">DESCRIPTION</span></span>
<span data-ttu-id="37235-108">Mit dem Cmdlet " **Backup-AzureKeyVaultSecret** " wird ein angegebener Schlüssel in einem Schlüsseldepot gesichert, indem es heruntergeladen und in einer Datei gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="37235-108">The **Backup-AzureKeyVaultSecret** cmdlet backs up a specified secret in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="37235-109">Wenn mehrere Versionen des geheimen Schlüssels vorhanden sind, werden alle Versionen in die Sicherung aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="37235-109">If there are multiple versions of the secret, all versions are included in the backup.</span></span>
<span data-ttu-id="37235-110">Da der heruntergeladene Inhalt verschlüsselt ist, kann er nicht außerhalb des Azure Key Vault verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37235-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="37235-111">Sie können ein gesichertes Geheimnis in einem beliebigen schlüsseltresor des Abonnements wiederherstellen, von dem es gesichert wurde.</span><span class="sxs-lookup"><span data-stu-id="37235-111">You can restore a backed-up secret to any key vault in the subscription that it was backed up from.</span></span>

<span data-ttu-id="37235-112">Typische Gründe für die Verwendung dieses Cmdlets sind:</span><span class="sxs-lookup"><span data-stu-id="37235-112">Typical reasons to use this cmdlet are:</span></span>

- <span data-ttu-id="37235-113">Sie möchten eine Kopie Ihres Geheimnisses hinterlegen, damit Sie eine Offlinekopie haben, falls Sie Ihr Kennwort versehentlich in Ihrem schlüsseltresor löschen.</span><span class="sxs-lookup"><span data-stu-id="37235-113">You want to escrow a copy of your secret, so that you have an offline copy in case you accidentally delete your secret in your key vault.</span></span>
- <span data-ttu-id="37235-114">Sie haben einem schlüsseltresor ein Kennwort hinzugefügt und möchten das Geheimnis nun in einen anderen Azure-Bereich Klonen, damit Sie es in allen Instanzen ihrer verteilten Anwendung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="37235-114">You added a secret to a key vault and now want to clone the secret into a different Azure region, so that you can use it from all instances of your distributed application.</span></span> <span data-ttu-id="37235-115">Verwenden Sie das Backup-AzureKeyVaultSecret-Cmdlet, um das Geheimnis im verschlüsselten Format abzurufen, und verwenden Sie dann das Cmdlet Restore-AzureKeyVaultSecret, und geben Sie einen schlüsseltresor im zweiten Bereich an.</span><span class="sxs-lookup"><span data-stu-id="37235-115">Use the Backup-AzureKeyVaultSecret cmdlet to retrieve the secret in encrypted format and then use the Restore-AzureKeyVaultSecret cmdlet and specify a key vault in the second region.</span></span> <span data-ttu-id="37235-116">(Beachten Sie, dass die Regionen zur gleichen geografischen Region gehören müssen.)</span><span class="sxs-lookup"><span data-stu-id="37235-116">(Note that the regions must belong to the same geography.)</span></span>

## <span data-ttu-id="37235-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37235-117">EXAMPLES</span></span>

### <span data-ttu-id="37235-118">Beispiel 1: Sichern eines Geheimnisses mit einem automatisch generierten Dateinamen</span><span class="sxs-lookup"><span data-stu-id="37235-118">Example 1: Back up a secret with an automatically generated file name</span></span>
```
PS C:\>Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="37235-119">Dieser Befehl ruft den geheimen Namen "MySecret" aus dem schlüsseltresor mit dem Namen MyKeyVault ab und speichert eine Sicherungskopie dieses Geheimnisses in einer Datei, die automatisch nach ihnen benannt wird, und zeigt den Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="37235-119">This command retrieves the secret named MySecret from the key vault named MyKeyVault and saves a backup of that secret to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="37235-120">Beispiel 2: Sichern eines Geheimnisses zu einem angegebenen Dateinamen, Überschreiben der vorhandenen Datei ohne Aufforderung</span><span class="sxs-lookup"><span data-stu-id="37235-120">Example 2: Back up a secret to a specified file name, overwriting the existing file without prompting</span></span>
```
PS C:\>Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force
```

<span data-ttu-id="37235-121">Dieser Befehl ruft den geheimen Namen "MySecret" aus dem Schlüssel vaultnamed MyKeyVault ab und speichert eine Sicherungskopie dieses Geheimnisses in einer Datei mit dem Namen Backup. BLOB.</span><span class="sxs-lookup"><span data-stu-id="37235-121">This command retrieves the secret named MySecret from the key vaultnamed MyKeyVault and saves a backup of that secret to a file named Backup.blob.</span></span>

### <span data-ttu-id="37235-122">Beispiel 3: Sichern eines zuvor abgerufenen Geheimnisses in einem angegebenen Dateinamen</span><span class="sxs-lookup"><span data-stu-id="37235-122">Example 3: Back up a secret previously retrieved to a specified file name</span></span>
```
PS C:\>$secret = Get-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\>Backup-AzureKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'
```

<span data-ttu-id="37235-123">Dieser Befehl verwendet den Tresor Namen und den Namen des $Secret Objekts, um den geheimen Schlüssel abzurufen und seine Sicherung in einer Datei mit dem Namen Backup. BLOB zu speichern.</span><span class="sxs-lookup"><span data-stu-id="37235-123">This command uses the $secret object's vault name and name to retrieves the secret and saves its backup to a file named Backup.blob.</span></span>

## <span data-ttu-id="37235-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="37235-124">PARAMETERS</span></span>

### <span data-ttu-id="37235-125">-Force</span><span class="sxs-lookup"><span data-stu-id="37235-125">-Force</span></span>
<span data-ttu-id="37235-126">Sie werden zur Bestätigung aufgefordert, bevor Sie die Ausgabedatei überschreiben (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="37235-126">Prompts you for confirmation before overwriting the output file, if that exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37235-127">-Name</span><span class="sxs-lookup"><span data-stu-id="37235-127">-Name</span></span>
<span data-ttu-id="37235-128">Gibt den Namen des zu sichernden Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="37235-128">Specifies the name of the secret to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37235-129">-Outputdatei</span><span class="sxs-lookup"><span data-stu-id="37235-129">-OutputFile</span></span>
<span data-ttu-id="37235-130">Gibt die Ausgabedatei an, in der das Sicherungs-BLOB gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="37235-130">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="37235-131">Wenn Sie diesen Parameter nicht angeben, generiert dieses Cmdlet einen Dateinamen für Sie.</span><span class="sxs-lookup"><span data-stu-id="37235-131">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="37235-132">Wenn Sie den Namen einer vorhandenen Ausgabedatei angeben, wird der Vorgang nicht abgeschlossen, und es wird eine Fehlermeldung zurückgegeben, dass die Sicherungsdatei bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="37235-132">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37235-133">-Secret</span><span class="sxs-lookup"><span data-stu-id="37235-133">-Secret</span></span>
<span data-ttu-id="37235-134">Gibt das Objekt an, dessen Name und Vault für den Sicherungsvorgang verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="37235-134">Specifies the object whose name and vault should be used for the backup operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.Secret
Parameter Sets: BySecret
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37235-135">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="37235-135">-VaultName</span></span>
<span data-ttu-id="37235-136">Gibt den Namen des Schlüssel Tresors an, der das zu sichernde Geheimnis enthält.</span><span class="sxs-lookup"><span data-stu-id="37235-136">Specifies the name of the key vault that contains the secret to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37235-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="37235-137">-Confirm</span></span>
<span data-ttu-id="37235-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="37235-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37235-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37235-139">-WhatIf</span></span>
<span data-ttu-id="37235-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37235-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37235-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37235-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37235-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37235-142">-DefaultProfile</span></span>
<span data-ttu-id="37235-143">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="37235-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37235-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37235-144">CommonParameters</span></span>
<span data-ttu-id="37235-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37235-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37235-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37235-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37235-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="37235-147">INPUTS</span></span>

## <span data-ttu-id="37235-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="37235-148">OUTPUTS</span></span>

### <span data-ttu-id="37235-149">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="37235-149">String</span></span>
<span data-ttu-id="37235-150">Das Cmdlet gibt den Pfad der Ausgabedatei zurück, die die Sicherung des Schlüssels enthält.</span><span class="sxs-lookup"><span data-stu-id="37235-150">The cmdlet returns the path of the output file containing the backup of the key.</span></span>

## <span data-ttu-id="37235-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="37235-151">NOTES</span></span>

## <span data-ttu-id="37235-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="37235-152">RELATED LINKS</span></span>

[<span data-ttu-id="37235-153">Satz-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="37235-153">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="37235-154">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="37235-154">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="37235-155">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="37235-155">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="37235-156">Wiederherstellen – AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="37235-156">Restore-AzureKeyVaultSecret</span></span>](./Restore-AzureKeyVaultSecret.md)

