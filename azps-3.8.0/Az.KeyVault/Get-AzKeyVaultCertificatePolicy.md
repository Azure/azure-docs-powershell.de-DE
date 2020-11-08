---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: d6e2225cc7441d4c370d990aa45c9b2c2bb40457
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995394"
---
# <span data-ttu-id="66f39-101">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="66f39-101">Get-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="66f39-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="66f39-102">SYNOPSIS</span></span>
<span data-ttu-id="66f39-103">Ruft die Richtlinie für ein Zertifikat in einem schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="66f39-103">Gets the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="66f39-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="66f39-104">SYNTAX</span></span>

### <span data-ttu-id="66f39-105">VaultAndCertName (Standard)</span><span class="sxs-lookup"><span data-stu-id="66f39-105">VaultAndCertName (Default)</span></span>
```
Get-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66f39-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="66f39-106">InputObject</span></span>
```
Get-AzKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66f39-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66f39-107">DESCRIPTION</span></span>
<span data-ttu-id="66f39-108">Das Cmdlet " **Get-AzKeyVaultCertificatePolicy** " Ruft die Richtlinie für ein Zertifikat in einem schlüsseltresor im Azure Key Vault ab.</span><span class="sxs-lookup"><span data-stu-id="66f39-108">The **Get-AzKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="66f39-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="66f39-109">EXAMPLES</span></span>

### <span data-ttu-id="66f39-110">Beispiel 1: Abrufen einer Zertifikatrichtlinie</span><span class="sxs-lookup"><span data-stu-id="66f39-110">Example 1: Get a certificate policy</span></span>
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

<span data-ttu-id="66f39-111">Dieser Befehl ruft die Zertifikatrichtlinie für TestCert01-Zertifikat im ContosoKV01-schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="66f39-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="66f39-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="66f39-112">PARAMETERS</span></span>

### <span data-ttu-id="66f39-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66f39-113">-DefaultProfile</span></span>
<span data-ttu-id="66f39-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="66f39-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66f39-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="66f39-115">-InputObject</span></span>
<span data-ttu-id="66f39-116">Certificate-Objekt.</span><span class="sxs-lookup"><span data-stu-id="66f39-116">Certificate Object.</span></span>

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

### <span data-ttu-id="66f39-117">-Name</span><span class="sxs-lookup"><span data-stu-id="66f39-117">-Name</span></span>
<span data-ttu-id="66f39-118">Gibt den Namen eines Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="66f39-118">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="66f39-119">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="66f39-119">-VaultName</span></span>
<span data-ttu-id="66f39-120">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="66f39-120">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="66f39-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66f39-121">CommonParameters</span></span>
<span data-ttu-id="66f39-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66f39-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66f39-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66f39-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66f39-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="66f39-124">INPUTS</span></span>

### <span data-ttu-id="66f39-125">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="66f39-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="66f39-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="66f39-126">OUTPUTS</span></span>

### <span data-ttu-id="66f39-127">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="66f39-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="66f39-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="66f39-128">NOTES</span></span>

## <span data-ttu-id="66f39-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="66f39-129">RELATED LINKS</span></span>

[<span data-ttu-id="66f39-130">Neu – AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="66f39-130">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="66f39-131">Satz-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="66f39-131">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

