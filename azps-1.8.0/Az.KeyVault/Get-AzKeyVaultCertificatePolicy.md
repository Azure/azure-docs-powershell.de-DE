---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: a6635afc19f95f32d7c50ff7a92ba5868a5945e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819631"
---
# <span data-ttu-id="024e8-101">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="024e8-101">Get-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="024e8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="024e8-102">SYNOPSIS</span></span>
<span data-ttu-id="024e8-103">Ruft die Richtlinie für ein Zertifikat in einem schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="024e8-103">Gets the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="024e8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="024e8-104">SYNTAX</span></span>

### <span data-ttu-id="024e8-105">VaultAndCertName (Standard)</span><span class="sxs-lookup"><span data-stu-id="024e8-105">VaultAndCertName (Default)</span></span>
```
Get-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="024e8-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="024e8-106">InputObject</span></span>
```
Get-AzKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="024e8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="024e8-107">DESCRIPTION</span></span>
<span data-ttu-id="024e8-108">Das Cmdlet " **Get-AzKeyVaultCertificatePolicy** " Ruft die Richtlinie für ein Zertifikat in einem schlüsseltresor im Azure Key Vault ab.</span><span class="sxs-lookup"><span data-stu-id="024e8-108">The **Get-AzKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="024e8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="024e8-109">EXAMPLES</span></span>

### <span data-ttu-id="024e8-110">Beispiel 1: Abrufen einer Zertifikatrichtlinie</span><span class="sxs-lookup"><span data-stu-id="024e8-110">Example 1: Get a certificate policy</span></span>
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

<span data-ttu-id="024e8-111">Dieser Befehl ruft die Zertifikatrichtlinie für TestCert01-Zertifikat im ContosoKV01-schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="024e8-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="024e8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="024e8-112">PARAMETERS</span></span>

### <span data-ttu-id="024e8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="024e8-113">-DefaultProfile</span></span>
<span data-ttu-id="024e8-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="024e8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="024e8-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="024e8-115">-InputObject</span></span>
<span data-ttu-id="024e8-116">Certificate-Objekt.</span><span class="sxs-lookup"><span data-stu-id="024e8-116">Certificate Object.</span></span>

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

### <span data-ttu-id="024e8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="024e8-117">-Name</span></span>
<span data-ttu-id="024e8-118">Gibt den Namen eines Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="024e8-118">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="024e8-119">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="024e8-119">-VaultName</span></span>
<span data-ttu-id="024e8-120">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="024e8-120">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="024e8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="024e8-121">CommonParameters</span></span>
<span data-ttu-id="024e8-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="024e8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="024e8-123">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="024e8-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="024e8-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="024e8-124">INPUTS</span></span>

### <span data-ttu-id="024e8-125">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="024e8-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="024e8-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="024e8-126">OUTPUTS</span></span>

### <span data-ttu-id="024e8-127">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="024e8-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="024e8-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="024e8-128">NOTES</span></span>

## <span data-ttu-id="024e8-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="024e8-129">RELATED LINKS</span></span>

[<span data-ttu-id="024e8-130">Neu – AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="024e8-130">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="024e8-131">Satz-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="024e8-131">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

