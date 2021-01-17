---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: d6e2225cc7441d4c370d990aa45c9b2c2bb40457
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469583"
---
# <span data-ttu-id="72877-101">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="72877-101">Get-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="72877-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72877-102">SYNOPSIS</span></span>
<span data-ttu-id="72877-103">Ruft die Richtlinie für ein Zertifikat in einem Schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="72877-103">Gets the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="72877-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72877-104">SYNTAX</span></span>

### <span data-ttu-id="72877-105">VaultAndCertName (Standard)</span><span class="sxs-lookup"><span data-stu-id="72877-105">VaultAndCertName (Default)</span></span>
```
Get-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72877-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="72877-106">InputObject</span></span>
```
Get-AzKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72877-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="72877-107">DESCRIPTION</span></span>
<span data-ttu-id="72877-108">Das **Cmdlet "Get-AzKeyVaultCertificatePolicy"** ruft die Richtlinie für ein Zertifikat in einem Schlüsseltresor im Azure Key Vault ab.</span><span class="sxs-lookup"><span data-stu-id="72877-108">The **Get-AzKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="72877-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="72877-109">EXAMPLES</span></span>

### <span data-ttu-id="72877-110">Beispiel 1: Erhalten einer Zertifikatrichtlinie</span><span class="sxs-lookup"><span data-stu-id="72877-110">Example 1: Get a certificate policy</span></span>
```powershell
PS C:\ >Get-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"

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
CertificateType                 :
RenewAtNumberOfDaysBeforeExpiry : 
RenewAtPercentageLifetime       : 80
EmailAtNumberOfDaysBeforeExpiry :
EmailAtPercentageLifetime       :
Enabled                         : True
Created                         : 2/8/2016 11:10:29 PM
Updated                         : 2/8/2016 11:10:29 PM
```

<span data-ttu-id="72877-111">Dieser Befehl ruft die Zertifikatrichtlinie für das TestCert01-Zertifikat im Schlüsseltresor ContosoKV01 ab.</span><span class="sxs-lookup"><span data-stu-id="72877-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="72877-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72877-112">PARAMETERS</span></span>

### <span data-ttu-id="72877-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72877-113">-DefaultProfile</span></span>
<span data-ttu-id="72877-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="72877-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72877-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72877-115">-InputObject</span></span>
<span data-ttu-id="72877-116">Zertifikatobjekt.</span><span class="sxs-lookup"><span data-stu-id="72877-116">Certificate Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72877-117">-Name</span><span class="sxs-lookup"><span data-stu-id="72877-117">-Name</span></span>
<span data-ttu-id="72877-118">Gibt den Namen eines Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="72877-118">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultAndCertName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72877-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="72877-119">-VaultName</span></span>
<span data-ttu-id="72877-120">Gibt den Namen eines Schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="72877-120">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultAndCertName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72877-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72877-121">CommonParameters</span></span>
<span data-ttu-id="72877-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72877-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72877-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72877-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72877-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="72877-124">INPUTS</span></span>

### <span data-ttu-id="72877-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="72877-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="72877-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="72877-126">OUTPUTS</span></span>

### <span data-ttu-id="72877-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="72877-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="72877-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="72877-128">NOTES</span></span>

## <span data-ttu-id="72877-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="72877-129">RELATED LINKS</span></span>

[<span data-ttu-id="72877-130">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="72877-130">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="72877-131">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="72877-131">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

