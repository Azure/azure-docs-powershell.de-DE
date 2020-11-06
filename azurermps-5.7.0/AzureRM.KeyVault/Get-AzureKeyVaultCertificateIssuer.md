---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: f19fa119bf307724fb318e0a1d9a390190523bd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481185"
---
# <span data-ttu-id="29d5e-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="29d5e-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="29d5e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="29d5e-102">SYNOPSIS</span></span>
<span data-ttu-id="29d5e-103">Ruft einen Zertifikataussteller für einen schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="29d5e-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29d5e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="29d5e-104">SYNTAX</span></span>

### <span data-ttu-id="29d5e-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="29d5e-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29d5e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="29d5e-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29d5e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29d5e-107">DESCRIPTION</span></span>
<span data-ttu-id="29d5e-108">Das Cmdlet " **Get-AzureKeyVaultCertificateIssuer** " Ruft einen angegebenen Zertifikataussteller oder alle Zertifikataussteller für einen schlüsseltresor im Azure Key Vault ab.</span><span class="sxs-lookup"><span data-stu-id="29d5e-108">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="29d5e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="29d5e-109">EXAMPLES</span></span>

### <span data-ttu-id="29d5e-110">Beispiel 1: Abrufen eines Zertifikats Emittenten</span><span class="sxs-lookup"><span data-stu-id="29d5e-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="29d5e-111">Dieser Befehl ruft den Aussteller des Zertifikats mit dem Namen TestIssuer01 ab.</span><span class="sxs-lookup"><span data-stu-id="29d5e-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="29d5e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="29d5e-112">PARAMETERS</span></span>

### <span data-ttu-id="29d5e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29d5e-113">-DefaultProfile</span></span>
<span data-ttu-id="29d5e-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="29d5e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29d5e-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="29d5e-115">-InputObject</span></span>
<span data-ttu-id="29d5e-116">Keyvault-Objekt.</span><span class="sxs-lookup"><span data-stu-id="29d5e-116">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29d5e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="29d5e-117">-Name</span></span>
<span data-ttu-id="29d5e-118">Gibt den Namen des abzurufenden Zertifikatausstellers an.</span><span class="sxs-lookup"><span data-stu-id="29d5e-118">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29d5e-119">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="29d5e-119">-VaultName</span></span>
<span data-ttu-id="29d5e-120">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="29d5e-120">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29d5e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29d5e-121">CommonParameters</span></span>
<span data-ttu-id="29d5e-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29d5e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29d5e-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29d5e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29d5e-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="29d5e-124">INPUTS</span></span>

### <span data-ttu-id="29d5e-125">Keine</span><span class="sxs-lookup"><span data-stu-id="29d5e-125">None</span></span>
<span data-ttu-id="29d5e-126">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="29d5e-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="29d5e-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="29d5e-127">OUTPUTS</span></span>

### <span data-ttu-id="29d5e-128">Liste<Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIssuerIdentityItem>, Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="29d5e-128">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="29d5e-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="29d5e-129">NOTES</span></span>

## <span data-ttu-id="29d5e-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="29d5e-130">RELATED LINKS</span></span>

[<span data-ttu-id="29d5e-131">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="29d5e-131">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="29d5e-132">Satz-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="29d5e-132">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


