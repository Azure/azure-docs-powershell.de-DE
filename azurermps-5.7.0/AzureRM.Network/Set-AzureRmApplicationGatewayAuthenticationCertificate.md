---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: ebeff6e8c8542d487305ec7570a30c26689e6885
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505781"
---
# <span data-ttu-id="f039b-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f039b-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="f039b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f039b-102">SYNOPSIS</span></span>
<span data-ttu-id="f039b-103">Aktualisiert ein Authentifizierungszertifikat für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="f039b-103">Updates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f039b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f039b-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f039b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f039b-105">DESCRIPTION</span></span>
<span data-ttu-id="f039b-106">Das Cmdlet " **Satz-AzureRmApplicationGatewayAuthenticationCertificate** " aktualisiert ein Authentifizierungszertifikat für ein Azure Application-Gateway.</span><span class="sxs-lookup"><span data-stu-id="f039b-106">The **Set-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="f039b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f039b-107">EXAMPLES</span></span>

## <span data-ttu-id="f039b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f039b-108">PARAMETERS</span></span>

### <span data-ttu-id="f039b-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f039b-109">-ApplicationGateway</span></span>
<span data-ttu-id="f039b-110">Gibt den Namen des Anwendungs Gateways an, für das dieses Cmdlet ein Authentifizierungszertifikat aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f039b-110">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="f039b-111">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="f039b-111">-CertificateFile</span></span>
<span data-ttu-id="f039b-112">Gibt den Pfad der Authentifizierungszertifikatdatei an, mit der dieses Cmdlet das Zertifikat aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f039b-112">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="f039b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f039b-113">-DefaultProfile</span></span>
<span data-ttu-id="f039b-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f039b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f039b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f039b-115">-Name</span></span>
<span data-ttu-id="f039b-116">Gibt den Namen des Authentifizierungszertifikats an, das vom Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="f039b-116">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="f039b-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f039b-117">-Confirm</span></span>
<span data-ttu-id="f039b-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f039b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f039b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f039b-119">-WhatIf</span></span>
<span data-ttu-id="f039b-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f039b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f039b-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f039b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f039b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f039b-122">CommonParameters</span></span>
<span data-ttu-id="f039b-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f039b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f039b-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f039b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f039b-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f039b-125">INPUTS</span></span>

### <span data-ttu-id="f039b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f039b-126">System.String</span></span>

## <span data-ttu-id="f039b-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f039b-127">OUTPUTS</span></span>

### <span data-ttu-id="f039b-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f039b-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f039b-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="f039b-129">NOTES</span></span>
* <span data-ttu-id="f039b-130">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="f039b-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="f039b-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f039b-131">RELATED LINKS</span></span>

[<span data-ttu-id="f039b-132">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f039b-132">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f039b-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f039b-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f039b-134">Neu – AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f039b-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f039b-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f039b-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)


