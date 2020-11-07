---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 83e81e479807c3eada25456d53521dfcecd81f40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664058"
---
# <span data-ttu-id="b75a8-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="b75a8-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="b75a8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b75a8-102">SYNOPSIS</span></span>
<span data-ttu-id="b75a8-103">Ruft einen Zertifikataussteller für einen schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="b75a8-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b75a8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b75a8-104">SYNTAX</span></span>

### <span data-ttu-id="b75a8-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b75a8-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b75a8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b75a8-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b75a8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b75a8-107">ByResourceId</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b75a8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b75a8-108">DESCRIPTION</span></span>
<span data-ttu-id="b75a8-109">Das Cmdlet " **Get-AzureKeyVaultCertificateIssuer** " Ruft einen angegebenen Zertifikataussteller oder alle Zertifikataussteller für einen schlüsseltresor im Azure Key Vault ab.</span><span class="sxs-lookup"><span data-stu-id="b75a8-109">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="b75a8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b75a8-110">EXAMPLES</span></span>

### <span data-ttu-id="b75a8-111">Beispiel 1: Abrufen eines Zertifikats Emittenten</span><span class="sxs-lookup"><span data-stu-id="b75a8-111">Example 1: Get a certificate issuer</span></span>
```powershell
PS C:\> Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="b75a8-112">Dieser Befehl ruft den Aussteller des Zertifikats mit dem Namen TestIssuer01 ab.</span><span class="sxs-lookup"><span data-stu-id="b75a8-112">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="b75a8-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b75a8-113">PARAMETERS</span></span>

### <span data-ttu-id="b75a8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b75a8-114">-DefaultProfile</span></span>
<span data-ttu-id="b75a8-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b75a8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b75a8-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b75a8-116">-InputObject</span></span>
<span data-ttu-id="b75a8-117">Keyvault-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b75a8-117">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b75a8-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b75a8-118">-Name</span></span>
<span data-ttu-id="b75a8-119">Gibt den Namen des abzurufenden Zertifikatausstellers an.</span><span class="sxs-lookup"><span data-stu-id="b75a8-119">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b75a8-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b75a8-120">-ResourceId</span></span>
<span data-ttu-id="b75a8-121">Keyvault-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b75a8-121">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b75a8-122">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="b75a8-122">-VaultName</span></span>
<span data-ttu-id="b75a8-123">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="b75a8-123">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="b75a8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b75a8-124">CommonParameters</span></span>
<span data-ttu-id="b75a8-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b75a8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b75a8-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b75a8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b75a8-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b75a8-127">INPUTS</span></span>

### <span data-ttu-id="b75a8-128">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="b75a8-128">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="b75a8-129">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b75a8-129">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="b75a8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b75a8-130">System.String</span></span>

## <span data-ttu-id="b75a8-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b75a8-131">OUTPUTS</span></span>

### <span data-ttu-id="b75a8-132">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="b75a8-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

### <span data-ttu-id="b75a8-133">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="b75a8-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="b75a8-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="b75a8-134">NOTES</span></span>

## <span data-ttu-id="b75a8-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b75a8-135">RELATED LINKS</span></span>

[<span data-ttu-id="b75a8-136">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="b75a8-136">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="b75a8-137">Satz-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="b75a8-137">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


