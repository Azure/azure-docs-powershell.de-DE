---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 370662b1d24f9b5b71653506be7a3add5a3801f8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166432"
---
# <span data-ttu-id="199ec-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="199ec-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="199ec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="199ec-102">SYNOPSIS</span></span>
<span data-ttu-id="199ec-103">Erstellt ein Zertifikatrichtlinien Objekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="199ec-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="199ec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="199ec-104">SYNTAX</span></span>

### <span data-ttu-id="199ec-105">SubjectName (Standard)</span><span class="sxs-lookup"><span data-stu-id="199ec-105">SubjectName (Default)</span></span>
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

### <span data-ttu-id="199ec-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="199ec-106">DNSNames</span></span>
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

## <span data-ttu-id="199ec-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="199ec-107">DESCRIPTION</span></span>
<span data-ttu-id="199ec-108">Das Cmdlet **New-AzKeyVaultCertificatePolicy** erstellt ein Zertifikatrichtlinien Objekt im Arbeitsspeicher für Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="199ec-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="199ec-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="199ec-109">EXAMPLES</span></span>

### <span data-ttu-id="199ec-110">Beispiel 1: Erstellen einer Zertifikatrichtlinie</span><span class="sxs-lookup"><span data-stu-id="199ec-110">Example 1: Create a certificate policy</span></span>
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

<span data-ttu-id="199ec-111">Dieser Befehl erstellt eine Zertifikatrichtlinie, die für sechs Monate gültig ist, und verwendet den Schlüssel zum Verlängern des Zertifikats erneut.</span><span class="sxs-lookup"><span data-stu-id="199ec-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

### <span data-ttu-id="199ec-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="199ec-112">Example 2</span></span>

