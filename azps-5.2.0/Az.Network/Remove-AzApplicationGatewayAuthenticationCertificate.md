---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 02416fdb18f01c9a2af6c091b0be109b479ce45d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292618"
---
# <span data-ttu-id="f638f-101">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f638f-101">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="f638f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f638f-102">SYNOPSIS</span></span>
<span data-ttu-id="f638f-103">Entfernt ein Authentifizierungszertifikat von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="f638f-103">Removes an authentication certificate from an application gateway.</span></span>

## <span data-ttu-id="f638f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f638f-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAuthenticationCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f638f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f638f-105">DESCRIPTION</span></span>
<span data-ttu-id="f638f-106">Das **Cmdlet "Remove-AzApplicationGatewayAuthenticationCertificate"** entfernt ein Authentifizierungszertifikat von einem Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="f638f-106">The **Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="f638f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f638f-107">EXAMPLES</span></span>

### <span data-ttu-id="f638f-108">Beispiel 1: Entfernen eines Authentifizierungszertifikats von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="f638f-108">Example 1: Remove an authentication certificate from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="f638f-109">Der erste Befehl ruft das Anwendungsgateway namens "appGwName" ab und speichert das Ergebnis in der $appgw Variable.</span><span class="sxs-lookup"><span data-stu-id="f638f-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="f638f-110">Der zweite Befehl entfernt das Authentifizierungszertifikat mit dem Namen "cert01" vom Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="f638f-110">The second command removes the authentication certificate named cert01 from the application gateway.</span></span>
<span data-ttu-id="f638f-111">Mit dem dritten Befehl wird das Anwendungsgateway aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f638f-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="f638f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f638f-112">PARAMETERS</span></span>

### <span data-ttu-id="f638f-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f638f-113">-ApplicationGateway</span></span>
<span data-ttu-id="f638f-114">Gibt den Namen des Anwendungsgateways an, von dem dieses Cmdlet ein Authentifizierungszertifikat entfernt.</span><span class="sxs-lookup"><span data-stu-id="f638f-114">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="f638f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f638f-115">-DefaultProfile</span></span>
<span data-ttu-id="f638f-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f638f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f638f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f638f-117">-Name</span></span>
<span data-ttu-id="f638f-118">Gibt den Namen des Authentifizierungszertifikats an, das von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="f638f-118">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f638f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f638f-119">-Confirm</span></span>
<span data-ttu-id="f638f-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f638f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f638f-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f638f-121">-WhatIf</span></span>
<span data-ttu-id="f638f-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f638f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f638f-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f638f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f638f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f638f-124">CommonParameters</span></span>
<span data-ttu-id="f638f-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f638f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f638f-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f638f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f638f-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f638f-127">INPUTS</span></span>

### <span data-ttu-id="f638f-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f638f-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f638f-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f638f-129">OUTPUTS</span></span>

### <span data-ttu-id="f638f-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f638f-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f638f-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f638f-131">NOTES</span></span>
* <span data-ttu-id="f638f-132">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="f638f-132">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="f638f-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f638f-133">RELATED LINKS</span></span>

[<span data-ttu-id="f638f-134">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f638f-134">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f638f-135">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f638f-135">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f638f-136">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f638f-136">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f638f-137">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f638f-137">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


