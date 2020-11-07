---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificate.md
ms.openlocfilehash: 4984ce5dde65be9e715a7e34a10e5671902b53cc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843923"
---
# <span data-ttu-id="321bb-101">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="321bb-101">Add-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="321bb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="321bb-102">SYNOPSIS</span></span>
<span data-ttu-id="321bb-103">Fügt ein Zertifikat zu einem schlüsseltresor hinzu.</span><span class="sxs-lookup"><span data-stu-id="321bb-103">Adds a certificate to a key vault.</span></span>

## <span data-ttu-id="321bb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="321bb-104">SYNTAX</span></span>

```
Add-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [[-CertificatePolicy] <KeyVaultCertificatePolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="321bb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="321bb-105">DESCRIPTION</span></span>
<span data-ttu-id="321bb-106">Mit dem Cmdlet **Add-AzKeyVaultCertificate** wird der Vorgang der Registrierung für ein Zertifikat in einem schlüsseltresor im Azure Key Vault gestartet.</span><span class="sxs-lookup"><span data-stu-id="321bb-106">The **Add-AzKeyVaultCertificate** cmdlet starts the process of enrolling for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="321bb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="321bb-107">EXAMPLES</span></span>

### <span data-ttu-id="321bb-108">Beispiel 1: Hinzufügen eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="321bb-108">Example 1: Add a certificate</span></span>
```
PS C:\>$Policy = New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
PS C:\> Add-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01" -CertificatePolicy $Policy

Status                    : inProgress
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              : PS C:\>Get-AzKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01"
Status                    : completed
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              : PS C:\>Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : testCert01
Certificate : [Subject]
                CN=contoso.com

              [Issuer]
                CN=contoso.com

              [Serial Number]
                05979C5A2F0741D5A3B6F97673E8A118

              [Not Before]
                2/8/2016 3:11:45 PM

              [Not After]
                8/8/2016 4:21:45 PM

              [Thumbprint]
                3E9B6848AD1834284157D68B060F748037F663C8

Thumbprint  : 3E9B6848AD1834284157D68B060F748037F663C8
Tags        :
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

<span data-ttu-id="321bb-109">Der erste Befehl verwendet das New-AzKeyVaultCertificatePolicy-Cmdlet, um eine Zertifikatrichtlinie zu erstellen, und speichert Sie dann in der $Policy-Variablen.</span><span class="sxs-lookup"><span data-stu-id="321bb-109">The first command uses the New-AzKeyVaultCertificatePolicy cmdlet to create a certificate policy, and then stores it in the $Policy variable.</span></span>

<span data-ttu-id="321bb-110">Der zweite Befehl verwendet **Add-AzKeyVaultCertificate** , um den Prozess zum Erstellen eines Zertifikats zu starten.</span><span class="sxs-lookup"><span data-stu-id="321bb-110">The second command uses **Add-AzKeyVaultCertificate** to start the process to create a certificate.</span></span>

<span data-ttu-id="321bb-111">Der dritte Befehl ruft mithilfe des Get-AzKeyVaultCertificateOperation-Cmdlets den Vorgang ab, um zu überprüfen, ob er abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="321bb-111">The third command uses the Get-AzKeyVaultCertificateOperation cmdlet to poll the operation to verify that it's complete.</span></span>

<span data-ttu-id="321bb-112">Der endgültige Befehl verwendet das Get-AzKeyVaultCertificate-Cmdlet zum Abrufen des Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="321bb-112">The final command uses the Get-AzKeyVaultCertificate cmdlet to get the certificate.</span></span>

## <span data-ttu-id="321bb-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="321bb-113">PARAMETERS</span></span>

### <span data-ttu-id="321bb-114">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="321bb-114">-CertificatePolicy</span></span>
<span data-ttu-id="321bb-115">Gibt ein **KeyVaultCertificatePolicy** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="321bb-115">Specifies a **KeyVaultCertificatePolicy** object.</span></span>

```yaml
Type: KeyVaultCertificatePolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="321bb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="321bb-116">-DefaultProfile</span></span>
<span data-ttu-id="321bb-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="321bb-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="321bb-118">-Name</span><span class="sxs-lookup"><span data-stu-id="321bb-118">-Name</span></span>
<span data-ttu-id="321bb-119">Gibt den Namen des Zertifikats an, das hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="321bb-119">Specifies the name of the certificate to add.</span></span>

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

### <span data-ttu-id="321bb-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="321bb-120">-Tag</span></span>
<span data-ttu-id="321bb-121">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="321bb-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="321bb-122">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="321bb-122">For example:</span></span>

<span data-ttu-id="321bb-123">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="321bb-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="321bb-124">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="321bb-124">-VaultName</span></span>
<span data-ttu-id="321bb-125">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="321bb-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="321bb-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="321bb-126">-Confirm</span></span>
<span data-ttu-id="321bb-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="321bb-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="321bb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="321bb-128">-WhatIf</span></span>
<span data-ttu-id="321bb-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="321bb-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="321bb-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="321bb-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="321bb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="321bb-131">CommonParameters</span></span>
<span data-ttu-id="321bb-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="321bb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="321bb-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="321bb-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="321bb-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="321bb-134">INPUTS</span></span>

### <span data-ttu-id="321bb-135">Keine</span><span class="sxs-lookup"><span data-stu-id="321bb-135">None</span></span>
<span data-ttu-id="321bb-136">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="321bb-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="321bb-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="321bb-137">OUTPUTS</span></span>

### <span data-ttu-id="321bb-138">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="321bb-138">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="321bb-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="321bb-139">NOTES</span></span>

## <span data-ttu-id="321bb-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="321bb-140">RELATED LINKS</span></span>

[<span data-ttu-id="321bb-141">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="321bb-141">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)

[<span data-ttu-id="321bb-142">Importieren-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="321bb-142">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="321bb-143">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="321bb-143">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)
