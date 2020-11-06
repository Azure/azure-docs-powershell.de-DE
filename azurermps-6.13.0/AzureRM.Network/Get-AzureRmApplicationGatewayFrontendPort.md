---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: 388c2d06f7ff62bfe5fc2f6fcf47d5fa9fa16877
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505357"
---
# <span data-ttu-id="57c1e-101">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="57c1e-101">Get-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="57c1e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="57c1e-102">SYNOPSIS</span></span>
<span data-ttu-id="57c1e-103">Ruft den Front-End-Port eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="57c1e-103">Gets the front-end port of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57c1e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="57c1e-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57c1e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="57c1e-105">DESCRIPTION</span></span>
<span data-ttu-id="57c1e-106">Mit dem Cmdlet **Get-AzureRmApplicationGatewayFrontendPort** wird der Front-End-Port eines Anwendungs Gateways abgerufen.</span><span class="sxs-lookup"><span data-stu-id="57c1e-106">The **Get-AzureRmApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="57c1e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="57c1e-107">EXAMPLES</span></span>

### <span data-ttu-id="57c1e-108">Beispiel 1: Abrufen eines angegebenen Front-End-Ports</span><span class="sxs-lookup"><span data-stu-id="57c1e-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="57c1e-109">Der erste Befehl ruft ein Anwendungsgateway mit dem Namen ApplicationGateway01 aus der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="57c1e-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="57c1e-110">Der zweite Befehl ruft den Front-End-Port mit dem Namen FrontEndPort01 aus $AppGw ab und speichert ihn in der $FrontEndPort-Variablen.</span><span class="sxs-lookup"><span data-stu-id="57c1e-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="57c1e-111">Beispiel 2: Abrufen einer Liste der Front-End-Ports</span><span class="sxs-lookup"><span data-stu-id="57c1e-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzureRmApplicationGatewayFrontendPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="57c1e-112">Der erste Befehl ruft ein Anwendungsgateway mit dem Namen ApplicationGateway01 aus der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="57c1e-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="57c1e-113">Der zweite Befehl ruft eine Liste der Front-End-Ports von $AppGw ab und speichert Sie in der $FrontEndPorts-Variablen.</span><span class="sxs-lookup"><span data-stu-id="57c1e-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="57c1e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="57c1e-114">PARAMETERS</span></span>

### <span data-ttu-id="57c1e-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="57c1e-115">-ApplicationGateway</span></span>
<span data-ttu-id="57c1e-116">Gibt das Application Gateway-Objekt an, das den Front-End-Port enthält.</span><span class="sxs-lookup"><span data-stu-id="57c1e-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="57c1e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57c1e-117">-DefaultProfile</span></span>
<span data-ttu-id="57c1e-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="57c1e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57c1e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="57c1e-119">-Name</span></span>
<span data-ttu-id="57c1e-120">Gibt den Namen des abzurufenden Front-End-Ports an.</span><span class="sxs-lookup"><span data-stu-id="57c1e-120">Specifies the name of the front-end port to get.</span></span>

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

### <span data-ttu-id="57c1e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57c1e-121">CommonParameters</span></span>
<span data-ttu-id="57c1e-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57c1e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57c1e-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57c1e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57c1e-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="57c1e-124">INPUTS</span></span>

### <span data-ttu-id="57c1e-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="57c1e-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="57c1e-126">Parameter: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="57c1e-126">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="57c1e-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="57c1e-127">OUTPUTS</span></span>

### <span data-ttu-id="57c1e-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="57c1e-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="57c1e-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="57c1e-129">NOTES</span></span>

## <span data-ttu-id="57c1e-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="57c1e-130">RELATED LINKS</span></span>

[<span data-ttu-id="57c1e-131">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="57c1e-131">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="57c1e-132">Neu – AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="57c1e-132">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="57c1e-133">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="57c1e-133">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="57c1e-134">Satz-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="57c1e-134">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


