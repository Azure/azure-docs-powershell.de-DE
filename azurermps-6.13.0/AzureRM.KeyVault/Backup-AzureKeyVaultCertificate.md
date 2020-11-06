---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultCertificate.md
ms.openlocfilehash: 7f75f07ee8f53a57cdb2e359fb4addb51b1d7f76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479589"
---
# <span data-ttu-id="fa129-101">Backup-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="fa129-101">Backup-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="fa129-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fa129-102">SYNOPSIS</span></span>
<span data-ttu-id="fa129-103">Sichern eines Zertifikats in einem schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="fa129-103">Backs up a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa129-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa129-104">SYNTAX</span></span>

### <span data-ttu-id="fa129-105">ByCertificateName (Standard)</span><span class="sxs-lookup"><span data-stu-id="fa129-105">ByCertificateName (Default)</span></span>
```
Backup-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa129-106">ByCertificate</span><span class="sxs-lookup"><span data-stu-id="fa129-106">ByCertificate</span></span>
```
Backup-AzureKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa129-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa129-107">DESCRIPTION</span></span>
<span data-ttu-id="fa129-108">Mit dem Cmdlet " **Backup-AzureKeyVaultCertificate** " wird ein angegebenes Zertifikat in einem schlüsseltresor gesichert, indem es heruntergeladen und in einer Datei gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="fa129-108">The **Backup-AzureKeyVaultCertificate** cmdlet backs up a specified certificate in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="fa129-109">Wenn das Zertifikat mehrere Versionen enthält, werden alle zugehörigen Versionen in die Sicherung aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="fa129-109">If the certificate has multiple versions, all its versions will be included in the backup.</span></span>
<span data-ttu-id="fa129-110">Da der heruntergeladene Inhalt verschlüsselt ist, kann er nicht außerhalb des Azure Key Vault verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fa129-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="fa129-111">Sie können ein gesichertes Zertifikat in einem beliebigen schlüsseltresor des Abonnements wiederherstellen, von dem es gesichert wurde, sofern sich der Tresor im gleichen Azure-geografischen Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="fa129-111">You can restore a backed-up certificate to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="fa129-112">Typische Gründe für die Verwendung dieses Cmdlets sind:</span><span class="sxs-lookup"><span data-stu-id="fa129-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="fa129-113">Sie möchten eine Offlinekopie des Zertifikats behalten, falls Sie das Original versehentlich aus dem Tresor löschen.</span><span class="sxs-lookup"><span data-stu-id="fa129-113">You want to retain an offline copy of the certificate in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="fa129-114">Sie haben ein Zertifikat mithilfe von Key Vault erstellt und möchten das Objekt nun in einen anderen Azure-Bereich Klonen, sodass Sie es in allen Instanzen ihrer verteilten Anwendung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="fa129-114">You created a certificate using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="fa129-115">Verwenden Sie das Cmdlet **Backup-AzureKeyVaultCertificate** , um das Zertifikat im verschlüsselten Format abzurufen, und verwenden Sie dann das Cmdlet **Restore-AzureKeyVaultCertificate** , und geben Sie einen schlüsseltresor in der zweiten Region an.</span><span class="sxs-lookup"><span data-stu-id="fa129-115">Use the **Backup-AzureKeyVaultCertificate** cmdlet to retrieve the certificate in encrypted format and then use the **Restore-AzureKeyVaultCertificate** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="fa129-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fa129-116">EXAMPLES</span></span>

### <span data-ttu-id="fa129-117">Beispiel 1: Sichern eines Zertifikats mit einem automatisch generierten Dateinamen</span><span class="sxs-lookup"><span data-stu-id="fa129-117">Example 1: Back up a certificate with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzureKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

