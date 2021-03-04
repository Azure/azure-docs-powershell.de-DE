---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 610fe3f2ba4867dc1145488dfe789dba051b23bb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936731"
---
# <span data-ttu-id="ed2d7-101">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed2d7-101">Remove-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="ed2d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed2d7-102">SYNOPSIS</span></span>
<span data-ttu-id="ed2d7-103">Entfernt eine IP-Konfiguration aus einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="ed2d7-103">Removes an IP configuration from an application gateway.</span></span>

## <span data-ttu-id="ed2d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed2d7-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed2d7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed2d7-105">DESCRIPTION</span></span>
<span data-ttu-id="ed2d7-106">Das **Cmdlet Remove-AzApplicationGatewayIPConfiguration** entfernt eine IP-Konfiguration aus einem Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="ed2d7-106">The **Remove-AzApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="ed2d7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ed2d7-107">EXAMPLES</span></span>

### <span data-ttu-id="ed2d7-108">Beispiel 1: Entfernen einer IP-Konfiguration aus einem Azure-Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="ed2d7-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="ed2d7-109">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="ed2d7-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ed2d7-110">Mit dem zweiten Befehl wird die IP-Konfiguration namens Subnetz02 aus dem anwendungsgateway entfernt, das in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ed2d7-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="ed2d7-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ed2d7-111">PARAMETERS</span></span>

### <span data-ttu-id="ed2d7-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ed2d7-112">-ApplicationGateway</span></span>
<span data-ttu-id="ed2d7-113">Gibt das Anwendungsgateway an, aus dem eine IP-Konfiguration entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed2d7-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="ed2d7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed2d7-114">-DefaultProfile</span></span>
<span data-ttu-id="ed2d7-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed2d7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed2d7-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ed2d7-116">-Name</span></span>
<span data-ttu-id="ed2d7-117">Gibt den Namen der zu entfernenden IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="ed2d7-117">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="ed2d7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed2d7-118">CommonParameters</span></span>
<span data-ttu-id="ed2d7-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed2d7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed2d7-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed2d7-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed2d7-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ed2d7-121">INPUTS</span></span>

### <span data-ttu-id="ed2d7-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ed2d7-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ed2d7-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ed2d7-123">OUTPUTS</span></span>

### <span data-ttu-id="ed2d7-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ed2d7-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ed2d7-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ed2d7-125">NOTES</span></span>

## <span data-ttu-id="ed2d7-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ed2d7-126">RELATED LINKS</span></span>

[<span data-ttu-id="ed2d7-127">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed2d7-127">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="ed2d7-128">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed2d7-128">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="ed2d7-129">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed2d7-129">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="ed2d7-130">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed2d7-130">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


