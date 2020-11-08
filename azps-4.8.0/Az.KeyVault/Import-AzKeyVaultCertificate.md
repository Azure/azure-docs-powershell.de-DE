---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/import-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
ms.openlocfilehash: 6a687f67741a8d4925e3253c9f787532501ad186
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009800"
---
# <span data-ttu-id="948a6-101">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="948a6-101">Import-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="948a6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="948a6-102">SYNOPSIS</span></span>
<span data-ttu-id="948a6-103">Importiert ein Zertifikat in einen schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="948a6-103">Imports a certificate to a key vault.</span></span>

## <span data-ttu-id="948a6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="948a6-104">SYNTAX</span></span>

### <span data-ttu-id="948a6-105">ImportCertificateFromFile (Standard)</span><span class="sxs-lookup"><span data-stu-id="948a6-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="948a6-106">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="948a6-106">ImportWithPrivateKeyFromString</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="948a6-107">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="948a6-107">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificateCollection] <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="948a6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="948a6-108">DESCRIPTION</span></span>
<span data-ttu-id="948a6-109">Mit dem Cmdlet " **Import-AzKeyVaultCertificate** " wird ein Zertifikat in einen schlüsseltresor importiert.</span><span class="sxs-lookup"><span data-stu-id="948a6-109">The **Import-AzKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>
<span data-ttu-id="948a6-110">Sie können das zu importierende Zertifikat mithilfe einer der folgenden Methoden erstellen:</span><span class="sxs-lookup"><span data-stu-id="948a6-110">You can create the certificate to import by using one of the following methods:</span></span>
- <span data-ttu-id="948a6-111">Hiermit können Sie `Add-AzKeyVaultCertificate` eine Zertifikatsignaturanforderung erstellen und an eine Zertifizierungsstelle übermitteln.</span><span class="sxs-lookup"><span data-stu-id="948a6-111">Use `Add-AzKeyVaultCertificate` to create a certificate signing request and submit it to a certificate authority.</span></span> <span data-ttu-id="948a6-112">Sieh https://docs.microsoft.com/en-us/azure/key-vault/certificates/create-certificate-signing-request</span><span class="sxs-lookup"><span data-stu-id="948a6-112">See https://docs.microsoft.com/en-us/azure/key-vault/certificates/create-certificate-signing-request</span></span>
- <span data-ttu-id="948a6-113">Verwenden Sie eine vorhandene Zertifikatspaket Datei, beispielsweise eine PFX-oder P12-Datei, die sowohl das Zertifikat als auch den privaten Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="948a6-113">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="948a6-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="948a6-114">EXAMPLES</span></span>

### <span data-ttu-id="948a6-115">Beispiel 1: Importieren eines schlüsseltresor-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="948a6-115">Example 1: Import a key vault certificate</span></span>
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

<span data-ttu-id="948a6-116">Der erste Befehl verwendet das ConvertTo-SecureString-Cmdlet, um ein sicheres Kennwort zu erstellen, und speichert es dann in der $Password-Variablen.</span><span class="sxs-lookup"><span data-stu-id="948a6-116">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>
<span data-ttu-id="948a6-117">Mit dem zweiten Befehl wird das Zertifikat mit dem Namen ImportCert01 in den CosotosoKV01-schlüsseltresor importiert.</span><span class="sxs-lookup"><span data-stu-id="948a6-117">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="948a6-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="948a6-118">PARAMETERS</span></span>

### <span data-ttu-id="948a6-119">-Certificatecollection</span><span class="sxs-lookup"><span data-stu-id="948a6-119">-CertificateCollection</span></span>
<span data-ttu-id="948a6-120">Gibt die Zertifikat Sammlung an, die einem schlüsseltresor hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="948a6-120">Specifies the certificate collection to add to a key vault.</span></span>

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

### <span data-ttu-id="948a6-121">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="948a6-121">-CertificateString</span></span>
<span data-ttu-id="948a6-122">Gibt eine Zertifikatzeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="948a6-122">Specifies a certificate string.</span></span>

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

### <span data-ttu-id="948a6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="948a6-123">-DefaultProfile</span></span>
<span data-ttu-id="948a6-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="948a6-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="948a6-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="948a6-125">-FilePath</span></span>
<span data-ttu-id="948a6-126">Gibt den Pfad der Zertifikatsdatei an, die dieses Cmdlet importiert.</span><span class="sxs-lookup"><span data-stu-id="948a6-126">Specifies the path of the certificate file that this cmdlet imports.</span></span>

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

### <span data-ttu-id="948a6-127">-Name</span><span class="sxs-lookup"><span data-stu-id="948a6-127">-Name</span></span>
<span data-ttu-id="948a6-128">Gibt den Zertifikatsnamen an.</span><span class="sxs-lookup"><span data-stu-id="948a6-128">Specifies the certificate name.</span></span> <span data-ttu-id="948a6-129">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Zertifikats aus dem schlüsseltresor Namen, der aktuell ausgewählten Umgebung und dem Zertifikatnamen.</span><span class="sxs-lookup"><span data-stu-id="948a6-129">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

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

### <span data-ttu-id="948a6-130">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="948a6-130">-Password</span></span>
<span data-ttu-id="948a6-131">Gibt das Kennwort für eine Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="948a6-131">Specifies the password for a certificate file.</span></span>

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

### <span data-ttu-id="948a6-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="948a6-132">-Tag</span></span>
<span data-ttu-id="948a6-133">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="948a6-133">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="948a6-134">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="948a6-134">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="948a6-135">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="948a6-135">-VaultName</span></span>
<span data-ttu-id="948a6-136">Gibt den Namen des Schlüssel Tresors an, in den dieses Cmdlet Zertifikate importiert.</span><span class="sxs-lookup"><span data-stu-id="948a6-136">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="948a6-137">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüsseldepots basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="948a6-137">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="948a6-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="948a6-138">-Confirm</span></span>
<span data-ttu-id="948a6-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="948a6-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="948a6-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="948a6-140">-WhatIf</span></span>
<span data-ttu-id="948a6-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="948a6-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="948a6-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="948a6-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="948a6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="948a6-143">CommonParameters</span></span>
<span data-ttu-id="948a6-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="948a6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="948a6-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="948a6-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="948a6-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="948a6-146">INPUTS</span></span>

### <span data-ttu-id="948a6-147">System. String</span><span class="sxs-lookup"><span data-stu-id="948a6-147">System.String</span></span>

### <span data-ttu-id="948a6-148">System. Security. Cryptography. X509Certificates. X509Certificate2Collection</span><span class="sxs-lookup"><span data-stu-id="948a6-148">System.Security.Cryptography.X509Certificates.X509Certificate2Collection</span></span>

### <span data-ttu-id="948a6-149">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="948a6-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="948a6-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="948a6-150">OUTPUTS</span></span>

### <span data-ttu-id="948a6-151">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="948a6-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="948a6-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="948a6-152">NOTES</span></span>

## <span data-ttu-id="948a6-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="948a6-153">RELATED LINKS</span></span>

[<span data-ttu-id="948a6-154">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="948a6-154">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="948a6-155">Erstellen und Zusammenführen von CSR in Key Vault</span><span class="sxs-lookup"><span data-stu-id="948a6-155">Creating and merging CSR in Key Vault</span></span>](https://docs.microsoft.com/en-us/azure/key-vault/certificates/create-certificate-signing-request)