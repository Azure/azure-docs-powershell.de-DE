---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: b9188e1bb4d5de4896bf0ca3b2844c7718593ca2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842155"
---
# <span data-ttu-id="d8930-101">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="d8930-101">Get-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="d8930-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d8930-102">SYNOPSIS</span></span>
<span data-ttu-id="d8930-103">Ruft einen Zertifikataussteller für einen schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="d8930-103">Gets a certificate issuer for a key vault.</span></span>

## <span data-ttu-id="d8930-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8930-104">SYNTAX</span></span>

### <span data-ttu-id="d8930-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d8930-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d8930-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d8930-106">ByName</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8930-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d8930-107">DESCRIPTION</span></span>
<span data-ttu-id="d8930-108">Das Cmdlet " **Get-AzKeyVaultCertificateIssuer** " Ruft einen angegebenen Zertifikataussteller oder alle Zertifikataussteller für einen schlüsseltresor im Azure Key Vault ab.</span><span class="sxs-lookup"><span data-stu-id="d8930-108">The **Get-AzKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="d8930-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d8930-109">EXAMPLES</span></span>

### <span data-ttu-id="d8930-110">Beispiel 1: Abrufen eines Zertifikats Emittenten</span><span class="sxs-lookup"><span data-stu-id="d8930-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="d8930-111">Dieser Befehl ruft den Aussteller des Zertifikats mit dem Namen TestIssuer01 ab.</span><span class="sxs-lookup"><span data-stu-id="d8930-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="d8930-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8930-112">PARAMETERS</span></span>

### <span data-ttu-id="d8930-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8930-113">-DefaultProfile</span></span>
<span data-ttu-id="d8930-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d8930-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8930-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d8930-115">-Name</span></span>
<span data-ttu-id="d8930-116">Gibt den Namen des abzurufenden Zertifikatausstellers an.</span><span class="sxs-lookup"><span data-stu-id="d8930-116">Specifies the name of the certificate issuer to get.</span></span>

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

### <span data-ttu-id="d8930-117">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="d8930-117">-VaultName</span></span>
<span data-ttu-id="d8930-118">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="d8930-118">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="d8930-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8930-119">CommonParameters</span></span>
<span data-ttu-id="d8930-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8930-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8930-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8930-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8930-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d8930-122">INPUTS</span></span>

### <span data-ttu-id="d8930-123">Keine</span><span class="sxs-lookup"><span data-stu-id="d8930-123">None</span></span>
<span data-ttu-id="d8930-124">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="d8930-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d8930-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d8930-125">OUTPUTS</span></span>

### <span data-ttu-id="d8930-126">Liste<Microsoft. Azure. Commands. keyvault. Models. CertificateIssuerIdentityItem>, Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="d8930-126">List<Microsoft.Azure.Commands.KeyVault.Models.CertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="d8930-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="d8930-127">NOTES</span></span>

## <span data-ttu-id="d8930-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d8930-128">RELATED LINKS</span></span>

[<span data-ttu-id="d8930-129">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="d8930-129">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="d8930-130">Satz-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="d8930-130">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


