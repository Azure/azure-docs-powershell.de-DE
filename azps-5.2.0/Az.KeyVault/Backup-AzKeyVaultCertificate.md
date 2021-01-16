---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
ms.openlocfilehash: 51d322ea738a56e4b1fa24cccdb7bb59a6cd0d21
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305219"
---
# <span data-ttu-id="9fe8e-101">Backup-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="9fe8e-101">Backup-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="9fe8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fe8e-102">SYNOPSIS</span></span>
<span data-ttu-id="9fe8e-103">Sichern eines Zertifikats in einem Schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="9fe8e-103">Backs up a certificate in a key vault.</span></span>

## <span data-ttu-id="9fe8e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9fe8e-104">SYNTAX</span></span>

### <span data-ttu-id="9fe8e-105">ByCertificateName (Standard)</span><span class="sxs-lookup"><span data-stu-id="9fe8e-105">ByCertificateName (Default)</span></span>
```
Backup-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fe8e-106">ByCertificate</span><span class="sxs-lookup"><span data-stu-id="9fe8e-106">ByCertificate</span></span>
```
Backup-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fe8e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9fe8e-107">DESCRIPTION</span></span>
<span data-ttu-id="9fe8e-108">Das **Cmdlet "Backup-AzKeyVaultCertificate"** sichern ein angegebenes Zertifikat in einem Schlüsseltresor, indem es heruntergeladen und in einer Datei gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-108">The **Backup-AzKeyVaultCertificate** cmdlet backs up a specified certificate in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="9fe8e-109">Wenn das Zertifikat über mehrere Versionen verfügt, werden alle diese Versionen in die Sicherung eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-109">If the certificate has multiple versions, all its versions will be included in the backup.</span></span>
<span data-ttu-id="9fe8e-110">Da die heruntergeladenen Inhalte verschlüsselt sind, können sie nicht außerhalb des Azure Key Vault verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="9fe8e-111">Sie können ein gesichertes Zertifikat in einem beliebigen Schlüsseltresor im Abonnement wiederherstellen, von dem es gesichert wurde, solange sich der Tresor in derselben Azure-Geografie befindet.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-111">You can restore a backed-up certificate to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="9fe8e-112">Typische Gründe für die Verwendung dieses Cmdlets sind:</span><span class="sxs-lookup"><span data-stu-id="9fe8e-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="9fe8e-113">Sie möchten eine Offlinekopie des Zertifikats für den Fall beibehalten, dass Sie das Original versehentlich aus dem Tresor löschen.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-113">You want to retain an offline copy of the certificate in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="9fe8e-114">Sie haben ein Zertifikat mithilfe des Schlüsseltresor erstellt und möchten nun das Objekt in eine andere Azure-Region klonen, damit Sie es in allen Instanzen Der verteilten Anwendung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-114">You created a certificate using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="9fe8e-115">Verwenden Sie das **Cmdlet "Backup-AzKeyVaultCertificate",** um das Zertifikat im verschlüsselten Format abzurufen, verwenden Sie dann das Cmdlet **"Restore-AzKeyVaultCertificate",** und geben Sie einen Schlüsseltresor in der zweiten Region an.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-115">Use the **Backup-AzKeyVaultCertificate** cmdlet to retrieve the certificate in encrypted format and then use the **Restore-AzKeyVaultCertificate** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="9fe8e-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9fe8e-116">EXAMPLES</span></span>

### <span data-ttu-id="9fe8e-117">Beispiel 1: Sichern eines Zertifikats mit einem automatisch generierten Dateinamen</span><span class="sxs-lookup"><span data-stu-id="9fe8e-117">Example 1: Back up a certificate with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

