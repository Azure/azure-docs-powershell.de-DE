---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/backup-AzKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: d5fce3a4c70593b9478c0efa8afef29021797bb3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842172"
---
# <span data-ttu-id="18401-101">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="18401-101">Backup-AzKeyVaultKey</span></span>

## <span data-ttu-id="18401-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="18401-102">SYNOPSIS</span></span>
<span data-ttu-id="18401-103">Sie können einen Schlüssel in einem schlüsseltresor sichern.</span><span class="sxs-lookup"><span data-stu-id="18401-103">Backs up a key in a key vault.</span></span>

## <span data-ttu-id="18401-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="18401-104">SYNTAX</span></span>

### <span data-ttu-id="18401-105">ByKeyName (Standard)</span><span class="sxs-lookup"><span data-stu-id="18401-105">ByKeyName (Default)</span></span>
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18401-106">ByKey</span><span class="sxs-lookup"><span data-stu-id="18401-106">ByKey</span></span>
```
Backup-AzKeyVaultKey [-Key] <KeyBundle> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18401-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18401-107">DESCRIPTION</span></span>
<span data-ttu-id="18401-108">Mit dem Cmdlet " **Backup-AzKeyVaultKey** " wird ein angegebener Schlüssel in einem schlüsseltresor gesichert, indem er heruntergeladen und in einer Datei gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="18401-108">The **Backup-AzKeyVaultKey** cmdlet backs up a specified key in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="18401-109">Wenn mehrere Versionen des Schlüssels vorhanden sind, werden alle Versionen in die Sicherung aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="18401-109">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="18401-110">Da der heruntergeladene Inhalt verschlüsselt ist, kann er nicht außerhalb des Azure Key Vault verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="18401-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="18401-111">Sie können einen gesicherten Schlüssel in einem beliebigen schlüsseltresor des Abonnements wiederherstellen, von dem es gesichert wurde.</span><span class="sxs-lookup"><span data-stu-id="18401-111">You can restore a backed-up key to any key vault in the subscription that it was backed up from.</span></span>

<span data-ttu-id="18401-112">Typische Gründe für die Verwendung dieses Cmdlets sind:</span><span class="sxs-lookup"><span data-stu-id="18401-112">Typical reasons to use this cmdlet are:</span></span> 

- <span data-ttu-id="18401-113">Sie möchten eine Kopie Ihres Schlüssels hinterlegen, damit Sie eine Offlinekopie haben, falls Sie Ihren Schlüssel versehentlich in Ihrem schlüsseltresor löschen.</span><span class="sxs-lookup"><span data-stu-id="18401-113">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your key vault.</span></span>
 
- <span data-ttu-id="18401-114">Sie haben einen Schlüssel mithilfe von Key Vault erstellt und möchten nun den Schlüssel in einen anderen Azure-Bereich Klonen, sodass Sie ihn aus allen Instanzen ihrer verteilten Anwendung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="18401-114">You created a key using Key Vault and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="18401-115">Verwenden Sie das Cmdlet **Backup-AzKeyVaultKey** , um den Schlüssel im verschlüsselten Format abzurufen, und verwenden Sie dann das Restore-AzKeyVaultKey-Cmdlet, und geben Sie einen schlüsseltresor im zweiten Bereich an.</span><span class="sxs-lookup"><span data-stu-id="18401-115">Use the **Backup-AzKeyVaultKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzKeyVaultKey cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="18401-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="18401-116">EXAMPLES</span></span>

### <span data-ttu-id="18401-117">Beispiel 1: Sichern eines Schlüssels mit einem automatisch generierten Dateinamen</span><span class="sxs-lookup"><span data-stu-id="18401-117">Example 1: Back up a key with an automatically generated file name</span></span>
```
PS C:\>Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="18401-118">Dieser Befehl ruft den Schlüssel mit dem Namen MyKey aus dem schlüsseltresor mit dem Namen MyKeyVault ab und speichert eine Sicherungskopie dieses Schlüssels in einer Datei, die automatisch nach ihnen benannt wird, und zeigt den Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="18401-118">This command retrieves the key named MyKey from the key vault named MyKeyVault and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="18401-119">Beispiel 2: Sichern eines Schlüssels in einem angegebenen Dateinamen</span><span class="sxs-lookup"><span data-stu-id="18401-119">Example 2: Back up a key to a specified file name</span></span>
```
PS C:\>Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'
```

