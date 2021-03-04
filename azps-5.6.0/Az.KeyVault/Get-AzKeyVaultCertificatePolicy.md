---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: cace261f300dc63b9568413fb8a709c323349531
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938667"
---
# <span data-ttu-id="c04a1-101">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c04a1-101">Get-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="c04a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c04a1-102">SYNOPSIS</span></span>
<span data-ttu-id="c04a1-103">Ruft die Richtlinie für ein Zertifikat in einem Schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="c04a1-103">Gets the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="c04a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c04a1-104">SYNTAX</span></span>

### <span data-ttu-id="c04a1-105">VaultAndCertName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c04a1-105">VaultAndCertName (Default)</span></span>
```
Get-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c04a1-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c04a1-106">InputObject</span></span>
```
Get-AzKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c04a1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c04a1-107">DESCRIPTION</span></span>
<span data-ttu-id="c04a1-108">Das **Cmdlet Get-AzKeyVaultCertificatePolicy** ruft die Richtlinie für ein Zertifikat in einem Schlüsseltresor im Azure Key Vault ab.</span><span class="sxs-lookup"><span data-stu-id="c04a1-108">The **Get-AzKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="c04a1-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c04a1-109">EXAMPLES</span></span>

### <span data-ttu-id="c04a1-110">Beispiel 1: Erhalten einer Zertifikatrichtlinie</span><span class="sxs-lookup"><span data-stu-id="c04a1-110">Example 1: Get a certificate policy</span></span>
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

<span data-ttu-id="c04a1-111">Dieser Befehl ruft die Zertifikatrichtlinie für das TestCert01-Zertifikat im ContosoKV01-Schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="c04a1-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="c04a1-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c04a1-112">PARAMETERS</span></span>

### <span data-ttu-id="c04a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c04a1-113">-DefaultProfile</span></span>
<span data-ttu-id="c04a1-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c04a1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c04a1-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c04a1-115">-InputObject</span></span>
<span data-ttu-id="c04a1-116">Zertifikatobjekt.</span><span class="sxs-lookup"><span data-stu-id="c04a1-116">Certificate Object.</span></span>

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

### <span data-ttu-id="c04a1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c04a1-117">-Name</span></span>
<span data-ttu-id="c04a1-118">Gibt den Namen eines Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="c04a1-118">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="c04a1-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c04a1-119">-VaultName</span></span>
<span data-ttu-id="c04a1-120">Gibt den Namen eines Schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="c04a1-120">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="c04a1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c04a1-121">CommonParameters</span></span>
<span data-ttu-id="c04a1-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c04a1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c04a1-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c04a1-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c04a1-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c04a1-124">INPUTS</span></span>

### <span data-ttu-id="c04a1-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="c04a1-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="c04a1-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c04a1-126">OUTPUTS</span></span>

### <span data-ttu-id="c04a1-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c04a1-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="c04a1-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c04a1-128">NOTES</span></span>

## <span data-ttu-id="c04a1-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c04a1-129">RELATED LINKS</span></span>

[<span data-ttu-id="c04a1-130">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c04a1-130">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="c04a1-131">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c04a1-131">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

