---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 3c70fcd0e04b566ff1cd3297525d3ed2c9ed95ba
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850580"
---
# <span data-ttu-id="dc85e-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="dc85e-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="dc85e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dc85e-102">SYNOPSIS</span></span>
<span data-ttu-id="dc85e-103">Aktualisiert ein Authentifizierungszertifikat für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="dc85e-103">Updates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc85e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc85e-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dc85e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc85e-105">DESCRIPTION</span></span>
<span data-ttu-id="dc85e-106">Das Cmdlet " **Satz-AzureRmApplicationGatewayAuthenticationCertificate** " aktualisiert ein Authentifizierungszertifikat für ein Azure Application-Gateway.</span><span class="sxs-lookup"><span data-stu-id="dc85e-106">The **Set-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="dc85e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dc85e-107">EXAMPLES</span></span>

### <span data-ttu-id="dc85e-108">1:</span><span class="sxs-lookup"><span data-stu-id="dc85e-108">1:</span></span>
```

```

## <span data-ttu-id="dc85e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc85e-109">PARAMETERS</span></span>

### <span data-ttu-id="dc85e-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dc85e-110">-ApplicationGateway</span></span>
<span data-ttu-id="dc85e-111">Gibt den Namen des Anwendungs Gateways an, für das dieses Cmdlet ein Authentifizierungszertifikat aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="dc85e-111">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="dc85e-112">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="dc85e-112">-CertificateFile</span></span>
<span data-ttu-id="dc85e-113">Gibt den Pfad der Authentifizierungszertifikatdatei an, mit der dieses Cmdlet das Zertifikat aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="dc85e-113">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="dc85e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc85e-114">-DefaultProfile</span></span>
<span data-ttu-id="dc85e-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dc85e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc85e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="dc85e-116">-Name</span></span>
<span data-ttu-id="dc85e-117">Gibt den Namen des Authentifizierungszertifikats an, das vom Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="dc85e-117">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="dc85e-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dc85e-118">-Confirm</span></span>
<span data-ttu-id="dc85e-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dc85e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc85e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc85e-120">-WhatIf</span></span>
<span data-ttu-id="dc85e-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dc85e-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc85e-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dc85e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc85e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc85e-123">CommonParameters</span></span>
<span data-ttu-id="dc85e-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc85e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc85e-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc85e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc85e-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dc85e-126">INPUTS</span></span>

### <span data-ttu-id="dc85e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="dc85e-127">System.String</span></span>

## <span data-ttu-id="dc85e-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dc85e-128">OUTPUTS</span></span>

### <span data-ttu-id="dc85e-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dc85e-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dc85e-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="dc85e-130">NOTES</span></span>
* <span data-ttu-id="dc85e-131">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="dc85e-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="dc85e-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dc85e-132">RELATED LINKS</span></span>

[<span data-ttu-id="dc85e-133">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="dc85e-133">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="dc85e-134">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="dc85e-134">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="dc85e-135">Neu – AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="dc85e-135">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="dc85e-136">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="dc85e-136">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)


