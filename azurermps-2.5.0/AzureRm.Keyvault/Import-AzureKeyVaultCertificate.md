---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/import-azurekeyvaultcertificate
schema: 2.0.0
ms.openlocfilehash: 2903aa294830b8f9a39578374c1c108fe91c36e4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850000"
---
# <span data-ttu-id="d3498-101">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d3498-101">Import-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="d3498-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d3498-102">SYNOPSIS</span></span>
<span data-ttu-id="d3498-103">Importiert ein Zertifikat in einen schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="d3498-103">Imports a certificate to a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3498-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3498-104">SYNTAX</span></span>

### <span data-ttu-id="d3498-105">ImportCertificateFromFile (Standard)</span><span class="sxs-lookup"><span data-stu-id="d3498-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3498-106">ImportWithPrivateKeyFromFile</span><span class="sxs-lookup"><span data-stu-id="d3498-106">ImportWithPrivateKeyFromFile</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d3498-107">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="d3498-107">ImportWithPrivateKeyFromString</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d3498-108">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="d3498-108">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 -CertificateCollection <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3498-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d3498-109">DESCRIPTION</span></span>
<span data-ttu-id="d3498-110">Mit dem Cmdlet " **Import-AzureKeyVaultCertificate** " wird ein Zertifikat in einen schlüsseltresor importiert.</span><span class="sxs-lookup"><span data-stu-id="d3498-110">The **Import-AzureKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>

<span data-ttu-id="d3498-111">Sie können das zu importierende Zertifikat mithilfe einer der folgenden Methoden erstellen:</span><span class="sxs-lookup"><span data-stu-id="d3498-111">You can create the certificate to import by using one of the following methods:</span></span>

- <span data-ttu-id="d3498-112">Verwenden Sie das New-AzureKeyVaultCertificateSigningRequest-Cmdlet, um eine Zertifikatsignaturanforderung zu erstellen und an eine Zertifizierungsstelle zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="d3498-112">Use the New-AzureKeyVaultCertificateSigningRequest cmdlet to create a certificate signing request and submit it to a certificate authority.</span></span>
- <span data-ttu-id="d3498-113">Verwenden Sie eine vorhandene Zertifikatspaket Datei, beispielsweise eine PFX-oder P12-Datei, die sowohl das Zertifikat als auch den privaten Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="d3498-113">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="d3498-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d3498-114">EXAMPLES</span></span>

### <span data-ttu-id="d3498-115">Beispiel 1: Importieren eines schlüsseltresor-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="d3498-115">Example 1: Import a key vault certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS C:\> Import-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "ImportCert01" -FilePath "C:\Users\contosoUser\Desktop\import.pfx" -Password $Password
Name        : importCert01
Certificate : [Subject]
                CN=contoso.com

              [Issuer]
                CN=contoso.com

              [Serial Number]
                05979C5A2F0741D5A3B6F97673E8A118

              [Not Before]
                2/8/2016 3:11:45 PM

              [Not After]
                8/8/2016 4:21:45 PM

              [Thumbprint]
                3E9B6848AD1834284157D68B060F748037F663C8

Thumbprint  : 3E9B6848AD1834284157D68B060F748037F663C8
Tags        :
Enabled     : True
Created     : 2/8/2016 11:50:43 PM
Updated     : 2/8/2016 11:50:43 PM
```

<span data-ttu-id="d3498-116">Der erste Befehl verwendet das ConvertTo-SecureString-Cmdlet, um ein sicheres Kennwort zu erstellen, und speichert es dann in der $Password-Variablen.</span><span class="sxs-lookup"><span data-stu-id="d3498-116">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>

<span data-ttu-id="d3498-117">Mit dem zweiten Befehl wird das Zertifikat mit dem Namen ImportCert01 in den CosotosoKV01-schlüsseltresor importiert.</span><span class="sxs-lookup"><span data-stu-id="d3498-117">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="d3498-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3498-118">PARAMETERS</span></span>

### <span data-ttu-id="d3498-119">-Certificatecollection</span><span class="sxs-lookup"><span data-stu-id="d3498-119">-CertificateCollection</span></span>
<span data-ttu-id="d3498-120">Gibt die Zertifikat Sammlung an, die einem schlüsseltresor hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d3498-120">Specifies the certificate collection to add to a key vault.</span></span>

```yaml
Type: X509Certificate2Collection
Parameter Sets: ImportWithPrivateKeyFromCollection
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3498-121">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="d3498-121">-CertificateString</span></span>
<span data-ttu-id="d3498-122">Gibt eine Zertifikatzeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="d3498-122">Specifies a certificate string.</span></span>

```yaml
Type: String
Parameter Sets: ImportWithPrivateKeyFromString
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3498-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3498-123">-DefaultProfile</span></span>
<span data-ttu-id="d3498-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d3498-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3498-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="d3498-125">-FilePath</span></span>
<span data-ttu-id="d3498-126">Gibt den Pfad der Zertifikatsdatei an, die dieses Cmdlet importiert.</span><span class="sxs-lookup"><span data-stu-id="d3498-126">Specifies the path of the certificate file that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: ImportCertificateFromFile, ImportWithPrivateKeyFromFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3498-127">-Name</span><span class="sxs-lookup"><span data-stu-id="d3498-127">-Name</span></span>
<span data-ttu-id="d3498-128">Gibt den Zertifikatsnamen an.</span><span class="sxs-lookup"><span data-stu-id="d3498-128">Specifies the certificate name.</span></span> <span data-ttu-id="d3498-129">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Zertifikats aus dem schlüsseltresor Namen, der aktuell ausgewählten Umgebung und dem Zertifikatnamen.</span><span class="sxs-lookup"><span data-stu-id="d3498-129">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3498-130">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="d3498-130">-Password</span></span>
<span data-ttu-id="d3498-131">Gibt das Kennwort für eine Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="d3498-131">Specifies the password for a certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: ImportWithPrivateKeyFromFile, ImportWithPrivateKeyFromString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3498-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="d3498-132">-Tag</span></span>
<span data-ttu-id="d3498-133">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="d3498-133">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d3498-134">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d3498-134">For example:</span></span>

<span data-ttu-id="d3498-135">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="d3498-135">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3498-136">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="d3498-136">-VaultName</span></span>
<span data-ttu-id="d3498-137">Gibt den Namen des Schlüssel Tresors an, in den dieses Cmdlet Zertifikate importiert.</span><span class="sxs-lookup"><span data-stu-id="d3498-137">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="d3498-138">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüsseldepots basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="d3498-138">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3498-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d3498-139">-Confirm</span></span>
<span data-ttu-id="d3498-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d3498-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3498-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3498-141">-WhatIf</span></span>
<span data-ttu-id="d3498-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d3498-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3498-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d3498-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3498-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3498-144">CommonParameters</span></span>
<span data-ttu-id="d3498-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3498-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3498-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3498-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3498-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d3498-147">INPUTS</span></span>

## <span data-ttu-id="d3498-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d3498-148">OUTPUTS</span></span>

### <span data-ttu-id="d3498-149">Microsoft. Azure. Commands. keyvault. Models. CertificateBundle</span><span class="sxs-lookup"><span data-stu-id="d3498-149">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="d3498-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="d3498-150">NOTES</span></span>

## <span data-ttu-id="d3498-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d3498-151">RELATED LINKS</span></span>

[<span data-ttu-id="d3498-152">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d3498-152">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)
