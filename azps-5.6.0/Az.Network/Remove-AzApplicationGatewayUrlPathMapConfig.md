---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 1d9caf3c95d7f8a508a41b8c047684b86c66227a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941696"
---
# <span data-ttu-id="6bb08-101">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6bb08-101">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="6bb08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bb08-102">SYNOPSIS</span></span>
<span data-ttu-id="6bb08-103">Entfernt URL-Pfadzuordnungen zu einem Back-End-Serverpool.</span><span class="sxs-lookup"><span data-stu-id="6bb08-103">Removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="6bb08-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6bb08-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6bb08-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6bb08-105">DESCRIPTION</span></span>
<span data-ttu-id="6bb08-106">Das **Cmdlet Remove-AzApplicationGatewayUrlPathMapConfig** entfernt URL-Pfadzuordnungen zu einem Back-End-Serverpool.</span><span class="sxs-lookup"><span data-stu-id="6bb08-106">The **Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="6bb08-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6bb08-107">EXAMPLES</span></span>

### <span data-ttu-id="6bb08-108">Beispiel 1: Entfernen einer URL-Pfadzuordnung aus einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="6bb08-108">Example 1: Remove an URL path mapping from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="6bb08-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen "appGwName" ab und speichert das Ergebnis in der $appgw Variablen.</span><span class="sxs-lookup"><span data-stu-id="6bb08-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="6bb08-110">Mit dem zweiten Befehl wird die URL-Pfadzuordnung mit dem Namen "map01" aus dem Anwendungsgateway entfernt.</span><span class="sxs-lookup"><span data-stu-id="6bb08-110">The second command removes the URL path mapping named map01 from the application gateway.</span></span>
<span data-ttu-id="6bb08-111">Mit dem dritten Befehl wird das Anwendungsgateway aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6bb08-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="6bb08-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6bb08-112">PARAMETERS</span></span>

### <span data-ttu-id="6bb08-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6bb08-113">-ApplicationGateway</span></span>
<span data-ttu-id="6bb08-114">Gibt das Anwendungsgateway an, zu dem dieses Cmdlet die Konfiguration der URL-Pfadzuordnung entfernt.</span><span class="sxs-lookup"><span data-stu-id="6bb08-114">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="6bb08-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bb08-115">-DefaultProfile</span></span>
<span data-ttu-id="6bb08-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6bb08-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bb08-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6bb08-117">-Name</span></span>
<span data-ttu-id="6bb08-118">Gibt den Namen der URL-Pfadzuordnung an, den dieses Cmdlet vom Back-End-Server entfernt.</span><span class="sxs-lookup"><span data-stu-id="6bb08-118">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="6bb08-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bb08-119">CommonParameters</span></span>
<span data-ttu-id="6bb08-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bb08-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bb08-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bb08-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bb08-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6bb08-122">INPUTS</span></span>

### <span data-ttu-id="6bb08-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6bb08-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6bb08-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6bb08-124">OUTPUTS</span></span>

### <span data-ttu-id="6bb08-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6bb08-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6bb08-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6bb08-126">NOTES</span></span>

## <span data-ttu-id="6bb08-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6bb08-127">RELATED LINKS</span></span>

[<span data-ttu-id="6bb08-128">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6bb08-128">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="6bb08-129">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6bb08-129">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="6bb08-130">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6bb08-130">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="6bb08-131">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6bb08-131">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


