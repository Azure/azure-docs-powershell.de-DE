---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 6652da4491bc503ecc2d0c8ee016416cefbff172
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841891"
---
# <span data-ttu-id="5cf95-101">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5cf95-101">Add-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="5cf95-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5cf95-102">SYNOPSIS</span></span>
<span data-ttu-id="5cf95-103">Fügt ein Authentifizierungszertifikat zu einem Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="5cf95-103">Adds an authentication certificate to an application gateway.</span></span>

## <span data-ttu-id="5cf95-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5cf95-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5cf95-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5cf95-105">DESCRIPTION</span></span>
<span data-ttu-id="5cf95-106">Mit dem Cmdlet **Add-AzApplicationGatewayAuthenticationCertificate** wird ein Authentifizierungszertifikat zu einem Azure Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5cf95-106">The **Add-AzApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="5cf95-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5cf95-107">EXAMPLES</span></span>

### <span data-ttu-id="5cf95-108">1:</span><span class="sxs-lookup"><span data-stu-id="5cf95-108">1:</span></span>
```

```

## <span data-ttu-id="5cf95-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5cf95-109">PARAMETERS</span></span>

### <span data-ttu-id="5cf95-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5cf95-110">-ApplicationGateway</span></span>
<span data-ttu-id="5cf95-111">Gibt den Namen des Anwendungs Gateways an, für das dieses Cmdlet ein Authentifizierungszertifikat hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="5cf95-111">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="5cf95-112">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="5cf95-112">-CertificateFile</span></span>
<span data-ttu-id="5cf95-113">Gibt den Pfad des vom Cmdlet hinzugefügten Authentifizierungszertifikats an.</span><span class="sxs-lookup"><span data-stu-id="5cf95-113">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="5cf95-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cf95-114">-DefaultProfile</span></span>
<span data-ttu-id="5cf95-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5cf95-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cf95-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5cf95-116">-Name</span></span>
<span data-ttu-id="5cf95-117">Gibt den Namen eines Zertifikats an, das dieses Cmdlet dem Anwendungsgateway hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="5cf95-117">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="5cf95-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5cf95-118">-Confirm</span></span>
<span data-ttu-id="5cf95-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5cf95-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cf95-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cf95-120">-WhatIf</span></span>
<span data-ttu-id="5cf95-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5cf95-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cf95-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5cf95-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cf95-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cf95-123">CommonParameters</span></span>
<span data-ttu-id="5cf95-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cf95-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cf95-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cf95-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cf95-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5cf95-126">INPUTS</span></span>

### <span data-ttu-id="5cf95-127">System. String</span><span class="sxs-lookup"><span data-stu-id="5cf95-127">System.String</span></span>

## <span data-ttu-id="5cf95-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5cf95-128">OUTPUTS</span></span>

### <span data-ttu-id="5cf95-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5cf95-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5cf95-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="5cf95-130">NOTES</span></span>
* <span data-ttu-id="5cf95-131">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="5cf95-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="5cf95-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5cf95-132">RELATED LINKS</span></span>

[<span data-ttu-id="5cf95-133">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5cf95-133">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5cf95-134">Neu – AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5cf95-134">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5cf95-135">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5cf95-135">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5cf95-136">Satz-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5cf95-136">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


