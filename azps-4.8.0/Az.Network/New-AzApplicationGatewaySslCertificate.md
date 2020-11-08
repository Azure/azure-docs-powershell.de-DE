---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: a5a1533038f8e11a30dd3fdeedd590b8186597b7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174584"
---
# <span data-ttu-id="b5fd0-101">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b5fd0-101">New-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="b5fd0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b5fd0-102">SYNOPSIS</span></span>
<span data-ttu-id="b5fd0-103">Erstellt ein SSL-Zertifikat für ein Azure Application-Gateway.</span><span class="sxs-lookup"><span data-stu-id="b5fd0-103">Creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="b5fd0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5fd0-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslCertificate -Name <String> [-CertificateFile <String>] [-Password <SecureString>]
 [-KeyVaultSecretId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5fd0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b5fd0-105">DESCRIPTION</span></span>
<span data-ttu-id="b5fd0-106">Das Cmdlet **New-AzApplicationGatewaySslCertificate** erstellt ein SSL-Zertifikat für ein Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="b5fd0-106">The **New-AzApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="b5fd0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b5fd0-107">EXAMPLES</span></span>

### <span data-ttu-id="b5fd0-108">Beispiel 1: Erstellen eines SSL-Zertifikats für ein Azure Application Gateway</span><span class="sxs-lookup"><span data-stu-id="b5fd0-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="b5fd0-109">Dieser Befehl erstellt ein SSL-Zertifikat mit dem Namen "Cert01" für das Standard Anwendungsgateway und speichert das Ergebnis in der Variablen mit dem Namen "$CERT".</span><span class="sxs-lookup"><span data-stu-id="b5fd0-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

### <span data-ttu-id="b5fd0-110">Beispiel 2: Erstellen eines SSL-Zertifikats mit dem Schlüssel "Secret Vault" (Version-less-Verschlüsselung) und hinzufügen zu einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="b5fd0-110">Example 2: Create an SSL certificate using KeyVault Secret (version-less secretId) and add to an application gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="b5fd0-111">Holen Sie sich das Geheimnis und erstellen Sie ein SSL-Zertifikat mit `New-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="b5fd0-111">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="b5fd0-112">Hinweis: Da Version-less-geheim-Nr hier bereitgestellt wird, synchronisiert Application Gateway das Zertifikat in regelmäßigen Abständen mit dem keyvault.</span><span class="sxs-lookup"><span data-stu-id="b5fd0-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="b5fd0-113">Beispiel 3: Erstellen eines SSL-Zertifikats mithilfe von keyvault Secret und hinzufügen zu einem Anwendungs Gateway</span><span class="sxs-lookup"><span data-stu-id="b5fd0-113">Example 3: Create an SSL certificate using KeyVault Secret and add to an Application Gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="b5fd0-114">Holen Sie sich das Geheimnis und erstellen Sie ein SSL-Zertifikat mit `New-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="b5fd0-114">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="b5fd0-115">Hinweis: Wenn es erforderlich ist, dass Application Gateway das Zertifikat mit dem keyvault synchronisiert, geben Sie bitte den versionslosen Geheimdienst an.</span><span class="sxs-lookup"><span data-stu-id="b5fd0-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="b5fd0-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5fd0-116">PARAMETERS</span></span>

### <span data-ttu-id="b5fd0-117">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="b5fd0-117">-CertificateFile</span></span>
<span data-ttu-id="b5fd0-118">Gibt den Pfad der PFX-Datei des SSL-Zertifikats an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b5fd0-118">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b5fd0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5fd0-119">-DefaultProfile</span></span>
<span data-ttu-id="b5fd0-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b5fd0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5fd0-121">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="b5fd0-121">-KeyVaultSecretId</span></span>
<span data-ttu-id="b5fd0-122">Geheim-URL (URI) des keyvault-Geheimnisses.</span><span class="sxs-lookup"><span data-stu-id="b5fd0-122">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="b5fd0-123">Verwenden Sie diese Option, wenn eine bestimmte Version von Secret verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="b5fd0-123">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="b5fd0-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b5fd0-124">-Name</span></span>
<span data-ttu-id="b5fd0-125">Gibt den Namen des SSL-Zertifikats an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b5fd0-125">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b5fd0-126">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="b5fd0-126">-Password</span></span>
<span data-ttu-id="b5fd0-127">Gibt das Kennwort des SSL an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b5fd0-127">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b5fd0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5fd0-128">CommonParameters</span></span>
<span data-ttu-id="b5fd0-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5fd0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5fd0-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5fd0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5fd0-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b5fd0-131">INPUTS</span></span>

### <span data-ttu-id="b5fd0-132">Keine</span><span class="sxs-lookup"><span data-stu-id="b5fd0-132">None</span></span>

## <span data-ttu-id="b5fd0-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b5fd0-133">OUTPUTS</span></span>

### <span data-ttu-id="b5fd0-134">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b5fd0-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="b5fd0-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="b5fd0-135">NOTES</span></span>

## <span data-ttu-id="b5fd0-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b5fd0-136">RELATED LINKS</span></span>

[<span data-ttu-id="b5fd0-137">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b5fd0-137">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b5fd0-138">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b5fd0-138">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b5fd0-139">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b5fd0-139">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b5fd0-140">Satz-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b5fd0-140">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


