---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: b0d690358fb5598b1a88ecb7fe169c8ef3d2718f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005087"
---
# <span data-ttu-id="53090-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="53090-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="53090-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="53090-102">SYNOPSIS</span></span>
<span data-ttu-id="53090-103">Erstellt ein Zertifikatrichtlinien Objekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="53090-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="53090-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="53090-104">SYNTAX</span></span>

### <span data-ttu-id="53090-105">SubjectName (Standard)</span><span class="sxs-lookup"><span data-stu-id="53090-105">SubjectName (Default)</span></span>
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

### <span data-ttu-id="53090-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="53090-106">DNSNames</span></span>
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

## <span data-ttu-id="53090-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="53090-107">DESCRIPTION</span></span>
<span data-ttu-id="53090-108">Das Cmdlet **New-AzKeyVaultCertificatePolicy** erstellt ein Zertifikatrichtlinien Objekt im Arbeitsspeicher für Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="53090-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="53090-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53090-109">EXAMPLES</span></span>

### <span data-ttu-id="53090-110">Beispiel 1: Erstellen einer Zertifikatrichtlinie</span><span class="sxs-lookup"><span data-stu-id="53090-110">Example 1: Create a certificate policy</span></span>
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

<span data-ttu-id="53090-111">Dieser Befehl erstellt eine Zertifikatrichtlinie, die für sechs Monate gültig ist, und verwendet den Schlüssel zum Verlängern des Zertifikats erneut.</span><span class="sxs-lookup"><span data-stu-id="53090-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="53090-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="53090-112">PARAMETERS</span></span>

### <span data-ttu-id="53090-113">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="53090-113">-CertificateTransparency</span></span>
<span data-ttu-id="53090-114">Gibt an, ob die Zertifikat Transparenz für dieses Zertifikat/den Aussteller aktiviert ist. Wenn keine Angabe erfolgt, lautet der Standardwert "wahr".</span><span class="sxs-lookup"><span data-stu-id="53090-114">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="53090-115">-Certificatetype</span><span class="sxs-lookup"><span data-stu-id="53090-115">-CertificateType</span></span>
<span data-ttu-id="53090-116">Gibt den Typ des Zertifikats an den Aussteller an.</span><span class="sxs-lookup"><span data-stu-id="53090-116">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="53090-117">-Curve</span><span class="sxs-lookup"><span data-stu-id="53090-117">-Curve</span></span>
<span data-ttu-id="53090-118">Gibt den Namen der elliptischen Kurve des Schlüssels des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="53090-118">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="53090-119">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="53090-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="53090-120">P-256</span><span class="sxs-lookup"><span data-stu-id="53090-120">P-256</span></span>
- <span data-ttu-id="53090-121">P-384</span><span class="sxs-lookup"><span data-stu-id="53090-121">P-384</span></span>
- <span data-ttu-id="53090-122">P-521</span><span class="sxs-lookup"><span data-stu-id="53090-122">P-521</span></span>
- <span data-ttu-id="53090-123">P-256 k</span><span class="sxs-lookup"><span data-stu-id="53090-123">P-256K</span></span>
- <span data-ttu-id="53090-124">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="53090-124">SECP256K1</span></span>

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

### <span data-ttu-id="53090-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53090-125">-DefaultProfile</span></span>
<span data-ttu-id="53090-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="53090-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53090-127">-Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="53090-127">-Disabled</span></span>
<span data-ttu-id="53090-128">Gibt an, dass die Zertifikatrichtlinie deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="53090-128">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="53090-129">-DnsName</span><span class="sxs-lookup"><span data-stu-id="53090-129">-DnsName</span></span>
<span data-ttu-id="53090-130">Gibt die DNS-Namen im Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="53090-130">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="53090-131">-EKUs</span><span class="sxs-lookup"><span data-stu-id="53090-131">-Ekus</span></span>
<span data-ttu-id="53090-132">Gibt die erweiterten Schlüsselverwendungen (EKUs) im Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="53090-132">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="53090-133">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="53090-133">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="53090-134">Gibt an, wie viele Tage vor Ablauf des automatischen Benachrichtigungsprozesses beginnen.</span><span class="sxs-lookup"><span data-stu-id="53090-134">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="53090-135">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="53090-135">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="53090-136">Gibt den Prozentsatz der Lebensdauer an, nach dem der automatische Prozess für die Benachrichtigung beginnt.</span><span class="sxs-lookup"><span data-stu-id="53090-136">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="53090-137">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="53090-137">-IssuerName</span></span>
<span data-ttu-id="53090-138">Gibt den Namen des Emittenten für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="53090-138">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="53090-139">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="53090-139">-KeyNotExportable</span></span>
<span data-ttu-id="53090-140">Gibt an, dass der Schlüssel nicht exportierbar ist.</span><span class="sxs-lookup"><span data-stu-id="53090-140">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="53090-141">-KeySize</span><span class="sxs-lookup"><span data-stu-id="53090-141">-KeySize</span></span>
<span data-ttu-id="53090-142">Gibt die Schlüsselgröße des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="53090-142">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="53090-143">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="53090-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="53090-144">2048</span><span class="sxs-lookup"><span data-stu-id="53090-144">2048</span></span>
- <span data-ttu-id="53090-145">3072</span><span class="sxs-lookup"><span data-stu-id="53090-145">3072</span></span>
- <span data-ttu-id="53090-146">4096</span><span class="sxs-lookup"><span data-stu-id="53090-146">4096</span></span>
- <span data-ttu-id="53090-147">256</span><span class="sxs-lookup"><span data-stu-id="53090-147">256</span></span>
- <span data-ttu-id="53090-148">384</span><span class="sxs-lookup"><span data-stu-id="53090-148">384</span></span>
- <span data-ttu-id="53090-149">521</span><span class="sxs-lookup"><span data-stu-id="53090-149">521</span></span>

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

