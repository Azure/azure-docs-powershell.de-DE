---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: e2cecb2061b605c5380597c51cb72860596690cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158900"
---
# <span data-ttu-id="cc2ac-101">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="cc2ac-101">Set-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="cc2ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc2ac-102">SYNOPSIS</span></span>
<span data-ttu-id="cc2ac-103">Ändert die Konfiguration für die Verbindungsentleerung eines Back-End-HTTP-Einstellungsobjekts.</span><span class="sxs-lookup"><span data-stu-id="cc2ac-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="cc2ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc2ac-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc2ac-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc2ac-105">DESCRIPTION</span></span>
<span data-ttu-id="cc2ac-106">Das **Cmdlet "Set-AzApplicationGatewayWebApplicationFirewallConfiguration"** ändert die Konfiguration für die Verbindungsentleerung eines Back-End-HTTP-Einstellungsobjekts.</span><span class="sxs-lookup"><span data-stu-id="cc2ac-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="cc2ac-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cc2ac-107">EXAMPLES</span></span>

### <span data-ttu-id="cc2ac-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cc2ac-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="cc2ac-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="cc2ac-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="cc2ac-110">Der zweite Befehl ruft die Back-End-HTTP-Einstellungen namens Settings01 für $AppGw und speichert die Einstellungen in der $Settings Variable.</span><span class="sxs-lookup"><span data-stu-id="cc2ac-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="cc2ac-111">Mit dem letzten Befehl wird die Konfiguration der Verbindungsentleerung des in $Settings gespeicherten Back-End-HTTP-Einstellungsobjekts geändert, indem "Enabled" auf "False" und "DrainTimeoutInSec" auf 3600 festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="cc2ac-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="cc2ac-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc2ac-112">PARAMETERS</span></span>

### <span data-ttu-id="cc2ac-113">-Back-EndHttpSettings</span><span class="sxs-lookup"><span data-stu-id="cc2ac-113">-BackendHttpSettings</span></span>
<span data-ttu-id="cc2ac-114">Die Back-End-HTTP-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="cc2ac-114">The backend http settings</span></span>

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

### <span data-ttu-id="cc2ac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc2ac-115">-DefaultProfile</span></span>
<span data-ttu-id="cc2ac-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc2ac-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc2ac-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="cc2ac-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="cc2ac-118">Die Anzahl der Sekunden, für die die Verbindungsentleerung aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="cc2ac-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="cc2ac-119">Zulässige Werte liegen zwischen einer Sekunde und 3600 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="cc2ac-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc2ac-120">-Enabled</span><span class="sxs-lookup"><span data-stu-id="cc2ac-120">-Enabled</span></span>
<span data-ttu-id="cc2ac-121">Ob die Verbindungsentleerung aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="cc2ac-121">Whether connection draining is enabled or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc2ac-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc2ac-122">CommonParameters</span></span>
<span data-ttu-id="cc2ac-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc2ac-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc2ac-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc2ac-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc2ac-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cc2ac-125">INPUTS</span></span>

### <span data-ttu-id="cc2ac-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="cc2ac-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="cc2ac-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cc2ac-127">OUTPUTS</span></span>

### <span data-ttu-id="cc2ac-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="cc2ac-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="cc2ac-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cc2ac-129">NOTES</span></span>

## <span data-ttu-id="cc2ac-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cc2ac-130">RELATED LINKS</span></span>

[<span data-ttu-id="cc2ac-131">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cc2ac-131">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="cc2ac-132">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="cc2ac-132">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="cc2ac-133">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="cc2ac-133">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="cc2ac-134">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="cc2ac-134">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="cc2ac-135">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="cc2ac-135">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

