---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0743C43D-2A1F-4950-B0F3-1FED4014EEC5
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: 522496e8b754f8f979fdf6fd4bdb5f8fb4fb3eb4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945088"
---
# <span data-ttu-id="b5337-101">Get-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="b5337-101">Get-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="b5337-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5337-102">SYNOPSIS</span></span>
<span data-ttu-id="b5337-103">Ruft den Status eines Zertifikatvorgangs ab.</span><span class="sxs-lookup"><span data-stu-id="b5337-103">Gets the status of a certificate operation.</span></span>

## <span data-ttu-id="b5337-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b5337-104">SYNTAX</span></span>

### <span data-ttu-id="b5337-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b5337-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5337-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b5337-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5337-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b5337-107">DESCRIPTION</span></span>
<span data-ttu-id="b5337-108">Das **Cmdlet Get-AzKeyVaultCertificateOperation** erhält den Status eines Zertifikatvorgangs.</span><span class="sxs-lookup"><span data-stu-id="b5337-108">The **Get-AzKeyVaultCertificateOperation** cmdlet gets the status of a certificate operation.</span></span>

## <span data-ttu-id="b5337-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b5337-109">EXAMPLES</span></span>

### <span data-ttu-id="b5337-110">Beispiel 1: Anzeigen des Status eines Zertifikatvorgangs</span><span class="sxs-lookup"><span data-stu-id="b5337-110">Example 1: Get the status of a certificate operation</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateOperation -VaultName "contosoKV01" -Name "TestCert01"

Id                        : https://contosoKV01.vault.azure.net/certificates/TestCert01/pending
Status                    : inProgress
StatusDetails             : Pending certificate created. Certificate request is in progress. This may take some time
                            based on the issuer provider. Please check again later.
RequestId                 : 32a63e80568442a2892dafb9f7cf366t
Target                    :
Issuer                    : Self
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              :
Name                      :
VaultName                 :
```

<span data-ttu-id="b5337-111">Dieser Befehl ruft den Status des Zertifikatvorgangs für TestCert01 im ContosoKV01-Schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="b5337-111">This command gets the status of the certificate operation for TestCert01 on the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="b5337-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b5337-112">PARAMETERS</span></span>

### <span data-ttu-id="b5337-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5337-113">-DefaultProfile</span></span>
<span data-ttu-id="b5337-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="b5337-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5337-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5337-115">-InputObject</span></span>
<span data-ttu-id="b5337-116">Zertifikatobjekt.</span><span class="sxs-lookup"><span data-stu-id="b5337-116">Certificate Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5337-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b5337-117">-Name</span></span>
<span data-ttu-id="b5337-118">Gibt den Namen eines Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="b5337-118">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5337-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b5337-119">-VaultName</span></span>
<span data-ttu-id="b5337-120">Gibt den Namen eines Schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="b5337-120">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5337-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5337-121">CommonParameters</span></span>
<span data-ttu-id="b5337-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5337-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5337-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5337-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5337-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b5337-124">INPUTS</span></span>

### <span data-ttu-id="b5337-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="b5337-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="b5337-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b5337-126">OUTPUTS</span></span>

### <span data-ttu-id="b5337-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="b5337-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="b5337-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b5337-128">NOTES</span></span>

## <span data-ttu-id="b5337-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b5337-129">RELATED LINKS</span></span>

[<span data-ttu-id="b5337-130">Remove-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="b5337-130">Remove-AzKeyVaultCertificateOperation</span></span>](./Remove-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="b5337-131">Stop-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="b5337-131">Stop-AzKeyVaultCertificateOperation</span></span>](./Stop-AzKeyVaultCertificateOperation.md)

