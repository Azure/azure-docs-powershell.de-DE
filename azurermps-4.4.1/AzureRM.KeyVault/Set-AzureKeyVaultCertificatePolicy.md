---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 94f8b6e136925956faf4402b583d80f6a675cca3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504106"
---
# <span data-ttu-id="d70f5-101">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="d70f5-101">Set-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="d70f5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d70f5-102">SYNOPSIS</span></span>
<span data-ttu-id="d70f5-103">Erstellt oder aktualisiert die Richtlinie für ein Zertifikat in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="d70f5-103">Creates or updates the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d70f5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d70f5-104">SYNTAX</span></span>

### <span data-ttu-id="d70f5-105">Erweitert (Standard)</span><span class="sxs-lookup"><span data-stu-id="d70f5-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-SecretContentType <String>]
 [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d70f5-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="d70f5-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [[-CertificatePolicy] <KeyVaultCertificatePolicy>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d70f5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d70f5-107">DESCRIPTION</span></span>
<span data-ttu-id="d70f5-108">Das Cmdlet " **festlegen-AzureKeyVaultCertificatePolicy** " erstellt oder aktualisiert die Richtlinie für ein Zertifikat in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="d70f5-108">The **Set-AzureKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="d70f5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d70f5-109">EXAMPLES</span></span>

### <span data-ttu-id="d70f5-110">Beispiel 1: Festlegen einer Zertifikatrichtlinie</span><span class="sxs-lookup"><span data-stu-id="d70f5-110">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="d70f5-111">Dieser Befehl legt die Richtlinie für das TestCert01-Zertifikat im ContosoKV01-schlüsseltresor fest.</span><span class="sxs-lookup"><span data-stu-id="d70f5-111">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="d70f5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d70f5-112">PARAMETERS</span></span>

### <span data-ttu-id="d70f5-113">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="d70f5-113">-CertificatePolicy</span></span>
<span data-ttu-id="d70f5-114">Gibt die Zertifikatrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="d70f5-114">Specifies the certificate policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d70f5-115">-Certificatetype</span><span class="sxs-lookup"><span data-stu-id="d70f5-115">-CertificateType</span></span>
<span data-ttu-id="d70f5-116">Gibt den Typ des Zertifikats an den Aussteller an.</span><span class="sxs-lookup"><span data-stu-id="d70f5-116">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d70f5-117">-Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="d70f5-117">-Disabled</span></span>
<span data-ttu-id="d70f5-118">Gibt an, dass die Zertifikatrichtlinie deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d70f5-118">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d70f5-119">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="d70f5-119">-DnsNames</span></span>
<span data-ttu-id="d70f5-120">Gibt die DNS-Namen im Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="d70f5-120">Specifies the DNS names in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d70f5-121">-EKUs</span><span class="sxs-lookup"><span data-stu-id="d70f5-121">-Ekus</span></span>
<span data-ttu-id="d70f5-122">Gibt die erweiterten Schlüsselverwendungen (EKUs) im Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="d70f5-122">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d70f5-123">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="d70f5-123">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="d70f5-124">Gibt an, wie viele Tage vor Ablauf des automatischen Benachrichtigungsprozesses beginnen.</span><span class="sxs-lookup"><span data-stu-id="d70f5-124">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="d70f5-125">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="d70f5-125">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="d70f5-126">Gibt den Prozentsatz der Lebensdauer an, nach dem der automatische Prozess für die Benachrichtigung beginnt.</span><span class="sxs-lookup"><span data-stu-id="d70f5-126">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="d70f5-127">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="d70f5-127">-IssuerName</span></span>
<span data-ttu-id="d70f5-128">Gibt den Namen des Emittenten für dieses Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="d70f5-128">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d70f5-129">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="d70f5-129">-KeyNotExportable</span></span>
<span data-ttu-id="d70f5-130">Gibt an, dass der Schlüssel nicht exportierbar ist.</span><span class="sxs-lookup"><span data-stu-id="d70f5-130">Indicates that the key is not exportable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d70f5-131">-KeyType</span><span class="sxs-lookup"><span data-stu-id="d70f5-131">-KeyType</span></span>
<span data-ttu-id="d70f5-132">Gibt den Schlüsseltyp des Schlüssels an, der das Zertifikat zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d70f5-132">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="d70f5-133">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d70f5-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d70f5-134">RSA</span><span class="sxs-lookup"><span data-stu-id="d70f5-134">RSA</span></span>
- <span data-ttu-id="d70f5-135">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="d70f5-135">RSA-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: RSA, RSA-HSM

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d70f5-136">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="d70f5-136">-KeyUsage</span></span>
<span data-ttu-id="d70f5-137">Gibt die Schlüsselverwendungen im Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="d70f5-137">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d70f5-138">-Name</span><span class="sxs-lookup"><span data-stu-id="d70f5-138">-Name</span></span>
<span data-ttu-id="d70f5-139">Gibt den Namen des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="d70f5-139">Specifies the name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d70f5-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d70f5-140">-PassThru</span></span>
<span data-ttu-id="d70f5-141">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="d70f5-141">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d70f5-142">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="d70f5-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d70f5-143">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="d70f5-143">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="d70f5-144">Gibt an, wie viele Tage vor dem Ablaufdatum der automatische Prozess für die Zertifikaterneuerung beginnt.</span><span class="sxs-lookup"><span data-stu-id="d70f5-144">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d70f5-145">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="d70f5-145">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="d70f5-146">Gibt den Prozentsatz der Lebensdauer an, nach dem der automatische Prozess für die Zertifikaterneuerung beginnt.</span><span class="sxs-lookup"><span data-stu-id="d70f5-146">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d70f5-147">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="d70f5-147">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="d70f5-148">Gibt an, dass das Zertifikat den Schlüssel während der Erneuerung wieder verwendet.</span><span class="sxs-lookup"><span data-stu-id="d70f5-148">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d70f5-149">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="d70f5-149">-SecretContentType</span></span>
<span data-ttu-id="d70f5-150">Gibt den Inhaltstyp des neuen Schlüssels Vault Secret an.</span><span class="sxs-lookup"><span data-stu-id="d70f5-150">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="d70f5-151">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d70f5-151">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d70f5-152">Anwendung/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="d70f5-152">application/x-pkcs12</span></span>
- <span data-ttu-id="d70f5-153">Application/x-PEM-Datei</span><span class="sxs-lookup"><span data-stu-id="d70f5-153">application/x-pem-file</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d70f5-154">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="d70f5-154">-SubjectName</span></span>
<span data-ttu-id="d70f5-155">Gibt den Namen des Antragstellers des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="d70f5-155">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d70f5-156">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="d70f5-156">-ValidityInMonths</span></span>
<span data-ttu-id="d70f5-157">Gibt an, wie viele Monate das Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="d70f5-157">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d70f5-158">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="d70f5-158">-VaultName</span></span>
<span data-ttu-id="d70f5-159">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="d70f5-159">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d70f5-160">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d70f5-160">-Confirm</span></span>
<span data-ttu-id="d70f5-161">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d70f5-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d70f5-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d70f5-162">-WhatIf</span></span>
<span data-ttu-id="d70f5-163">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d70f5-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d70f5-164">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d70f5-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d70f5-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d70f5-165">-DefaultProfile</span></span>
<span data-ttu-id="d70f5-166">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d70f5-166">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d70f5-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d70f5-167">CommonParameters</span></span>
<span data-ttu-id="d70f5-168">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d70f5-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d70f5-169">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d70f5-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d70f5-170">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d70f5-170">INPUTS</span></span>

## <span data-ttu-id="d70f5-171">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d70f5-171">OUTPUTS</span></span>

### <span data-ttu-id="d70f5-172">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="d70f5-172">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="d70f5-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="d70f5-173">NOTES</span></span>

## <span data-ttu-id="d70f5-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d70f5-174">RELATED LINKS</span></span>

[<span data-ttu-id="d70f5-175">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="d70f5-175">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="d70f5-176">Neu – AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="d70f5-176">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

