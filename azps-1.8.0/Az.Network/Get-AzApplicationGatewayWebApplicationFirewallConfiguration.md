---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: e2f477aa657bc4d21a650edffb7f014ae3c1ba62
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660828"
---
# <span data-ttu-id="252c6-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="252c6-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="252c6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="252c6-102">SYNOPSIS</span></span>
<span data-ttu-id="252c6-103">Ruft die WAF-Konfiguration eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="252c6-103">Gets the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="252c6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="252c6-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="252c6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="252c6-105">DESCRIPTION</span></span>
<span data-ttu-id="252c6-106">Das Cmdlet " **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** " Ruft die WAF-Konfiguration (Web Application Firewall) eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="252c6-106">The **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="252c6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="252c6-107">EXAMPLES</span></span>

### <span data-ttu-id="252c6-108">Beispiel 1: Abrufen der Firewall-Konfiguration einer Application Gateway-Webanwendung</span><span class="sxs-lookup"><span data-stu-id="252c6-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="252c6-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab und speichert es dann in der $AppGW-Variablen.</span><span class="sxs-lookup"><span data-stu-id="252c6-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>
<span data-ttu-id="252c6-110">Der zweite Befehl ruft die Firewall-Konfiguration des Anwendungs Gateways in $AppGW ab und speichert Sie dann in $FirewallConfig.</span><span class="sxs-lookup"><span data-stu-id="252c6-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="252c6-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="252c6-111">PARAMETERS</span></span>

### <span data-ttu-id="252c6-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="252c6-112">-ApplicationGateway</span></span>
<span data-ttu-id="252c6-113">Gibt ein Application Gateway-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="252c6-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="252c6-114">Sie können das Get-AzApplicationGateway-Cmdlet verwenden, um ein Application Gateway-Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="252c6-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="252c6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="252c6-115">-DefaultProfile</span></span>
<span data-ttu-id="252c6-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="252c6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="252c6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="252c6-117">CommonParameters</span></span>
<span data-ttu-id="252c6-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="252c6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="252c6-119">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="252c6-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="252c6-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="252c6-120">INPUTS</span></span>

### <span data-ttu-id="252c6-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="252c6-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="252c6-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="252c6-122">OUTPUTS</span></span>

### <span data-ttu-id="252c6-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="252c6-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="252c6-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="252c6-124">NOTES</span></span>

## <span data-ttu-id="252c6-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="252c6-125">RELATED LINKS</span></span>

[<span data-ttu-id="252c6-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="252c6-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="252c6-127">Neu – AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="252c6-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="252c6-128">Satz-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="252c6-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