<span data-ttu-id="fa129-118">Dieser Befehl ruft das Zertifikat mit dem Namen MyCert aus dem schlüsseltresor mit dem Namen MyKeyVault ab und speichert eine Sicherungskopie dieses Zertifikats in einer Datei, die automatisch nach ihnen benannt wird, und zeigt den Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="fa129-118">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="fa129-119">Beispiel 2: Sichern eines Zertifikats unter einem angegebenen Dateinamen</span><span class="sxs-lookup"><span data-stu-id="fa129-119">Example 2: Back up a certificate to a specified file name</span></span>
```powershell
PS C:\> Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="fa129-120">Dieser Befehl ruft das Zertifikat mit dem Namen MyCert aus dem schlüsseltresor mit dem Namen MyKeyVault ab und speichert eine Sicherungskopie dieses Zertifikats in einer Datei mit dem Namen Backup. BLOB.</span><span class="sxs-lookup"><span data-stu-id="fa129-120">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file named Backup.blob.</span></span>

### <span data-ttu-id="fa129-121">Beispiel 3: Sichern Sie ein zuvor abgerufenes Zertifikat unter einem angegebenen Dateinamen, und überschreiben Sie die Zieldatei ohne Aufforderung.</span><span class="sxs-lookup"><span data-stu-id="fa129-121">Example 3: Back up a previously retrieved certificate to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $cert = Get-AzureKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzureKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="fa129-122">Mit diesem Befehl wird eine Sicherungskopie des Zertifikats mit dem Namen $CERT erstellt. Name im Tresor mit dem Namen $cert. Vaultname in eine Datei mit dem Namen "Backup. BLOB", wobei die Datei im Hintergrund überschrieben wird, wenn Sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="fa129-122">This command creates a backup of the certificate named $cert.Name in the vault named $cert.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="fa129-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa129-123">PARAMETERS</span></span>

### <span data-ttu-id="fa129-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa129-124">-DefaultProfile</span></span>
<span data-ttu-id="fa129-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fa129-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa129-126">-Force</span><span class="sxs-lookup"><span data-stu-id="fa129-126">-Force</span></span>
<span data-ttu-id="fa129-127">Überschreiben der angegebenen Datei, sofern vorhanden</span><span class="sxs-lookup"><span data-stu-id="fa129-127">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="fa129-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fa129-128">-InputObject</span></span>
<span data-ttu-id="fa129-129">Secret, die gesichert werden soll, in der Ausgabe eines Abruf Anrufs.</span><span class="sxs-lookup"><span data-stu-id="fa129-129">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByCertificate
Aliases: Certificate

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa129-130">-Name</span><span class="sxs-lookup"><span data-stu-id="fa129-130">-Name</span></span>
<span data-ttu-id="fa129-131">Geheimer Name.</span><span class="sxs-lookup"><span data-stu-id="fa129-131">Secret name.</span></span>
<span data-ttu-id="fa129-132">Cmdlet erstellt den FQDN eines geheimen Schlüssels aus Vault-Name, aktuell ausgewählter Umgebung und geheimem Namen.</span><span class="sxs-lookup"><span data-stu-id="fa129-132">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa129-133">-Outputdatei</span><span class="sxs-lookup"><span data-stu-id="fa129-133">-OutputFile</span></span>
<span data-ttu-id="fa129-134">Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="fa129-134">Output file.</span></span>
<span data-ttu-id="fa129-135">Die Ausgabedatei zum Speichern der Sicherung des Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="fa129-135">The output file to store the backup of the certificate.</span></span>
<span data-ttu-id="fa129-136">Wenn keine Angabe erfolgt, wird ein Standarddateiname generiert.</span><span class="sxs-lookup"><span data-stu-id="fa129-136">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="fa129-137">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="fa129-137">-VaultName</span></span>
<span data-ttu-id="fa129-138">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="fa129-138">Vault name.</span></span>
<span data-ttu-id="fa129-139">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="fa129-139">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa129-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fa129-140">-Confirm</span></span>
<span data-ttu-id="fa129-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fa129-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa129-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa129-142">-WhatIf</span></span>
<span data-ttu-id="fa129-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fa129-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa129-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fa129-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa129-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa129-145">CommonParameters</span></span>
<span data-ttu-id="fa129-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa129-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa129-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa129-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa129-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fa129-148">INPUTS</span></span>

### <span data-ttu-id="fa129-149">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="fa129-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>
<span data-ttu-id="fa129-150">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fa129-150">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="fa129-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fa129-151">OUTPUTS</span></span>

### <span data-ttu-id="fa129-152">System. String</span><span class="sxs-lookup"><span data-stu-id="fa129-152">System.String</span></span>

## <span data-ttu-id="fa129-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="fa129-153">NOTES</span></span>

## <span data-ttu-id="fa129-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fa129-154">RELATED LINKS</span></span>
