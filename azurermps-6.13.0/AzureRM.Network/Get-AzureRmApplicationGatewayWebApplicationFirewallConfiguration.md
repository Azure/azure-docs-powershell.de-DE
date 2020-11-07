---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 1456afca27b6a5993fa014b738c415af5db98c6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663655"
---
# <span data-ttu-id="e01f9-101">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="e01f9-101">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="e01f9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e01f9-102">SYNOPSIS</span></span>
<span data-ttu-id="e01f9-103">Ruft die WAF-Konfiguration eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="e01f9-103">Gets the WAF configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e01f9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e01f9-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e01f9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e01f9-105">DESCRIPTION</span></span>
<span data-ttu-id="e01f9-106">Das Cmdlet " **Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** " Ruft die WAF-Konfiguration (Web Application Firewall) eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="e01f9-106">The **Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="e01f9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e01f9-107">EXAMPLES</span></span>

### <span data-ttu-id="e01f9-108">Beispiel 1: Abrufen der Firewall-Konfiguration einer Application Gateway-Webanwendung</span><span class="sxs-lookup"><span data-stu-id="e01f9-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="e01f9-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab und speichert es dann in der $AppGW-Variablen.</span><span class="sxs-lookup"><span data-stu-id="e01f9-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>
<span data-ttu-id="e01f9-110">Der zweite Befehl ruft die Firewall-Konfiguration des Anwendungs Gateways in $AppGW ab und speichert Sie dann in $FirewallConfig.</span><span class="sxs-lookup"><span data-stu-id="e01f9-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="e01f9-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e01f9-111">PARAMETERS</span></span>

### <span data-ttu-id="e01f9-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e01f9-112">-ApplicationGateway</span></span>
<span data-ttu-id="e01f9-113">Gibt ein Application Gateway-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="e01f9-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="e01f9-114">Sie können das Get-AzureRmApplicationGateway-Cmdlet verwenden, um ein Application Gateway-Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e01f9-114">You can use the Get-AzureRmApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="e01f9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e01f9-115">-DefaultProfile</span></span>
<span data-ttu-id="e01f9-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e01f9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e01f9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e01f9-117">CommonParameters</span></span>
<span data-ttu-id="e01f9-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e01f9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e01f9-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e01f9-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e01f9-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e01f9-120">INPUTS</span></span>

### <span data-ttu-id="e01f9-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e01f9-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="e01f9-122">Parameter: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e01f9-122">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="e01f9-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e01f9-123">OUTPUTS</span></span>

### <span data-ttu-id="e01f9-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="e01f9-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="e01f9-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="e01f9-125">NOTES</span></span>

## <span data-ttu-id="e01f9-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e01f9-126">RELATED LINKS</span></span>

[<span data-ttu-id="e01f9-127">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e01f9-127">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="e01f9-128">Neu – AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="e01f9-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="e01f9-129">Satz-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="e01f9-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


