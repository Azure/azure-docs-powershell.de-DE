---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 88393e7c40ba9888602f144410263e7210a3db9e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660862"
---
# <span data-ttu-id="13776-101">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="13776-101">Get-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="13776-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="13776-102">SYNOPSIS</span></span>
<span data-ttu-id="13776-103">Ruft die Front-End-IP-Konfiguration eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="13776-103">Gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="13776-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="13776-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13776-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="13776-105">DESCRIPTION</span></span>
<span data-ttu-id="13776-106">Das Cmdlet " **Get-AzApplicationGatewayFrontendIPConfig** " Ruft die Front-End-IP-Konfiguration eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="13776-106">The **Get-AzApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="13776-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="13776-107">EXAMPLES</span></span>

### <span data-ttu-id="13776-108">Beispiel 1: Abrufen einer angegebenen Front-End-IP-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="13776-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="13776-109">Der erste Befehl ruft ein Anwendungsgateway mit dem Namen ApplicationGateway01 aus der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen. Der zweite Befehl ruft die Front-End-IP-Konfiguration mit dem Namen FrontEndIP01 aus $AppGw ab und speichert Sie in der $FrontEndIP-Variablen.</span><span class="sxs-lookup"><span data-stu-id="13776-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="13776-110">Beispiel 2: Abrufen einer Liste der Front-End-IP-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="13776-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="13776-111">Der erste Befehl ruft ein Anwendungsgateway mit dem Namen ApplicationGateway01 aus der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen. Der zweite Befehl ruft eine Liste der Front-End-IP-Konfigurationen von $AppGw ab und speichert Sie in der $FrontEndIPs-Variablen.</span><span class="sxs-lookup"><span data-stu-id="13776-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="13776-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="13776-112">PARAMETERS</span></span>

### <span data-ttu-id="13776-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13776-113">-ApplicationGateway</span></span>
<span data-ttu-id="13776-114">Gibt das Application Gateway-Objekt an, das die Front-End-IP-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="13776-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

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

### <span data-ttu-id="13776-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13776-115">-DefaultProfile</span></span>
<span data-ttu-id="13776-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="13776-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13776-117">-Name</span><span class="sxs-lookup"><span data-stu-id="13776-117">-Name</span></span>
<span data-ttu-id="13776-118">Gibt den Namen der Front-End-IP-Konfiguration an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="13776-118">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13776-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13776-119">CommonParameters</span></span>
<span data-ttu-id="13776-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13776-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13776-121">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13776-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13776-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="13776-122">INPUTS</span></span>

### <span data-ttu-id="13776-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13776-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="13776-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="13776-124">OUTPUTS</span></span>

### <span data-ttu-id="13776-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="13776-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="13776-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="13776-126">NOTES</span></span>

## <span data-ttu-id="13776-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="13776-127">RELATED LINKS</span></span>

[<span data-ttu-id="13776-128">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="13776-128">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="13776-129">Neu – AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="13776-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="13776-130">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="13776-130">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="13776-131">Satz-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="13776-131">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


