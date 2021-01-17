---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 1efce67698ca6d2e3a8bc9eeab3d89e00e1833f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473497"
---
# <span data-ttu-id="aedda-101">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="aedda-101">Get-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="aedda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aedda-102">SYNOPSIS</span></span>
<span data-ttu-id="aedda-103">Ruft die Front-End-IP-Konfiguration eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="aedda-103">Gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="aedda-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aedda-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aedda-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aedda-105">DESCRIPTION</span></span>
<span data-ttu-id="aedda-106">Das **Cmdlet "Get-AzApplicationGatewayFrontendIPConfig"** ruft die Front-End-IP-Konfiguration eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="aedda-106">The **Get-AzApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="aedda-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aedda-107">EXAMPLES</span></span>

### <span data-ttu-id="aedda-108">Beispiel 1: Erhalten einer angegebenen Front-End-IP-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="aedda-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="aedda-109">Der erste Befehl ruft ein Anwendungsgateway namens ApplicationGateway01 aus der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variable. Der zweite Befehl ruft die Front-End-IP-Konfiguration namens FrontEndIP01 aus $AppGw und speichert sie in der $FrontEndIP Variable.</span><span class="sxs-lookup"><span data-stu-id="aedda-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="aedda-110">Beispiel 2: Erhalten einer Liste der Front-End-IP-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="aedda-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="aedda-111">Der erste Befehl ruft ein Anwendungsgateway namens ApplicationGateway01 aus der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variable. Der zweite Befehl ruft eine Liste der Front-End-IP-Konfigurationen von $AppGw und speichert sie in der $FrontEndIPs Variable.</span><span class="sxs-lookup"><span data-stu-id="aedda-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="aedda-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aedda-112">PARAMETERS</span></span>

### <span data-ttu-id="aedda-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="aedda-113">-ApplicationGateway</span></span>
<span data-ttu-id="aedda-114">Gibt das Anwendungsgatewayobjekt an, das die Front-End-IP-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="aedda-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

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

### <span data-ttu-id="aedda-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aedda-115">-DefaultProfile</span></span>
<span data-ttu-id="aedda-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aedda-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedda-117">-Name</span><span class="sxs-lookup"><span data-stu-id="aedda-117">-Name</span></span>
<span data-ttu-id="aedda-118">Gibt den Namen der Front-End-IP-Konfiguration an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="aedda-118">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedda-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aedda-119">CommonParameters</span></span>
<span data-ttu-id="aedda-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aedda-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aedda-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aedda-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aedda-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aedda-122">INPUTS</span></span>

### <span data-ttu-id="aedda-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="aedda-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="aedda-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aedda-124">OUTPUTS</span></span>

### <span data-ttu-id="aedda-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="aedda-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="aedda-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="aedda-126">NOTES</span></span>

## <span data-ttu-id="aedda-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="aedda-127">RELATED LINKS</span></span>

[<span data-ttu-id="aedda-128">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="aedda-128">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="aedda-129">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="aedda-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="aedda-130">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="aedda-130">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="aedda-131">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="aedda-131">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


