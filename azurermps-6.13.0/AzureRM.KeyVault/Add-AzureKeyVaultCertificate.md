---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 89299823-3382-402D-9458-519466748051
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificate.md
ms.openlocfilehash: dd51ca4bc6d238d2aac1e4dccea4ad3a89bc8d35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503638"
---
# <span data-ttu-id="3f323-101">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3f323-101">Add-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="3f323-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3f323-102">SYNOPSIS</span></span>
<span data-ttu-id="3f323-103">Fügt ein Zertifikat zu einem schlüsseltresor hinzu.</span><span class="sxs-lookup"><span data-stu-id="3f323-103">Adds a certificate to a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f323-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f323-104">SYNTAX</span></span>

```
Add-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificatePolicy] <PSKeyVaultCertificatePolicy> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f323-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3f323-105">DESCRIPTION</span></span>
<span data-ttu-id="3f323-106">Mit dem Cmdlet **Add-AzureKeyVaultCertificate** wird der Vorgang der Registrierung für ein Zertifikat in einem schlüsseltresor im Azure Key Vault gestartet.</span><span class="sxs-lookup"><span data-stu-id="3f323-106">The **Add-AzureKeyVaultCertificate** cmdlet starts the process of enrolling for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="3f323-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3f323-107">EXAMPLES</span></span>

### <span data-ttu-id="3f323-108">Beispiel 1: Hinzufügen eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="3f323-108">Example 1: Add a certificate</span></span>
```powershell
PS C:\> $Policy = New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
PS C:\> Add-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01" -CertificatePolicy $Policy

Status                    : inProgress
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              : 

PS C:\> Get-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01"
Status                    : completed
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              : 

PS C:\> Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"

Name        : testCert01
Certificate : [Subject]
                CN=contoso.com

              [Issuer]
                CN=contoso.com

              [Serial Number]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before]
                2/8/2016 3:11:45 PM

              [Not After]
                8/8/2016 4:21:45 PM

              [Thumbprint]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        :
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

<span data-ttu-id="3f323-109">Der erste Befehl verwendet das New-AzureKeyVaultCertificatePolicy-Cmdlet, um eine Zertifikatrichtlinie zu erstellen, und speichert Sie dann in der $Policy-Variablen.</span><span class="sxs-lookup"><span data-stu-id="3f323-109">The first command uses the New-AzureKeyVaultCertificatePolicy cmdlet to create a certificate policy, and then stores it in the $Policy variable.</span></span>
<span data-ttu-id="3f323-110">Der zweite Befehl verwendet **Add-AzureKeyVaultCertificate** , um den Prozess zum Erstellen eines Zertifikats zu starten.</span><span class="sxs-lookup"><span data-stu-id="3f323-110">The second command uses **Add-AzureKeyVaultCertificate** to start the process to create a certificate.</span></span>
<span data-ttu-id="3f323-111">Der dritte Befehl ruft mithilfe des Get-AzureKeyVaultCertificateOperation-Cmdlets den Vorgang ab, um zu überprüfen, ob er abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="3f323-111">The third command uses the Get-AzureKeyVaultCertificateOperation cmdlet to poll the operation to verify that it's complete.</span></span>
<span data-ttu-id="3f323-112">Der endgültige Befehl verwendet das Get-AzureKeyVaultCertificate-Cmdlet zum Abrufen des Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="3f323-112">The final command uses the Get-AzureKeyVaultCertificate cmdlet to get the certificate.</span></span>

## <span data-ttu-id="3f323-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f323-113">PARAMETERS</span></span>

### <span data-ttu-id="3f323-114">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="3f323-114">-CertificatePolicy</span></span>
<span data-ttu-id="3f323-115">Gibt ein **KeyVaultCertificatePolicy** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="3f323-115">Specifies a **KeyVaultCertificatePolicy** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f323-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f323-116">-DefaultProfile</span></span>
<span data-ttu-id="3f323-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3f323-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f323-118">-Name</span><span class="sxs-lookup"><span data-stu-id="3f323-118">-Name</span></span>
<span data-ttu-id="3f323-119">Gibt den Namen des Zertifikats an, das hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f323-119">Specifies the name of the certificate to add.</span></span>

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

### <span data-ttu-id="3f323-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="3f323-120">-Tag</span></span>
<span data-ttu-id="3f323-121">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="3f323-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3f323-122">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="3f323-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f323-123">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="3f323-123">-VaultName</span></span>
<span data-ttu-id="3f323-124">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="3f323-124">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="3f323-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3f323-125">-Confirm</span></span>
<span data-ttu-id="3f323-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3f323-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f323-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f323-127">-WhatIf</span></span>
<span data-ttu-id="3f323-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3f323-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f323-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3f323-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f323-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f323-130">CommonParameters</span></span>
<span data-ttu-id="3f323-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f323-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f323-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f323-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f323-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3f323-133">INPUTS</span></span>

### <span data-ttu-id="3f323-134">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="3f323-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>
<span data-ttu-id="3f323-135">Parameter: CertificatePolicy (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3f323-135">Parameters: CertificatePolicy (ByValue)</span></span>

## <span data-ttu-id="3f323-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3f323-136">OUTPUTS</span></span>

### <span data-ttu-id="3f323-137">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="3f323-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="3f323-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="3f323-138">NOTES</span></span>

## <span data-ttu-id="3f323-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3f323-139">RELATED LINKS</span></span>

[<span data-ttu-id="3f323-140">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3f323-140">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="3f323-141">Importieren-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3f323-141">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="3f323-142">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3f323-142">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)
