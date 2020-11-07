---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 77a87d80e656098eeb9450b0ed612d82a8b9e7fa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841687"
---
# <span data-ttu-id="2617f-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="2617f-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="2617f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2617f-102">SYNOPSIS</span></span>
<span data-ttu-id="2617f-103">Ruft die WAF-Konfiguration eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="2617f-103">Gets the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="2617f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2617f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2617f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2617f-105">DESCRIPTION</span></span>
<span data-ttu-id="2617f-106">Das Cmdlet " **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** " Ruft die WAF-Konfiguration (Web Application Firewall) eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="2617f-106">The **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="2617f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2617f-107">EXAMPLES</span></span>

### <span data-ttu-id="2617f-108">Beispiel 1: Abrufen der Firewall-Konfiguration einer Application Gateway-Webanwendung</span><span class="sxs-lookup"><span data-stu-id="2617f-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="2617f-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab und speichert es dann in der $AppGW-Variablen.</span><span class="sxs-lookup"><span data-stu-id="2617f-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>

<span data-ttu-id="2617f-110">Der zweite Befehl ruft die Firewall-Konfiguration des Anwendungs Gateways in $AppGW ab und speichert Sie dann in $FirewallConfig.</span><span class="sxs-lookup"><span data-stu-id="2617f-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="2617f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2617f-111">PARAMETERS</span></span>

### <span data-ttu-id="2617f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2617f-112">-ApplicationGateway</span></span>
<span data-ttu-id="2617f-113">Gibt ein Application Gateway-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="2617f-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="2617f-114">Sie können das Get-AzApplicationGateway-Cmdlet verwenden, um ein Application Gateway-Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2617f-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="2617f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2617f-115">-DefaultProfile</span></span>
<span data-ttu-id="2617f-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2617f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2617f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2617f-117">CommonParameters</span></span>
<span data-ttu-id="2617f-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2617f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2617f-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2617f-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2617f-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2617f-120">INPUTS</span></span>

### <span data-ttu-id="2617f-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2617f-121">PSApplicationGateway</span></span>
<span data-ttu-id="2617f-122">Der Parameter "ApplicationGateway" akzeptiert den Wert vom Typ "PSApplicationGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="2617f-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="2617f-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2617f-123">OUTPUTS</span></span>

### <span data-ttu-id="2617f-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="2617f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="2617f-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="2617f-125">NOTES</span></span>

## <span data-ttu-id="2617f-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2617f-126">RELATED LINKS</span></span>

[<span data-ttu-id="2617f-127">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2617f-127">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="2617f-128">Neu – AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="2617f-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="2617f-129">Satz-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="2617f-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


