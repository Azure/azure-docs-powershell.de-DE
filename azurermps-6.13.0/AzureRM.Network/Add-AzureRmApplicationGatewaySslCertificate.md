---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: fc4457e23f50dea3d70a3af2115a93e460dc6a1f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502041"
---
# <span data-ttu-id="4bf7b-101">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4bf7b-101">Add-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="4bf7b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4bf7b-102">SYNOPSIS</span></span>
<span data-ttu-id="4bf7b-103">Fügt ein SSL-Zertifikat zu einem Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="4bf7b-103">Adds an SSL certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bf7b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bf7b-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4bf7b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4bf7b-105">DESCRIPTION</span></span>
<span data-ttu-id="4bf7b-106">Mit dem Cmdlet **Add-AzureRmApplicationGatewaySslCertificate** wird ein SSL-Zertifikat zu einem Anwendungsgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4bf7b-106">The **Add-AzureRmApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="4bf7b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4bf7b-107">EXAMPLES</span></span>

### <span data-ttu-id="4bf7b-108">Beispiel 1: Hinzufügen eines SSL-Zertifikats zu einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="4bf7b-108">Example 1: Add an SSL certificate to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $AppGW = Add-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="4bf7b-109">Dieser Befehl ruft ein Anwendungsgateway mit dem Namen ApplicationGateway01 ab und fügt dann ein SSL-Zertifikat mit dem Namen Cert01 hinzu.</span><span class="sxs-lookup"><span data-stu-id="4bf7b-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

## <span data-ttu-id="4bf7b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4bf7b-110">PARAMETERS</span></span>

### <span data-ttu-id="4bf7b-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4bf7b-111">-ApplicationGateway</span></span>
<span data-ttu-id="4bf7b-112">Gibt den Namen des Anwendungs Gateways an, dem dieses Cmdlet ein SSL-Zertifikat hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="4bf7b-112">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="4bf7b-113">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="4bf7b-113">-CertificateFile</span></span>
<span data-ttu-id="4bf7b-114">Gibt die PFX-Datei eines SSL-Zertifikats an, das von diesem Cmdlet hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="4bf7b-114">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="4bf7b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bf7b-115">-DefaultProfile</span></span>
<span data-ttu-id="4bf7b-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4bf7b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bf7b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4bf7b-117">-Name</span></span>
<span data-ttu-id="4bf7b-118">Gibt den Namen des SSL-Zertifikats an, das von diesem Cmdlet hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="4bf7b-118">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="4bf7b-119">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="4bf7b-119">-Password</span></span>
<span data-ttu-id="4bf7b-120">Gibt das Kennwort des SSL-Zertifikats an, das von diesem Cmdlet hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="4bf7b-120">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bf7b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bf7b-121">CommonParameters</span></span>
<span data-ttu-id="4bf7b-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bf7b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bf7b-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bf7b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bf7b-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4bf7b-124">INPUTS</span></span>

### <span data-ttu-id="4bf7b-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4bf7b-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="4bf7b-126">Parameter: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4bf7b-126">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="4bf7b-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4bf7b-127">OUTPUTS</span></span>

### <span data-ttu-id="4bf7b-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4bf7b-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4bf7b-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="4bf7b-129">NOTES</span></span>

## <span data-ttu-id="4bf7b-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4bf7b-130">RELATED LINKS</span></span>

[<span data-ttu-id="4bf7b-131">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4bf7b-131">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="4bf7b-132">Neu – AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4bf7b-132">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="4bf7b-133">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4bf7b-133">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="4bf7b-134">Satz-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4bf7b-134">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


