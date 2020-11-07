---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateissuer
schema: 2.0.0
ms.openlocfilehash: fcbb19936bb9924f95aa3a20fa026a9c8c723033
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849679"
---
# <span data-ttu-id="c16d4-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="c16d4-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="c16d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c16d4-102">SYNOPSIS</span></span>
<span data-ttu-id="c16d4-103">Ruft einen Zertifikataussteller für einen schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="c16d4-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c16d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c16d4-104">SYNTAX</span></span>

### <span data-ttu-id="c16d4-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c16d4-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c16d4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c16d4-106">ByName</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c16d4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c16d4-107">DESCRIPTION</span></span>
<span data-ttu-id="c16d4-108">Das Cmdlet " **Get-AzureKeyVaultCertificateIssuer** " Ruft einen angegebenen Zertifikataussteller oder alle Zertifikataussteller für einen schlüsseltresor im Azure Key Vault ab.</span><span class="sxs-lookup"><span data-stu-id="c16d4-108">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="c16d4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c16d4-109">EXAMPLES</span></span>

### <span data-ttu-id="c16d4-110">Beispiel 1: Abrufen eines Zertifikats Emittenten</span><span class="sxs-lookup"><span data-stu-id="c16d4-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="c16d4-111">Dieser Befehl ruft den Aussteller des Zertifikats mit dem Namen TestIssuer01 ab.</span><span class="sxs-lookup"><span data-stu-id="c16d4-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="c16d4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c16d4-112">PARAMETERS</span></span>

### <span data-ttu-id="c16d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c16d4-113">-DefaultProfile</span></span>
<span data-ttu-id="c16d4-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c16d4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c16d4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c16d4-115">-Name</span></span>
<span data-ttu-id="c16d4-116">Gibt den Namen des abzurufenden Zertifikatausstellers an.</span><span class="sxs-lookup"><span data-stu-id="c16d4-116">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c16d4-117">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="c16d4-117">-VaultName</span></span>
<span data-ttu-id="c16d4-118">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="c16d4-118">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="c16d4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c16d4-119">CommonParameters</span></span>
<span data-ttu-id="c16d4-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c16d4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c16d4-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c16d4-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c16d4-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c16d4-122">INPUTS</span></span>

## <span data-ttu-id="c16d4-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c16d4-123">OUTPUTS</span></span>

### <span data-ttu-id="c16d4-124">Liste<Microsoft. Azure. Commands. keyvault. Models. CertificateIssuerIdentityItem>, Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="c16d4-124">List<Microsoft.Azure.Commands.KeyVault.Models.CertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="c16d4-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="c16d4-125">NOTES</span></span>

## <span data-ttu-id="c16d4-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c16d4-126">RELATED LINKS</span></span>

[<span data-ttu-id="c16d4-127">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="c16d4-127">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="c16d4-128">Satz-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="c16d4-128">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


