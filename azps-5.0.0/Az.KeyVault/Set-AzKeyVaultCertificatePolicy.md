---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 963a7005e95941a644b35a57f80b558f02e2d6a0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296847"
---
# <span data-ttu-id="12dc5-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="12dc5-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="12dc5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="12dc5-102">SYNOPSIS</span></span>
<span data-ttu-id="12dc5-103">Erstellt oder aktualisiert die Richtlinie für ein Zertifikat in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="12dc5-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="12dc5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="12dc5-104">SYNTAX</span></span>

### <span data-ttu-id="12dc5-105">ExpandedRenewPercentage (Standard)</span><span class="sxs-lookup"><span data-stu-id="12dc5-105">ExpandedRenewPercentage (Default)</span></span>
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

### <span data-ttu-id="12dc5-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="12dc5-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-KeySize <Int32>]
 [-CertificateTransparency <Boolean>] [-PassThru] [-Curve <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12dc5-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="12dc5-107">ExpandedRenewNumber</span></span>
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

## <span data-ttu-id="12dc5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12dc5-108">DESCRIPTION</span></span>
<span data-ttu-id="12dc5-109">Das Cmdlet " **festlegen-AzKeyVaultCertificatePolicy** " erstellt oder aktualisiert die Richtlinie für ein Zertifikat in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="12dc5-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="12dc5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="12dc5-110">EXAMPLES</span></span>

### <span data-ttu-id="12dc5-111">Beispiel 1: Festlegen einer Zertifikatrichtlinie</span><span class="sxs-lookup"><span data-stu-id="12dc5-111">Example 1: Set a certificate policy</span></span>
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

<span data-ttu-id="12dc5-112">Dieser Befehl legt die Richtlinie für das TestCert01-Zertifikat im ContosoKV01-schlüsseltresor fest.</span><span class="sxs-lookup"><span data-stu-id="12dc5-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="12dc5-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="12dc5-113">PARAMETERS</span></span>

### <span data-ttu-id="12dc5-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="12dc5-114">-CertificateTransparency</span></span>
<span data-ttu-id="12dc5-115">Gibt an, ob die Zertifikat Transparenz für dieses Zertifikat/den Aussteller aktiviert ist. Wenn keine Angabe erfolgt, lautet der Standardwert "wahr".</span><span class="sxs-lookup"><span data-stu-id="12dc5-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'.</span></span>
<span data-ttu-id="12dc5-116">`-IssuerName` muss beim Festlegen dieser Eigenschaft angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="12dc5-116">`-IssuerName` needs to be specified when setting this property.</span></span>

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

### <span data-ttu-id="12dc5-117">-Certificatetype</span><span class="sxs-lookup"><span data-stu-id="12dc5-117">-CertificateType</span></span>
<span data-ttu-id="12dc5-118">Gibt den Typ des Zertifikats an den Aussteller an.</span><span class="sxs-lookup"><span data-stu-id="12dc5-118">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="12dc5-119">-Curve</span><span class="sxs-lookup"><span data-stu-id="12dc5-119">-Curve</span></span>
<span data-ttu-id="12dc5-120">Gibt den Namen der elliptischen Kurve des Schlüssels des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="12dc5-120">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="12dc5-121">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="12dc5-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="12dc5-122">P-256</span><span class="sxs-lookup"><span data-stu-id="12dc5-122">P-256</span></span>
- <span data-ttu-id="12dc5-123">P-384</span><span class="sxs-lookup"><span data-stu-id="12dc5-123">P-384</span></span>
- <span data-ttu-id="12dc5-124">P-521</span><span class="sxs-lookup"><span data-stu-id="12dc5-124">P-521</span></span>
- <span data-ttu-id="12dc5-125">P-256 k</span><span class="sxs-lookup"><span data-stu-id="12dc5-125">P-256K</span></span>
- <span data-ttu-id="12dc5-126">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="12dc5-126">SECP256K1</span></span>

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

### <span data-ttu-id="12dc5-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12dc5-127">-DefaultProfile</span></span>
<span data-ttu-id="12dc5-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="12dc5-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12dc5-129">-Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="12dc5-129">-Disabled</span></span>
<span data-ttu-id="12dc5-130">Gibt an, dass die Zertifikatrichtlinie deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="12dc5-130">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="12dc5-131">-DnsName</span><span class="sxs-lookup"><span data-stu-id="12dc5-131">-DnsName</span></span>
<span data-ttu-id="12dc5-132">Gibt den Namen des Antragstellers des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="12dc5-132">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="12dc5-133">-EKUs</span><span class="sxs-lookup"><span data-stu-id="12dc5-133">-Ekus</span></span>
<span data-ttu-id="12dc5-134">Gibt die erweiterten Schlüsselverwendungen (EKUs) im Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="12dc5-134">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="12dc5-135">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="12dc5-135">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="12dc5-136">Gibt die Anzahl der Tage vor Ablauf an, wenn die automatische Verlängerung beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="12dc5-136">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="12dc5-137">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="12dc5-137">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="12dc5-138">Gibt den Prozentsatz der Lebensdauer an, nach dem der automatische Prozess für die Benachrichtigung beginnt.</span><span class="sxs-lookup"><span data-stu-id="12dc5-138">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="12dc5-139">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="12dc5-139">-InputObject</span></span>
<span data-ttu-id="12dc5-140">Gibt die Zertifikatrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="12dc5-140">Specifies the certificate policy.</span></span>

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

### <span data-ttu-id="12dc5-141">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="12dc5-141">-IssuerName</span></span>
<span data-ttu-id="12dc5-142">Gibt den Namen des Emittenten für dieses Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="12dc5-142">Specifies the name of the issuer for this certificate.</span></span>

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

### <span data-ttu-id="12dc5-143">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="12dc5-143">-KeyNotExportable</span></span>
<span data-ttu-id="12dc5-144">Gibt an, dass der Schlüssel nicht exportierbar ist.</span><span class="sxs-lookup"><span data-stu-id="12dc5-144">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="12dc5-145">-KeySize</span><span class="sxs-lookup"><span data-stu-id="12dc5-145">-KeySize</span></span>
<span data-ttu-id="12dc5-146">Gibt die Schlüsselgröße des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="12dc5-146">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="12dc5-147">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="12dc5-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="12dc5-148">2048</span><span class="sxs-lookup"><span data-stu-id="12dc5-148">2048</span></span>
- <span data-ttu-id="12dc5-149">3072</span><span class="sxs-lookup"><span data-stu-id="12dc5-149">3072</span></span>
- <span data-ttu-id="12dc5-150">4096</span><span class="sxs-lookup"><span data-stu-id="12dc5-150">4096</span></span>
- <span data-ttu-id="12dc5-151">256</span><span class="sxs-lookup"><span data-stu-id="12dc5-151">256</span></span>
- <span data-ttu-id="12dc5-152">384</span><span class="sxs-lookup"><span data-stu-id="12dc5-152">384</span></span>
- <span data-ttu-id="12dc5-153">521</span><span class="sxs-lookup"><span data-stu-id="12dc5-153">521</span></span>

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

### <span data-ttu-id="12dc5-154">-KeyType</span><span class="sxs-lookup"><span data-stu-id="12dc5-154">-KeyType</span></span>
<span data-ttu-id="12dc5-155">Gibt den Schlüsseltyp des Schlüssels an, der das Zertifikat zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="12dc5-155">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="12dc5-156">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="12dc5-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="12dc5-157">RSA</span><span class="sxs-lookup"><span data-stu-id="12dc5-157">RSA</span></span>
- <span data-ttu-id="12dc5-158">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="12dc5-158">RSA-HSM</span></span>
- <span data-ttu-id="12dc5-159">EC des Rates</span><span class="sxs-lookup"><span data-stu-id="12dc5-159">EC</span></span>
- <span data-ttu-id="12dc5-160">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="12dc5-160">EC-HSM</span></span>

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

### <span data-ttu-id="12dc5-161">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="12dc5-161">-KeyUsage</span></span>
<span data-ttu-id="12dc5-162">Gibt die Schlüsselverwendungen im Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="12dc5-162">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="12dc5-163">-Name</span><span class="sxs-lookup"><span data-stu-id="12dc5-163">-Name</span></span>
<span data-ttu-id="12dc5-164">Gibt den Namen des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="12dc5-164">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="12dc5-165">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12dc5-165">-PassThru</span></span>
<span data-ttu-id="12dc5-166">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="12dc5-166">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="12dc5-167">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="12dc5-167">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="12dc5-168">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="12dc5-168">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="12dc5-169">Gibt an, wie viele Tage vor dem Ablaufdatum der automatische Prozess für die Zertifikaterneuerung beginnt.</span><span class="sxs-lookup"><span data-stu-id="12dc5-169">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="12dc5-170">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="12dc5-170">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="12dc5-171">Gibt den Prozentsatz der Lebensdauer an, nach dem der automatische Prozess für die Zertifikaterneuerung beginnt.</span><span class="sxs-lookup"><span data-stu-id="12dc5-171">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="12dc5-172">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="12dc5-172">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="12dc5-173">Gibt an, dass das Zertifikat den Schlüssel während der Erneuerung wieder verwendet.</span><span class="sxs-lookup"><span data-stu-id="12dc5-173">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="12dc5-174">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="12dc5-174">-SecretContentType</span></span>
<span data-ttu-id="12dc5-175">Gibt den Inhaltstyp des neuen Schlüssels Vault Secret an.</span><span class="sxs-lookup"><span data-stu-id="12dc5-175">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="12dc5-176">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="12dc5-176">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="12dc5-177">Anwendung/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="12dc5-177">application/x-pkcs12</span></span>
- <span data-ttu-id="12dc5-178">Application/x-PEM-Datei</span><span class="sxs-lookup"><span data-stu-id="12dc5-178">application/x-pem-file</span></span>

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

### <span data-ttu-id="12dc5-179">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="12dc5-179">-SubjectName</span></span>
<span data-ttu-id="12dc5-180">Gibt den Namen des Antragstellers des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="12dc5-180">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="12dc5-181">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="12dc5-181">-ValidityInMonths</span></span>
<span data-ttu-id="12dc5-182">Gibt an, wie viele Monate das Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="12dc5-182">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="12dc5-183">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="12dc5-183">-VaultName</span></span>
<span data-ttu-id="12dc5-184">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="12dc5-184">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="12dc5-185">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="12dc5-185">-Confirm</span></span>
<span data-ttu-id="12dc5-186">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="12dc5-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12dc5-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12dc5-187">-WhatIf</span></span>
<span data-ttu-id="12dc5-188">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12dc5-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12dc5-189">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="12dc5-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12dc5-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12dc5-190">CommonParameters</span></span>
<span data-ttu-id="12dc5-191">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12dc5-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12dc5-192">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12dc5-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12dc5-193">Eingaben</span><span class="sxs-lookup"><span data-stu-id="12dc5-193">INPUTS</span></span>

### <span data-ttu-id="12dc5-194">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="12dc5-194">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="12dc5-195">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="12dc5-195">OUTPUTS</span></span>

### <span data-ttu-id="12dc5-196">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="12dc5-196">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="12dc5-197">Notizen</span><span class="sxs-lookup"><span data-stu-id="12dc5-197">NOTES</span></span>

## <span data-ttu-id="12dc5-198">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="12dc5-198">RELATED LINKS</span></span>

[<span data-ttu-id="12dc5-199">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="12dc5-199">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="12dc5-200">Neu – AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="12dc5-200">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

