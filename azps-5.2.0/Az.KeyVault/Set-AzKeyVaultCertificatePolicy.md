---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 963a7005e95941a644b35a57f80b558f02e2d6a0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294814"
---
# <span data-ttu-id="4309b-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4309b-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="4309b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4309b-102">SYNOPSIS</span></span>
<span data-ttu-id="4309b-103">Erstellt oder aktualisiert die Richtlinie für ein Zertifikat in einem Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="4309b-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="4309b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4309b-104">SYNTAX</span></span>

### <span data-ttu-id="4309b-105">ExpandedRenewPercentage (Standard)</span><span class="sxs-lookup"><span data-stu-id="4309b-105">ExpandedRenewPercentage (Default)</span></span>
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

### <span data-ttu-id="4309b-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="4309b-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-KeySize <Int32>]
 [-CertificateTransparency <Boolean>] [-PassThru] [-Curve <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4309b-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="4309b-107">ExpandedRenewNumber</span></span>
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

## <span data-ttu-id="4309b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4309b-108">DESCRIPTION</span></span>
<span data-ttu-id="4309b-109">Das **Cmdlet Set-AzKeyVaultCertificatePolicy** erstellt oder aktualisiert die Richtlinie für ein Zertifikat in einem Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="4309b-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="4309b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4309b-110">EXAMPLES</span></span>

### <span data-ttu-id="4309b-111">Beispiel 1: Festlegen einer Zertifikatrichtlinie</span><span class="sxs-lookup"><span data-stu-id="4309b-111">Example 1: Set a certificate policy</span></span>
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

<span data-ttu-id="4309b-112">Mit diesem Befehl wird die Richtlinie für das Zertifikat "TestCert01" im Schlüsseltresor ContosoKV01 bestimmt.</span><span class="sxs-lookup"><span data-stu-id="4309b-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="4309b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4309b-113">PARAMETERS</span></span>

### <span data-ttu-id="4309b-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="4309b-114">-CertificateTransparency</span></span>
<span data-ttu-id="4309b-115">Gibt an, ob für dieses Zertifikat/den Aussteller Zertifikattransparenz aktiviert ist. falls nicht angegeben, ist der Standardwert "true".</span><span class="sxs-lookup"><span data-stu-id="4309b-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'.</span></span>
<span data-ttu-id="4309b-116">`-IssuerName` muss beim Festlegen dieser Eigenschaft angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4309b-116">`-IssuerName` needs to be specified when setting this property.</span></span>

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

### <span data-ttu-id="4309b-117">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="4309b-117">-CertificateType</span></span>
<span data-ttu-id="4309b-118">Gibt den Typ des Zertifikats für den Aussteller an.</span><span class="sxs-lookup"><span data-stu-id="4309b-118">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="4309b-119">-Curve</span><span class="sxs-lookup"><span data-stu-id="4309b-119">-Curve</span></span>
<span data-ttu-id="4309b-120">Gibt den auslassungspunktenden Kurvennamen des Schlüssels des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="4309b-120">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="4309b-121">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="4309b-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4309b-122">P-256</span><span class="sxs-lookup"><span data-stu-id="4309b-122">P-256</span></span>
- <span data-ttu-id="4309b-123">P-384</span><span class="sxs-lookup"><span data-stu-id="4309b-123">P-384</span></span>
- <span data-ttu-id="4309b-124">P-521</span><span class="sxs-lookup"><span data-stu-id="4309b-124">P-521</span></span>
- <span data-ttu-id="4309b-125">P-256K</span><span class="sxs-lookup"><span data-stu-id="4309b-125">P-256K</span></span>
- <span data-ttu-id="4309b-126">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="4309b-126">SECP256K1</span></span>

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

### <span data-ttu-id="4309b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4309b-127">-DefaultProfile</span></span>
<span data-ttu-id="4309b-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4309b-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4309b-129">-Disabled</span><span class="sxs-lookup"><span data-stu-id="4309b-129">-Disabled</span></span>
<span data-ttu-id="4309b-130">Gibt an, dass die Zertifikatrichtlinie deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4309b-130">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="4309b-131">-DnsName</span><span class="sxs-lookup"><span data-stu-id="4309b-131">-DnsName</span></span>
<span data-ttu-id="4309b-132">Gibt den Betreffnamen des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="4309b-132">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="4309b-133">-EKUS</span><span class="sxs-lookup"><span data-stu-id="4309b-133">-Ekus</span></span>
<span data-ttu-id="4309b-134">Gibt die erweiterten Schlüsselverwendungen (ENHANCEDUs) im Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="4309b-134">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="4309b-135">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="4309b-135">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="4309b-136">Gibt die Anzahl von Tagen vor dem Ablauf an, um den Beginn der automatischen Verlängerung zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="4309b-136">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="4309b-137">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="4309b-137">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="4309b-138">Gibt den Prozentsatz der Lebensdauer an, nach dem der automatische Prozess für die Benachrichtigung beginnt.</span><span class="sxs-lookup"><span data-stu-id="4309b-138">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="4309b-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4309b-139">-InputObject</span></span>
<span data-ttu-id="4309b-140">Gibt die Zertifikatrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="4309b-140">Specifies the certificate policy.</span></span>

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

### <span data-ttu-id="4309b-141">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="4309b-141">-IssuerName</span></span>
<span data-ttu-id="4309b-142">Gibt den Namen des Ausstellers für dieses Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="4309b-142">Specifies the name of the issuer for this certificate.</span></span>

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

### <span data-ttu-id="4309b-143">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="4309b-143">-KeyNotExportable</span></span>
<span data-ttu-id="4309b-144">Gibt an, dass der Schlüssel nicht exportiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="4309b-144">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="4309b-145">-KeySize</span><span class="sxs-lookup"><span data-stu-id="4309b-145">-KeySize</span></span>
<span data-ttu-id="4309b-146">Gibt die Schlüsselgröße des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="4309b-146">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="4309b-147">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="4309b-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4309b-148">2048</span><span class="sxs-lookup"><span data-stu-id="4309b-148">2048</span></span>
- <span data-ttu-id="4309b-149">3072</span><span class="sxs-lookup"><span data-stu-id="4309b-149">3072</span></span>
- <span data-ttu-id="4309b-150">4096</span><span class="sxs-lookup"><span data-stu-id="4309b-150">4096</span></span>
- <span data-ttu-id="4309b-151">256</span><span class="sxs-lookup"><span data-stu-id="4309b-151">256</span></span>
- <span data-ttu-id="4309b-152">384</span><span class="sxs-lookup"><span data-stu-id="4309b-152">384</span></span>
- <span data-ttu-id="4309b-153">521</span><span class="sxs-lookup"><span data-stu-id="4309b-153">521</span></span>

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

### <span data-ttu-id="4309b-154">-KeyType</span><span class="sxs-lookup"><span data-stu-id="4309b-154">-KeyType</span></span>
<span data-ttu-id="4309b-155">Gibt den Schlüsseltyp des Schlüssels an, der das Zertifikat zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4309b-155">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="4309b-156">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="4309b-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4309b-157">RSA</span><span class="sxs-lookup"><span data-stu-id="4309b-157">RSA</span></span>
- <span data-ttu-id="4309b-158">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="4309b-158">RSA-HSM</span></span>
- <span data-ttu-id="4309b-159">EC</span><span class="sxs-lookup"><span data-stu-id="4309b-159">EC</span></span>
- <span data-ttu-id="4309b-160">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="4309b-160">EC-HSM</span></span>

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

### <span data-ttu-id="4309b-161">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="4309b-161">-KeyUsage</span></span>
<span data-ttu-id="4309b-162">Gibt die Schlüsselverwendungen im Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="4309b-162">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="4309b-163">-Name</span><span class="sxs-lookup"><span data-stu-id="4309b-163">-Name</span></span>
<span data-ttu-id="4309b-164">Gibt den Namen des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="4309b-164">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="4309b-165">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4309b-165">-PassThru</span></span>
<span data-ttu-id="4309b-166">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="4309b-166">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4309b-167">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="4309b-167">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4309b-168">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="4309b-168">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="4309b-169">Gibt die Anzahl von Tagen vor dem Ablauf an, nach der der automatische Prozess für die Zertifikaterneuerung beginnt.</span><span class="sxs-lookup"><span data-stu-id="4309b-169">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="4309b-170">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="4309b-170">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="4309b-171">Gibt den Prozentsatz der Lebensdauer an, nach dem der automatische Prozess für die Zertifikaterneuerung beginnt.</span><span class="sxs-lookup"><span data-stu-id="4309b-171">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="4309b-172">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="4309b-172">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="4309b-173">Gibt an, dass das Zertifikat den Schlüssel während der Verlängerung wiederverwendet.</span><span class="sxs-lookup"><span data-stu-id="4309b-173">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="4309b-174">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="4309b-174">-SecretContentType</span></span>
<span data-ttu-id="4309b-175">Gibt den Inhaltstyp des neuen Schlüsseltresorschlüssels an.</span><span class="sxs-lookup"><span data-stu-id="4309b-175">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="4309b-176">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="4309b-176">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4309b-177">application/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="4309b-177">application/x-pkcs12</span></span>
- <span data-ttu-id="4309b-178">application/x-pem-file</span><span class="sxs-lookup"><span data-stu-id="4309b-178">application/x-pem-file</span></span>

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

### <span data-ttu-id="4309b-179">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="4309b-179">-SubjectName</span></span>
<span data-ttu-id="4309b-180">Gibt den Betreffnamen des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="4309b-180">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="4309b-181">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="4309b-181">-ValidityInMonths</span></span>
<span data-ttu-id="4309b-182">Gibt die Anzahl der Monate an, für die das Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="4309b-182">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="4309b-183">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4309b-183">-VaultName</span></span>
<span data-ttu-id="4309b-184">Gibt den Namen eines Schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="4309b-184">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="4309b-185">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4309b-185">-Confirm</span></span>
<span data-ttu-id="4309b-186">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4309b-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4309b-187">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4309b-187">-WhatIf</span></span>
<span data-ttu-id="4309b-188">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4309b-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4309b-189">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4309b-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4309b-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4309b-190">CommonParameters</span></span>
<span data-ttu-id="4309b-191">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4309b-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4309b-192">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4309b-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4309b-193">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4309b-193">INPUTS</span></span>

### <span data-ttu-id="4309b-194">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4309b-194">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="4309b-195">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4309b-195">OUTPUTS</span></span>

### <span data-ttu-id="4309b-196">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4309b-196">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="4309b-197">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4309b-197">NOTES</span></span>

## <span data-ttu-id="4309b-198">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4309b-198">RELATED LINKS</span></span>

[<span data-ttu-id="4309b-199">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4309b-199">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="4309b-200">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4309b-200">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

