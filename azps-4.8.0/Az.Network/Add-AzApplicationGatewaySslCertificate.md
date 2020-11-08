---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 47c2f4dcb3e18c969c57d037d9e4f0104b1980f3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009736"
---
# <span data-ttu-id="38be2-101">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="38be2-101">Add-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="38be2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="38be2-102">SYNOPSIS</span></span>
<span data-ttu-id="38be2-103">Fügt ein SSL-Zertifikat zu einem Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="38be2-103">Adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="38be2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="38be2-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38be2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="38be2-105">DESCRIPTION</span></span>
<span data-ttu-id="38be2-106">Mit dem Cmdlet **Add-AzApplicationGatewaySslCertificate** wird ein SSL-Zertifikat zu einem Anwendungsgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="38be2-106">The **Add-AzApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="38be2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="38be2-107">EXAMPLES</span></span>

### <span data-ttu-id="38be2-108">Beispiel 1: Hinzufügen eines SSL-Zertifikats mit PFX zu einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="38be2-108">Example 1: Add an SSL certificate using pfx to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="38be2-109">Dieser Befehl ruft ein Anwendungsgateway mit dem Namen ApplicationGateway01 ab und fügt dann ein SSL-Zertifikat mit dem Namen Cert01 hinzu.</span><span class="sxs-lookup"><span data-stu-id="38be2-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

### <span data-ttu-id="38be2-110">Beispiel 2: Fügen Sie ein SSL-Zertifikat unter Verwendung von keyvault Secret (Version-less Secret-Code) zu einem Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="38be2-110">Example 2: Add an SSL certificate using KeyVault Secret (version-less secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.SecretId.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="38be2-111">Rufen Sie das Geheimnis ab, und verweisen Sie es in der `Add-AzApplicationGatewaySslCertificate` , um es dem Anwendungs Gateway mit dem Namen hinzuzufügen `Cert01` .</span><span class="sxs-lookup"><span data-stu-id="38be2-111">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="38be2-112">Hinweis: Da Version-less-geheim-Nr hier bereitgestellt wird, synchronisiert Application Gateway das Zertifikat in regelmäßigen Abständen mit dem keyvault.</span><span class="sxs-lookup"><span data-stu-id="38be2-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="38be2-113">Beispiel 3: Hinzufügen eines SSL-Zertifikats unter Verwendung von keyvault Secret (Versionsverwaltung) zu einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="38be2-113">Example 3: Add an SSL certificate using KeyVault Secret (versioned secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="38be2-114">Rufen Sie das Geheimnis ab, und verweisen Sie es in der `Add-AzApplicationGatewaySslCertificate` , um es dem Anwendungs Gateway mit dem Namen hinzuzufügen `Cert01` .</span><span class="sxs-lookup"><span data-stu-id="38be2-114">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="38be2-115">Hinweis: Wenn es erforderlich ist, dass Application Gateway das Zertifikat mit dem keyvault synchronisiert, geben Sie bitte den versionslosen Geheimdienst an.</span><span class="sxs-lookup"><span data-stu-id="38be2-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="38be2-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="38be2-116">PARAMETERS</span></span>

### <span data-ttu-id="38be2-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="38be2-117">-ApplicationGateway</span></span>
<span data-ttu-id="38be2-118">Gibt den Namen des Anwendungs Gateways an, dem dieses Cmdlet ein SSL-Zertifikat hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="38be2-118">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="38be2-119">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="38be2-119">-CertificateFile</span></span>
<span data-ttu-id="38be2-120">Gibt die PFX-Datei eines SSL-Zertifikats an, das von diesem Cmdlet hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="38be2-120">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="38be2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38be2-121">-DefaultProfile</span></span>
<span data-ttu-id="38be2-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="38be2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38be2-123">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="38be2-123">-KeyVaultSecretId</span></span>
<span data-ttu-id="38be2-124">Geheim-URL (URI) des keyvault-Geheimnisses.</span><span class="sxs-lookup"><span data-stu-id="38be2-124">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="38be2-125">Verwenden Sie diese Option, wenn eine bestimmte Version von Secret verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="38be2-125">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="38be2-126">-Name</span><span class="sxs-lookup"><span data-stu-id="38be2-126">-Name</span></span>
<span data-ttu-id="38be2-127">Gibt den Namen des SSL-Zertifikats an, das von diesem Cmdlet hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="38be2-127">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="38be2-128">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="38be2-128">-Password</span></span>
<span data-ttu-id="38be2-129">Gibt das Kennwort des SSL-Zertifikats an, das von diesem Cmdlet hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="38be2-129">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="38be2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38be2-130">CommonParameters</span></span>
<span data-ttu-id="38be2-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38be2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38be2-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38be2-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38be2-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="38be2-133">INPUTS</span></span>

### <span data-ttu-id="38be2-134">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="38be2-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="38be2-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="38be2-135">OUTPUTS</span></span>

### <span data-ttu-id="38be2-136">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="38be2-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="38be2-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="38be2-137">NOTES</span></span>

## <span data-ttu-id="38be2-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="38be2-138">RELATED LINKS</span></span>

[<span data-ttu-id="38be2-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="38be2-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="38be2-140">Neu – AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="38be2-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="38be2-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="38be2-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="38be2-142">Satz-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="38be2-142">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


