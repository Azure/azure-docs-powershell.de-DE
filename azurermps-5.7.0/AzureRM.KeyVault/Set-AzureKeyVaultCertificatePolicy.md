---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: e960aa211b53c79087e67e2bd86504e597a718d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504546"
---
# <span data-ttu-id="7c25e-101">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="7c25e-101">Set-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="7c25e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7c25e-102">SYNOPSIS</span></span>
<span data-ttu-id="7c25e-103">Erstellt oder aktualisiert die Richtlinie für ein Zertifikat in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="7c25e-103">Creates or updates the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c25e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c25e-104">SYNTAX</span></span>

### <span data-ttu-id="7c25e-105">ExpandedRenewPercentage (Standard)</span><span class="sxs-lookup"><span data-stu-id="7c25e-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c25e-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="7c25e-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c25e-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="7c25e-107">ExpandedRenewNumber</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 -RenewAtNumberOfDaysBeforeExpiry <Int32> [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>]
 [-Disabled] [-SubjectName <String>] [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c25e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7c25e-108">DESCRIPTION</span></span>
<span data-ttu-id="7c25e-109">Das Cmdlet " **festlegen-AzureKeyVaultCertificatePolicy** " erstellt oder aktualisiert die Richtlinie für ein Zertifikat in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="7c25e-109">The **Set-AzureKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="7c25e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7c25e-110">EXAMPLES</span></span>

### <span data-ttu-id="7c25e-111">Beispiel 1: Festlegen einer Zertifikatrichtlinie</span><span class="sxs-lookup"><span data-stu-id="7c25e-111">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="7c25e-112">Dieser Befehl legt die Richtlinie für das TestCert01-Zertifikat im ContosoKV01-schlüsseltresor fest.</span><span class="sxs-lookup"><span data-stu-id="7c25e-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="7c25e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c25e-113">PARAMETERS</span></span>

### <span data-ttu-id="7c25e-114">-Certificatetype</span><span class="sxs-lookup"><span data-stu-id="7c25e-114">-CertificateType</span></span>
<span data-ttu-id="7c25e-115">Gibt den Typ des Zertifikats an den Aussteller an.</span><span class="sxs-lookup"><span data-stu-id="7c25e-115">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c25e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c25e-116">-DefaultProfile</span></span>
<span data-ttu-id="7c25e-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7c25e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c25e-118">-Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="7c25e-118">-Disabled</span></span>
<span data-ttu-id="7c25e-119">Gibt an, dass die Zertifikatrichtlinie deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7c25e-119">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c25e-120">-DnsName</span><span class="sxs-lookup"><span data-stu-id="7c25e-120">-DnsName</span></span>
<span data-ttu-id="7c25e-121">Gibt den Namen des Antragstellers des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="7c25e-121">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases: DnsNames

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c25e-122">-EKUs</span><span class="sxs-lookup"><span data-stu-id="7c25e-122">-Ekus</span></span>
<span data-ttu-id="7c25e-123">Gibt die erweiterten Schlüsselverwendungen (EKUs) im Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="7c25e-123">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c25e-124">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="7c25e-124">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="7c25e-125">Gibt die Anzahl der Tage vor Ablauf an, wenn die automatische Verlängerung beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="7c25e-125">Specifies the number of days before expiration when automatic renewal should start.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c25e-126">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="7c25e-126">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="7c25e-127">Gibt den Prozentsatz der Lebensdauer an, nach dem der automatische Prozess für die Benachrichtigung beginnt.</span><span class="sxs-lookup"><span data-stu-id="7c25e-127">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c25e-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7c25e-128">-InputObject</span></span>
<span data-ttu-id="7c25e-129">Gibt die Zertifikatrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="7c25e-129">Specifies the certificate policy.</span></span>

```yaml
Type: PSKeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: CertificatePolicy

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c25e-130">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="7c25e-130">-IssuerName</span></span>
<span data-ttu-id="7c25e-131">Gibt den Namen des Emittenten für dieses Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="7c25e-131">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c25e-132">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="7c25e-132">-KeyNotExportable</span></span>
<span data-ttu-id="7c25e-133">Gibt an, dass der Schlüssel nicht exportierbar ist.</span><span class="sxs-lookup"><span data-stu-id="7c25e-133">Indicates that the key is not exportable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c25e-134">-KeyType</span><span class="sxs-lookup"><span data-stu-id="7c25e-134">-KeyType</span></span>
<span data-ttu-id="7c25e-135">Gibt den Schlüsseltyp des Schlüssels an, der das Zertifikat zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="7c25e-135">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="7c25e-136">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7c25e-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7c25e-137">RSA</span><span class="sxs-lookup"><span data-stu-id="7c25e-137">RSA</span></span>
- <span data-ttu-id="7c25e-138">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="7c25e-138">RSA-HSM</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c25e-139">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="7c25e-139">-KeyUsage</span></span>
<span data-ttu-id="7c25e-140">Gibt die Schlüsselverwendungen im Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="7c25e-140">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c25e-141">-Name</span><span class="sxs-lookup"><span data-stu-id="7c25e-141">-Name</span></span>
<span data-ttu-id="7c25e-142">Gibt den Namen des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="7c25e-142">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="7c25e-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c25e-143">-PassThru</span></span>
<span data-ttu-id="7c25e-144">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="7c25e-144">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7c25e-145">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="7c25e-145">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c25e-146">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="7c25e-146">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="7c25e-147">Gibt an, wie viele Tage vor dem Ablaufdatum der automatische Prozess für die Zertifikaterneuerung beginnt.</span><span class="sxs-lookup"><span data-stu-id="7c25e-147">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: ExpandedRenewNumber
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c25e-148">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="7c25e-148">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="7c25e-149">Gibt den Prozentsatz der Lebensdauer an, nach dem der automatische Prozess für die Zertifikaterneuerung beginnt.</span><span class="sxs-lookup"><span data-stu-id="7c25e-149">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: ExpandedRenewPercentage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c25e-150">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="7c25e-150">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="7c25e-151">Gibt an, dass das Zertifikat den Schlüssel während der Erneuerung wieder verwendet.</span><span class="sxs-lookup"><span data-stu-id="7c25e-151">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: Boolean
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c25e-152">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="7c25e-152">-SecretContentType</span></span>
<span data-ttu-id="7c25e-153">Gibt den Inhaltstyp des neuen Schlüssels Vault Secret an.</span><span class="sxs-lookup"><span data-stu-id="7c25e-153">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="7c25e-154">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7c25e-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7c25e-155">Anwendung/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="7c25e-155">application/x-pkcs12</span></span>
- <span data-ttu-id="7c25e-156">Application/x-PEM-Datei</span><span class="sxs-lookup"><span data-stu-id="7c25e-156">application/x-pem-file</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c25e-157">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="7c25e-157">-SubjectName</span></span>
<span data-ttu-id="7c25e-158">Gibt den Namen des Antragstellers des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="7c25e-158">Specifies the subject name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c25e-159">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="7c25e-159">-ValidityInMonths</span></span>
<span data-ttu-id="7c25e-160">Gibt an, wie viele Monate das Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="7c25e-160">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: Int32
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c25e-161">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="7c25e-161">-VaultName</span></span>
<span data-ttu-id="7c25e-162">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="7c25e-162">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="7c25e-163">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7c25e-163">-Confirm</span></span>
<span data-ttu-id="7c25e-164">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7c25e-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c25e-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c25e-165">-WhatIf</span></span>
<span data-ttu-id="7c25e-166">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c25e-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c25e-167">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7c25e-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c25e-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c25e-168">CommonParameters</span></span>
<span data-ttu-id="7c25e-169">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c25e-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c25e-170">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c25e-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c25e-171">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7c25e-171">INPUTS</span></span>

### <span data-ttu-id="7c25e-172">Keine</span><span class="sxs-lookup"><span data-stu-id="7c25e-172">None</span></span>
<span data-ttu-id="7c25e-173">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="7c25e-173">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7c25e-174">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7c25e-174">OUTPUTS</span></span>

### <span data-ttu-id="7c25e-175">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="7c25e-175">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="7c25e-176">Notizen</span><span class="sxs-lookup"><span data-stu-id="7c25e-176">NOTES</span></span>

## <span data-ttu-id="7c25e-177">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7c25e-177">RELATED LINKS</span></span>

[<span data-ttu-id="7c25e-178">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="7c25e-178">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="7c25e-179">Neu – AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="7c25e-179">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

