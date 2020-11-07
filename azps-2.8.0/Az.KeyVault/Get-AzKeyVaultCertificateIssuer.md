---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: dc1ee6f168a417c612e01d02c93d8729cc2563af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650904"
---
# <span data-ttu-id="deb8f-101">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="deb8f-101">Get-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="deb8f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="deb8f-102">SYNOPSIS</span></span>
<span data-ttu-id="deb8f-103">Ruft einen Zertifikataussteller für einen schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="deb8f-103">Gets a certificate issuer for a key vault.</span></span>

## <span data-ttu-id="deb8f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="deb8f-104">SYNTAX</span></span>

### <span data-ttu-id="deb8f-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="deb8f-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="deb8f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="deb8f-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="deb8f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="deb8f-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateIssuer [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="deb8f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="deb8f-108">DESCRIPTION</span></span>
<span data-ttu-id="deb8f-109">Das Cmdlet " **Get-AzKeyVaultCertificateIssuer** " Ruft einen angegebenen Zertifikataussteller oder alle Zertifikataussteller für einen schlüsseltresor im Azure Key Vault ab.</span><span class="sxs-lookup"><span data-stu-id="deb8f-109">The **Get-AzKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="deb8f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="deb8f-110">EXAMPLES</span></span>

### <span data-ttu-id="deb8f-111">Beispiel 1: Abrufen eines Zertifikats Emittenten</span><span class="sxs-lookup"><span data-stu-id="deb8f-111">Example 1: Get a certificate issuer</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="deb8f-112">Dieser Befehl ruft den Aussteller des Zertifikats mit dem Namen TestIssuer01 ab.</span><span class="sxs-lookup"><span data-stu-id="deb8f-112">This command gets the certificate issuer named TestIssuer01.</span></span>

### <span data-ttu-id="deb8f-113">Beispiel 2: Auflisten von Zertifikat Emittenten mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="deb8f-113">Example 2: List certificate issuers using filtering</span></span>
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

<span data-ttu-id="deb8f-114">Dieser Befehl ruft die Zertifikataussteller ab, die mit "Test" beginnen.</span><span class="sxs-lookup"><span data-stu-id="deb8f-114">This command gets the certificate issuers that start with "test".</span></span>

## <span data-ttu-id="deb8f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="deb8f-115">PARAMETERS</span></span>

### <span data-ttu-id="deb8f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deb8f-116">-DefaultProfile</span></span>
<span data-ttu-id="deb8f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="deb8f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="deb8f-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="deb8f-118">-InputObject</span></span>
<span data-ttu-id="deb8f-119">Keyvault-Objekt.</span><span class="sxs-lookup"><span data-stu-id="deb8f-119">KeyVault object.</span></span>

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

### <span data-ttu-id="deb8f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="deb8f-120">-Name</span></span>
<span data-ttu-id="deb8f-121">Gibt den Namen des abzurufenden Zertifikatausstellers an.</span><span class="sxs-lookup"><span data-stu-id="deb8f-121">Specifies the name of the certificate issuer to get.</span></span>

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

### <span data-ttu-id="deb8f-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="deb8f-122">-ResourceId</span></span>
<span data-ttu-id="deb8f-123">Keyvault-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="deb8f-123">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="deb8f-124">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="deb8f-124">-VaultName</span></span>
<span data-ttu-id="deb8f-125">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="deb8f-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="deb8f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deb8f-126">CommonParameters</span></span>
<span data-ttu-id="deb8f-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="deb8f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deb8f-128">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="deb8f-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deb8f-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="deb8f-129">INPUTS</span></span>

### <span data-ttu-id="deb8f-130">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="deb8f-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="deb8f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="deb8f-131">System.String</span></span>

## <span data-ttu-id="deb8f-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="deb8f-132">OUTPUTS</span></span>

### <span data-ttu-id="deb8f-133">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="deb8f-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

### <span data-ttu-id="deb8f-134">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="deb8f-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="deb8f-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="deb8f-135">NOTES</span></span>

## <span data-ttu-id="deb8f-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="deb8f-136">RELATED LINKS</span></span>

[<span data-ttu-id="deb8f-137">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="deb8f-137">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="deb8f-138">Satz-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="deb8f-138">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


