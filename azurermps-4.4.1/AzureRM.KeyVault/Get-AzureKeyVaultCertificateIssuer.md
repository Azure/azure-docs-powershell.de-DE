---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 66c5e949cca8a6f53fdbac89e2745ac7697e14ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502722"
---
# <span data-ttu-id="6c29b-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="6c29b-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="6c29b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6c29b-102">SYNOPSIS</span></span>
<span data-ttu-id="6c29b-103">Ruft einen Zertifikataussteller für einen schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="6c29b-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c29b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c29b-104">SYNTAX</span></span>

### <span data-ttu-id="6c29b-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="6c29b-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6c29b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6c29b-106">ByName</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c29b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c29b-107">DESCRIPTION</span></span>
<span data-ttu-id="6c29b-108">Das Cmdlet " **Get-AzureKeyVaultCertificateIssuer** " Ruft einen angegebenen Zertifikataussteller oder alle Zertifikataussteller für einen schlüsseltresor im Azure Key Vault ab.</span><span class="sxs-lookup"><span data-stu-id="6c29b-108">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="6c29b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6c29b-109">EXAMPLES</span></span>

### <span data-ttu-id="6c29b-110">Beispiel 1: Abrufen eines Zertifikats Emittenten</span><span class="sxs-lookup"><span data-stu-id="6c29b-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="6c29b-111">Dieser Befehl ruft den Aussteller des Zertifikats mit dem Namen TestIssuer01 ab.</span><span class="sxs-lookup"><span data-stu-id="6c29b-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="6c29b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c29b-112">PARAMETERS</span></span>

### <span data-ttu-id="6c29b-113">-Name</span><span class="sxs-lookup"><span data-stu-id="6c29b-113">-Name</span></span>
<span data-ttu-id="6c29b-114">Gibt den Namen des abzurufenden Zertifikatausstellers an.</span><span class="sxs-lookup"><span data-stu-id="6c29b-114">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: IssuerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c29b-115">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="6c29b-115">-VaultName</span></span>
<span data-ttu-id="6c29b-116">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="6c29b-116">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="6c29b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c29b-117">-DefaultProfile</span></span>
<span data-ttu-id="6c29b-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6c29b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c29b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c29b-119">CommonParameters</span></span>
<span data-ttu-id="6c29b-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c29b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c29b-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c29b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c29b-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6c29b-122">INPUTS</span></span>

## <span data-ttu-id="6c29b-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6c29b-123">OUTPUTS</span></span>

### <span data-ttu-id="6c29b-124">Liste<Microsoft. Azure. Commands. keyvault. Models. CertificateIssuerIdentityItem>, Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="6c29b-124">List<Microsoft.Azure.Commands.KeyVault.Models.CertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="6c29b-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="6c29b-125">NOTES</span></span>

## <span data-ttu-id="6c29b-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6c29b-126">RELATED LINKS</span></span>

[<span data-ttu-id="6c29b-127">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="6c29b-127">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="6c29b-128">Satz-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="6c29b-128">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


