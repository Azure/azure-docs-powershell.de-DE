---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: eec95cd9c7873d26f88390c5a623a6af40991dfd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819539"
---
# <span data-ttu-id="d19b2-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="d19b2-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="d19b2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d19b2-102">SYNOPSIS</span></span>
<span data-ttu-id="d19b2-103">Erstellt oder aktualisiert die Richtlinie für ein Zertifikat in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="d19b2-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="d19b2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d19b2-104">SYNTAX</span></span>

### <span data-ttu-id="d19b2-105">ExpandedRenewPercentage (Standard)</span><span class="sxs-lookup"><span data-stu-id="d19b2-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d19b2-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="d19b2-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d19b2-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="d19b2-107">ExpandedRenewNumber</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> -RenewAtNumberOfDaysBeforeExpiry <Int32>
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d19b2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d19b2-108">DESCRIPTION</span></span>
<span data-ttu-id="d19b2-109">Das Cmdlet " **festlegen-AzKeyVaultCertificatePolicy** " erstellt oder aktualisiert die Richtlinie für ein Zertifikat in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="d19b2-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="d19b2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d19b2-110">EXAMPLES</span></span>

### <span data-ttu-id="d19b2-111">Beispiel 1: Festlegen einer Zertifikatrichtlinie</span><span class="sxs-lookup"><span data-stu-id="d19b2-111">Example 1: Set a certificate policy</span></span>
```powershell
PS C:\> Set-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True -PassThru

SecretContentType               : application/x-pkcs12
Kty                             :
KeySize                         : 2048
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

<span data-ttu-id="d19b2-112">Dieser Befehl legt die Richtlinie für das TestCert01-Zertifikat im ContosoKV01-schlüsseltresor fest.</span><span class="sxs-lookup"><span data-stu-id="d19b2-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="d19b2-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d19b2-113">PARAMETERS</span></span>

### <span data-ttu-id="d19b2-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="d19b2-114">-CertificateTransparency</span></span>
<span data-ttu-id="d19b2-115">Gibt an, ob die Zertifikat Transparenz für dieses Zertifikat/den Aussteller aktiviert ist. Wenn keine Angabe erfolgt, lautet der Standardwert "wahr".</span><span class="sxs-lookup"><span data-stu-id="d19b2-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="d19b2-116">-Certificatetype</span><span class="sxs-lookup"><span data-stu-id="d19b2-116">-CertificateType</span></span>
<span data-ttu-id="d19b2-117">Gibt den Typ des Zertifikats an den Aussteller an.</span><span class="sxs-lookup"><span data-stu-id="d19b2-117">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="d19b2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d19b2-118">-DefaultProfile</span></span>
<span data-ttu-id="d19b2-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d19b2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d19b2-120">-Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="d19b2-120">-Disabled</span></span>
<span data-ttu-id="d19b2-121">Gibt an, dass die Zertifikatrichtlinie deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d19b2-121">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="d19b2-122">-DnsName</span><span class="sxs-lookup"><span data-stu-id="d19b2-122">-DnsName</span></span>
<span data-ttu-id="d19b2-123">Gibt den Namen des Antragstellers des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="d19b2-123">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="d19b2-124">-EKUs</span><span class="sxs-lookup"><span data-stu-id="d19b2-124">-Ekus</span></span>
<span data-ttu-id="d19b2-125">Gibt die erweiterten Schlüsselverwendungen (EKUs) im Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="d19b2-125">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="d19b2-126">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="d19b2-126">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="d19b2-127">Gibt die Anzahl der Tage vor Ablauf an, wenn die automatische Verlängerung beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="d19b2-127">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="d19b2-128">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="d19b2-128">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="d19b2-129">Gibt den Prozentsatz der Lebensdauer an, nach dem der automatische Prozess für die Benachrichtigung beginnt.</span><span class="sxs-lookup"><span data-stu-id="d19b2-129">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="d19b2-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d19b2-130">-InputObject</span></span>
<span data-ttu-id="d19b2-131">Gibt die Zertifikatrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="d19b2-131">Specifies the certificate policy.</span></span>

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

### <span data-ttu-id="d19b2-132">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="d19b2-132">-IssuerName</span></span>
<span data-ttu-id="d19b2-133">Gibt den Namen des Emittenten für dieses Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="d19b2-133">Specifies the name of the issuer for this certificate.</span></span>

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

### <span data-ttu-id="d19b2-134">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="d19b2-134">-KeyNotExportable</span></span>
<span data-ttu-id="d19b2-135">Gibt an, dass der Schlüssel nicht exportierbar ist.</span><span class="sxs-lookup"><span data-stu-id="d19b2-135">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="d19b2-136">-KeyType</span><span class="sxs-lookup"><span data-stu-id="d19b2-136">-KeyType</span></span>
<span data-ttu-id="d19b2-137">Gibt den Schlüsseltyp des Schlüssels an, der das Zertifikat zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d19b2-137">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="d19b2-138">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d19b2-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d19b2-139">RSA</span><span class="sxs-lookup"><span data-stu-id="d19b2-139">RSA</span></span>
- <span data-ttu-id="d19b2-140">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="d19b2-140">RSA-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d19b2-141">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="d19b2-141">-KeyUsage</span></span>
<span data-ttu-id="d19b2-142">Gibt die Schlüsselverwendungen im Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="d19b2-142">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="d19b2-143">-Name</span><span class="sxs-lookup"><span data-stu-id="d19b2-143">-Name</span></span>
<span data-ttu-id="d19b2-144">Gibt den Namen des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="d19b2-144">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="d19b2-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d19b2-145">-PassThru</span></span>
<span data-ttu-id="d19b2-146">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="d19b2-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d19b2-147">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="d19b2-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d19b2-148">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="d19b2-148">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="d19b2-149">Gibt an, wie viele Tage vor dem Ablaufdatum der automatische Prozess für die Zertifikaterneuerung beginnt.</span><span class="sxs-lookup"><span data-stu-id="d19b2-149">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="d19b2-150">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="d19b2-150">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="d19b2-151">Gibt den Prozentsatz der Lebensdauer an, nach dem der automatische Prozess für die Zertifikaterneuerung beginnt.</span><span class="sxs-lookup"><span data-stu-id="d19b2-151">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="d19b2-152">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="d19b2-152">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="d19b2-153">Gibt an, dass das Zertifikat den Schlüssel während der Erneuerung wieder verwendet.</span><span class="sxs-lookup"><span data-stu-id="d19b2-153">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="d19b2-154">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="d19b2-154">-SecretContentType</span></span>
<span data-ttu-id="d19b2-155">Gibt den Inhaltstyp des neuen Schlüssels Vault Secret an.</span><span class="sxs-lookup"><span data-stu-id="d19b2-155">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="d19b2-156">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d19b2-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d19b2-157">Anwendung/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="d19b2-157">application/x-pkcs12</span></span>
- <span data-ttu-id="d19b2-158">Application/x-PEM-Datei</span><span class="sxs-lookup"><span data-stu-id="d19b2-158">application/x-pem-file</span></span>

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

### <span data-ttu-id="d19b2-159">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="d19b2-159">-SubjectName</span></span>
<span data-ttu-id="d19b2-160">Gibt den Namen des Antragstellers des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="d19b2-160">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="d19b2-161">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="d19b2-161">-ValidityInMonths</span></span>
<span data-ttu-id="d19b2-162">Gibt an, wie viele Monate das Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="d19b2-162">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="d19b2-163">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="d19b2-163">-VaultName</span></span>
<span data-ttu-id="d19b2-164">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="d19b2-164">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="d19b2-165">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d19b2-165">-Confirm</span></span>
<span data-ttu-id="d19b2-166">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d19b2-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d19b2-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d19b2-167">-WhatIf</span></span>
<span data-ttu-id="d19b2-168">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d19b2-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d19b2-169">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d19b2-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d19b2-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d19b2-170">CommonParameters</span></span>
<span data-ttu-id="d19b2-171">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d19b2-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d19b2-172">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d19b2-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d19b2-173">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d19b2-173">INPUTS</span></span>

### <span data-ttu-id="d19b2-174">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="d19b2-174">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="d19b2-175">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d19b2-175">OUTPUTS</span></span>

### <span data-ttu-id="d19b2-176">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="d19b2-176">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="d19b2-177">Notizen</span><span class="sxs-lookup"><span data-stu-id="d19b2-177">NOTES</span></span>

## <span data-ttu-id="d19b2-178">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d19b2-178">RELATED LINKS</span></span>

[<span data-ttu-id="d19b2-179">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="d19b2-179">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="d19b2-180">Neu – AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="d19b2-180">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

