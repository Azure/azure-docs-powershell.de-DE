---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: caa0961c1b7aebd5fd2f9883831d733a0fa69f1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502569"
---
# <span data-ttu-id="485a9-101">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="485a9-101">New-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="485a9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="485a9-102">SYNOPSIS</span></span>
<span data-ttu-id="485a9-103">Erstellt ein Zertifikatrichtlinien Objekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="485a9-103">Creates an in-memory certificate policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="485a9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="485a9-104">SYNTAX</span></span>

### <span data-ttu-id="485a9-105">SubjectName (Standard)</span><span class="sxs-lookup"><span data-stu-id="485a9-105">SubjectName (Default)</span></span>
```
New-AzureKeyVaultCertificatePolicy [-IssuerName] <String> [-SubjectName] <String>
 [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>]
 [-ReuseKeyOnRenewal] [-Disabled] [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="485a9-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="485a9-106">DNSNames</span></span>
```
New-AzureKeyVaultCertificatePolicy [-IssuerName] <String> [[-SubjectName] <String>]
 [-DnsName] <System.Collections.Generic.List`1[System.String]> [-RenewAtNumberOfDaysBeforeExpiry <Int32>]
 [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="485a9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="485a9-107">DESCRIPTION</span></span>
<span data-ttu-id="485a9-108">Das Cmdlet **New-AzureKeyVaultCertificatePolicy** erstellt ein Zertifikatrichtlinien Objekt im Arbeitsspeicher für Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="485a9-108">The **New-AzureKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="485a9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="485a9-109">EXAMPLES</span></span>

### <span data-ttu-id="485a9-110">Beispiel 1: Erstellen einer Zertifikatrichtlinie</span><span class="sxs-lookup"><span data-stu-id="485a9-110">Example 1: Create a certificate policy</span></span>
```
PS C:\>New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
```

<span data-ttu-id="485a9-111">Dieser Befehl erstellt eine Zertifikatrichtlinie, die für sechs Monate gültig ist, und verwendet den Schlüssel zum Verlängern des Zertifikats erneut.</span><span class="sxs-lookup"><span data-stu-id="485a9-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="485a9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="485a9-112">PARAMETERS</span></span>

### <span data-ttu-id="485a9-113">-Certificatetype</span><span class="sxs-lookup"><span data-stu-id="485a9-113">-CertificateType</span></span>
<span data-ttu-id="485a9-114">Gibt den Typ des Zertifikats an den Aussteller an.</span><span class="sxs-lookup"><span data-stu-id="485a9-114">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="485a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="485a9-115">-DefaultProfile</span></span>
<span data-ttu-id="485a9-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="485a9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="485a9-117">-Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="485a9-117">-Disabled</span></span>
<span data-ttu-id="485a9-118">Gibt an, dass die Zertifikatrichtlinie deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="485a9-118">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="485a9-119">-DnsName</span><span class="sxs-lookup"><span data-stu-id="485a9-119">-DnsName</span></span>
<span data-ttu-id="485a9-120">Gibt die DNS-Namen im Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="485a9-120">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="485a9-121">-EKUs</span><span class="sxs-lookup"><span data-stu-id="485a9-121">-Ekus</span></span>
<span data-ttu-id="485a9-122">Gibt die erweiterten Schlüsselverwendungen (EKUs) im Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="485a9-122">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="485a9-123">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="485a9-123">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="485a9-124">Gibt an, wie viele Tage vor Ablauf des automatischen Benachrichtigungsprozesses beginnen.</span><span class="sxs-lookup"><span data-stu-id="485a9-124">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="485a9-125">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="485a9-125">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="485a9-126">Gibt den Prozentsatz der Lebensdauer an, nach dem der automatische Prozess für die Benachrichtigung beginnt.</span><span class="sxs-lookup"><span data-stu-id="485a9-126">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="485a9-127">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="485a9-127">-IssuerName</span></span>
<span data-ttu-id="485a9-128">Gibt den Namen des Emittenten für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="485a9-128">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="485a9-129">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="485a9-129">-KeyNotExportable</span></span>
<span data-ttu-id="485a9-130">Gibt an, dass der Schlüssel nicht exportierbar ist.</span><span class="sxs-lookup"><span data-stu-id="485a9-130">Indicates that the key is not exportable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="485a9-131">-KeyType</span><span class="sxs-lookup"><span data-stu-id="485a9-131">-KeyType</span></span>
<span data-ttu-id="485a9-132">Gibt den Schlüsseltyp des Schlüssels an, der das Zertifikat zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="485a9-132">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="485a9-133">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="485a9-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="485a9-134">RSA</span><span class="sxs-lookup"><span data-stu-id="485a9-134">RSA</span></span>
- <span data-ttu-id="485a9-135">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="485a9-135">RSA-HSM</span></span>

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

### <span data-ttu-id="485a9-136">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="485a9-136">-KeyUsage</span></span>
<span data-ttu-id="485a9-137">Gibt die Schlüsselverwendungen im Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="485a9-137">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="485a9-138">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="485a9-138">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="485a9-139">Gibt an, wie viele Tage vor dem Ablaufdatum der automatische Prozess für die Zertifikaterneuerung beginnt.</span><span class="sxs-lookup"><span data-stu-id="485a9-139">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="485a9-140">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="485a9-140">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="485a9-141">Gibt den Prozentsatz der Lebensdauer an, nach dem der automatische Prozess für die Zertifikaterneuerung beginnt.</span><span class="sxs-lookup"><span data-stu-id="485a9-141">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="485a9-142">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="485a9-142">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="485a9-143">Gibt an, dass das Zertifikat den Schlüssel während der Erneuerung wieder verwendet.</span><span class="sxs-lookup"><span data-stu-id="485a9-143">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="485a9-144">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="485a9-144">-SecretContentType</span></span>
<span data-ttu-id="485a9-145">Gibt den Inhaltstyp des neuen Schlüssels Vault Secret an.</span><span class="sxs-lookup"><span data-stu-id="485a9-145">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="485a9-146">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="485a9-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="485a9-147">Anwendung/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="485a9-147">application/x-pkcs12</span></span>
- <span data-ttu-id="485a9-148">Application/x-PEM-Datei</span><span class="sxs-lookup"><span data-stu-id="485a9-148">application/x-pem-file</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="485a9-149">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="485a9-149">-SubjectName</span></span>
<span data-ttu-id="485a9-150">Gibt den Namen des Antragstellers des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="485a9-150">Specifies the subject name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: SubjectName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DNSNames
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="485a9-151">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="485a9-151">-ValidityInMonths</span></span>
<span data-ttu-id="485a9-152">Gibt an, wie viele Monate das Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="485a9-152">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="485a9-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="485a9-153">-Confirm</span></span>
<span data-ttu-id="485a9-154">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="485a9-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="485a9-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="485a9-155">-WhatIf</span></span>
<span data-ttu-id="485a9-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="485a9-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="485a9-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="485a9-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="485a9-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="485a9-158">CommonParameters</span></span>
<span data-ttu-id="485a9-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="485a9-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="485a9-160">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="485a9-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="485a9-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="485a9-161">INPUTS</span></span>

### <span data-ttu-id="485a9-162">Keine</span><span class="sxs-lookup"><span data-stu-id="485a9-162">None</span></span>
<span data-ttu-id="485a9-163">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="485a9-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="485a9-164">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="485a9-164">OUTPUTS</span></span>

### <span data-ttu-id="485a9-165">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="485a9-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="485a9-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="485a9-166">NOTES</span></span>

## <span data-ttu-id="485a9-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="485a9-167">RELATED LINKS</span></span>

[<span data-ttu-id="485a9-168">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="485a9-168">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="485a9-169">Satz-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="485a9-169">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

