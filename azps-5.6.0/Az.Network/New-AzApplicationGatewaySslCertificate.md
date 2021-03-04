---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 84465161d726108749e09d4a928e22aea8050c92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950144"
---
# <span data-ttu-id="cb23d-101">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cb23d-101">New-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="cb23d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb23d-102">SYNOPSIS</span></span>
<span data-ttu-id="cb23d-103">Erstellt ein SSL-Zertifikat für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="cb23d-103">Creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="cb23d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb23d-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslCertificate -Name <String> [-CertificateFile <String>] [-Password <SecureString>]
 [-KeyVaultSecretId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb23d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cb23d-105">DESCRIPTION</span></span>
<span data-ttu-id="cb23d-106">Das **Cmdlet New-AzApplicationGatewaySslCertificate** erstellt ein SSL-Zertifikat für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="cb23d-106">The **New-AzApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="cb23d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cb23d-107">EXAMPLES</span></span>

### <span data-ttu-id="cb23d-108">Beispiel 1: Erstellen eines SSL-Zertifikats für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="cb23d-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="cb23d-109">Mit diesem Befehl wird ein #A0 namens Cert01 für das Standardanwendungsgateway erstellt und das Ergebnis in der Variablen namens $Cert.</span><span class="sxs-lookup"><span data-stu-id="cb23d-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

### <span data-ttu-id="cb23d-110">Beispiel 2: Erstellen Sie ein SSL-Zertifikat mit KeyVault Secret (version-less secretId), und fügen Sie es einem Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="cb23d-110">Example 2: Create an SSL certificate using KeyVault Secret (version-less secretId) and add to an application gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="cb23d-111">Holen Sie sich den Geheimtipp, und erstellen Sie ein SSL-Zertifikat mit `New-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="cb23d-111">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="cb23d-112">Hinweis: Da hier versions-less secretId bereitgestellt wird, synchronisiert das Anwendungsgateway das Zertifikat in regelmäßigen Abständen mit keyVault.</span><span class="sxs-lookup"><span data-stu-id="cb23d-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="cb23d-113">Beispiel 3: Erstellen Sie ein SSL-Zertifikat mit KeyVault Secret, und fügen Sie es einem Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="cb23d-113">Example 3: Create an SSL certificate using KeyVault Secret and add to an Application Gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="cb23d-114">Holen Sie sich den Geheimtipp, und erstellen Sie ein SSL-Zertifikat mit `New-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="cb23d-114">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="cb23d-115">Hinweis: Wenn das Application Gateway das Zertifikat mit keyVault synchronisiert, geben Sie bitte die version-less secretId an.</span><span class="sxs-lookup"><span data-stu-id="cb23d-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="cb23d-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="cb23d-116">PARAMETERS</span></span>

### <span data-ttu-id="cb23d-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="cb23d-117">-CertificateFile</span></span>
<span data-ttu-id="cb23d-118">Gibt den Pfad der PFX-Datei des von diesem Cmdlet erstellten SSL-Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="cb23d-118">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="cb23d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb23d-119">-DefaultProfile</span></span>
<span data-ttu-id="cb23d-120">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cb23d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb23d-121">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="cb23d-121">-KeyVaultSecretId</span></span>
<span data-ttu-id="cb23d-122">SecretId (uri) des KeyVault Secret.</span><span class="sxs-lookup"><span data-stu-id="cb23d-122">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="cb23d-123">Verwenden Sie diese Option, wenn eine bestimmte Version von Secret verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="cb23d-123">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="cb23d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="cb23d-124">-Name</span></span>
<span data-ttu-id="cb23d-125">Gibt den Namen des von diesem Cmdlet erstellten SSL-Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="cb23d-125">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="cb23d-126">-Password</span><span class="sxs-lookup"><span data-stu-id="cb23d-126">-Password</span></span>
<span data-ttu-id="cb23d-127">Gibt das Kennwort des SSL an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="cb23d-127">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="cb23d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb23d-128">CommonParameters</span></span>
<span data-ttu-id="cb23d-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb23d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb23d-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb23d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb23d-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cb23d-131">INPUTS</span></span>

### <span data-ttu-id="cb23d-132">Keine</span><span class="sxs-lookup"><span data-stu-id="cb23d-132">None</span></span>

## <span data-ttu-id="cb23d-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cb23d-133">OUTPUTS</span></span>

### <span data-ttu-id="cb23d-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cb23d-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="cb23d-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="cb23d-135">NOTES</span></span>

## <span data-ttu-id="cb23d-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="cb23d-136">RELATED LINKS</span></span>

[<span data-ttu-id="cb23d-137">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cb23d-137">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="cb23d-138">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cb23d-138">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="cb23d-139">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cb23d-139">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="cb23d-140">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cb23d-140">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


