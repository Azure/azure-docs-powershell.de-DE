---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 5af778b84981b5b15acaa688bd8ad1702e5ab7e3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160652"
---
# <span data-ttu-id="80ba2-101">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="80ba2-101">Set-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="80ba2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80ba2-102">SYNOPSIS</span></span>
<span data-ttu-id="80ba2-103">Aktualisiert ein Authentifizierungszertifikat für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="80ba2-103">Updates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="80ba2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="80ba2-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80ba2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="80ba2-105">DESCRIPTION</span></span>
<span data-ttu-id="80ba2-106">Das **Cmdlet Set-AzApplicationGatewayAuthenticationCertificate** aktualisiert ein Authentifizierungszertifikat für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="80ba2-106">The **Set-AzApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="80ba2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="80ba2-107">EXAMPLES</span></span>

### <span data-ttu-id="80ba2-108">Beispiel 1: Aktualisieren eines Authentifizierungszertifikats</span><span class="sxs-lookup"><span data-stu-id="80ba2-108">Example 1: Update an authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert2.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="80ba2-109">Der erste Befehl ruft das Anwendungsgateway namens "appGwName" ab und speichert das Ergebnis in der $appgw Variable.</span><span class="sxs-lookup"><span data-stu-id="80ba2-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="80ba2-110">Der zweite Befehl aktualisiert das Authentifizierungszertifikat mit dem Namen "cert01" im Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="80ba2-110">The second command updates the authentication certificate named cert01 in the application gateway.</span></span>
<span data-ttu-id="80ba2-111">Mit dem dritten Befehl wird das Anwendungsgateway aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="80ba2-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="80ba2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80ba2-112">PARAMETERS</span></span>

### <span data-ttu-id="80ba2-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="80ba2-113">-ApplicationGateway</span></span>
<span data-ttu-id="80ba2-114">Gibt den Namen des Anwendungsgateways an, für das dieses Cmdlet ein Authentifizierungszertifikat aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="80ba2-114">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="80ba2-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="80ba2-115">-CertificateFile</span></span>
<span data-ttu-id="80ba2-116">Gibt den Pfad der Authentifizierungszertifikatdatei an, mit der dieses Cmdlet das Zertifikat aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="80ba2-116">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="80ba2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80ba2-117">-DefaultProfile</span></span>
<span data-ttu-id="80ba2-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="80ba2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80ba2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="80ba2-119">-Name</span></span>
<span data-ttu-id="80ba2-120">Gibt den Namen des Authentifizierungszertifikats an, das von diesem Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="80ba2-120">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="80ba2-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80ba2-121">-Confirm</span></span>
<span data-ttu-id="80ba2-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="80ba2-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ba2-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="80ba2-123">-WhatIf</span></span>
<span data-ttu-id="80ba2-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="80ba2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80ba2-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="80ba2-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ba2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80ba2-126">CommonParameters</span></span>
<span data-ttu-id="80ba2-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80ba2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80ba2-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80ba2-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80ba2-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="80ba2-129">INPUTS</span></span>

### <span data-ttu-id="80ba2-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="80ba2-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="80ba2-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="80ba2-131">OUTPUTS</span></span>

### <span data-ttu-id="80ba2-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="80ba2-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="80ba2-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="80ba2-133">NOTES</span></span>
* <span data-ttu-id="80ba2-134">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="80ba2-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="80ba2-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="80ba2-135">RELATED LINKS</span></span>

[<span data-ttu-id="80ba2-136">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="80ba2-136">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="80ba2-137">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="80ba2-137">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="80ba2-138">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="80ba2-138">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="80ba2-139">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="80ba2-139">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)


