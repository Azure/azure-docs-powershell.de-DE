---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/import-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
ms.openlocfilehash: 6a687f67741a8d4925e3253c9f787532501ad186
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175244"
---
# <span data-ttu-id="baf30-101">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="baf30-101">Import-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="baf30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="baf30-102">SYNOPSIS</span></span>
<span data-ttu-id="baf30-103">Importiert ein Zertifikat in einen Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="baf30-103">Imports a certificate to a key vault.</span></span>

## <span data-ttu-id="baf30-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="baf30-104">SYNTAX</span></span>

### <span data-ttu-id="baf30-105">ImportCertificateFromFile (Standard)</span><span class="sxs-lookup"><span data-stu-id="baf30-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="baf30-106">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="baf30-106">ImportWithPrivateKeyFromString</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="baf30-107">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="baf30-107">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificateCollection] <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="baf30-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="baf30-108">DESCRIPTION</span></span>
<span data-ttu-id="baf30-109">Das **Cmdlet "Import-AzKeyVaultCertificate"** importiert ein Zertifikat in einen Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="baf30-109">The **Import-AzKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>
<span data-ttu-id="baf30-110">Sie können das zu importierende Zertifikat mit einer der folgenden Methoden erstellen:</span><span class="sxs-lookup"><span data-stu-id="baf30-110">You can create the certificate to import by using one of the following methods:</span></span>
- <span data-ttu-id="baf30-111">Wird `Add-AzKeyVaultCertificate` verwendet, um eine Zertifikatsignaturanforderung zu erstellen und an eine Zertifizierungsstelle zu senden.</span><span class="sxs-lookup"><span data-stu-id="baf30-111">Use `Add-AzKeyVaultCertificate` to create a certificate signing request and submit it to a certificate authority.</span></span> <span data-ttu-id="baf30-112">Sieh https://docs.microsoft.com/en-us/azure/key-vault/certificates/create-certificate-signing-request</span><span class="sxs-lookup"><span data-stu-id="baf30-112">See https://docs.microsoft.com/en-us/azure/key-vault/certificates/create-certificate-signing-request</span></span>
- <span data-ttu-id="baf30-113">Verwenden Sie eine vorhandene Zertifikatpaketdatei, z. B. eine PFX- oder P12-Datei, die sowohl das Zertifikat als auch den privaten Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="baf30-113">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="baf30-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="baf30-114">EXAMPLES</span></span>

### <span data-ttu-id="baf30-115">Beispiel 1: Importieren eines Schlüsseltresorzertifikats</span><span class="sxs-lookup"><span data-stu-id="baf30-115">Example 1: Import a key vault certificate</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS C:\> Import-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "ImportCert01" -FilePath "C:\Users\contosoUser\Desktop\import.pfx" -Password $Password

Name        : importCert01
Certificate : [Subject]
                CN=contoso.com

              [Issuer]
                CN=contoso.com

              [Serial Number]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before]
                2/8/2016 3:11:45 PM

              [Not After]
                8/8/2016 4:21:45 PM

              [Thumbprint]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        :
