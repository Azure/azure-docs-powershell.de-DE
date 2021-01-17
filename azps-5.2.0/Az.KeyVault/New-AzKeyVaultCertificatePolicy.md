---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 370662b1d24f9b5b71653506be7a3add5a3801f8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367294"
---
# <span data-ttu-id="4ea85-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4ea85-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="4ea85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ea85-102">SYNOPSIS</span></span>
<span data-ttu-id="4ea85-103">Erstellt ein Speicherzertifikatrichtlinienobjekt.</span><span class="sxs-lookup"><span data-stu-id="4ea85-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="4ea85-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ea85-104">SYNTAX</span></span>

### <span data-ttu-id="4ea85-105">SubjectName (Standard)</span><span class="sxs-lookup"><span data-stu-id="4ea85-105">SubjectName (Default)</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [-SubjectName] <String>
 [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>]
 [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ea85-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="4ea85-106">DNSNames</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [[-SubjectName] <String>]
 [-DnsName] <System.Collections.Generic.List`1[System.String]> [-RenewAtNumberOfDaysBeforeExpiry <Int32>]
 [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ea85-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ea85-107">DESCRIPTION</span></span>
<span data-ttu-id="4ea85-108">Das **Cmdlet "New-AzKeyVaultCertificatePolicy"** erstellt ein Speicherzertifikatrichtlinienobjekt für den Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="4ea85-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="4ea85-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4ea85-109">EXAMPLES</span></span>

### <span data-ttu-id="4ea85-110">Beispiel 1: Erstellen einer Zertifikatrichtlinie</span><span class="sxs-lookup"><span data-stu-id="4ea85-110">Example 1: Create a certificate policy</span></span>
```powershell
PS C:\> New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal

SecretContentType               : application/x-pkcs12
Kty                             :
KeySize                         : 2048
Curve                           :
Exportable                      :
ReuseKeyOnRenewal               : True
SubjectName                     : CN=contoso.com
DnsNames                        :
KeyUsage                        :
Ekus                            :
ValidityInMonths                : 6
IssuerName                      : Self
CertificateType                 :
RenewAtNumberOfDaysBeforeExpiry :
RenewAtPercentageLifetime       :
EmailAtNumberOfDaysBeforeExpiry :
EmailAtPercentageLifetime       :
CertificateTransparency         :
Enabled                         : True
Created                         :
Updated                         :
```

<span data-ttu-id="4ea85-111">Mit diesem Befehl wird eine Zertifikatrichtlinie erstellt, die sechs Monate lang gültig ist, und der Schlüssel zum Erneuern des Zertifikats erneut verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ea85-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

### <span data-ttu-id="4ea85-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4ea85-112">Example 2</span></span>

<span data-ttu-id="4ea85-113">Erstellt ein Speicherzertifikatrichtlinienobjekt.</span><span class="sxs-lookup"><span data-stu-id="4ea85-113">Creates an in-memory certificate policy object.</span></span> <span data-ttu-id="4ea85-114">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="4ea85-114">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzKeyVaultCertificatePolicy -IssuerName 'Self' -KeyType RSA -RenewAtNumberOfDaysBeforeExpiry <Int32> -SecretContentType application/x-pkcs12 -SubjectName 'CN=contoso.com' -ValidityInMonths 6
```

### <span data-ttu-id="4ea85-115">Beispiel 3: Erstellen eines Zertifikats vom Typennamen (Subject Alternate Name, SAN)</span><span class="sxs-lookup"><span data-stu-id="4ea85-115">Example 3: Create a Subject Alternate Name (or SAN) certificate</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -DnsName "contoso.com","support.contoso.com","docs.contoso.com" -IssuerName "Self"

SecretContentType               : application/x-pkcs12
Kty                             : RSA
KeySize                         : 2048
Curve                           :
Exportable                      :
ReuseKeyOnRenewal               : False
SubjectName                     : CN=contoso.com
DnsNames                        : {contoso.com, support.contoso.com, docs.contoso.com}
KeyUsage                        :
Ekus                            :
ValidityInMonths                :
IssuerName                      : Self
CertificateType                 :
RenewAtNumberOfDaysBeforeExpiry :
RenewAtPercentageLifetime       :
EmailAtNumberOfDaysBeforeExpiry :
EmailAtPercentageLifetime       :
CertificateTransparency         :
Enabled                         : True
Created                         :
Updated                         :
```

<span data-ttu-id="4ea85-116">In diesem Beispiel wird ein SAN-Zertifikat mit drei DNS-Namen erstellt.</span><span class="sxs-lookup"><span data-stu-id="4ea85-116">This example creates a SAN certificate with 3 DNS names.</span></span>

## <span data-ttu-id="4ea85-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ea85-117">PARAMETERS</span></span>

### <span data-ttu-id="4ea85-118">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="4ea85-118">-CertificateTransparency</span></span>
<span data-ttu-id="4ea85-119">Gibt an, ob für dieses Zertifikat/den Aussteller Zertifikattransparenz aktiviert ist. wenn nicht angegeben, ist der Standardwert "true".</span><span class="sxs-lookup"><span data-stu-id="4ea85-119">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea85-120">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="4ea85-120">-CertificateType</span></span>
<span data-ttu-id="4ea85-121">Gibt den Typ des Zertifikats für den Aussteller an.</span><span class="sxs-lookup"><span data-stu-id="4ea85-121">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea85-122">-Curve</span><span class="sxs-lookup"><span data-stu-id="4ea85-122">-Curve</span></span>
<span data-ttu-id="4ea85-123">Gibt den auslassungspunktenden Kurvennamen des Schlüssels des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="4ea85-123">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="4ea85-124">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="4ea85-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4ea85-125">P-256</span><span class="sxs-lookup"><span data-stu-id="4ea85-125">P-256</span></span>
- <span data-ttu-id="4ea85-126">P-384</span><span class="sxs-lookup"><span data-stu-id="4ea85-126">P-384</span></span>
- <span data-ttu-id="4ea85-127">P-521</span><span class="sxs-lookup"><span data-stu-id="4ea85-127">P-521</span></span>
- <span data-ttu-id="4ea85-128">P-256K</span><span class="sxs-lookup"><span data-stu-id="4ea85-128">P-256K</span></span>
- <span data-ttu-id="4ea85-129">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="4ea85-129">SECP256K1</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: P-256, P-384, P-521, P-256K, SECP256K1

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea85-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ea85-130">-DefaultProfile</span></span>
<span data-ttu-id="4ea85-131">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4ea85-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ea85-132">-Disabled</span><span class="sxs-lookup"><span data-stu-id="4ea85-132">-Disabled</span></span>
<span data-ttu-id="4ea85-133">Gibt an, dass die Zertifikatrichtlinie deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4ea85-133">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea85-134">-DnsName</span><span class="sxs-lookup"><span data-stu-id="4ea85-134">-DnsName</span></span>
<span data-ttu-id="4ea85-135">Gibt die DNS-Namen im Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="4ea85-135">Specifies the DNS names in the certificate.</span></span> <span data-ttu-id="4ea85-136">Subject Alternative Names (SANs) können als DNS-Namen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4ea85-136">Subject Alternative Names (SANs) can be specified as DNS names.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: DNSNames
Aliases: DnsNames

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea85-137">-EKUS</span><span class="sxs-lookup"><span data-stu-id="4ea85-137">-Ekus</span></span>
<span data-ttu-id="4ea85-138">Gibt die erweiterten Schlüsselverwendungen (ENHANCEDUs) im Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="4ea85-138">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea85-139">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="4ea85-139">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="4ea85-140">Gibt an, wie viele Tage vor Ablauf der automatische Benachrichtigungsprozess beginnt.</span><span class="sxs-lookup"><span data-stu-id="4ea85-140">Specifies how many days before expiry the automatic notification process begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea85-141">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="4ea85-141">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="4ea85-142">Gibt den Prozentsatz der Lebensdauer an, nach dem der automatische Prozess für die Benachrichtigung beginnt.</span><span class="sxs-lookup"><span data-stu-id="4ea85-142">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea85-143">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="4ea85-143">-IssuerName</span></span>
<span data-ttu-id="4ea85-144">Gibt den Namen des Ausstellers für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="4ea85-144">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="4ea85-145">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="4ea85-145">-KeyNotExportable</span></span>
<span data-ttu-id="4ea85-146">Gibt an, dass der Schlüssel nicht exportiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="4ea85-146">Indicates that the key is not exportable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea85-147">-KeySize</span><span class="sxs-lookup"><span data-stu-id="4ea85-147">-KeySize</span></span>
<span data-ttu-id="4ea85-148">Gibt die Schlüsselgröße des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="4ea85-148">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="4ea85-149">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="4ea85-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4ea85-150">2048</span><span class="sxs-lookup"><span data-stu-id="4ea85-150">2048</span></span>
- <span data-ttu-id="4ea85-151">3072</span><span class="sxs-lookup"><span data-stu-id="4ea85-151">3072</span></span>
- <span data-ttu-id="4ea85-152">4096</span><span class="sxs-lookup"><span data-stu-id="4ea85-152">4096</span></span>
- <span data-ttu-id="4ea85-153">256</span><span class="sxs-lookup"><span data-stu-id="4ea85-153">256</span></span>
- <span data-ttu-id="4ea85-154">384</span><span class="sxs-lookup"><span data-stu-id="4ea85-154">384</span></span>
- <span data-ttu-id="4ea85-155">521</span><span class="sxs-lookup"><span data-stu-id="4ea85-155">521</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:
Accepted values: 2048, 3072, 4096, 256, 384, 521

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea85-156">-KeyType</span><span class="sxs-lookup"><span data-stu-id="4ea85-156">-KeyType</span></span>
<span data-ttu-id="4ea85-157">Gibt den Schlüsseltyp des Schlüssels an, der das Zertifikat zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4ea85-157">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="4ea85-158">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="4ea85-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4ea85-159">RSA</span><span class="sxs-lookup"><span data-stu-id="4ea85-159">RSA</span></span>
- <span data-ttu-id="4ea85-160">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="4ea85-160">RSA-HSM</span></span>
- <span data-ttu-id="4ea85-161">EC</span><span class="sxs-lookup"><span data-stu-id="4ea85-161">EC</span></span>
- <span data-ttu-id="4ea85-162">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="4ea85-162">EC-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM, EC, EC-HSM

Required: False
Position: Named
Default value: RSA
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea85-163">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="4ea85-163">-KeyUsage</span></span>
<span data-ttu-id="4ea85-164">Gibt die Schlüsselverwendungen im Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="4ea85-164">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]
Parameter Sets: (All)
Aliases:
Accepted values: None, EncipherOnly, CrlSign, KeyCertSign, KeyAgreement, DataEncipherment, KeyEncipherment, NonRepudiation, DigitalSignature, DecipherOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea85-165">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="4ea85-165">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="4ea85-166">Gibt die Anzahl von Tagen vor dem Ablauf an, nach der der automatische Prozess für die Zertifikaterneuerung beginnt.</span><span class="sxs-lookup"><span data-stu-id="4ea85-166">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea85-167">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="4ea85-167">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="4ea85-168">Gibt den Prozentsatz der Lebensdauer an, nach dem der automatische Prozess für die Zertifikaterneuerung beginnt.</span><span class="sxs-lookup"><span data-stu-id="4ea85-168">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea85-169">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="4ea85-169">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="4ea85-170">Gibt an, dass das Zertifikat den Schlüssel während der Verlängerung wiederverwendet.</span><span class="sxs-lookup"><span data-stu-id="4ea85-170">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea85-171">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="4ea85-171">-SecretContentType</span></span>
<span data-ttu-id="4ea85-172">Gibt den Inhaltstyp des neuen Schlüsseltresorschlüssels an.</span><span class="sxs-lookup"><span data-stu-id="4ea85-172">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="4ea85-173">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="4ea85-173">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4ea85-174">application/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="4ea85-174">application/x-pkcs12</span></span>
- <span data-ttu-id="4ea85-175">application/x-pem-file</span><span class="sxs-lookup"><span data-stu-id="4ea85-175">application/x-pem-file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea85-176">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="4ea85-176">-SubjectName</span></span>
<span data-ttu-id="4ea85-177">Gibt den Betreffnamen des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="4ea85-177">Specifies the subject name of the certificate.</span></span> 

> [!NOTE]
> <span data-ttu-id="4ea85-178">Wenn Sie innerhalb einer Eigenschaft im Parameter ein Komma (,) oder einen Komma (.) verwenden müssen, müssen Sie das Eigenschaftsfeld `SubjectName` in Anführungszeichen setzen.</span><span class="sxs-lookup"><span data-stu-id="4ea85-178">If you must use a comma (,) or a period (.) within a property in the `SubjectName` parameter, you must enclose the property field in quotation marks.</span></span> <span data-ttu-id="4ea85-179">Sie können z. B. O="Contoso, Ltd." verwenden.</span><span class="sxs-lookup"><span data-stu-id="4ea85-179">For example, you may use O="Contoso, Ltd."</span></span> <span data-ttu-id="4ea85-180">im Feld "Organisationsname".</span><span class="sxs-lookup"><span data-stu-id="4ea85-180">in the Organization Name field.</span></span>

```yaml
Type: System.String
Parameter Sets: SubjectName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DNSNames
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea85-181">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="4ea85-181">-ValidityInMonths</span></span>
<span data-ttu-id="4ea85-182">Gibt die Anzahl der Monate an, für die das Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="4ea85-182">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea85-183">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ea85-183">-Confirm</span></span>
<span data-ttu-id="4ea85-184">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4ea85-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ea85-185">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4ea85-185">-WhatIf</span></span>
<span data-ttu-id="4ea85-186">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4ea85-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ea85-187">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4ea85-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ea85-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ea85-188">CommonParameters</span></span>
<span data-ttu-id="4ea85-189">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ea85-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ea85-190">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ea85-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ea85-191">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4ea85-191">INPUTS</span></span>

### <span data-ttu-id="4ea85-192">System.String</span><span class="sxs-lookup"><span data-stu-id="4ea85-192">System.String</span></span>

### <span data-ttu-id="4ea85-193">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4ea85-193">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4ea85-194">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4ea85-194">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4ea85-195">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4ea85-195">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="4ea85-196">System.Collections.Generic.List'1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span><span class="sxs-lookup"><span data-stu-id="4ea85-196">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="4ea85-197">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4ea85-197">OUTPUTS</span></span>

### <span data-ttu-id="4ea85-198">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4ea85-198">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="4ea85-199">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4ea85-199">NOTES</span></span>

## <span data-ttu-id="4ea85-200">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4ea85-200">RELATED LINKS</span></span>

[<span data-ttu-id="4ea85-201">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4ea85-201">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="4ea85-202">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4ea85-202">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

