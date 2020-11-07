---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: be1e70538aae66b05bdff5b06859cfb2f30681ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841731"
---
# <span data-ttu-id="e517f-101">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="e517f-101">Get-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="e517f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e517f-102">SYNOPSIS</span></span>
<span data-ttu-id="e517f-103">Ruft den Front-End-Port eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="e517f-103">Gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="e517f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e517f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e517f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e517f-105">DESCRIPTION</span></span>
<span data-ttu-id="e517f-106">Mit dem Cmdlet **Get-AzApplicationGatewayFrontendPort** wird der Front-End-Port eines Anwendungs Gateways abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e517f-106">The **Get-AzApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="e517f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e517f-107">EXAMPLES</span></span>

### <span data-ttu-id="e517f-108">Beispiel 1: Abrufen eines angegebenen Front-End-Ports</span><span class="sxs-lookup"><span data-stu-id="e517f-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzApplicationGatewayFrontendIPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="e517f-109">Der erste Befehl ruft ein Anwendungsgateway mit dem Namen ApplicationGateway01 aus der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="e517f-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e517f-110">Der zweite Befehl ruft den Front-End-Port mit dem Namen FrontEndPort01 aus $AppGw ab und speichert ihn in der $FrontEndPort-Variablen.</span><span class="sxs-lookup"><span data-stu-id="e517f-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="e517f-111">Beispiel 2: Abrufen einer Liste der Front-End-Ports</span><span class="sxs-lookup"><span data-stu-id="e517f-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzApplicationGatewayFrontendIPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="e517f-112">Der erste Befehl ruft ein Anwendungsgateway mit dem Namen ApplicationGateway01 aus der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="e517f-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e517f-113">Der zweite Befehl ruft eine Liste der Front-End-Ports von $AppGw ab und speichert Sie in der $FrontEndPorts-Variablen.</span><span class="sxs-lookup"><span data-stu-id="e517f-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="e517f-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="e517f-114">PARAMETERS</span></span>

### <span data-ttu-id="e517f-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e517f-115">-ApplicationGateway</span></span>
<span data-ttu-id="e517f-116">Gibt das Application Gateway-Objekt an, das den Front-End-Port enthält.</span><span class="sxs-lookup"><span data-stu-id="e517f-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="e517f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e517f-117">-DefaultProfile</span></span>
<span data-ttu-id="e517f-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e517f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e517f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e517f-119">-Name</span></span>
<span data-ttu-id="e517f-120">Gibt den Namen des abzurufenden Front-End-Ports an.</span><span class="sxs-lookup"><span data-stu-id="e517f-120">Specifies the name of the front-end port to get.</span></span>

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

### <span data-ttu-id="e517f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e517f-121">CommonParameters</span></span>
<span data-ttu-id="e517f-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e517f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e517f-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e517f-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e517f-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e517f-124">INPUTS</span></span>

### <span data-ttu-id="e517f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e517f-125">System.String</span></span>

## <span data-ttu-id="e517f-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e517f-126">OUTPUTS</span></span>

### <span data-ttu-id="e517f-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="e517f-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="e517f-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="e517f-128">NOTES</span></span>

## <span data-ttu-id="e517f-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e517f-129">RELATED LINKS</span></span>

[<span data-ttu-id="e517f-130">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="e517f-130">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="e517f-131">Neu – AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="e517f-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="e517f-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="e517f-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="e517f-133">Satz-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="e517f-133">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


