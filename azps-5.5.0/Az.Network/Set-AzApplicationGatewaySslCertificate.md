---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 1dd4285b75f8c1c067f15be34a334d4d48fb4f7e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158876"
---
# <span data-ttu-id="7764a-101">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7764a-101">Set-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="7764a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7764a-102">SYNOPSIS</span></span>
<span data-ttu-id="7764a-103">Aktualisiert ein SSL-Zertifikat für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="7764a-103">Updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="7764a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7764a-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7764a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7764a-105">DESCRIPTION</span></span>
<span data-ttu-id="7764a-106">Das **Cmdlet Set-AzApplicationGatewaySslCertificate** aktualisiert ein SSL-Zertifikat für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="7764a-106">The **Set-AzApplicationGatewaySslCertificate** cmdlet updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="7764a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7764a-107">EXAMPLES</span></span>

### <span data-ttu-id="7764a-108">Beispiel 1: Aktualisieren eines vorhandenen Zertifikats auf dem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="7764a-108">Example 1: Update an existing SSL certificate on Application Gateway</span></span>
```
PS C:\> $appGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="7764a-109">Aktualisieren Sie ein vorhandenes ZERTIFIKAT für das Anwendungsgateway namens ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="7764a-109">Update an existing SSL certificate for the application gateway named ApplicationGateway01.</span></span>

### <span data-ttu-id="7764a-110">Beispiel 2: Aktualisieren eines vorhandenen SSL-Zertifikats mit geheimer SchlüsselVault -Version (version-less secretId) auf dem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="7764a-110">Example 2: Update an existing SSL certificate using KeyVault Secret (version-less secretId) on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="7764a-111">Holen Sie sich den Geheimen, und aktualisieren Sie ein vorhandenes SSL-Zertifikat mithilfe `Set-AzApplicationGatewaySslCertificate` von .</span><span class="sxs-lookup"><span data-stu-id="7764a-111">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>

### <span data-ttu-id="7764a-112">Beispiel 3: Aktualisieren eines vorhandenen SSL-Zertifikats mit dem geheimen SchlüsselVault auf dem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="7764a-112">Example 3: Update an existing SSL certificate using KeyVault Secret on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="7764a-113">Holen Sie sich den Geheimen, und aktualisieren Sie ein vorhandenes SSL-Zertifikat mithilfe `Set-AzApplicationGatewaySslCertificate` von .</span><span class="sxs-lookup"><span data-stu-id="7764a-113">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="7764a-114">Hinweis: Wenn das Anwendungsgateway das Zertifikat mit KeyVault synchronisieren muss, geben Sie die version-less secretId an.</span><span class="sxs-lookup"><span data-stu-id="7764a-114">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="7764a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7764a-115">PARAMETERS</span></span>

### <span data-ttu-id="7764a-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7764a-116">-ApplicationGateway</span></span>
<span data-ttu-id="7764a-117">Gibt das Anwendungsgateway an, dem das Zertifikat für secure Socket Layer (SSL) zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7764a-117">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7764a-118">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="7764a-118">-CertificateFile</span></span>
<span data-ttu-id="7764a-119">Gibt den Pfad des SSL-Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="7764a-119">Specifies the path of the SSL certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7764a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7764a-120">-DefaultProfile</span></span>
<span data-ttu-id="7764a-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7764a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7764a-122">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="7764a-122">-KeyVaultSecretId</span></span>
<span data-ttu-id="7764a-123">SecretId (URI) des geheimen Schlüssels (KeyVault Secret).</span><span class="sxs-lookup"><span data-stu-id="7764a-123">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="7764a-124">Verwenden Sie diese Option, wenn eine bestimmte Version des geheimen Schlüssels verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="7764a-124">Use this option when a specific version of secret needs to be used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7764a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7764a-125">-Name</span></span>
<span data-ttu-id="7764a-126">Gibt den Namen des SSL-Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="7764a-126">Specifies the name of the SSL certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7764a-127">-Password</span><span class="sxs-lookup"><span data-stu-id="7764a-127">-Password</span></span>
<span data-ttu-id="7764a-128">Gibt das Kennwort des SSL-Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="7764a-128">Specifies the password of the SSL certificate.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7764a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7764a-129">CommonParameters</span></span>
<span data-ttu-id="7764a-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7764a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7764a-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7764a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7764a-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7764a-132">INPUTS</span></span>

### <span data-ttu-id="7764a-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7764a-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7764a-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7764a-134">OUTPUTS</span></span>

### <span data-ttu-id="7764a-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7764a-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7764a-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7764a-136">NOTES</span></span>

## <span data-ttu-id="7764a-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7764a-137">RELATED LINKS</span></span>

[<span data-ttu-id="7764a-138">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7764a-138">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="7764a-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7764a-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="7764a-140">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7764a-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="7764a-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7764a-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)


