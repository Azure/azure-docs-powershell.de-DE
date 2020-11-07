---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/new-AzKeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 83eea8c8a030c5d22368bc0ede42c71e92df14a2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842128"
---
# <span data-ttu-id="67364-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="67364-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="67364-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="67364-102">SYNOPSIS</span></span>
<span data-ttu-id="67364-103">Erstellt ein Zertifikatrichtlinien Objekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="67364-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="67364-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="67364-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificatePolicy [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-SubjectName <String>] [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] -IssuerName <String>
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67364-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="67364-105">DESCRIPTION</span></span>
<span data-ttu-id="67364-106">Das Cmdlet **New-AzKeyVaultCertificatePolicy** erstellt ein Zertifikatrichtlinien Objekt im Arbeitsspeicher für Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="67364-106">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="67364-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="67364-107">EXAMPLES</span></span>

### <span data-ttu-id="67364-108">Beispiel 1: Erstellen einer Zertifikatrichtlinie</span><span class="sxs-lookup"><span data-stu-id="67364-108">Example 1: Create a certificate policy</span></span>
```
PS C:\>New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
```

<span data-ttu-id="67364-109">Dieser Befehl erstellt eine Zertifikatrichtlinie, die für sechs Monate gültig ist, und verwendet den Schlüssel zum Verlängern des Zertifikats erneut.</span><span class="sxs-lookup"><span data-stu-id="67364-109">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="67364-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="67364-110">PARAMETERS</span></span>

### <span data-ttu-id="67364-111">-Certificatetype</span><span class="sxs-lookup"><span data-stu-id="67364-111">-CertificateType</span></span>
<span data-ttu-id="67364-112">Gibt den Typ des Zertifikats an den Aussteller an.</span><span class="sxs-lookup"><span data-stu-id="67364-112">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="67364-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67364-113">-DefaultProfile</span></span>
<span data-ttu-id="67364-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="67364-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67364-115">-Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="67364-115">-Disabled</span></span>
<span data-ttu-id="67364-116">Gibt an, dass die Zertifikatrichtlinie deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="67364-116">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="67364-117">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="67364-117">-DnsNames</span></span>
<span data-ttu-id="67364-118">Gibt die DNS-Namen im Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="67364-118">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="67364-119">-EKUs</span><span class="sxs-lookup"><span data-stu-id="67364-119">-Ekus</span></span>
<span data-ttu-id="67364-120">Gibt die erweiterten Schlüsselverwendungen (EKUs) im Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="67364-120">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="67364-121">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="67364-121">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="67364-122">Gibt an, wie viele Tage vor Ablauf des automatischen Benachrichtigungsprozesses beginnen.</span><span class="sxs-lookup"><span data-stu-id="67364-122">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="67364-123">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="67364-123">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="67364-124">Gibt den Prozentsatz der Lebensdauer an, nach dem der automatische Prozess für die Benachrichtigung beginnt.</span><span class="sxs-lookup"><span data-stu-id="67364-124">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="67364-125">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="67364-125">-IssuerName</span></span>
<span data-ttu-id="67364-126">Gibt den Namen des Emittenten für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="67364-126">Specifies the name of the issuer for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67364-127">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="67364-127">-KeyNotExportable</span></span>
<span data-ttu-id="67364-128">Gibt an, dass der Schlüssel nicht exportierbar ist.</span><span class="sxs-lookup"><span data-stu-id="67364-128">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="67364-129">-KeyType</span><span class="sxs-lookup"><span data-stu-id="67364-129">-KeyType</span></span>
<span data-ttu-id="67364-130">Gibt den Schlüsseltyp des Schlüssels an, der das Zertifikat zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="67364-130">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="67364-131">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="67364-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="67364-132">RSA</span><span class="sxs-lookup"><span data-stu-id="67364-132">RSA</span></span>
- <span data-ttu-id="67364-133">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="67364-133">RSA-HSM</span></span>

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

### <span data-ttu-id="67364-134">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="67364-134">-KeyUsage</span></span>
<span data-ttu-id="67364-135">Gibt die Schlüsselverwendungen im Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="67364-135">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="67364-136">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="67364-136">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="67364-137">Gibt an, wie viele Tage vor dem Ablaufdatum der automatische Prozess für die Zertifikaterneuerung beginnt.</span><span class="sxs-lookup"><span data-stu-id="67364-137">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="67364-138">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="67364-138">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="67364-139">Gibt den Prozentsatz der Lebensdauer an, nach dem der automatische Prozess für die Zertifikaterneuerung beginnt.</span><span class="sxs-lookup"><span data-stu-id="67364-139">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="67364-140">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="67364-140">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="67364-141">Gibt an, dass das Zertifikat den Schlüssel während der Erneuerung wieder verwendet.</span><span class="sxs-lookup"><span data-stu-id="67364-141">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="67364-142">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="67364-142">-SecretContentType</span></span>
<span data-ttu-id="67364-143">Gibt den Inhaltstyp des neuen Schlüssels Vault Secret an.</span><span class="sxs-lookup"><span data-stu-id="67364-143">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="67364-144">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="67364-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="67364-145">Anwendung/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="67364-145">application/x-pkcs12</span></span>
- <span data-ttu-id="67364-146">Application/x-PEM-Datei</span><span class="sxs-lookup"><span data-stu-id="67364-146">application/x-pem-file</span></span>

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

### <span data-ttu-id="67364-147">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="67364-147">-SubjectName</span></span>
<span data-ttu-id="67364-148">Gibt den Namen des Antragstellers des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="67364-148">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="67364-149">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="67364-149">-ValidityInMonths</span></span>
<span data-ttu-id="67364-150">Gibt an, wie viele Monate das Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="67364-150">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="67364-151">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="67364-151">-Confirm</span></span>
<span data-ttu-id="67364-152">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="67364-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67364-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67364-153">-WhatIf</span></span>
<span data-ttu-id="67364-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="67364-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67364-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="67364-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67364-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67364-156">CommonParameters</span></span>
<span data-ttu-id="67364-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67364-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67364-158">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67364-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67364-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="67364-159">INPUTS</span></span>

### <span data-ttu-id="67364-160">Keine</span><span class="sxs-lookup"><span data-stu-id="67364-160">None</span></span>
<span data-ttu-id="67364-161">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="67364-161">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="67364-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="67364-162">OUTPUTS</span></span>

### <span data-ttu-id="67364-163">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="67364-163">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="67364-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="67364-164">NOTES</span></span>

## <span data-ttu-id="67364-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="67364-165">RELATED LINKS</span></span>

[<span data-ttu-id="67364-166">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="67364-166">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="67364-167">Satz-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="67364-167">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

