---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 6939f26dc06e0aa5ed56d3e905d30960094e8961
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458887"
---
# <span data-ttu-id="b37bb-101">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b37bb-101">Add-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="b37bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b37bb-102">SYNOPSIS</span></span>
<span data-ttu-id="b37bb-103">Fügt einem Anwendungsgateway ein Zertifikat hinzu.</span><span class="sxs-lookup"><span data-stu-id="b37bb-103">Adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="b37bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b37bb-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b37bb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b37bb-105">DESCRIPTION</span></span>
<span data-ttu-id="b37bb-106">Das **Cmdlet "Add-AzApplicationGatewaySslCertificate"** fügt einem Anwendungsgateway ein SSL-Zertifikat hinzu.</span><span class="sxs-lookup"><span data-stu-id="b37bb-106">The **Add-AzApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="b37bb-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b37bb-107">EXAMPLES</span></span>

### <span data-ttu-id="b37bb-108">Beispiel 1: Hinzufügen eines SSL-Zertifikats mithilfe von pfx zu einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="b37bb-108">Example 1: Add an SSL certificate using pfx to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="b37bb-109">Dieser Befehl ruft ein Anwendungsgateway namens ApplicationGateway01 ab und fügt ihm dann ein #A0 namens Cert01 hinzu.</span><span class="sxs-lookup"><span data-stu-id="b37bb-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

### <span data-ttu-id="b37bb-110">Beispiel 2: Hinzufügen eines SSL-Zertifikats mit dem geheimen SchlüsselVaultschlüssel (version-less secretId) zu einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="b37bb-110">Example 2: Add an SSL certificate using KeyVault Secret (version-less secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.SecretId.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="b37bb-111">Holen Sie sich das Geheimnis, und verweisen Sie in der Adresse darauf, um sie dem `Add-AzApplicationGatewaySslCertificate` Anwendungsgateway mit dem Namen `Cert01` hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b37bb-111">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="b37bb-112">Hinweis: Da hier die Datei "Version-less secretId" bereitgestellt wird, synchronisiert das Anwendungsgateway das Zertifikat in regelmäßigen Abständen mit KeyVault.</span><span class="sxs-lookup"><span data-stu-id="b37bb-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="b37bb-113">Beispiel 3: Hinzufügen eines SSL-Zertifikats mit dem geheimen SchlüsselVault Secret (versioned secretId) zu einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="b37bb-113">Example 3: Add an SSL certificate using KeyVault Secret (versioned secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="b37bb-114">Holen Sie sich das Geheimnis, und verweisen Sie in der Adresse darauf, um sie dem `Add-AzApplicationGatewaySslCertificate` Anwendungsgateway mit dem Namen `Cert01` hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b37bb-114">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="b37bb-115">Hinweis: Wenn das Anwendungsgateway das Zertifikat mit KeyVault synchronisieren muss, geben Sie die version-less secretId an.</span><span class="sxs-lookup"><span data-stu-id="b37bb-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="b37bb-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b37bb-116">PARAMETERS</span></span>

### <span data-ttu-id="b37bb-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b37bb-117">-ApplicationGateway</span></span>
<span data-ttu-id="b37bb-118">Gibt den Namen des Anwendungsgateways an, dem dieses Cmdlet ein ZERTIFIKAT hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="b37bb-118">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="b37bb-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="b37bb-119">-CertificateFile</span></span>
<span data-ttu-id="b37bb-120">Gibt die ".pfx"-Datei eines SSL-Zertifikats an, das von diesem Cmdlet hinzufügt wird.</span><span class="sxs-lookup"><span data-stu-id="b37bb-120">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="b37bb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b37bb-121">-DefaultProfile</span></span>
<span data-ttu-id="b37bb-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b37bb-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b37bb-123">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="b37bb-123">-KeyVaultSecretId</span></span>
<span data-ttu-id="b37bb-124">SecretId (URI) des geheimen Schlüsselvaultschlüssels.</span><span class="sxs-lookup"><span data-stu-id="b37bb-124">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="b37bb-125">Verwenden Sie diese Option, wenn eine bestimmte Version des geheimen Schlüssels verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="b37bb-125">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="b37bb-126">-Name</span><span class="sxs-lookup"><span data-stu-id="b37bb-126">-Name</span></span>
<span data-ttu-id="b37bb-127">Gibt den Namen des SSL-Zertifikats an, das von diesem Cmdlet hinzufügt wird.</span><span class="sxs-lookup"><span data-stu-id="b37bb-127">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="b37bb-128">-Password</span><span class="sxs-lookup"><span data-stu-id="b37bb-128">-Password</span></span>
<span data-ttu-id="b37bb-129">Gibt das Kennwort des SSL-Zertifikats an, das von diesem Cmdlet hinzufügt wird.</span><span class="sxs-lookup"><span data-stu-id="b37bb-129">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="b37bb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b37bb-130">CommonParameters</span></span>
<span data-ttu-id="b37bb-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b37bb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b37bb-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b37bb-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b37bb-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b37bb-133">INPUTS</span></span>

### <span data-ttu-id="b37bb-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b37bb-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b37bb-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b37bb-135">OUTPUTS</span></span>

### <span data-ttu-id="b37bb-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b37bb-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b37bb-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b37bb-137">NOTES</span></span>

## <span data-ttu-id="b37bb-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b37bb-138">RELATED LINKS</span></span>

[<span data-ttu-id="b37bb-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b37bb-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b37bb-140">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b37bb-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b37bb-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b37bb-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b37bb-142">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b37bb-142">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