<span data-ttu-id="9fe8e-118">Dieser Befehl ruft das Zertifikat namens "MyCert" aus dem Schlüsseltresor "MyKeyVault" ab, speichert eine Sicherung dieses Zertifikats in einer Datei, die automatisch nach Ihnen benannt wird, und zeigt den Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-118">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="9fe8e-119">Beispiel 2: Sichern eines Zertifikats unter einem angegebenen Dateinamen</span><span class="sxs-lookup"><span data-stu-id="9fe8e-119">Example 2: Back up a certificate to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="9fe8e-120">Mit diesem Befehl wird das Zertifikat namens "MyCert" aus dem Schlüsseltresor "MyKeyVault" abgerufen und eine Sicherung des Zertifikats in einer Datei namens "Backup.blob" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-120">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file named Backup.blob.</span></span>

### <span data-ttu-id="9fe8e-121">Beispiel 3: Sichern Sie ein zuvor abgerufenes Zertifikat unter einem angegebenen Dateinamen, und überschreiben Sie die Zieldatei ohne Eingabeaufforderung.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-121">Example 3: Back up a previously retrieved certificate to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $cert = Get-AzKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="9fe8e-122">Mit diesem Befehl wird eine Sicherung des Zertifikats namens "$cert. Name im Tresor namens $cert. VaultName in eine Datei mit dem Namen "Backup.blob", und überschreiben die Datei, sofern sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-122">This command creates a backup of the certificate named $cert.Name in the vault named $cert.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="9fe8e-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9fe8e-123">PARAMETERS</span></span>

### <span data-ttu-id="9fe8e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fe8e-124">-DefaultProfile</span></span>
<span data-ttu-id="9fe8e-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fe8e-126">-Force</span><span class="sxs-lookup"><span data-stu-id="9fe8e-126">-Force</span></span>
<span data-ttu-id="9fe8e-127">Überschreiben der vorhandenen Datei</span><span class="sxs-lookup"><span data-stu-id="9fe8e-127">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="9fe8e-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9fe8e-128">-InputObject</span></span>
<span data-ttu-id="9fe8e-129">Das Geheime, das gesichert werden soll, wird aus der Ausgabe eines Abrufanrufs pipelineiert.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-129">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="9fe8e-130">-Name</span><span class="sxs-lookup"><span data-stu-id="9fe8e-130">-Name</span></span>
<span data-ttu-id="9fe8e-131">Geheimer Name.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-131">Secret name.</span></span>
<span data-ttu-id="9fe8e-132">Das Cmdlet erstellt den FQDN eines Geheimen aus dem Namen des Tresors, die aktuell ausgewählte Umgebung und den geheimen Namen.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-132">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="9fe8e-133">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="9fe8e-133">-OutputFile</span></span>
<span data-ttu-id="9fe8e-134">Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-134">Output file.</span></span>
<span data-ttu-id="9fe8e-135">Die Ausgabedatei zum Speichern der Sicherung des Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-135">The output file to store the backup of the certificate.</span></span>
<span data-ttu-id="9fe8e-136">Ohne Angabe wird ein Standarddateiname generiert.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-136">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="9fe8e-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9fe8e-137">-VaultName</span></span>
<span data-ttu-id="9fe8e-138">Name des Tresors.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-138">Vault name.</span></span>
<span data-ttu-id="9fe8e-139">Das Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-139">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="9fe8e-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9fe8e-140">-Confirm</span></span>
<span data-ttu-id="9fe8e-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fe8e-142">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-142">-WhatIf</span></span>
<span data-ttu-id="9fe8e-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fe8e-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fe8e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fe8e-145">CommonParameters</span></span>
<span data-ttu-id="9fe8e-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fe8e-147">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9fe8e-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fe8e-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9fe8e-148">INPUTS</span></span>

### <span data-ttu-id="9fe8e-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="9fe8e-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="9fe8e-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9fe8e-150">OUTPUTS</span></span>

### <span data-ttu-id="9fe8e-151">System.String</span><span class="sxs-lookup"><span data-stu-id="9fe8e-151">System.String</span></span>

## <span data-ttu-id="9fe8e-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9fe8e-152">NOTES</span></span>

## <span data-ttu-id="9fe8e-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9fe8e-153">RELATED LINKS</span></span>
