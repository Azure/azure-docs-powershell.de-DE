---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 6939f26dc06e0aa5ed56d3e905d30960094e8961
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172980"
---
# <span data-ttu-id="e4510-101">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e4510-101">Add-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="e4510-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4510-102">SYNOPSIS</span></span>
<span data-ttu-id="e4510-103">Fügt einem Anwendungsgateway ein Zertifikat hinzu.</span><span class="sxs-lookup"><span data-stu-id="e4510-103">Adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="e4510-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4510-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4510-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4510-105">DESCRIPTION</span></span>
<span data-ttu-id="e4510-106">Das **Cmdlet "Add-AzApplicationGatewaySslCertificate"** fügt einem Anwendungsgateway ein SSL-Zertifikat hinzu.</span><span class="sxs-lookup"><span data-stu-id="e4510-106">The **Add-AzApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="e4510-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e4510-107">EXAMPLES</span></span>

### <span data-ttu-id="e4510-108">Beispiel 1: Hinzufügen eines SSL-Zertifikats mithilfe von pfx zu einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="e4510-108">Example 1: Add an SSL certificate using pfx to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="e4510-109">Dieser Befehl ruft ein Anwendungsgateway namens ApplicationGateway01 ab und fügt ihm dann ein #A0 namens Cert01 hinzu.</span><span class="sxs-lookup"><span data-stu-id="e4510-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

### <span data-ttu-id="e4510-110">Beispiel 2: Hinzufügen eines SSL-Zertifikats mit dem geheimen SchlüsselVaultschlüssel (version-less secretId) zu einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="e4510-110">Example 2: Add an SSL certificate using KeyVault Secret (version-less secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.SecretId.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="e4510-111">Holen Sie sich das Geheimnis, und verweisen Sie darauf, um es `Add-AzApplicationGatewaySslCertificate` dem Anwendungsgateway mit dem Namen `Cert01` hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e4510-111">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="e4510-112">Hinweis: Da hier die Datei "Version-less secretId" bereitgestellt wird, synchronisiert das Anwendungsgateway das Zertifikat in regelmäßigen Abständen mit KeyVault.</span><span class="sxs-lookup"><span data-stu-id="e4510-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="e4510-113">Beispiel 3: Hinzufügen eines SSL-Zertifikats mit dem geheimen SchlüsselVault (versioned secretId) zu einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="e4510-113">Example 3: Add an SSL certificate using KeyVault Secret (versioned secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="e4510-114">Holen Sie sich das Geheimnis, und verweisen Sie darauf, um es `Add-AzApplicationGatewaySslCertificate` dem Anwendungsgateway mit dem Namen `Cert01` hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e4510-114">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="e4510-115">Hinweis: Wenn anwendungsgateway das Zertifikat mit KeyVault synchronisiert, geben Sie die version-less secretId an.</span><span class="sxs-lookup"><span data-stu-id="e4510-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="e4510-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4510-116">PARAMETERS</span></span>

### <span data-ttu-id="e4510-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e4510-117">-ApplicationGateway</span></span>
<span data-ttu-id="e4510-118">Gibt den Namen des Anwendungsgateways an, dem dieses Cmdlet ein ZERTIFIKAT hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="e4510-118">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="e4510-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="e4510-119">-CertificateFile</span></span>
<span data-ttu-id="e4510-120">Gibt die ".pfx"-Datei eines SSL-Zertifikats an, das von diesem Cmdlet hinzufügt wird.</span><span class="sxs-lookup"><span data-stu-id="e4510-120">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="e4510-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4510-121">-DefaultProfile</span></span>
<span data-ttu-id="e4510-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e4510-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4510-123">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="e4510-123">-KeyVaultSecretId</span></span>
<span data-ttu-id="e4510-124">SecretId (URI) des geheimen Schlüssels (KeyVault Secret).</span><span class="sxs-lookup"><span data-stu-id="e4510-124">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="e4510-125">Verwenden Sie diese Option, wenn eine bestimmte Version des geheimen Schlüssels verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="e4510-125">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="e4510-126">-Name</span><span class="sxs-lookup"><span data-stu-id="e4510-126">-Name</span></span>
<span data-ttu-id="e4510-127">Gibt den Namen des SSL-Zertifikats an, das von diesem Cmdlet hinzufügt wird.</span><span class="sxs-lookup"><span data-stu-id="e4510-127">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="e4510-128">-Password</span><span class="sxs-lookup"><span data-stu-id="e4510-128">-Password</span></span>
<span data-ttu-id="e4510-129">Gibt das Kennwort des SSL-Zertifikats an, das von diesem Cmdlet hinzufügt wird.</span><span class="sxs-lookup"><span data-stu-id="e4510-129">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="e4510-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4510-130">CommonParameters</span></span>
<span data-ttu-id="e4510-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4510-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4510-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4510-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4510-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e4510-133">INPUTS</span></span>

### <span data-ttu-id="e4510-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e4510-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e4510-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e4510-135">OUTPUTS</span></span>

### <span data-ttu-id="e4510-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e4510-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e4510-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e4510-137">NOTES</span></span>

## <span data-ttu-id="e4510-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e4510-138">RELATED LINKS</span></span>

[<span data-ttu-id="e4510-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e4510-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e4510-140">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e4510-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e4510-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e4510-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e4510-142">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e4510-142">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


