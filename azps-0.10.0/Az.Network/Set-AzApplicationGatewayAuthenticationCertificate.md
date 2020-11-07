---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 23b337779da46169be29e3dd6fef55fc70f4f035
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843720"
---
# <span data-ttu-id="b9dff-101">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b9dff-101">Set-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="b9dff-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b9dff-102">SYNOPSIS</span></span>
<span data-ttu-id="b9dff-103">Aktualisiert ein Authentifizierungszertifikat für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="b9dff-103">Updates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="b9dff-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9dff-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b9dff-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b9dff-105">DESCRIPTION</span></span>
<span data-ttu-id="b9dff-106">Das Cmdlet " **Satz-AzApplicationGatewayAuthenticationCertificate** " aktualisiert ein Authentifizierungszertifikat für ein Azure Application-Gateway.</span><span class="sxs-lookup"><span data-stu-id="b9dff-106">The **Set-AzApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="b9dff-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b9dff-107">EXAMPLES</span></span>

### <span data-ttu-id="b9dff-108">1:</span><span class="sxs-lookup"><span data-stu-id="b9dff-108">1:</span></span>
```

```

## <span data-ttu-id="b9dff-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9dff-109">PARAMETERS</span></span>

### <span data-ttu-id="b9dff-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9dff-110">-ApplicationGateway</span></span>
<span data-ttu-id="b9dff-111">Gibt den Namen des Anwendungs Gateways an, für das dieses Cmdlet ein Authentifizierungszertifikat aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b9dff-111">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="b9dff-112">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="b9dff-112">-CertificateFile</span></span>
<span data-ttu-id="b9dff-113">Gibt den Pfad der Authentifizierungszertifikatdatei an, mit der dieses Cmdlet das Zertifikat aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b9dff-113">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="b9dff-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9dff-114">-DefaultProfile</span></span>
<span data-ttu-id="b9dff-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b9dff-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9dff-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b9dff-116">-Name</span></span>
<span data-ttu-id="b9dff-117">Gibt den Namen des Authentifizierungszertifikats an, das vom Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b9dff-117">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="b9dff-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b9dff-118">-Confirm</span></span>
<span data-ttu-id="b9dff-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b9dff-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9dff-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9dff-120">-WhatIf</span></span>
<span data-ttu-id="b9dff-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b9dff-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9dff-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b9dff-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9dff-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9dff-123">CommonParameters</span></span>
<span data-ttu-id="b9dff-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9dff-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9dff-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9dff-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9dff-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b9dff-126">INPUTS</span></span>

### <span data-ttu-id="b9dff-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b9dff-127">System.String</span></span>

## <span data-ttu-id="b9dff-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b9dff-128">OUTPUTS</span></span>

### <span data-ttu-id="b9dff-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9dff-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b9dff-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="b9dff-130">NOTES</span></span>
* <span data-ttu-id="b9dff-131">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="b9dff-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b9dff-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b9dff-132">RELATED LINKS</span></span>

[<span data-ttu-id="b9dff-133">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b9dff-133">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b9dff-134">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b9dff-134">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b9dff-135">Neu – AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b9dff-135">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b9dff-136">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b9dff-136">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)


