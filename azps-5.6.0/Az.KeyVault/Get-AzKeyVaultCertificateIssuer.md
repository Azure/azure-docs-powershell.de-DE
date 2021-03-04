---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: d9d77eaac735044091aacbce6f92ee51be1210ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945095"
---
# <span data-ttu-id="09f7a-101">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="09f7a-101">Get-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="09f7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09f7a-102">SYNOPSIS</span></span>
<span data-ttu-id="09f7a-103">Ruft einen Zertifikataussteller für einen Schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="09f7a-103">Gets a certificate issuer for a key vault.</span></span>

## <span data-ttu-id="09f7a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09f7a-104">SYNTAX</span></span>

### <span data-ttu-id="09f7a-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="09f7a-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09f7a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="09f7a-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09f7a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="09f7a-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateIssuer [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09f7a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="09f7a-108">DESCRIPTION</span></span>
<span data-ttu-id="09f7a-109">Das **Get-AzKeyVertificateIssuer-Cmdlet** ruft einen angegebenen Zertifikataussteller oder alle Zertifikataussteller für einen Schlüsseltresor im Azure Key Vault ab.</span><span class="sxs-lookup"><span data-stu-id="09f7a-109">The **Get-AzKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="09f7a-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="09f7a-110">EXAMPLES</span></span>

### <span data-ttu-id="09f7a-111">Beispiel 1: Erhalten eines Zertifikatausstellers</span><span class="sxs-lookup"><span data-stu-id="09f7a-111">Example 1: Get a certificate issuer</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="09f7a-112">Dieser Befehl ruft den Zertifikataussteller mit dem Namen TestIssuer01 ab.</span><span class="sxs-lookup"><span data-stu-id="09f7a-112">This command gets the certificate issuer named TestIssuer01.</span></span>

### <span data-ttu-id="09f7a-113">Beispiel 2: Auflisten von Zertifikatausstellern mithilfe von Filterung</span><span class="sxs-lookup"><span data-stu-id="09f7a-113">Example 2: List certificate issuers using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "test*"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer02
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="09f7a-114">Dieser Befehl ruft die Zertifikataussteller ab, die mit "test" beginnen.</span><span class="sxs-lookup"><span data-stu-id="09f7a-114">This command gets the certificate issuers that start with "test".</span></span>

## <span data-ttu-id="09f7a-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="09f7a-115">PARAMETERS</span></span>

### <span data-ttu-id="09f7a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09f7a-116">-DefaultProfile</span></span>
<span data-ttu-id="09f7a-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="09f7a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09f7a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09f7a-118">-InputObject</span></span>
<span data-ttu-id="09f7a-119">KeyVault-Objekt.</span><span class="sxs-lookup"><span data-stu-id="09f7a-119">KeyVault object.</span></span>

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

### <span data-ttu-id="09f7a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="09f7a-120">-Name</span></span>
<span data-ttu-id="09f7a-121">Gibt den Namen des Zertifikatausstellers an, den Sie erhalten müssen.</span><span class="sxs-lookup"><span data-stu-id="09f7a-121">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="09f7a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09f7a-122">-ResourceId</span></span>
<span data-ttu-id="09f7a-123">KeyVault-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="09f7a-123">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="09f7a-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="09f7a-124">-VaultName</span></span>
<span data-ttu-id="09f7a-125">Gibt den Namen eines Schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="09f7a-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="09f7a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09f7a-126">CommonParameters</span></span>
<span data-ttu-id="09f7a-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09f7a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09f7a-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09f7a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09f7a-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="09f7a-129">INPUTS</span></span>

### <span data-ttu-id="09f7a-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="09f7a-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="09f7a-131">System.String</span><span class="sxs-lookup"><span data-stu-id="09f7a-131">System.String</span></span>

## <span data-ttu-id="09f7a-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="09f7a-132">OUTPUTS</span></span>

### <span data-ttu-id="09f7a-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="09f7a-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

### <span data-ttu-id="09f7a-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="09f7a-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="09f7a-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="09f7a-135">NOTES</span></span>

## <span data-ttu-id="09f7a-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="09f7a-136">RELATED LINKS</span></span>

[<span data-ttu-id="09f7a-137">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="09f7a-137">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="09f7a-138">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="09f7a-138">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