Enabled     : True
Created     : 2/8/2016 11:50:43 PM
Updated     : 2/8/2016 11:50:43 PM
```

<span data-ttu-id="baf30-116">Der erste Befehl verwendet das cmdlet ConvertTo-SecureString, um ein sicheres Kennwort zu erstellen, und speichert es dann in $Password Variable.</span><span class="sxs-lookup"><span data-stu-id="baf30-116">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>
<span data-ttu-id="baf30-117">Der zweite Befehl importiert das Zertifikat mit dem Namen "ImportCert01" in den Schlüsseltresor "Cos vaultsoKV01".</span><span class="sxs-lookup"><span data-stu-id="baf30-117">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="baf30-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="baf30-118">PARAMETERS</span></span>

### <span data-ttu-id="baf30-119">-CertificateCollection</span><span class="sxs-lookup"><span data-stu-id="baf30-119">-CertificateCollection</span></span>
<span data-ttu-id="baf30-120">Gibt die Zertifikatsammlung an, die einem Schlüsseltresor hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="baf30-120">Specifies the certificate collection to add to a key vault.</span></span>

```yaml
Type: System.Security.Cryptography.X509Certificates.X509Certificate2Collection
Parameter Sets: ImportWithPrivateKeyFromCollection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="baf30-121">-CertificateString</span><span class="sxs-lookup"><span data-stu-id="baf30-121">-CertificateString</span></span>
<span data-ttu-id="baf30-122">Gibt eine Zertifikatzeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="baf30-122">Specifies a certificate string.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportWithPrivateKeyFromString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baf30-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baf30-123">-DefaultProfile</span></span>
<span data-ttu-id="baf30-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="baf30-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="baf30-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="baf30-125">-FilePath</span></span>
<span data-ttu-id="baf30-126">Gibt den Pfad der Zertifikatdatei an, die von diesem Cmdlet importiert wird.</span><span class="sxs-lookup"><span data-stu-id="baf30-126">Specifies the path of the certificate file that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportCertificateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baf30-127">-Name</span><span class="sxs-lookup"><span data-stu-id="baf30-127">-Name</span></span>
<span data-ttu-id="baf30-128">Gibt den Zertifikatnamen an.</span><span class="sxs-lookup"><span data-stu-id="baf30-128">Specifies the certificate name.</span></span> <span data-ttu-id="baf30-129">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Zertifikats aus dem Schlüsseltresornamen, der aktuell ausgewählten Umgebung und dem Zertifikatnamen.</span><span class="sxs-lookup"><span data-stu-id="baf30-129">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baf30-130">-Password</span><span class="sxs-lookup"><span data-stu-id="baf30-130">-Password</span></span>
<span data-ttu-id="baf30-131">Gibt das Kennwort für eine Zertifikatdatei an.</span><span class="sxs-lookup"><span data-stu-id="baf30-131">Specifies the password for a certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ImportCertificateFromFile, ImportWithPrivateKeyFromString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baf30-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="baf30-132">-Tag</span></span>
<span data-ttu-id="baf30-133">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="baf30-133">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="baf30-134">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="baf30-134">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baf30-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="baf30-135">-VaultName</span></span>
<span data-ttu-id="baf30-136">Gibt den Schlüsseltresornamen an, in den dieses Cmdlet Zertifikate importiert.</span><span class="sxs-lookup"><span data-stu-id="baf30-136">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="baf30-137">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüsseltresor basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="baf30-137">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baf30-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="baf30-138">-Confirm</span></span>
<span data-ttu-id="baf30-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="baf30-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="baf30-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="baf30-140">-WhatIf</span></span>
<span data-ttu-id="baf30-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="baf30-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="baf30-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="baf30-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="baf30-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baf30-143">CommonParameters</span></span>
<span data-ttu-id="baf30-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baf30-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baf30-145">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="baf30-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baf30-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="baf30-146">INPUTS</span></span>

### <span data-ttu-id="baf30-147">System.String</span><span class="sxs-lookup"><span data-stu-id="baf30-147">System.String</span></span>

### <span data-ttu-id="baf30-148">System.Security.Cryptography.X509Certificates.X509Certificate2Collection</span><span class="sxs-lookup"><span data-stu-id="baf30-148">System.Security.Cryptography.X509Certificates.X509Certificate2Collection</span></span>

### <span data-ttu-id="baf30-149">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="baf30-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="baf30-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="baf30-150">OUTPUTS</span></span>

### <span data-ttu-id="baf30-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="baf30-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="baf30-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="baf30-152">NOTES</span></span>

## <span data-ttu-id="baf30-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="baf30-153">RELATED LINKS</span></span>

[<span data-ttu-id="baf30-154">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="baf30-154">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="baf30-155">Erstellen und Zusammenführen von CSR im Schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="baf30-155">Creating and merging CSR in Key Vault</span></span>](https://docs.microsoft.com/en-us/azure/key-vault/certificates/create-certificate-signing-request)