<span data-ttu-id="199ec-113">Erstellt ein Zertifikatrichtlinien Objekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="199ec-113">Creates an in-memory certificate policy object.</span></span> <span data-ttu-id="199ec-114">automatisch</span><span class="sxs-lookup"><span data-stu-id="199ec-114">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzKeyVaultCertificatePolicy -IssuerName 'Self' -KeyType RSA -RenewAtNumberOfDaysBeforeExpiry <Int32> -SecretContentType application/x-pkcs12 -SubjectName 'CN=contoso.com' -ValidityInMonths 6
```

### <span data-ttu-id="199ec-115">Beispiel 3: Erstellen eines Subject Alternative Name (oder San)-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="199ec-115">Example 3: Create a Subject Alternate Name (or SAN) certificate</span></span>

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

<span data-ttu-id="199ec-116">In diesem Beispiel wird ein San-Zertifikat mit 3 DNS-Namen erstellt.</span><span class="sxs-lookup"><span data-stu-id="199ec-116">This example creates a SAN certificate with 3 DNS names.</span></span>

## <span data-ttu-id="199ec-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="199ec-117">PARAMETERS</span></span>

### <span data-ttu-id="199ec-118">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="199ec-118">-CertificateTransparency</span></span>
<span data-ttu-id="199ec-119">Gibt an, ob die Zertifikat Transparenz für dieses Zertifikat/den Aussteller aktiviert ist. Wenn keine Angabe erfolgt, lautet der Standardwert "wahr".</span><span class="sxs-lookup"><span data-stu-id="199ec-119">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="199ec-120">-Certificatetype</span><span class="sxs-lookup"><span data-stu-id="199ec-120">-CertificateType</span></span>
<span data-ttu-id="199ec-121">Gibt den Typ des Zertifikats an den Aussteller an.</span><span class="sxs-lookup"><span data-stu-id="199ec-121">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="199ec-122">-Curve</span><span class="sxs-lookup"><span data-stu-id="199ec-122">-Curve</span></span>
<span data-ttu-id="199ec-123">Gibt den Namen der elliptischen Kurve des Schlüssels des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="199ec-123">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="199ec-124">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="199ec-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="199ec-125">P-256</span><span class="sxs-lookup"><span data-stu-id="199ec-125">P-256</span></span>
- <span data-ttu-id="199ec-126">P-384</span><span class="sxs-lookup"><span data-stu-id="199ec-126">P-384</span></span>
- <span data-ttu-id="199ec-127">P-521</span><span class="sxs-lookup"><span data-stu-id="199ec-127">P-521</span></span>
- <span data-ttu-id="199ec-128">P-256 k</span><span class="sxs-lookup"><span data-stu-id="199ec-128">P-256K</span></span>
- <span data-ttu-id="199ec-129">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="199ec-129">SECP256K1</span></span>

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

### <span data-ttu-id="199ec-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="199ec-130">-DefaultProfile</span></span>
<span data-ttu-id="199ec-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="199ec-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="199ec-132">-Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="199ec-132">-Disabled</span></span>
<span data-ttu-id="199ec-133">Gibt an, dass die Zertifikatrichtlinie deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="199ec-133">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="199ec-134">-DnsName</span><span class="sxs-lookup"><span data-stu-id="199ec-134">-DnsName</span></span>
<span data-ttu-id="199ec-135">Gibt die DNS-Namen im Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="199ec-135">Specifies the DNS names in the certificate.</span></span> <span data-ttu-id="199ec-136">Alternative Subjektnamen (SANs) können als DNS-Namen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="199ec-136">Subject Alternative Names (SANs) can be specified as DNS names.</span></span>

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

### <span data-ttu-id="199ec-137">-EKUs</span><span class="sxs-lookup"><span data-stu-id="199ec-137">-Ekus</span></span>
<span data-ttu-id="199ec-138">Gibt die erweiterten Schlüsselverwendungen (EKUs) im Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="199ec-138">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="199ec-139">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="199ec-139">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="199ec-140">Gibt an, wie viele Tage vor Ablauf des automatischen Benachrichtigungsprozesses beginnen.</span><span class="sxs-lookup"><span data-stu-id="199ec-140">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="199ec-141">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="199ec-141">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="199ec-142">Gibt den Prozentsatz der Lebensdauer an, nach dem der automatische Prozess für die Benachrichtigung beginnt.</span><span class="sxs-lookup"><span data-stu-id="199ec-142">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="199ec-143">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="199ec-143">-IssuerName</span></span>
<span data-ttu-id="199ec-144">Gibt den Namen des Emittenten für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="199ec-144">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="199ec-145">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="199ec-145">-KeyNotExportable</span></span>
<span data-ttu-id="199ec-146">Gibt an, dass der Schlüssel nicht exportierbar ist.</span><span class="sxs-lookup"><span data-stu-id="199ec-146">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="199ec-147">-KeySize</span><span class="sxs-lookup"><span data-stu-id="199ec-147">-KeySize</span></span>
<span data-ttu-id="199ec-148">Gibt die Schlüsselgröße des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="199ec-148">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="199ec-149">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="199ec-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="199ec-150">2048</span><span class="sxs-lookup"><span data-stu-id="199ec-150">2048</span></span>
- <span data-ttu-id="199ec-151">3072</span><span class="sxs-lookup"><span data-stu-id="199ec-151">3072</span></span>
- <span data-ttu-id="199ec-152">4096</span><span class="sxs-lookup"><span data-stu-id="199ec-152">4096</span></span>
- <span data-ttu-id="199ec-153">256</span><span class="sxs-lookup"><span data-stu-id="199ec-153">256</span></span>
- <span data-ttu-id="199ec-154">384</span><span class="sxs-lookup"><span data-stu-id="199ec-154">384</span></span>
- <span data-ttu-id="199ec-155">521</span><span class="sxs-lookup"><span data-stu-id="199ec-155">521</span></span>

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

### <span data-ttu-id="199ec-156">-KeyType</span><span class="sxs-lookup"><span data-stu-id="199ec-156">-KeyType</span></span>
<span data-ttu-id="199ec-157">Gibt den Schlüsseltyp des Schlüssels an, der das Zertifikat zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="199ec-157">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="199ec-158">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="199ec-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="199ec-159">RSA</span><span class="sxs-lookup"><span data-stu-id="199ec-159">RSA</span></span>
- <span data-ttu-id="199ec-160">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="199ec-160">RSA-HSM</span></span>
- <span data-ttu-id="199ec-161">EC des Rates</span><span class="sxs-lookup"><span data-stu-id="199ec-161">EC</span></span>
- <span data-ttu-id="199ec-162">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="199ec-162">EC-HSM</span></span>

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

### <span data-ttu-id="199ec-163">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="199ec-163">-KeyUsage</span></span>
<span data-ttu-id="199ec-164">Gibt die Schlüsselverwendungen im Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="199ec-164">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="199ec-165">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="199ec-165">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="199ec-166">Gibt an, wie viele Tage vor dem Ablaufdatum der automatische Prozess für die Zertifikaterneuerung beginnt.</span><span class="sxs-lookup"><span data-stu-id="199ec-166">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="199ec-167">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="199ec-167">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="199ec-168">Gibt den Prozentsatz der Lebensdauer an, nach dem der automatische Prozess für die Zertifikaterneuerung beginnt.</span><span class="sxs-lookup"><span data-stu-id="199ec-168">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="199ec-169">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="199ec-169">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="199ec-170">Gibt an, dass das Zertifikat den Schlüssel während der Erneuerung wieder verwendet.</span><span class="sxs-lookup"><span data-stu-id="199ec-170">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="199ec-171">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="199ec-171">-SecretContentType</span></span>
<span data-ttu-id="199ec-172">Gibt den Inhaltstyp des neuen Schlüssels Vault Secret an.</span><span class="sxs-lookup"><span data-stu-id="199ec-172">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="199ec-173">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="199ec-173">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="199ec-174">Anwendung/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="199ec-174">application/x-pkcs12</span></span>
- <span data-ttu-id="199ec-175">Application/x-PEM-Datei</span><span class="sxs-lookup"><span data-stu-id="199ec-175">application/x-pem-file</span></span>

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

### <span data-ttu-id="199ec-176">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="199ec-176">-SubjectName</span></span>
<span data-ttu-id="199ec-177">Gibt den Namen des Antragstellers des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="199ec-177">Specifies the subject name of the certificate.</span></span> 

> [!NOTE]
> <span data-ttu-id="199ec-178">Wenn Sie ein Komma (,) oder einen Punkt (.) innerhalb einer Eigenschaft des `SubjectName` Parameters verwenden müssen, müssen Sie das Eigenschaftsfeld in Anführungszeichen setzen.</span><span class="sxs-lookup"><span data-stu-id="199ec-178">If you must use a comma (,) or a period (.) within a property in the `SubjectName` parameter, you must enclose the property field in quotation marks.</span></span> <span data-ttu-id="199ec-179">So können Sie beispielsweise O = "contoso, Ltd." verwenden.</span><span class="sxs-lookup"><span data-stu-id="199ec-179">For example, you may use O="Contoso, Ltd."</span></span> <span data-ttu-id="199ec-180">im Feld Organisations Name.</span><span class="sxs-lookup"><span data-stu-id="199ec-180">in the Organization Name field.</span></span>

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

### <span data-ttu-id="199ec-181">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="199ec-181">-ValidityInMonths</span></span>
<span data-ttu-id="199ec-182">Gibt an, wie viele Monate das Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="199ec-182">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="199ec-183">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="199ec-183">-Confirm</span></span>
<span data-ttu-id="199ec-184">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="199ec-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="199ec-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="199ec-185">-WhatIf</span></span>
<span data-ttu-id="199ec-186">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="199ec-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="199ec-187">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="199ec-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="199ec-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="199ec-188">CommonParameters</span></span>
<span data-ttu-id="199ec-189">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="199ec-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="199ec-190">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="199ec-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="199ec-191">Eingaben</span><span class="sxs-lookup"><span data-stu-id="199ec-191">INPUTS</span></span>

### <span data-ttu-id="199ec-192">System. String</span><span class="sxs-lookup"><span data-stu-id="199ec-192">System.String</span></span>

### <span data-ttu-id="199ec-193">System. Collections. Generic. List ' 1 [[System. String, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="199ec-193">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="199ec-194">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="199ec-194">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="199ec-195">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="199ec-195">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="199ec-196">System. Collections. Generic. List ' 1 [[System. Security. Cryptography. X509Certificates. X509KeyUsageFlags, System. Security. Cryptography. X509Certificates, Version = 4.2.1.0, Culture = neutral, PublicKeyToken = b03f5f7f11d50a3a]]</span><span class="sxs-lookup"><span data-stu-id="199ec-196">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="199ec-197">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="199ec-197">OUTPUTS</span></span>

### <span data-ttu-id="199ec-198">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="199ec-198">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="199ec-199">Notizen</span><span class="sxs-lookup"><span data-stu-id="199ec-199">NOTES</span></span>

## <span data-ttu-id="199ec-200">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="199ec-200">RELATED LINKS</span></span>

[<span data-ttu-id="199ec-201">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="199ec-201">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="199ec-202">Satz-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="199ec-202">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

