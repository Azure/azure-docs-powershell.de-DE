---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 1317b35e957b46e6f39bfb0866e0429c01d35533
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481173"
---
# <span data-ttu-id="0e644-101">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0e644-101">Get-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="0e644-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0e644-102">SYNOPSIS</span></span>
<span data-ttu-id="0e644-103">Ruft die Richtlinie für ein Zertifikat in einem schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="0e644-103">Gets the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e644-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e644-104">SYNTAX</span></span>

### <span data-ttu-id="0e644-105">VaultAndCertName (Standard)</span><span class="sxs-lookup"><span data-stu-id="0e644-105">VaultAndCertName (Default)</span></span>
```
Get-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e644-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0e644-106">InputObject</span></span>
```
Get-AzureKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e644-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e644-107">DESCRIPTION</span></span>
<span data-ttu-id="0e644-108">Das Cmdlet " **Get-AzureKeyVaultCertificatePolicy** " Ruft die Richtlinie für ein Zertifikat in einem schlüsseltresor im Azure Key Vault ab.</span><span class="sxs-lookup"><span data-stu-id="0e644-108">The **Get-AzureKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="0e644-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0e644-109">EXAMPLES</span></span>

### <span data-ttu-id="0e644-110">Beispiel 1: Abrufen einer Zertifikatrichtlinie</span><span class="sxs-lookup"><span data-stu-id="0e644-110">Example 1: Get a certificate policy</span></span>
```
PS C:\>Get-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"
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
RenewAtNumberOfDaysBeforeExpiry : 
RenewAtPercentageLifetime       : 80
EmailOnly                       : False
Enabled                         : True
Created                         : 2/8/2016 11:10:29 PM
Updated                         : 2/8/2016 11:10:29 PM
```

<span data-ttu-id="0e644-111">Dieser Befehl ruft die Zertifikatrichtlinie für TestCert01-Zertifikat im ContosoKV01-schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="0e644-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="0e644-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e644-112">PARAMETERS</span></span>

### <span data-ttu-id="0e644-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e644-113">-DefaultProfile</span></span>
<span data-ttu-id="0e644-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="0e644-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e644-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0e644-115">-InputObject</span></span>
<span data-ttu-id="0e644-116">Certificate-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0e644-116">Certificate Object.</span></span>

```yaml
Type: PSKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e644-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0e644-117">-Name</span></span>
<span data-ttu-id="0e644-118">Gibt den Namen eines Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="0e644-118">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: VaultAndCertName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e644-119">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="0e644-119">-VaultName</span></span>
<span data-ttu-id="0e644-120">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="0e644-120">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: VaultAndCertName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e644-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e644-121">CommonParameters</span></span>
<span data-ttu-id="0e644-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e644-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e644-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e644-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e644-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0e644-124">INPUTS</span></span>

### <span data-ttu-id="0e644-125">Keine</span><span class="sxs-lookup"><span data-stu-id="0e644-125">None</span></span>
<span data-ttu-id="0e644-126">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="0e644-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0e644-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0e644-127">OUTPUTS</span></span>

### <span data-ttu-id="0e644-128">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0e644-128">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="0e644-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="0e644-129">NOTES</span></span>

## <span data-ttu-id="0e644-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0e644-130">RELATED LINKS</span></span>

[<span data-ttu-id="0e644-131">Neu – AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0e644-131">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="0e644-132">Satz-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0e644-132">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

