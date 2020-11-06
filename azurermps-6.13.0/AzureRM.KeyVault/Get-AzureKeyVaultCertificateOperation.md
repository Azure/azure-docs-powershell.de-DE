---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0743C43D-2A1F-4950-B0F3-1FED4014EEC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: bc5b7b47c5567867a857ab32fe34c287e896ae75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502101"
---
# <span data-ttu-id="c8d14-101">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="c8d14-101">Get-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="c8d14-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c8d14-102">SYNOPSIS</span></span>
<span data-ttu-id="c8d14-103">Ruft den Status eines Zertifikat Vorgangs ab.</span><span class="sxs-lookup"><span data-stu-id="c8d14-103">Gets the status of a certificate operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8d14-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8d14-104">SYNTAX</span></span>

### <span data-ttu-id="c8d14-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c8d14-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8d14-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c8d14-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8d14-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8d14-107">DESCRIPTION</span></span>
<span data-ttu-id="c8d14-108">Das Cmdlet " **Get-AzureKeyVaultCertificateOperation** " Ruft den Status eines Zertifikat Vorgangs ab.</span><span class="sxs-lookup"><span data-stu-id="c8d14-108">The **Get-AzureKeyVaultCertificateOperation** cmdlet gets the status of a certificate operation.</span></span>

## <span data-ttu-id="c8d14-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c8d14-109">EXAMPLES</span></span>

### <span data-ttu-id="c8d14-110">Beispiel 1: Abrufen des Status eines Zertifikat Vorgangs</span><span class="sxs-lookup"><span data-stu-id="c8d14-110">Example 1: Get the status of a certificate operation</span></span>
```powershell
PS C:\> Get-AzureKeyVaultCertificateOperation -VaultName "contosoKV01" -Name "TestCert01"

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

<span data-ttu-id="c8d14-111">Dieser Befehl ruft den Status des Zertifikat Vorgangs für TestCert01 im ContosoKV01-schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="c8d14-111">This command gets the status of the certificate operation for TestCert01 on the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="c8d14-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8d14-112">PARAMETERS</span></span>

### <span data-ttu-id="c8d14-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8d14-113">-DefaultProfile</span></span>
<span data-ttu-id="c8d14-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c8d14-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8d14-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c8d14-115">-InputObject</span></span>
<span data-ttu-id="c8d14-116">Certificate-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c8d14-116">Certificate Object.</span></span>

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

### <span data-ttu-id="c8d14-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c8d14-117">-Name</span></span>
<span data-ttu-id="c8d14-118">Gibt den Namen eines Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="c8d14-118">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="c8d14-119">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="c8d14-119">-VaultName</span></span>
<span data-ttu-id="c8d14-120">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="c8d14-120">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="c8d14-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8d14-121">CommonParameters</span></span>
<span data-ttu-id="c8d14-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8d14-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8d14-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8d14-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8d14-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c8d14-124">INPUTS</span></span>

### <span data-ttu-id="c8d14-125">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="c8d14-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>
<span data-ttu-id="c8d14-126">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c8d14-126">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="c8d14-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c8d14-127">OUTPUTS</span></span>

### <span data-ttu-id="c8d14-128">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="c8d14-128">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="c8d14-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="c8d14-129">NOTES</span></span>

## <span data-ttu-id="c8d14-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c8d14-130">RELATED LINKS</span></span>

[<span data-ttu-id="c8d14-131">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="c8d14-131">Remove-AzureKeyVaultCertificateOperation</span></span>](./Remove-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="c8d14-132">Stopp-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="c8d14-132">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)

