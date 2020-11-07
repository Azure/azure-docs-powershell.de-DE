---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 36f45cc5c49cbdf3183f34068fd5b87000c1ede5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660240"
---
# <span data-ttu-id="763e4-101">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="763e4-101">Set-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="763e4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="763e4-102">SYNOPSIS</span></span>
<span data-ttu-id="763e4-103">Aktualisiert ein SSL-Zertifikat für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="763e4-103">Updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="763e4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="763e4-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="763e4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="763e4-105">DESCRIPTION</span></span>
<span data-ttu-id="763e4-106">Das Cmdlet " **Satz-AzApplicationGatewaySslCertificate** " aktualisiert ein SSL-Zertifikat für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="763e4-106">The **Set-AzApplicationGatewaySslCertificate** cmdlet updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="763e4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="763e4-107">EXAMPLES</span></span>

### <span data-ttu-id="763e4-108">Beispiel 1: Aktualisieren eines vorhandenen SSL-Zertifikats auf dem Anwendungs Gateway</span><span class="sxs-lookup"><span data-stu-id="763e4-108">Example 1: Update an existing SSL certificate on Application Gateway</span></span>
```
PS C:\> $appGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="763e4-109">Aktualisieren Sie ein vorhandenes SSL-Zertifikat für das Anwendungsgateway mit dem Namen ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="763e4-109">Update an existing SSL certificate for the application gateway named ApplicationGateway01.</span></span>

### <span data-ttu-id="763e4-110">Beispiel 2: Aktualisieren eines vorhandenen SSL-Zertifikats unter Verwendung von keyvault Secret (Version-less-Secret-Code) auf dem Anwendungs Gateway</span><span class="sxs-lookup"><span data-stu-id="763e4-110">Example 2: Update an existing SSL certificate using KeyVault Secret (version-less secretId) on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="763e4-111">Besorgen Sie sich das Geheimnis und aktualisieren Sie ein vorhandenes SSL-Zertifikat mit `Set-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="763e4-111">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>

### <span data-ttu-id="763e4-112">Beispiel 3: Aktualisieren eines vorhandenen SSL-Zertifikats mithilfe von keyvault Secret auf dem Anwendungs Gateway</span><span class="sxs-lookup"><span data-stu-id="763e4-112">Example 3: Update an existing SSL certificate using KeyVault Secret on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="763e4-113">Besorgen Sie sich das Geheimnis und aktualisieren Sie ein vorhandenes SSL-Zertifikat mit `Set-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="763e4-113">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="763e4-114">Hinweis: Wenn es erforderlich ist, dass Application Gateway das Zertifikat mit dem keyvault synchronisiert, geben Sie bitte den versionslosen Geheimdienst an.</span><span class="sxs-lookup"><span data-stu-id="763e4-114">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="763e4-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="763e4-115">PARAMETERS</span></span>

### <span data-ttu-id="763e4-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="763e4-116">-ApplicationGateway</span></span>
<span data-ttu-id="763e4-117">Gibt das Anwendungsgateway an, dem das Secure Socket Layer (SSL)-Zertifikat zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="763e4-117">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="763e4-118">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="763e4-118">-CertificateFile</span></span>
<span data-ttu-id="763e4-119">Gibt den Pfad des SSL-Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="763e4-119">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="763e4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="763e4-120">-DefaultProfile</span></span>
<span data-ttu-id="763e4-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="763e4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="763e4-122">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="763e4-122">-KeyVaultSecretId</span></span>
<span data-ttu-id="763e4-123">Geheim-URL (URI) des keyvault-Geheimnisses.</span><span class="sxs-lookup"><span data-stu-id="763e4-123">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="763e4-124">Verwenden Sie diese Option, wenn eine bestimmte Version von Secret verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="763e4-124">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="763e4-125">-Name</span><span class="sxs-lookup"><span data-stu-id="763e4-125">-Name</span></span>
<span data-ttu-id="763e4-126">Gibt den Namen des SSL-Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="763e4-126">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="763e4-127">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="763e4-127">-Password</span></span>
<span data-ttu-id="763e4-128">Gibt das Kennwort des SSL-Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="763e4-128">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="763e4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="763e4-129">CommonParameters</span></span>
<span data-ttu-id="763e4-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="763e4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="763e4-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="763e4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="763e4-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="763e4-132">INPUTS</span></span>

### <span data-ttu-id="763e4-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="763e4-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="763e4-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="763e4-134">OUTPUTS</span></span>

### <span data-ttu-id="763e4-135">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="763e4-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="763e4-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="763e4-136">NOTES</span></span>

## <span data-ttu-id="763e4-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="763e4-137">RELATED LINKS</span></span>

[<span data-ttu-id="763e4-138">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="763e4-138">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="763e4-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="763e4-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="763e4-140">Neu – AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="763e4-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="763e4-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="763e4-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)


