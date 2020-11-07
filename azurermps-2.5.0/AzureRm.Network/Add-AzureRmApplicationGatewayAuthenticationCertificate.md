---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 4d664018592f05203c684a896f0a0701940301a6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849640"
---
# <span data-ttu-id="d3f6c-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d3f6c-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="d3f6c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d3f6c-102">SYNOPSIS</span></span>
<span data-ttu-id="d3f6c-103">Fügt ein Authentifizierungszertifikat zu einem Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="d3f6c-103">Adds an authentication certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3f6c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3f6c-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d3f6c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d3f6c-105">DESCRIPTION</span></span>
<span data-ttu-id="d3f6c-106">Mit dem Cmdlet **Add-AzureRmApplicationGatewayAuthenticationCertificate** wird ein Authentifizierungszertifikat zu einem Azure Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d3f6c-106">The **Add-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="d3f6c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d3f6c-107">EXAMPLES</span></span>

### <span data-ttu-id="d3f6c-108">1:</span><span class="sxs-lookup"><span data-stu-id="d3f6c-108">1:</span></span>
```

```

## <span data-ttu-id="d3f6c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3f6c-109">PARAMETERS</span></span>

### <span data-ttu-id="d3f6c-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d3f6c-110">-ApplicationGateway</span></span>
<span data-ttu-id="d3f6c-111">Gibt den Namen des Anwendungs Gateways an, für das dieses Cmdlet ein Authentifizierungszertifikat hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="d3f6c-111">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="d3f6c-112">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="d3f6c-112">-CertificateFile</span></span>
<span data-ttu-id="d3f6c-113">Gibt den Pfad des vom Cmdlet hinzugefügten Authentifizierungszertifikats an.</span><span class="sxs-lookup"><span data-stu-id="d3f6c-113">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="d3f6c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3f6c-114">-DefaultProfile</span></span>
<span data-ttu-id="d3f6c-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d3f6c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3f6c-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d3f6c-116">-Name</span></span>
<span data-ttu-id="d3f6c-117">Gibt den Namen eines Zertifikats an, das dieses Cmdlet dem Anwendungsgateway hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="d3f6c-117">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="d3f6c-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d3f6c-118">-Confirm</span></span>
<span data-ttu-id="d3f6c-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d3f6c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3f6c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3f6c-120">-WhatIf</span></span>
<span data-ttu-id="d3f6c-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d3f6c-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3f6c-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d3f6c-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3f6c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3f6c-123">CommonParameters</span></span>
<span data-ttu-id="d3f6c-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3f6c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3f6c-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3f6c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3f6c-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d3f6c-126">INPUTS</span></span>

### <span data-ttu-id="d3f6c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d3f6c-127">System.String</span></span>

## <span data-ttu-id="d3f6c-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d3f6c-128">OUTPUTS</span></span>

### <span data-ttu-id="d3f6c-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d3f6c-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d3f6c-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="d3f6c-130">NOTES</span></span>
* <span data-ttu-id="d3f6c-131">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="d3f6c-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="d3f6c-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d3f6c-132">RELATED LINKS</span></span>

[<span data-ttu-id="d3f6c-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d3f6c-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="d3f6c-134">Neu – AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d3f6c-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="d3f6c-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d3f6c-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="d3f6c-136">Satz-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d3f6c-136">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


