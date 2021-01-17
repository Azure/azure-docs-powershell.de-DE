---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ec2c73be940e887b4cd1ca96da1442f8ae007ab6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472206"
---
# <span data-ttu-id="2834c-101">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2834c-101">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="2834c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2834c-102">SYNOPSIS</span></span>
<span data-ttu-id="2834c-103">Entfernt URL-Pfadzuordnungen zu einem Back-End-Server-Pool.</span><span class="sxs-lookup"><span data-stu-id="2834c-103">Removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="2834c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2834c-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2834c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2834c-105">DESCRIPTION</span></span>
<span data-ttu-id="2834c-106">Das **Cmdlet "Remove-AzApplicationGatewayUrlPathMapConfig"** entfernt die URL-Pfadzuordnungen zu einem Back-End-Serverpool.</span><span class="sxs-lookup"><span data-stu-id="2834c-106">The **Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="2834c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2834c-107">EXAMPLES</span></span>

### <span data-ttu-id="2834c-108">Beispiel 1: Entfernen einer URL-Pfadzuordnung von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="2834c-108">Example 1: Remove an URL path mapping from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="2834c-109">Der erste Befehl ruft das Anwendungsgateway namens "appGwName" ab und speichert das Ergebnis in der $appgw Variable.</span><span class="sxs-lookup"><span data-stu-id="2834c-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="2834c-110">Mit dem zweiten Befehl wird die URL-Pfadzuordnung namens "map01" vom Anwendungsgateway entfernt.</span><span class="sxs-lookup"><span data-stu-id="2834c-110">The second command removes the URL path mapping named map01 from the application gateway.</span></span>
<span data-ttu-id="2834c-111">Mit dem dritten Befehl wird das Anwendungsgateway aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2834c-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="2834c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2834c-112">PARAMETERS</span></span>

### <span data-ttu-id="2834c-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2834c-113">-ApplicationGateway</span></span>
<span data-ttu-id="2834c-114">Gibt das Anwendungsgateway an, zu dem dieses Cmdlet die Konfiguration der URL-Pfadzuordnung entfernt.</span><span class="sxs-lookup"><span data-stu-id="2834c-114">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="2834c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2834c-115">-DefaultProfile</span></span>
<span data-ttu-id="2834c-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2834c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2834c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2834c-117">-Name</span></span>
<span data-ttu-id="2834c-118">Gibt den Namen der URL-Pfadzuordnung an, den dieses Cmdlet vom Back-End-Server entfernt.</span><span class="sxs-lookup"><span data-stu-id="2834c-118">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="2834c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2834c-119">CommonParameters</span></span>
<span data-ttu-id="2834c-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2834c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2834c-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2834c-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2834c-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2834c-122">INPUTS</span></span>

### <span data-ttu-id="2834c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2834c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2834c-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2834c-124">OUTPUTS</span></span>

### <span data-ttu-id="2834c-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2834c-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2834c-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2834c-126">NOTES</span></span>

## <span data-ttu-id="2834c-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2834c-127">RELATED LINKS</span></span>

[<span data-ttu-id="2834c-128">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2834c-128">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2834c-129">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2834c-129">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2834c-130">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2834c-130">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2834c-131">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2834c-131">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


