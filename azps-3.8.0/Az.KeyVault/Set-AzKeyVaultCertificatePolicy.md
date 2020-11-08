---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 5a6b88ce85b8b9296d9666955a93d1240b631634
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997244"
---
# <span data-ttu-id="2ba54-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="2ba54-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="2ba54-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2ba54-102">SYNOPSIS</span></span>
<span data-ttu-id="2ba54-103">Erstellt oder aktualisiert die Richtlinie für ein Zertifikat in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="2ba54-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="2ba54-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ba54-104">SYNTAX</span></span>

### <span data-ttu-id="2ba54-105">ExpandedRenewPercentage (Standard)</span><span class="sxs-lookup"><span data-stu-id="2ba54-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ba54-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="2ba54-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-KeySize <Int32>]
 [-CertificateTransparency <Boolean>] [-PassThru] [-Curve <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ba54-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="2ba54-107">ExpandedRenewNumber</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> -RenewAtNumberOfDaysBeforeExpiry <Int32>
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ba54-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ba54-108">DESCRIPTION</span></span>
<span data-ttu-id="2ba54-109">Das Cmdlet " **festlegen-AzKeyVaultCertificatePolicy** " erstellt oder aktualisiert die Richtlinie für ein Zertifikat in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="2ba54-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="2ba54-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2ba54-110">EXAMPLES</span></span>

### <span data-ttu-id="2ba54-111">Beispiel 1: Festlegen einer Zertifikatrichtlinie</span><span class="sxs-lookup"><span data-stu-id="2ba54-111">Example 1: Set a certificate policy</span></span>
```powershell
PS C:\> Set-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True -PassThru

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

<span data-ttu-id="2ba54-112">Dieser Befehl legt die Richtlinie für das TestCert01-Zertifikat im ContosoKV01-schlüsseltresor fest.</span><span class="sxs-lookup"><span data-stu-id="2ba54-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="2ba54-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ba54-113">PARAMETERS</span></span>

### <span data-ttu-id="2ba54-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="2ba54-114">-CertificateTransparency</span></span>
<span data-ttu-id="2ba54-115">Gibt an, ob die Zertifikat Transparenz für dieses Zertifikat/den Aussteller aktiviert ist. Wenn keine Angabe erfolgt, lautet der Standardwert "wahr".</span><span class="sxs-lookup"><span data-stu-id="2ba54-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba54-116">-Certificatetype</span><span class="sxs-lookup"><span data-stu-id="2ba54-116">-CertificateType</span></span>
<span data-ttu-id="2ba54-117">Gibt den Typ des Zertifikats an den Aussteller an.</span><span class="sxs-lookup"><span data-stu-id="2ba54-117">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba54-118">-Curve</span><span class="sxs-lookup"><span data-stu-id="2ba54-118">-Curve</span></span>
<span data-ttu-id="2ba54-119">Gibt den Namen der elliptischen Kurve des Schlüssels des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="2ba54-119">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="2ba54-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2ba54-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2ba54-121">P-256</span><span class="sxs-lookup"><span data-stu-id="2ba54-121">P-256</span></span>
- <span data-ttu-id="2ba54-122">P-384</span><span class="sxs-lookup"><span data-stu-id="2ba54-122">P-384</span></span>
- <span data-ttu-id="2ba54-123">P-521</span><span class="sxs-lookup"><span data-stu-id="2ba54-123">P-521</span></span>
- <span data-ttu-id="2ba54-124">P-256 k</span><span class="sxs-lookup"><span data-stu-id="2ba54-124">P-256K</span></span>
- <span data-ttu-id="2ba54-125">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="2ba54-125">SECP256K1</span></span>

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

### <span data-ttu-id="2ba54-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ba54-126">-DefaultProfile</span></span>
<span data-ttu-id="2ba54-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2ba54-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ba54-128">-Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="2ba54-128">-Disabled</span></span>
<span data-ttu-id="2ba54-129">Gibt an, dass die Zertifikatrichtlinie deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2ba54-129">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba54-130">-DnsName</span><span class="sxs-lookup"><span data-stu-id="2ba54-130">-DnsName</span></span>
<span data-ttu-id="2ba54-131">Gibt den Namen des Antragstellers des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="2ba54-131">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases: DnsNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba54-132">-EKUs</span><span class="sxs-lookup"><span data-stu-id="2ba54-132">-Ekus</span></span>
<span data-ttu-id="2ba54-133">Gibt die erweiterten Schlüsselverwendungen (EKUs) im Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="2ba54-133">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba54-134">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="2ba54-134">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="2ba54-135">Gibt die Anzahl der Tage vor Ablauf an, wenn die automatische Verlängerung beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="2ba54-135">Specifies the number of days before expiration when automatic renewal should start.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba54-136">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="2ba54-136">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="2ba54-137">Gibt den Prozentsatz der Lebensdauer an, nach dem der automatische Prozess für die Benachrichtigung beginnt.</span><span class="sxs-lookup"><span data-stu-id="2ba54-137">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba54-138">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2ba54-138">-InputObject</span></span>
<span data-ttu-id="2ba54-139">Gibt die Zertifikatrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="2ba54-139">Specifies the certificate policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: CertificatePolicy

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ba54-140">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="2ba54-140">-IssuerName</span></span>
<span data-ttu-id="2ba54-141">Gibt den Namen des Emittenten für dieses Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="2ba54-141">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba54-142">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="2ba54-142">-KeyNotExportable</span></span>
<span data-ttu-id="2ba54-143">Gibt an, dass der Schlüssel nicht exportierbar ist.</span><span class="sxs-lookup"><span data-stu-id="2ba54-143">Indicates that the key is not exportable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba54-144">-KeySize</span><span class="sxs-lookup"><span data-stu-id="2ba54-144">-KeySize</span></span>
<span data-ttu-id="2ba54-145">Gibt die Schlüsselgröße des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="2ba54-145">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="2ba54-146">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2ba54-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2ba54-147">2048</span><span class="sxs-lookup"><span data-stu-id="2ba54-147">2048</span></span>
- <span data-ttu-id="2ba54-148">3072</span><span class="sxs-lookup"><span data-stu-id="2ba54-148">3072</span></span>
- <span data-ttu-id="2ba54-149">4096</span><span class="sxs-lookup"><span data-stu-id="2ba54-149">4096</span></span>
- <span data-ttu-id="2ba54-150">256</span><span class="sxs-lookup"><span data-stu-id="2ba54-150">256</span></span>
- <span data-ttu-id="2ba54-151">384</span><span class="sxs-lookup"><span data-stu-id="2ba54-151">384</span></span>
- <span data-ttu-id="2ba54-152">521</span><span class="sxs-lookup"><span data-stu-id="2ba54-152">521</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:
Accepted values: 2048, 3072, 4096, 256, 384, 521

Required: False
Position: Named
Default value: 2048
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ba54-153">-KeyType</span><span class="sxs-lookup"><span data-stu-id="2ba54-153">-KeyType</span></span>
<span data-ttu-id="2ba54-154">Gibt den Schlüsseltyp des Schlüssels an, der das Zertifikat zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="2ba54-154">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="2ba54-155">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2ba54-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2ba54-156">RSA</span><span class="sxs-lookup"><span data-stu-id="2ba54-156">RSA</span></span>
- <span data-ttu-id="2ba54-157">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="2ba54-157">RSA-HSM</span></span>
- <span data-ttu-id="2ba54-158">EC des Rates</span><span class="sxs-lookup"><span data-stu-id="2ba54-158">EC</span></span>
- <span data-ttu-id="2ba54-159">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="2ba54-159">EC-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM, EC, EC-HSM

Required: False
Position: Named
Default value: RSA
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba54-160">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="2ba54-160">-KeyUsage</span></span>
<span data-ttu-id="2ba54-161">Gibt die Schlüsselverwendungen im Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="2ba54-161">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: None, EncipherOnly, CrlSign, KeyCertSign, KeyAgreement, DataEncipherment, KeyEncipherment, NonRepudiation, DigitalSignature, DecipherOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba54-162">-Name</span><span class="sxs-lookup"><span data-stu-id="2ba54-162">-Name</span></span>
<span data-ttu-id="2ba54-163">Gibt den Namen des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="2ba54-163">Specifies the name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba54-164">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ba54-164">-PassThru</span></span>
<span data-ttu-id="2ba54-165">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="2ba54-165">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2ba54-166">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="2ba54-166">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2ba54-167">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="2ba54-167">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="2ba54-168">Gibt an, wie viele Tage vor dem Ablaufdatum der automatische Prozess für die Zertifikaterneuerung beginnt.</span><span class="sxs-lookup"><span data-stu-id="2ba54-168">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewNumber
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba54-169">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="2ba54-169">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="2ba54-170">Gibt den Prozentsatz der Lebensdauer an, nach dem der automatische Prozess für die Zertifikaterneuerung beginnt.</span><span class="sxs-lookup"><span data-stu-id="2ba54-170">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewPercentage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba54-171">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="2ba54-171">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="2ba54-172">Gibt an, dass das Zertifikat den Schlüssel während der Erneuerung wieder verwendet.</span><span class="sxs-lookup"><span data-stu-id="2ba54-172">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba54-173">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="2ba54-173">-SecretContentType</span></span>
<span data-ttu-id="2ba54-174">Gibt den Inhaltstyp des neuen Schlüssels Vault Secret an.</span><span class="sxs-lookup"><span data-stu-id="2ba54-174">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="2ba54-175">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2ba54-175">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2ba54-176">Anwendung/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="2ba54-176">application/x-pkcs12</span></span>
- <span data-ttu-id="2ba54-177">Application/x-PEM-Datei</span><span class="sxs-lookup"><span data-stu-id="2ba54-177">application/x-pem-file</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba54-178">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="2ba54-178">-SubjectName</span></span>
<span data-ttu-id="2ba54-179">Gibt den Namen des Antragstellers des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="2ba54-179">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba54-180">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="2ba54-180">-ValidityInMonths</span></span>
<span data-ttu-id="2ba54-181">Gibt an, wie viele Monate das Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="2ba54-181">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba54-182">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="2ba54-182">-VaultName</span></span>
<span data-ttu-id="2ba54-183">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="2ba54-183">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba54-184">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2ba54-184">-Confirm</span></span>
<span data-ttu-id="2ba54-185">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2ba54-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ba54-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ba54-186">-WhatIf</span></span>
<span data-ttu-id="2ba54-187">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2ba54-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ba54-188">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2ba54-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ba54-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ba54-189">CommonParameters</span></span>
<span data-ttu-id="2ba54-190">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ba54-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ba54-191">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ba54-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ba54-192">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2ba54-192">INPUTS</span></span>

### <span data-ttu-id="2ba54-193">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="2ba54-193">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="2ba54-194">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2ba54-194">OUTPUTS</span></span>

### <span data-ttu-id="2ba54-195">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="2ba54-195">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="2ba54-196">Notizen</span><span class="sxs-lookup"><span data-stu-id="2ba54-196">NOTES</span></span>

## <span data-ttu-id="2ba54-197">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2ba54-197">RELATED LINKS</span></span>

[<span data-ttu-id="2ba54-198">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="2ba54-198">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="2ba54-199">Neu – AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="2ba54-199">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

