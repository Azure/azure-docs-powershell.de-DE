---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 3d1df3262fa9cee55d5aa49c026b7b1e681b5c00
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941779"
---
# <span data-ttu-id="585df-101">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="585df-101">Get-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="585df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="585df-102">SYNOPSIS</span></span>
<span data-ttu-id="585df-103">Ruft die Verbindungsablaufkonfiguration eines Back-End-HTTP-Einstellungsobjekts ab.</span><span class="sxs-lookup"><span data-stu-id="585df-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="585df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="585df-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="585df-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="585df-105">DESCRIPTION</span></span>
<span data-ttu-id="585df-106">Das **Get-AzApplicationGatewayConnectionDraining-Cmdlet** ruft die Verbindungsablaufkonfiguration eines Back-End-HTTP-Einstellungsobjekts ab.</span><span class="sxs-lookup"><span data-stu-id="585df-106">The **Get-AzApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="585df-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="585df-107">EXAMPLES</span></span>

### <span data-ttu-id="585df-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="585df-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="585df-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="585df-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="585df-110">Der zweite Befehl ruft die Back-End-HTTP-Einstellungen mit dem Namen Settings01 für $AppGw ab und speichert die Einstellungen in der $Settings Variablen.</span><span class="sxs-lookup"><span data-stu-id="585df-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="585df-111">Der letzte Befehl ruft die Verbindungsablaufkonfiguration aus den Back-End-HTTP-Einstellungen $Settings und speichert sie in der $ConnectionDraining Variablen.</span><span class="sxs-lookup"><span data-stu-id="585df-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="585df-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="585df-112">PARAMETERS</span></span>

### <span data-ttu-id="585df-113">-Back-EndHttpSettings</span><span class="sxs-lookup"><span data-stu-id="585df-113">-BackendHttpSettings</span></span>
<span data-ttu-id="585df-114">Die Back-End-Http-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="585df-114">The backend http settings</span></span>

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

### <span data-ttu-id="585df-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="585df-115">-DefaultProfile</span></span>
<span data-ttu-id="585df-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="585df-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="585df-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="585df-117">CommonParameters</span></span>
<span data-ttu-id="585df-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="585df-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="585df-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="585df-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="585df-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="585df-120">INPUTS</span></span>

### <span data-ttu-id="585df-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="585df-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="585df-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="585df-122">OUTPUTS</span></span>

### <span data-ttu-id="585df-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="585df-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="585df-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="585df-124">NOTES</span></span>

## <span data-ttu-id="585df-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="585df-125">RELATED LINKS</span></span>

[<span data-ttu-id="585df-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="585df-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="585df-127">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="585df-127">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="585df-128">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="585df-128">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="585df-129">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="585df-129">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="585df-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="585df-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)