<span data-ttu-id="18401-120">Dieser Befehl ruft den Schlüssel mit dem Namen MyKey aus dem Schlüssel vaultnamed MyKeyVault ab und speichert eine Sicherung dieses Schlüssels in einer Datei mit dem Namen Backup. BLOB.</span><span class="sxs-lookup"><span data-stu-id="18401-120">This command retrieves the key named MyKey from the key vaultnamed MyKeyVault and saves a backup of that key to a file named Backup.blob.</span></span>

### <span data-ttu-id="18401-121">Beispiel 3: Sichern Sie einen zuvor abgerufenen Schlüssel in einem angegebenen Dateinamen, und überschreiben Sie die Zieldatei ohne Aufforderung.</span><span class="sxs-lookup"><span data-stu-id="18401-121">Example 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.</span></span>
```
PS C:\>$key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\>Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force
```

<span data-ttu-id="18401-122">Mit diesem Befehl wird eine Sicherungskopie des Schlüssels mit dem Namen $Key erstellt. Name im Tresor mit dem Namen $Key. Vaultname in eine Datei mit dem Namen "Backup. BLOB", wobei die Datei im Hintergrund überschrieben wird, wenn Sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="18401-122">This command creates a backup of the key named $key.Name in the vault named $key.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="18401-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="18401-123">PARAMETERS</span></span>

### <span data-ttu-id="18401-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18401-124">-DefaultProfile</span></span>
<span data-ttu-id="18401-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="18401-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18401-126">-Force</span><span class="sxs-lookup"><span data-stu-id="18401-126">-Force</span></span>
<span data-ttu-id="18401-127">Überschreiben der angegebenen Datei, sofern vorhanden</span><span class="sxs-lookup"><span data-stu-id="18401-127">Overwrite the given file if it exists</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18401-128">-Taste</span><span class="sxs-lookup"><span data-stu-id="18401-128">-Key</span></span>
<span data-ttu-id="18401-129">Gibt einen zuvor abgerufenen Schlüssel an, der gesichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="18401-129">Specifies a previously retrieved key which is to be backed up.</span></span>

```yaml
Type: KeyBundle
Parameter Sets: ByKey
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18401-130">-Name</span><span class="sxs-lookup"><span data-stu-id="18401-130">-Name</span></span>
<span data-ttu-id="18401-131">Gibt den Namen des Schlüssels an, der gesichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="18401-131">Specifies the name of the key to back up.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18401-132">-Outputdatei</span><span class="sxs-lookup"><span data-stu-id="18401-132">-OutputFile</span></span>
<span data-ttu-id="18401-133">Gibt die Ausgabedatei an, in der das Sicherungs-BLOB gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="18401-133">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="18401-134">Wenn Sie diesen Parameter nicht angeben, generiert dieses Cmdlet einen Dateinamen für Sie.</span><span class="sxs-lookup"><span data-stu-id="18401-134">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="18401-135">Wenn Sie den Namen einer vorhandenen Ausgabedatei angeben, wird der Vorgang nicht abgeschlossen, und es wird eine Fehlermeldung zurückgegeben, dass die Sicherungsdatei bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="18401-135">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="18401-136">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="18401-136">-VaultName</span></span>
<span data-ttu-id="18401-137">Gibt den Namen des Schlüssel Tresors an, der den zu sichernden Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="18401-137">Specifies the name of the key vault that contains the key to back up.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18401-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="18401-138">-Confirm</span></span>
<span data-ttu-id="18401-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="18401-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18401-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18401-140">-WhatIf</span></span>
<span data-ttu-id="18401-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="18401-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18401-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="18401-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18401-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18401-143">CommonParameters</span></span>
<span data-ttu-id="18401-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18401-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18401-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18401-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18401-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="18401-146">INPUTS</span></span>

### <span data-ttu-id="18401-147">Keine</span><span class="sxs-lookup"><span data-stu-id="18401-147">None</span></span>
<span data-ttu-id="18401-148">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="18401-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="18401-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="18401-149">OUTPUTS</span></span>

### <span data-ttu-id="18401-150">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="18401-150">String</span></span>
<span data-ttu-id="18401-151">Das Cmdlet gibt den Pfad der Ausgabedatei zurück, die die Sicherung des Schlüssels enthält.</span><span class="sxs-lookup"><span data-stu-id="18401-151">The cmdlet returns the path of the output file containing the backup of the key.</span></span>

## <span data-ttu-id="18401-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="18401-152">NOTES</span></span>

## <span data-ttu-id="18401-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="18401-153">RELATED LINKS</span></span>

[<span data-ttu-id="18401-154">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="18401-154">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="18401-155">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="18401-155">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="18401-156">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="18401-156">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="18401-157">Wiederherstellen – AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="18401-157">Restore-AzKeyVaultKey</span></span>](./Restore-AzKeyVaultKey.md)

