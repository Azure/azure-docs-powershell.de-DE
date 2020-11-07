---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/import-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
ms.openlocfilehash: 6591b96257a1c94cd2da9d0bc6f2995dc2034a40
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650889"
---
# <span data-ttu-id="1f252-101">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="1f252-101">Import-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="1f252-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1f252-102">SYNOPSIS</span></span>
<span data-ttu-id="1f252-103">Importiert ein Zertifikat in einen schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="1f252-103">Imports a certificate to a key vault.</span></span>

## <span data-ttu-id="1f252-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f252-104">SYNTAX</span></span>

### <span data-ttu-id="1f252-105">ImportCertificateFromFile (Standard)</span><span class="sxs-lookup"><span data-stu-id="1f252-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f252-106">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="1f252-106">ImportWithPrivateKeyFromString</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f252-107">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="1f252-107">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificateCollection] <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f252-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f252-108">DESCRIPTION</span></span>
<span data-ttu-id="1f252-109">Mit dem Cmdlet " **Import-AzKeyVaultCertificate** " wird ein Zertifikat in einen schlüsseltresor importiert.</span><span class="sxs-lookup"><span data-stu-id="1f252-109">The **Import-AzKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>
<span data-ttu-id="1f252-110">Sie können das zu importierende Zertifikat mithilfe einer der folgenden Methoden erstellen:</span><span class="sxs-lookup"><span data-stu-id="1f252-110">You can create the certificate to import by using one of the following methods:</span></span>
- <span data-ttu-id="1f252-111">Verwenden Sie das New-AzKeyVaultCertificateSigningRequest-Cmdlet, um eine Zertifikatsignaturanforderung zu erstellen und an eine Zertifizierungsstelle zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="1f252-111">Use the New-AzKeyVaultCertificateSigningRequest cmdlet to create a certificate signing request and submit it to a certificate authority.</span></span>
- <span data-ttu-id="1f252-112">Verwenden Sie eine vorhandene Zertifikatspaket Datei, beispielsweise eine PFX-oder P12-Datei, die sowohl das Zertifikat als auch den privaten Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="1f252-112">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="1f252-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1f252-113">EXAMPLES</span></span>

### <span data-ttu-id="1f252-114">Beispiel 1: Importieren eines schlüsseltresor-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="1f252-114">Example 1: Import a key vault certificate</span></span>
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

<span data-ttu-id="1f252-115">Der erste Befehl verwendet das ConvertTo-SecureString-Cmdlet, um ein sicheres Kennwort zu erstellen, und speichert es dann in der $Password-Variablen.</span><span class="sxs-lookup"><span data-stu-id="1f252-115">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>
<span data-ttu-id="1f252-116">Mit dem zweiten Befehl wird das Zertifikat mit dem Namen ImportCert01 in den CosotosoKV01-schlüsseltresor importiert.</span><span class="sxs-lookup"><span data-stu-id="1f252-116">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="1f252-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f252-117">PARAMETERS</span></span>

### <span data-ttu-id="1f252-118">-Certificatecollection</span><span class="sxs-lookup"><span data-stu-id="1f252-118">-CertificateCollection</span></span>
<span data-ttu-id="1f252-119">Gibt die Zertifikat Sammlung an, die einem schlüsseltresor hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1f252-119">Specifies the certificate collection to add to a key vault.</span></span>

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

### <span data-ttu-id="1f252-120">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="1f252-120">-CertificateString</span></span>
<span data-ttu-id="1f252-121">Gibt eine Zertifikatzeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="1f252-121">Specifies a certificate string.</span></span>

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

### <span data-ttu-id="1f252-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f252-122">-DefaultProfile</span></span>
<span data-ttu-id="1f252-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1f252-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f252-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="1f252-124">-FilePath</span></span>
<span data-ttu-id="1f252-125">Gibt den Pfad der Zertifikatsdatei an, die dieses Cmdlet importiert.</span><span class="sxs-lookup"><span data-stu-id="1f252-125">Specifies the path of the certificate file that this cmdlet imports.</span></span>

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

### <span data-ttu-id="1f252-126">-Name</span><span class="sxs-lookup"><span data-stu-id="1f252-126">-Name</span></span>
<span data-ttu-id="1f252-127">Gibt den Zertifikatsnamen an.</span><span class="sxs-lookup"><span data-stu-id="1f252-127">Specifies the certificate name.</span></span> <span data-ttu-id="1f252-128">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Zertifikats aus dem schlüsseltresor Namen, der aktuell ausgewählten Umgebung und dem Zertifikatnamen.</span><span class="sxs-lookup"><span data-stu-id="1f252-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

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

### <span data-ttu-id="1f252-129">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="1f252-129">-Password</span></span>
<span data-ttu-id="1f252-130">Gibt das Kennwort für eine Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="1f252-130">Specifies the password for a certificate file.</span></span>

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

### <span data-ttu-id="1f252-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="1f252-131">-Tag</span></span>
<span data-ttu-id="1f252-132">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="1f252-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1f252-133">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="1f252-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1f252-134">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="1f252-134">-VaultName</span></span>
<span data-ttu-id="1f252-135">Gibt den Namen des Schlüssel Tresors an, in den dieses Cmdlet Zertifikate importiert.</span><span class="sxs-lookup"><span data-stu-id="1f252-135">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="1f252-136">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüsseldepots basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="1f252-136">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="1f252-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1f252-137">-Confirm</span></span>
<span data-ttu-id="1f252-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1f252-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f252-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f252-139">-WhatIf</span></span>
<span data-ttu-id="1f252-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1f252-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f252-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1f252-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f252-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f252-142">CommonParameters</span></span>
<span data-ttu-id="1f252-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f252-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f252-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f252-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f252-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1f252-145">INPUTS</span></span>

### <span data-ttu-id="1f252-146">System. String</span><span class="sxs-lookup"><span data-stu-id="1f252-146">System.String</span></span>

### <span data-ttu-id="1f252-147">System. Security. Cryptography. X509Certificates. X509Certificate2Collection</span><span class="sxs-lookup"><span data-stu-id="1f252-147">System.Security.Cryptography.X509Certificates.X509Certificate2Collection</span></span>

### <span data-ttu-id="1f252-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1f252-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1f252-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1f252-149">OUTPUTS</span></span>

### <span data-ttu-id="1f252-150">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="1f252-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="1f252-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="1f252-151">NOTES</span></span>

## <span data-ttu-id="1f252-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1f252-152">RELATED LINKS</span></span>

[<span data-ttu-id="1f252-153">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="1f252-153">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)
