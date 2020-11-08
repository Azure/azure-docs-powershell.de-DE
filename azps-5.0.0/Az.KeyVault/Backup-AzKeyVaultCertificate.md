---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
ms.openlocfilehash: 51d322ea738a56e4b1fa24cccdb7bb59a6cd0d21
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180437"
---
# <span data-ttu-id="d33ea-101">Backup-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d33ea-101">Backup-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="d33ea-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d33ea-102">SYNOPSIS</span></span>
<span data-ttu-id="d33ea-103">Sichern eines Zertifikats in einem schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="d33ea-103">Backs up a certificate in a key vault.</span></span>

## <span data-ttu-id="d33ea-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d33ea-104">SYNTAX</span></span>

### <span data-ttu-id="d33ea-105">ByCertificateName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d33ea-105">ByCertificateName (Default)</span></span>
```
Backup-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d33ea-106">ByCertificate</span><span class="sxs-lookup"><span data-stu-id="d33ea-106">ByCertificate</span></span>
```
Backup-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d33ea-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d33ea-107">DESCRIPTION</span></span>
<span data-ttu-id="d33ea-108">Mit dem Cmdlet " **Backup-AzKeyVaultCertificate** " wird ein angegebenes Zertifikat in einem schlüsseltresor gesichert, indem es heruntergeladen und in einer Datei gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="d33ea-108">The **Backup-AzKeyVaultCertificate** cmdlet backs up a specified certificate in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="d33ea-109">Wenn das Zertifikat mehrere Versionen enthält, werden alle zugehörigen Versionen in die Sicherung aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="d33ea-109">If the certificate has multiple versions, all its versions will be included in the backup.</span></span>
<span data-ttu-id="d33ea-110">Da der heruntergeladene Inhalt verschlüsselt ist, kann er nicht außerhalb des Azure Key Vault verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d33ea-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="d33ea-111">Sie können ein gesichertes Zertifikat in einem beliebigen schlüsseltresor des Abonnements wiederherstellen, von dem es gesichert wurde, sofern sich der Tresor im gleichen Azure-geografischen Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="d33ea-111">You can restore a backed-up certificate to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="d33ea-112">Typische Gründe für die Verwendung dieses Cmdlets sind:</span><span class="sxs-lookup"><span data-stu-id="d33ea-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="d33ea-113">Sie möchten eine Offlinekopie des Zertifikats behalten, falls Sie das Original versehentlich aus dem Tresor löschen.</span><span class="sxs-lookup"><span data-stu-id="d33ea-113">You want to retain an offline copy of the certificate in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="d33ea-114">Sie haben ein Zertifikat mithilfe von Key Vault erstellt und möchten das Objekt nun in einen anderen Azure-Bereich Klonen, sodass Sie es in allen Instanzen ihrer verteilten Anwendung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="d33ea-114">You created a certificate using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="d33ea-115">Verwenden Sie das Cmdlet **Backup-AzKeyVaultCertificate** , um das Zertifikat im verschlüsselten Format abzurufen, und verwenden Sie dann das Cmdlet **Restore-AzKeyVaultCertificate** , und geben Sie einen schlüsseltresor in der zweiten Region an.</span><span class="sxs-lookup"><span data-stu-id="d33ea-115">Use the **Backup-AzKeyVaultCertificate** cmdlet to retrieve the certificate in encrypted format and then use the **Restore-AzKeyVaultCertificate** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="d33ea-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d33ea-116">EXAMPLES</span></span>

### <span data-ttu-id="d33ea-117">Beispiel 1: Sichern eines Zertifikats mit einem automatisch generierten Dateinamen</span><span class="sxs-lookup"><span data-stu-id="d33ea-117">Example 1: Back up a certificate with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

<span data-ttu-id="d33ea-118">Dieser Befehl ruft das Zertifikat mit dem Namen MyCert aus dem schlüsseltresor mit dem Namen MyKeyVault ab und speichert eine Sicherungskopie dieses Zertifikats in einer Datei, die automatisch nach ihnen benannt wird, und zeigt den Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="d33ea-118">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="d33ea-119">Beispiel 2: Sichern eines Zertifikats unter einem angegebenen Dateinamen</span><span class="sxs-lookup"><span data-stu-id="d33ea-119">Example 2: Back up a certificate to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="d33ea-120">Dieser Befehl ruft das Zertifikat mit dem Namen MyCert aus dem schlüsseltresor mit dem Namen MyKeyVault ab und speichert eine Sicherungskopie dieses Zertifikats in einer Datei mit dem Namen Backup. BLOB.</span><span class="sxs-lookup"><span data-stu-id="d33ea-120">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file named Backup.blob.</span></span>

