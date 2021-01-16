---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: b6fe7d8be92e2d82762557a05bf88ef053e0d407
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468211"
---
# <span data-ttu-id="c6977-101">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c6977-101">Get-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="c6977-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6977-102">SYNOPSIS</span></span>
<span data-ttu-id="c6977-103">Ruft die Konfiguration zur Entleerung der Verbindung eines Back-End-HTTP-Einstellungsobjekts ab.</span><span class="sxs-lookup"><span data-stu-id="c6977-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="c6977-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6977-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6977-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6977-105">DESCRIPTION</span></span>
<span data-ttu-id="c6977-106">Das **Cmdlet "Get-AzApplicationGatewayConnectionDraining"** ruft die Konfiguration zur Entleerung der Verbindung eines Back-End-HTTP-Einstellungsobjekts ab.</span><span class="sxs-lookup"><span data-stu-id="c6977-106">The **Get-AzApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="c6977-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c6977-107">EXAMPLES</span></span>

### <span data-ttu-id="c6977-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c6977-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="c6977-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="c6977-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c6977-110">Der zweite Befehl ruft die Back-End-HTTP-Einstellungen namens Settings01 für $AppGw und speichert die Einstellungen in der $Settings Variable.</span><span class="sxs-lookup"><span data-stu-id="c6977-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="c6977-111">Der letzte Befehl ruft die Konfiguration zur Entleerung der Verbindung aus den Back-End-HTTP-Einstellungen $Settings und speichert sie in $ConnectionDraining Variable.</span><span class="sxs-lookup"><span data-stu-id="c6977-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="c6977-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6977-112">PARAMETERS</span></span>

### <span data-ttu-id="c6977-113">-Back-EndHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c6977-113">-BackendHttpSettings</span></span>
<span data-ttu-id="c6977-114">Die Back-End-HTTP-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="c6977-114">The backend http settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6977-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6977-115">-DefaultProfile</span></span>
<span data-ttu-id="c6977-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6977-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6977-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6977-117">CommonParameters</span></span>
<span data-ttu-id="c6977-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6977-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6977-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6977-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6977-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c6977-120">INPUTS</span></span>

### <span data-ttu-id="c6977-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c6977-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="c6977-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c6977-122">OUTPUTS</span></span>

### <span data-ttu-id="c6977-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c6977-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="c6977-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c6977-124">NOTES</span></span>

## <span data-ttu-id="c6977-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c6977-125">RELATED LINKS</span></span>

[<span data-ttu-id="c6977-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c6977-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="c6977-127">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="c6977-127">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="c6977-128">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c6977-128">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="c6977-129">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c6977-129">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="c6977-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c6977-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)