### <span data-ttu-id="53090-150">-KeyType</span><span class="sxs-lookup"><span data-stu-id="53090-150">-KeyType</span></span>
<span data-ttu-id="53090-151">Gibt den Schlüsseltyp des Schlüssels an, der das Zertifikat zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="53090-151">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="53090-152">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="53090-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="53090-153">RSA</span><span class="sxs-lookup"><span data-stu-id="53090-153">RSA</span></span>
- <span data-ttu-id="53090-154">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="53090-154">RSA-HSM</span></span>
- <span data-ttu-id="53090-155">EC des Rates</span><span class="sxs-lookup"><span data-stu-id="53090-155">EC</span></span>
- <span data-ttu-id="53090-156">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="53090-156">EC-HSM</span></span>

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

### <span data-ttu-id="53090-157">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="53090-157">-KeyUsage</span></span>
<span data-ttu-id="53090-158">Gibt die Schlüsselverwendungen im Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="53090-158">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="53090-159">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="53090-159">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="53090-160">Gibt an, wie viele Tage vor dem Ablaufdatum der automatische Prozess für die Zertifikaterneuerung beginnt.</span><span class="sxs-lookup"><span data-stu-id="53090-160">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="53090-161">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="53090-161">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="53090-162">Gibt den Prozentsatz der Lebensdauer an, nach dem der automatische Prozess für die Zertifikaterneuerung beginnt.</span><span class="sxs-lookup"><span data-stu-id="53090-162">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="53090-163">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="53090-163">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="53090-164">Gibt an, dass das Zertifikat den Schlüssel während der Erneuerung wieder verwendet.</span><span class="sxs-lookup"><span data-stu-id="53090-164">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="53090-165">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="53090-165">-SecretContentType</span></span>
<span data-ttu-id="53090-166">Gibt den Inhaltstyp des neuen Schlüssels Vault Secret an.</span><span class="sxs-lookup"><span data-stu-id="53090-166">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="53090-167">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="53090-167">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="53090-168">Anwendung/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="53090-168">application/x-pkcs12</span></span>
- <span data-ttu-id="53090-169">Application/x-PEM-Datei</span><span class="sxs-lookup"><span data-stu-id="53090-169">application/x-pem-file</span></span>

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

### <span data-ttu-id="53090-170">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="53090-170">-SubjectName</span></span>
<span data-ttu-id="53090-171">Gibt den Namen des Antragstellers des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="53090-171">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="53090-172">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="53090-172">-ValidityInMonths</span></span>
<span data-ttu-id="53090-173">Gibt an, wie viele Monate das Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="53090-173">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="53090-174">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="53090-174">-Confirm</span></span>
<span data-ttu-id="53090-175">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="53090-175">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53090-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53090-176">-WhatIf</span></span>
<span data-ttu-id="53090-177">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="53090-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53090-178">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="53090-178">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53090-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53090-179">CommonParameters</span></span>
<span data-ttu-id="53090-180">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53090-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53090-181">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53090-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53090-182">Eingaben</span><span class="sxs-lookup"><span data-stu-id="53090-182">INPUTS</span></span>

### <span data-ttu-id="53090-183">System. String</span><span class="sxs-lookup"><span data-stu-id="53090-183">System.String</span></span>

### <span data-ttu-id="53090-184">System. Collections. Generic. List ' 1 [[System. String, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="53090-184">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="53090-185">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="53090-185">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="53090-186">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="53090-186">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="53090-187">System. Collections. Generic. List ' 1 [[System. Security. Cryptography. X509Certificates. X509KeyUsageFlags, System. Security. Cryptography. X509Certificates, Version = 4.2.1.0, Culture = neutral, PublicKeyToken = b03f5f7f11d50a3a]]</span><span class="sxs-lookup"><span data-stu-id="53090-187">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="53090-188">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="53090-188">OUTPUTS</span></span>

### <span data-ttu-id="53090-189">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="53090-189">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="53090-190">Notizen</span><span class="sxs-lookup"><span data-stu-id="53090-190">NOTES</span></span>

## <span data-ttu-id="53090-191">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="53090-191">RELATED LINKS</span></span>

[<span data-ttu-id="53090-192">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="53090-192">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="53090-193">Satz-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="53090-193">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

