---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 1630b0177efbccbf4d1cba674f0cf11ab457307e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402115"
---
# <span data-ttu-id="4518c-101">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="4518c-101">Get-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="4518c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4518c-102">SYNOPSIS</span></span>
<span data-ttu-id="4518c-103">Ruft die Konfiguration zur Entleerung der Verbindung eines Back-End-HTTP-Einstellungsobjekts ab.</span><span class="sxs-lookup"><span data-stu-id="4518c-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="4518c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4518c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4518c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4518c-105">DESCRIPTION</span></span>
<span data-ttu-id="4518c-106">Das **Cmdlet "Get-AzApplicationGatewayConnectionDraining"** ruft die Konfiguration zur Entleerung der Verbindung eines Back-End-HTTP-Einstellungsobjekts ab.</span><span class="sxs-lookup"><span data-stu-id="4518c-106">The **Get-AzApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="4518c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4518c-107">EXAMPLES</span></span>

### <span data-ttu-id="4518c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4518c-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="4518c-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="4518c-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4518c-110">Der zweite Befehl ruft die Back-End-HTTP-Einstellungen namens Settings01 für $AppGw und speichert die Einstellungen in der $Settings Variable.</span><span class="sxs-lookup"><span data-stu-id="4518c-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="4518c-111">Der letzte Befehl ruft die Konfiguration zur Entleerung der Verbindung aus den Back-End-HTTP-Einstellungen $Settings und speichert sie in $ConnectionDraining Variable.</span><span class="sxs-lookup"><span data-stu-id="4518c-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="4518c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4518c-112">PARAMETERS</span></span>

### <span data-ttu-id="4518c-113">-Back-EndHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4518c-113">-BackendHttpSettings</span></span>
<span data-ttu-id="4518c-114">Die Back-End-HTTP-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="4518c-114">The backend http settings</span></span>

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

### <span data-ttu-id="4518c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4518c-115">-DefaultProfile</span></span>
<span data-ttu-id="4518c-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4518c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4518c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4518c-117">CommonParameters</span></span>
<span data-ttu-id="4518c-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4518c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4518c-119">Weitere Informationen finden Sie unter [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4518c-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4518c-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4518c-120">INPUTS</span></span>

### <span data-ttu-id="4518c-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4518c-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="4518c-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4518c-122">OUTPUTS</span></span>

### <span data-ttu-id="4518c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="4518c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="4518c-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4518c-124">NOTES</span></span>

## <span data-ttu-id="4518c-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4518c-125">RELATED LINKS</span></span>

[<span data-ttu-id="4518c-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4518c-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)


[<span data-ttu-id="4518c-127">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="4518c-127">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="4518c-128">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="4518c-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="4518c-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="4518c-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)