### <span data-ttu-id="d33ea-121">Beispiel 3: Sichern Sie ein zuvor abgerufenes Zertifikat unter einem angegebenen Dateinamen, und überschreiben Sie die Zieldatei ohne Aufforderung.</span><span class="sxs-lookup"><span data-stu-id="d33ea-121">Example 3: Back up a previously retrieved certificate to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $cert = Get-AzKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="d33ea-122">Mit diesem Befehl wird eine Sicherungskopie des Zertifikats mit dem Namen $CERT erstellt. Name im Tresor mit dem Namen $cert. Vaultname in eine Datei mit dem Namen "Backup. BLOB", wobei die Datei im Hintergrund überschrieben wird, wenn Sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d33ea-122">This command creates a backup of the certificate named $cert.Name in the vault named $cert.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="d33ea-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="d33ea-123">PARAMETERS</span></span>

### <span data-ttu-id="d33ea-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d33ea-124">-DefaultProfile</span></span>
<span data-ttu-id="d33ea-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d33ea-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d33ea-126">-Force</span><span class="sxs-lookup"><span data-stu-id="d33ea-126">-Force</span></span>
<span data-ttu-id="d33ea-127">Überschreiben der angegebenen Datei, sofern vorhanden</span><span class="sxs-lookup"><span data-stu-id="d33ea-127">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="d33ea-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d33ea-128">-InputObject</span></span>
<span data-ttu-id="d33ea-129">Secret, die gesichert werden soll, in der Ausgabe eines Abruf Anrufs.</span><span class="sxs-lookup"><span data-stu-id="d33ea-129">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="d33ea-130">-Name</span><span class="sxs-lookup"><span data-stu-id="d33ea-130">-Name</span></span>
<span data-ttu-id="d33ea-131">Geheimer Name.</span><span class="sxs-lookup"><span data-stu-id="d33ea-131">Secret name.</span></span>
<span data-ttu-id="d33ea-132">Cmdlet erstellt den FQDN eines geheimen Schlüssels aus Vault-Name, aktuell ausgewählter Umgebung und geheimem Namen.</span><span class="sxs-lookup"><span data-stu-id="d33ea-132">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="d33ea-133">-Outputdatei</span><span class="sxs-lookup"><span data-stu-id="d33ea-133">-OutputFile</span></span>
<span data-ttu-id="d33ea-134">Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="d33ea-134">Output file.</span></span>
<span data-ttu-id="d33ea-135">Die Ausgabedatei zum Speichern der Sicherung des Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="d33ea-135">The output file to store the backup of the certificate.</span></span>
<span data-ttu-id="d33ea-136">Wenn keine Angabe erfolgt, wird ein Standarddateiname generiert.</span><span class="sxs-lookup"><span data-stu-id="d33ea-136">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="d33ea-137">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="d33ea-137">-VaultName</span></span>
<span data-ttu-id="d33ea-138">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="d33ea-138">Vault name.</span></span>
<span data-ttu-id="d33ea-139">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="d33ea-139">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="d33ea-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d33ea-140">-Confirm</span></span>
<span data-ttu-id="d33ea-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d33ea-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d33ea-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d33ea-142">-WhatIf</span></span>
<span data-ttu-id="d33ea-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d33ea-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d33ea-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d33ea-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d33ea-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d33ea-145">CommonParameters</span></span>
<span data-ttu-id="d33ea-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d33ea-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d33ea-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d33ea-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d33ea-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d33ea-148">INPUTS</span></span>

### <span data-ttu-id="d33ea-149">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d33ea-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="d33ea-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d33ea-150">OUTPUTS</span></span>

### <span data-ttu-id="d33ea-151">System. String</span><span class="sxs-lookup"><span data-stu-id="d33ea-151">System.String</span></span>

## <span data-ttu-id="d33ea-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="d33ea-152">NOTES</span></span>

## <span data-ttu-id="d33ea-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d33ea-153">RELATED LINKS</span></span>
