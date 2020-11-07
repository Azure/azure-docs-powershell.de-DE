---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
ms.openlocfilehash: 7b83e7f8ca372faf8158e248d326595a0d162d6a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848463"
---
# <span data-ttu-id="d1293-101">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1293-101">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="d1293-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d1293-102">SYNOPSIS</span></span>
<span data-ttu-id="d1293-103">Ruft die WAF-Konfiguration eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="d1293-103">Gets the WAF configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1293-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1293-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1293-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1293-105">DESCRIPTION</span></span>
<span data-ttu-id="d1293-106">Das Cmdlet " **Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** " Ruft die WAF-Konfiguration (Web Application Firewall) eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="d1293-106">The **Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="d1293-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d1293-107">EXAMPLES</span></span>

### <span data-ttu-id="d1293-108">Beispiel 1: Abrufen der Firewall-Konfiguration einer Application Gateway-Webanwendung</span><span class="sxs-lookup"><span data-stu-id="d1293-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="d1293-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab und speichert es dann in der $AppGW-Variablen.</span><span class="sxs-lookup"><span data-stu-id="d1293-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>

<span data-ttu-id="d1293-110">Der zweite Befehl ruft die Firewall-Konfiguration des Anwendungs Gateways in $AppGW ab und speichert Sie dann in $FirewallConfig.</span><span class="sxs-lookup"><span data-stu-id="d1293-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="d1293-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1293-111">PARAMETERS</span></span>

### <span data-ttu-id="d1293-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1293-112">-ApplicationGateway</span></span>
<span data-ttu-id="d1293-113">Gibt ein Application Gateway-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d1293-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="d1293-114">Sie können das Get-AzureRmApplicationGateway-Cmdlet verwenden, um ein Application Gateway-Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d1293-114">You can use the Get-AzureRmApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="d1293-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1293-115">-DefaultProfile</span></span>
<span data-ttu-id="d1293-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d1293-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1293-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1293-117">CommonParameters</span></span>
<span data-ttu-id="d1293-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1293-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1293-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1293-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1293-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d1293-120">INPUTS</span></span>

### <span data-ttu-id="d1293-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1293-121">PSApplicationGateway</span></span>
<span data-ttu-id="d1293-122">Der Parameter "ApplicationGateway" akzeptiert den Wert vom Typ "PSApplicationGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="d1293-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="d1293-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d1293-123">OUTPUTS</span></span>

### <span data-ttu-id="d1293-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1293-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="d1293-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="d1293-125">NOTES</span></span>

## <span data-ttu-id="d1293-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d1293-126">RELATED LINKS</span></span>

[<span data-ttu-id="d1293-127">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1293-127">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="d1293-128">Neu – AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1293-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="d1293-129">Satz-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1293-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


