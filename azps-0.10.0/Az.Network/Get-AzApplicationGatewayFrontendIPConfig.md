---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 2004fe6a10fe2700d256ae4cae8419ab631a2f64
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841728"
---
# <span data-ttu-id="4258a-101">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="4258a-101">Get-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="4258a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4258a-102">SYNOPSIS</span></span>
<span data-ttu-id="4258a-103">Ruft die Front-End-IP-Konfiguration eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="4258a-103">Gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="4258a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4258a-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4258a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4258a-105">DESCRIPTION</span></span>
<span data-ttu-id="4258a-106">Das Cmdlet " **Get-AzApplicationGatewayFrontendIPConfig** " Ruft die Front-End-IP-Konfiguration eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="4258a-106">The **Get-AzApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="4258a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4258a-107">EXAMPLES</span></span>

### <span data-ttu-id="4258a-108">Beispiel 1: Abrufen einer angegebenen Front-End-IP-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="4258a-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="4258a-109">Der erste Befehl ruft ein Anwendungsgateway mit dem Namen ApplicationGateway01 aus der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen. Der zweite Befehl ruft die Front-End-IP-Konfiguration mit dem Namen FrontEndIP01 aus $AppGw ab und speichert Sie in der $FrontEndIP-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4258a-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="4258a-110">Beispiel 2: Abrufen einer Liste der Front-End-IP-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="4258a-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="4258a-111">Der erste Befehl ruft ein Anwendungsgateway mit dem Namen ApplicationGateway01 aus der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen. Der zweite Befehl ruft eine Liste der Front-End-IP-Konfigurationen von $AppGw ab und speichert Sie in der $FrontEndIPs-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4258a-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="4258a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4258a-112">PARAMETERS</span></span>

### <span data-ttu-id="4258a-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4258a-113">-ApplicationGateway</span></span>
<span data-ttu-id="4258a-114">Gibt das Application Gateway-Objekt an, das die Front-End-IP-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="4258a-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

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

### <span data-ttu-id="4258a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4258a-115">-DefaultProfile</span></span>
<span data-ttu-id="4258a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4258a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4258a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4258a-117">-Name</span></span>
<span data-ttu-id="4258a-118">Gibt den Namen der Front-End-IP-Konfiguration an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="4258a-118">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4258a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4258a-119">CommonParameters</span></span>
<span data-ttu-id="4258a-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4258a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4258a-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4258a-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4258a-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4258a-122">INPUTS</span></span>

### <span data-ttu-id="4258a-123">System. String</span><span class="sxs-lookup"><span data-stu-id="4258a-123">System.String</span></span>

## <span data-ttu-id="4258a-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4258a-124">OUTPUTS</span></span>

### <span data-ttu-id="4258a-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4258a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="4258a-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="4258a-126">NOTES</span></span>

## <span data-ttu-id="4258a-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4258a-127">RELATED LINKS</span></span>

[<span data-ttu-id="4258a-128">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="4258a-128">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="4258a-129">Neu – AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="4258a-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="4258a-130">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="4258a-130">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="4258a-131">Satz-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="4258a-131">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


