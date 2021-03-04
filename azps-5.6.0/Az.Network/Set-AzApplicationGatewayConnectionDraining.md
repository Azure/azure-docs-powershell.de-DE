---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 84a9ccb86f9fd1d4995ad52e913059181c0b887e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926507"
---
# <span data-ttu-id="04ac1-101">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="04ac1-101">Set-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="04ac1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04ac1-102">SYNOPSIS</span></span>
<span data-ttu-id="04ac1-103">Ändert die Verbindungsablaufkonfiguration eines Back-End-HTTP-Einstellungsobjekts.</span><span class="sxs-lookup"><span data-stu-id="04ac1-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="04ac1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04ac1-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04ac1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="04ac1-105">DESCRIPTION</span></span>
<span data-ttu-id="04ac1-106">Das **Cmdlet Set-AzApplicationGatewayWebApplicationFirewallConfiguration** ändert die Verbindungsablaufkonfiguration eines Back-End-HTTP-Einstellungsobjekts.</span><span class="sxs-lookup"><span data-stu-id="04ac1-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="04ac1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="04ac1-107">EXAMPLES</span></span>

### <span data-ttu-id="04ac1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="04ac1-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="04ac1-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="04ac1-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="04ac1-110">Der zweite Befehl ruft die Back-End-HTTP-Einstellungen mit dem Namen Settings01 für $AppGw ab und speichert die Einstellungen in der $Settings Variablen.</span><span class="sxs-lookup"><span data-stu-id="04ac1-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="04ac1-111">Mit dem letzten Befehl wird die Verbindungsablaufkonfiguration des in $Settings gespeicherten Back-End-HTTP-Einstellungsobjekts geändert, indem Auf False aktiviert und DrainTimeoutInSec auf 3600 festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="04ac1-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="04ac1-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="04ac1-112">PARAMETERS</span></span>

### <span data-ttu-id="04ac1-113">-Back-EndHttpSettings</span><span class="sxs-lookup"><span data-stu-id="04ac1-113">-BackendHttpSettings</span></span>
<span data-ttu-id="04ac1-114">Die Back-End-Http-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="04ac1-114">The backend http settings</span></span>

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

### <span data-ttu-id="04ac1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04ac1-115">-DefaultProfile</span></span>
<span data-ttu-id="04ac1-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="04ac1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04ac1-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="04ac1-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="04ac1-118">Die Anzahl der Sekunden, in der die Verbindung entleert wird, ist aktiv.</span><span class="sxs-lookup"><span data-stu-id="04ac1-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="04ac1-119">Zulässige Werte liegen zwischen 1 Sekunde und 3600 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="04ac1-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="04ac1-120">-Enabled</span><span class="sxs-lookup"><span data-stu-id="04ac1-120">-Enabled</span></span>
<span data-ttu-id="04ac1-121">Ob die Verbindungsentwässerung aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="04ac1-121">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="04ac1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04ac1-122">CommonParameters</span></span>
<span data-ttu-id="04ac1-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04ac1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04ac1-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04ac1-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04ac1-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="04ac1-125">INPUTS</span></span>

### <span data-ttu-id="04ac1-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="04ac1-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="04ac1-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="04ac1-127">OUTPUTS</span></span>

### <span data-ttu-id="04ac1-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="04ac1-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="04ac1-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="04ac1-129">NOTES</span></span>

## <span data-ttu-id="04ac1-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="04ac1-130">RELATED LINKS</span></span>

[<span data-ttu-id="04ac1-131">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="04ac1-131">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="04ac1-132">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="04ac1-132">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="04ac1-133">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="04ac1-133">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="04ac1-134">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="04ac1-134">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="04ac1-135">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="04ac1-135">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

