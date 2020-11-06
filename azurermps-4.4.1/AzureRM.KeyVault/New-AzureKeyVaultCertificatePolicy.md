---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 381ce302a8404c0bb643db0fc82e392fe53d956a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479181"
---
# <span data-ttu-id="9db8a-101">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9db8a-101">New-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="9db8a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9db8a-102">SYNOPSIS</span></span>
<span data-ttu-id="9db8a-103">Erstellt ein Zertifikatrichtlinien Objekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="9db8a-103">Creates an in-memory certificate policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9db8a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9db8a-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificatePolicy [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-SubjectName <String>] [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] -IssuerName <String>
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9db8a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9db8a-105">DESCRIPTION</span></span>
<span data-ttu-id="9db8a-106">Das Cmdlet **New-AzureKeyVaultCertificatePolicy** erstellt ein Zertifikatrichtlinien Objekt im Arbeitsspeicher für Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="9db8a-106">The **New-AzureKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="9db8a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9db8a-107">EXAMPLES</span></span>

### <span data-ttu-id="9db8a-108">Beispiel 1: Erstellen einer Zertifikatrichtlinie</span><span class="sxs-lookup"><span data-stu-id="9db8a-108">Example 1: Create a certificate policy</span></span>
```
PS C:\>New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
```

<span data-ttu-id="9db8a-109">Dieser Befehl erstellt eine Zertifikatrichtlinie, die für sechs Monate gültig ist, und verwendet den Schlüssel zum Verlängern des Zertifikats erneut.</span><span class="sxs-lookup"><span data-stu-id="9db8a-109">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="9db8a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9db8a-110">PARAMETERS</span></span>

### <span data-ttu-id="9db8a-111">-Certificatetype</span><span class="sxs-lookup"><span data-stu-id="9db8a-111">-CertificateType</span></span>
<span data-ttu-id="9db8a-112">Gibt den Typ des Zertifikats an den Aussteller an.</span><span class="sxs-lookup"><span data-stu-id="9db8a-112">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="9db8a-113">-Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="9db8a-113">-Disabled</span></span>
<span data-ttu-id="9db8a-114">Gibt an, dass die Zertifikatrichtlinie deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9db8a-114">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="9db8a-115">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="9db8a-115">-DnsNames</span></span>
<span data-ttu-id="9db8a-116">Gibt die DNS-Namen im Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="9db8a-116">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="9db8a-117">-EKUs</span><span class="sxs-lookup"><span data-stu-id="9db8a-117">-Ekus</span></span>
<span data-ttu-id="9db8a-118">Gibt die erweiterten Schlüsselverwendungen (EKUs) im Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="9db8a-118">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="9db8a-119">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="9db8a-119">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="9db8a-120">Gibt an, wie viele Tage vor Ablauf des automatischen Benachrichtigungsprozesses beginnen.</span><span class="sxs-lookup"><span data-stu-id="9db8a-120">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="9db8a-121">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="9db8a-121">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="9db8a-122">Gibt den Prozentsatz der Lebensdauer an, nach dem der automatische Prozess für die Benachrichtigung beginnt.</span><span class="sxs-lookup"><span data-stu-id="9db8a-122">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="9db8a-123">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="9db8a-123">-IssuerName</span></span>
<span data-ttu-id="9db8a-124">Gibt den Namen des Emittenten für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="9db8a-124">Specifies the name of the issuer for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9db8a-125">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="9db8a-125">-KeyNotExportable</span></span>
<span data-ttu-id="9db8a-126">Gibt an, dass der Schlüssel nicht exportierbar ist.</span><span class="sxs-lookup"><span data-stu-id="9db8a-126">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="9db8a-127">-KeyType</span><span class="sxs-lookup"><span data-stu-id="9db8a-127">-KeyType</span></span>
<span data-ttu-id="9db8a-128">Gibt den Schlüsseltyp des Schlüssels an, der das Zertifikat zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="9db8a-128">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="9db8a-129">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9db8a-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9db8a-130">RSA</span><span class="sxs-lookup"><span data-stu-id="9db8a-130">RSA</span></span>
- <span data-ttu-id="9db8a-131">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="9db8a-131">RSA-HSM</span></span>

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

### <span data-ttu-id="9db8a-132">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="9db8a-132">-KeyUsage</span></span>
<span data-ttu-id="9db8a-133">Gibt die Schlüsselverwendungen im Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="9db8a-133">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="9db8a-134">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="9db8a-134">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="9db8a-135">Gibt an, wie viele Tage vor dem Ablaufdatum der automatische Prozess für die Zertifikaterneuerung beginnt.</span><span class="sxs-lookup"><span data-stu-id="9db8a-135">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="9db8a-136">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="9db8a-136">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="9db8a-137">Gibt den Prozentsatz der Lebensdauer an, nach dem der automatische Prozess für die Zertifikaterneuerung beginnt.</span><span class="sxs-lookup"><span data-stu-id="9db8a-137">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="9db8a-138">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="9db8a-138">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="9db8a-139">Gibt an, dass das Zertifikat den Schlüssel während der Erneuerung wieder verwendet.</span><span class="sxs-lookup"><span data-stu-id="9db8a-139">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="9db8a-140">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="9db8a-140">-SecretContentType</span></span>
<span data-ttu-id="9db8a-141">Gibt den Inhaltstyp des neuen Schlüssels Vault Secret an.</span><span class="sxs-lookup"><span data-stu-id="9db8a-141">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="9db8a-142">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9db8a-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9db8a-143">Anwendung/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="9db8a-143">application/x-pkcs12</span></span>
- <span data-ttu-id="9db8a-144">Application/x-PEM-Datei</span><span class="sxs-lookup"><span data-stu-id="9db8a-144">application/x-pem-file</span></span>

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

### <span data-ttu-id="9db8a-145">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="9db8a-145">-SubjectName</span></span>
<span data-ttu-id="9db8a-146">Gibt den Namen des Antragstellers des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="9db8a-146">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="9db8a-147">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="9db8a-147">-ValidityInMonths</span></span>
<span data-ttu-id="9db8a-148">Gibt an, wie viele Monate das Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="9db8a-148">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="9db8a-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9db8a-149">-Confirm</span></span>
<span data-ttu-id="9db8a-150">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9db8a-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9db8a-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9db8a-151">-WhatIf</span></span>
<span data-ttu-id="9db8a-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9db8a-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9db8a-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9db8a-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9db8a-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9db8a-154">-DefaultProfile</span></span>
<span data-ttu-id="9db8a-155">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9db8a-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9db8a-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9db8a-156">CommonParameters</span></span>
<span data-ttu-id="9db8a-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9db8a-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9db8a-158">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9db8a-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9db8a-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9db8a-159">INPUTS</span></span>

## <span data-ttu-id="9db8a-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9db8a-160">OUTPUTS</span></span>

### <span data-ttu-id="9db8a-161">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9db8a-161">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="9db8a-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="9db8a-162">NOTES</span></span>

## <span data-ttu-id="9db8a-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9db8a-163">RELATED LINKS</span></span>

[<span data-ttu-id="9db8a-164">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9db8a-164">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="9db8a-165">Satz-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9db8a-165">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

