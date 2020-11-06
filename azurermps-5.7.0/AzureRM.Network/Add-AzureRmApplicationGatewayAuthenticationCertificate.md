---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 317fd5bf8306416ad4cbef3d1fb64d56d556ed1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496481"
---
# <span data-ttu-id="c0431-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c0431-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="c0431-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c0431-102">SYNOPSIS</span></span>
<span data-ttu-id="c0431-103">Fügt ein Authentifizierungszertifikat zu einem Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="c0431-103">Adds an authentication certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0431-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0431-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0431-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c0431-105">DESCRIPTION</span></span>
<span data-ttu-id="c0431-106">Mit dem Cmdlet **Add-AzureRmApplicationGatewayAuthenticationCertificate** wird ein Authentifizierungszertifikat zu einem Azure Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c0431-106">The **Add-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="c0431-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c0431-107">EXAMPLES</span></span>

## <span data-ttu-id="c0431-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0431-108">PARAMETERS</span></span>

### <span data-ttu-id="c0431-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c0431-109">-ApplicationGateway</span></span>
<span data-ttu-id="c0431-110">Gibt den Namen des Anwendungs Gateways an, für das dieses Cmdlet ein Authentifizierungszertifikat hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="c0431-110">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0431-111">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="c0431-111">-CertificateFile</span></span>
<span data-ttu-id="c0431-112">Gibt den Pfad des vom Cmdlet hinzugefügten Authentifizierungszertifikats an.</span><span class="sxs-lookup"><span data-stu-id="c0431-112">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0431-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0431-113">-DefaultProfile</span></span>
<span data-ttu-id="c0431-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c0431-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0431-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c0431-115">-Name</span></span>
<span data-ttu-id="c0431-116">Gibt den Namen eines Zertifikats an, das dieses Cmdlet dem Anwendungsgateway hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="c0431-116">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0431-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c0431-117">-Confirm</span></span>
<span data-ttu-id="c0431-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c0431-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0431-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0431-119">-WhatIf</span></span>
<span data-ttu-id="c0431-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c0431-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0431-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0431-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0431-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0431-122">CommonParameters</span></span>
<span data-ttu-id="c0431-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0431-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0431-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0431-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0431-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c0431-125">INPUTS</span></span>

### <span data-ttu-id="c0431-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c0431-126">System.String</span></span>

## <span data-ttu-id="c0431-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c0431-127">OUTPUTS</span></span>

### <span data-ttu-id="c0431-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c0431-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c0431-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="c0431-129">NOTES</span></span>
* <span data-ttu-id="c0431-130">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="c0431-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c0431-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c0431-131">RELATED LINKS</span></span>

[<span data-ttu-id="c0431-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c0431-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="c0431-133">Neu – AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c0431-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="c0431-134">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c0431-134">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="c0431-135">Satz-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c0431-135">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


