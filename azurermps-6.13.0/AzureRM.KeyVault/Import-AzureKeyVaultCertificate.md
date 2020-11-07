---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/import-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Import-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Import-AzureKeyVaultCertificate.md
ms.openlocfilehash: 5cc7846ae1d5eba5764c524e4edfb470a7cd562b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664048"
---
# <span data-ttu-id="112dd-101">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="112dd-101">Import-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="112dd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="112dd-102">SYNOPSIS</span></span>
<span data-ttu-id="112dd-103">Importiert ein Zertifikat in einen schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="112dd-103">Imports a certificate to a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="112dd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="112dd-104">SYNTAX</span></span>

### <span data-ttu-id="112dd-105">ImportCertificateFromFile (Standard)</span><span class="sxs-lookup"><span data-stu-id="112dd-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="112dd-106">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="112dd-106">ImportWithPrivateKeyFromString</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="112dd-107">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="112dd-107">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificateCollection] <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="112dd-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="112dd-108">DESCRIPTION</span></span>
<span data-ttu-id="112dd-109">Mit dem Cmdlet " **Import-AzureKeyVaultCertificate** " wird ein Zertifikat in einen schlüsseltresor importiert.</span><span class="sxs-lookup"><span data-stu-id="112dd-109">The **Import-AzureKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>
<span data-ttu-id="112dd-110">Sie können das zu importierende Zertifikat mithilfe einer der folgenden Methoden erstellen:</span><span class="sxs-lookup"><span data-stu-id="112dd-110">You can create the certificate to import by using one of the following methods:</span></span>
- <span data-ttu-id="112dd-111">Verwenden Sie das New-AzureKeyVaultCertificateSigningRequest-Cmdlet, um eine Zertifikatsignaturanforderung zu erstellen und an eine Zertifizierungsstelle zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="112dd-111">Use the New-AzureKeyVaultCertificateSigningRequest cmdlet to create a certificate signing request and submit it to a certificate authority.</span></span>
- <span data-ttu-id="112dd-112">Verwenden Sie eine vorhandene Zertifikatspaket Datei, beispielsweise eine PFX-oder P12-Datei, die sowohl das Zertifikat als auch den privaten Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="112dd-112">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="112dd-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="112dd-113">EXAMPLES</span></span>

### <span data-ttu-id="112dd-114">Beispiel 1: Importieren eines schlüsseltresor-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="112dd-114">Example 1: Import a key vault certificate</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS C:\> Import-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "ImportCert01" -FilePath "C:\Users\contosoUser\Desktop\import.pfx" -Password $Password

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

<span data-ttu-id="112dd-115">Der erste Befehl verwendet das ConvertTo-SecureString-Cmdlet, um ein sicheres Kennwort zu erstellen, und speichert es dann in der $Password-Variablen.</span><span class="sxs-lookup"><span data-stu-id="112dd-115">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>
<span data-ttu-id="112dd-116">Mit dem zweiten Befehl wird das Zertifikat mit dem Namen ImportCert01 in den CosotosoKV01-schlüsseltresor importiert.</span><span class="sxs-lookup"><span data-stu-id="112dd-116">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="112dd-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="112dd-117">PARAMETERS</span></span>

### <span data-ttu-id="112dd-118">-Certificatecollection</span><span class="sxs-lookup"><span data-stu-id="112dd-118">-CertificateCollection</span></span>
<span data-ttu-id="112dd-119">Gibt die Zertifikat Sammlung an, die einem schlüsseltresor hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="112dd-119">Specifies the certificate collection to add to a key vault.</span></span>

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

### <span data-ttu-id="112dd-120">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="112dd-120">-CertificateString</span></span>
<span data-ttu-id="112dd-121">Gibt eine Zertifikatzeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="112dd-121">Specifies a certificate string.</span></span>

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

### <span data-ttu-id="112dd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="112dd-122">-DefaultProfile</span></span>
<span data-ttu-id="112dd-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="112dd-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="112dd-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="112dd-124">-FilePath</span></span>
<span data-ttu-id="112dd-125">Gibt den Pfad der Zertifikatsdatei an, die dieses Cmdlet importiert.</span><span class="sxs-lookup"><span data-stu-id="112dd-125">Specifies the path of the certificate file that this cmdlet imports.</span></span>

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

### <span data-ttu-id="112dd-126">-Name</span><span class="sxs-lookup"><span data-stu-id="112dd-126">-Name</span></span>
<span data-ttu-id="112dd-127">Gibt den Zertifikatsnamen an.</span><span class="sxs-lookup"><span data-stu-id="112dd-127">Specifies the certificate name.</span></span> <span data-ttu-id="112dd-128">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Zertifikats aus dem schlüsseltresor Namen, der aktuell ausgewählten Umgebung und dem Zertifikatnamen.</span><span class="sxs-lookup"><span data-stu-id="112dd-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

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

### <span data-ttu-id="112dd-129">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="112dd-129">-Password</span></span>
<span data-ttu-id="112dd-130">Gibt das Kennwort für eine Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="112dd-130">Specifies the password for a certificate file.</span></span>

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

### <span data-ttu-id="112dd-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="112dd-131">-Tag</span></span>
<span data-ttu-id="112dd-132">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="112dd-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="112dd-133">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="112dd-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="112dd-134">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="112dd-134">-VaultName</span></span>
<span data-ttu-id="112dd-135">Gibt den Namen des Schlüssel Tresors an, in den dieses Cmdlet Zertifikate importiert.</span><span class="sxs-lookup"><span data-stu-id="112dd-135">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="112dd-136">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüsseldepots basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="112dd-136">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="112dd-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="112dd-137">-Confirm</span></span>
<span data-ttu-id="112dd-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="112dd-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="112dd-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="112dd-139">-WhatIf</span></span>
<span data-ttu-id="112dd-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="112dd-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="112dd-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="112dd-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="112dd-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="112dd-142">CommonParameters</span></span>
<span data-ttu-id="112dd-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="112dd-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="112dd-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="112dd-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="112dd-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="112dd-145">INPUTS</span></span>

### <span data-ttu-id="112dd-146">System. String</span><span class="sxs-lookup"><span data-stu-id="112dd-146">System.String</span></span>

### <span data-ttu-id="112dd-147">System. Security. Cryptography. X509Certificates. X509Certificate2Collection</span><span class="sxs-lookup"><span data-stu-id="112dd-147">System.Security.Cryptography.X509Certificates.X509Certificate2Collection</span></span>
<span data-ttu-id="112dd-148">Parameter: certificatecollection (ByValue)</span><span class="sxs-lookup"><span data-stu-id="112dd-148">Parameters: CertificateCollection (ByValue)</span></span>

### <span data-ttu-id="112dd-149">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="112dd-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="112dd-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="112dd-150">OUTPUTS</span></span>

### <span data-ttu-id="112dd-151">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="112dd-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="112dd-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="112dd-152">NOTES</span></span>

## <span data-ttu-id="112dd-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="112dd-153">RELATED LINKS</span></span>

[<span data-ttu-id="112dd-154">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="112dd-154">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)
