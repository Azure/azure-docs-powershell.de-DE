---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatepolicy
schema: 2.0.0
ms.openlocfilehash: 692c639ac42d0a8f2dc2bf121321dfc116ebce1b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849675"
---
# <span data-ttu-id="4a288-101">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4a288-101">Get-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="4a288-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4a288-102">SYNOPSIS</span></span>
<span data-ttu-id="4a288-103">Ruft die Richtlinie für ein Zertifikat in einem schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="4a288-103">Gets the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a288-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a288-104">SYNTAX</span></span>

```
Get-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a288-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4a288-105">DESCRIPTION</span></span>
<span data-ttu-id="4a288-106">Das Cmdlet " **Get-AzureKeyVaultCertificatePolicy** " Ruft die Richtlinie für ein Zertifikat in einem schlüsseltresor im Azure Key Vault ab.</span><span class="sxs-lookup"><span data-stu-id="4a288-106">The **Get-AzureKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="4a288-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4a288-107">EXAMPLES</span></span>

### <span data-ttu-id="4a288-108">Beispiel 1: Abrufen einer Zertifikatrichtlinie</span><span class="sxs-lookup"><span data-stu-id="4a288-108">Example 1: Get a certificate policy</span></span>
```
PS C:\>Get-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"
SecretContentType               : application/x-pkcs12
Kty                             : RSA
KeySize                         : 2048
Exportable                      : True
ReuseKeyOnRenewal               : True
SubjectName                     : CN=contoso.com
DnsNames                        : 
Ekus                            : {1.3.6.1.5.5.7.3.1, 1.3.6.1.5.5.7.3.2}
ValidityInMonths                : 6
IssuerName                      : Self
RenewAtNumberOfDaysBeforeExpiry : 
RenewAtPercentageLifetime       : 80
EmailOnly                       : False
Enabled                         : True
Created                         : 2/8/2016 11:10:29 PM
Updated                         : 2/8/2016 11:10:29 PM
```

<span data-ttu-id="4a288-109">Dieser Befehl ruft die Zertifikatrichtlinie für TestCert01-Zertifikat im ContosoKV01-schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="4a288-109">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="4a288-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a288-110">PARAMETERS</span></span>

### <span data-ttu-id="4a288-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a288-111">-DefaultProfile</span></span>
<span data-ttu-id="4a288-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4a288-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a288-113">-Name</span><span class="sxs-lookup"><span data-stu-id="4a288-113">-Name</span></span>
<span data-ttu-id="4a288-114">Gibt den Namen eines Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="4a288-114">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="4a288-115">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="4a288-115">-VaultName</span></span>
<span data-ttu-id="4a288-116">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="4a288-116">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="4a288-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a288-117">CommonParameters</span></span>
<span data-ttu-id="4a288-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a288-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a288-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a288-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a288-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4a288-120">INPUTS</span></span>

## <span data-ttu-id="4a288-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4a288-121">OUTPUTS</span></span>

### <span data-ttu-id="4a288-122">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4a288-122">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="4a288-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="4a288-123">NOTES</span></span>

## <span data-ttu-id="4a288-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4a288-124">RELATED LINKS</span></span>

[<span data-ttu-id="4a288-125">Neu – AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4a288-125">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="4a288-126">Satz-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4a288-126">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

