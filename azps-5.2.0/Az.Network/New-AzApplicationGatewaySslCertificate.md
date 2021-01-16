---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 31d9c5d5c627f4d3451c47584b09760655e77342
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306056"
---
# <span data-ttu-id="9bcfc-101">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9bcfc-101">New-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="9bcfc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bcfc-102">SYNOPSIS</span></span>
<span data-ttu-id="9bcfc-103">Erstellt ein SSL-Zertifikat für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="9bcfc-103">Creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="9bcfc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9bcfc-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslCertificate -Name <String> [-CertificateFile <String>] [-Password <SecureString>]
 [-KeyVaultSecretId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bcfc-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9bcfc-105">DESCRIPTION</span></span>
<span data-ttu-id="9bcfc-106">Das **Cmdlet "New-AzApplicationGatewaySslCertificate"** erstellt ein SSL-Zertifikat für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="9bcfc-106">The **New-AzApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="9bcfc-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9bcfc-107">EXAMPLES</span></span>

### <span data-ttu-id="9bcfc-108">Beispiel 1: Erstellen eines SSL-Zertifikats für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="9bcfc-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="9bcfc-109">Dieser Befehl erstellt ein #A0 namens Cert01 für das Standardanwendungsgateway und speichert das Ergebnis in der Variablen namens $Cert.</span><span class="sxs-lookup"><span data-stu-id="9bcfc-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

### <span data-ttu-id="9bcfc-110">Beispiel 2: Erstellen sie ein SSL-Zertifikat mit dem geheimen Schlüsselvault Secret (version-less secretId), und fügen Sie es einem Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="9bcfc-110">Example 2: Create an SSL certificate using KeyVault Secret (version-less secretId) and add to an application gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="9bcfc-111">Machen Sie sich das Geheimnis, und erstellen Sie ein SSL-Zertifikat mithilfe `New-AzApplicationGatewaySslCertificate` von .</span><span class="sxs-lookup"><span data-stu-id="9bcfc-111">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="9bcfc-112">Hinweis: Da hier die Datei "Version-less secretId" bereitgestellt wird, synchronisiert das Anwendungsgateway das Zertifikat in regelmäßigen Abständen mit KeyVault.</span><span class="sxs-lookup"><span data-stu-id="9bcfc-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="9bcfc-113">Beispiel 3: Erstellen Sie ein SSL-Zertifikat, indem Sie den geheimen Schlüssel "KeyVault Secret" verwenden, und fügen Sie es einem Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="9bcfc-113">Example 3: Create an SSL certificate using KeyVault Secret and add to an Application Gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="9bcfc-114">Machen Sie sich das Geheimnis, und erstellen Sie ein SSL-Zertifikat mithilfe `New-AzApplicationGatewaySslCertificate` von .</span><span class="sxs-lookup"><span data-stu-id="9bcfc-114">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="9bcfc-115">Hinweis: Wenn anwendungsgateway das Zertifikat mit KeyVault synchronisiert, geben Sie die version-less secretId an.</span><span class="sxs-lookup"><span data-stu-id="9bcfc-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="9bcfc-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9bcfc-116">PARAMETERS</span></span>

### <span data-ttu-id="9bcfc-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="9bcfc-117">-CertificateFile</span></span>
<span data-ttu-id="9bcfc-118">Gibt den Pfad der Datei "PFX" des von diesem Cmdlet erstellten SSL-Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="9bcfc-118">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9bcfc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bcfc-119">-DefaultProfile</span></span>
<span data-ttu-id="9bcfc-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9bcfc-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bcfc-121">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="9bcfc-121">-KeyVaultSecretId</span></span>
<span data-ttu-id="9bcfc-122">SecretId (URI) des geheimen Schlüsselvaultschlüssels.</span><span class="sxs-lookup"><span data-stu-id="9bcfc-122">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="9bcfc-123">Verwenden Sie diese Option, wenn eine bestimmte Version des geheimen Schlüssels verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="9bcfc-123">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="9bcfc-124">-Name</span><span class="sxs-lookup"><span data-stu-id="9bcfc-124">-Name</span></span>
<span data-ttu-id="9bcfc-125">Gibt den Namen des von diesem Cmdlet erstellten SSL-Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="9bcfc-125">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9bcfc-126">-Password</span><span class="sxs-lookup"><span data-stu-id="9bcfc-126">-Password</span></span>
<span data-ttu-id="9bcfc-127">Gibt das Kennwort für ssl an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="9bcfc-127">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9bcfc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bcfc-128">CommonParameters</span></span>
<span data-ttu-id="9bcfc-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bcfc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bcfc-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bcfc-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bcfc-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9bcfc-131">INPUTS</span></span>

### <span data-ttu-id="9bcfc-132">Keine</span><span class="sxs-lookup"><span data-stu-id="9bcfc-132">None</span></span>

## <span data-ttu-id="9bcfc-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9bcfc-133">OUTPUTS</span></span>

### <span data-ttu-id="9bcfc-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9bcfc-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="9bcfc-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9bcfc-135">NOTES</span></span>

## <span data-ttu-id="9bcfc-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9bcfc-136">RELATED LINKS</span></span>

[<span data-ttu-id="9bcfc-137">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9bcfc-137">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9bcfc-138">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9bcfc-138">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9bcfc-139">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9bcfc-139">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9bcfc-140">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9bcfc-140">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


